# On Writing Software Well #4: Not every model is backed by a database — Summary

**Author:** David Heinemeier Hansson (DHH)
**Published:** February 16, 2018
**Series:** On Writing Software Well
**Episode:** 4 — Not every model is backed by a database
**Source:** <https://www.youtube.com/watch?v=MQw9zF9IehI>

---

## Overview

DHH walks through Basecamp's notification settings system to demonstrate that `app/models` isn't exclusively for Active Record classes. The episode showcases how plain old Ruby objects (POROs) can be composed with concerns to create elegant APIs, using the notification granularity feature as a case study — a setting backed by Redis rather than a database.

---

## The Core Argument: Models ≠ Active Record

People often assume that everything in `app/models` must inherit from `ActiveRecord::Base`. In Basecamp, many models are plain Ruby classes — no database, no inheritance. The `app/models` directory is for domain objects, not just database-backed records.

---

## Concerns + Composition: Better Together

DHH shows how concerns and composed objects complement each other:

### Layer 1: The Notifyee Concern (on User)
A slim concern mixed into `User` that provides a single method: `notifications`. Its only purpose is API elegance — enabling `current.user.notifications.granularity` instead of the awkward `Notifications.new(current.user).granularity`.

> "For me at least, it's well worth adding this concern just to have this nicer notation."

### Layer 2: The Notifications Class (PORO)
A plain Ruby class (no inheritance) that aggregates all notification-related concerns:
- **Snooze** — temporarily silence notifications
- **Platform** — where you receive notifications (native app, email, etc.)
- **Schedule** — "work can wait" off-hours settings
- **Granularity** — what level of notifications you want

Each sub-concern is a separate composed class that receives `notifications` as a constructor parameter and delegates back to it for shared resources (the user, the Redis connection).

### Layer 3: The Granularity Class (PORO)
Another plain Ruby class that encapsulates one specific setting:
- **Two choices**: "everything" or "pings and mentions only"
- **`allows?(deliverable)`** — checks whether a given notification type (mention, assignment, etc.) passes the granularity filter
- **Backed by Redis**, not the database

---

## Surface Area Isn't Inherently Bad

DHH pushes back on the criticism that objects with many methods are poorly designed:

- Ruby's `String` class has many methods — nobody complains
- Rails core classes have hundreds of methods — they work fine
- Concerns provide logical cohesion even when the aggregate method count is large
- What matters is **cohesion when reading the source** and **elegance when using the API**

---

## Redis vs. Database: A Criticality Heuristic

Basecamp's rule of thumb for choosing storage:

| Storage | Use for | Criticality |
|---------|---------|-------------|
| **Database** | Store of record — messages, files, content | Loss is catastrophic |
| **Redis** | Settings, preferences, transient state | Loss is annoying but recoverable |

Notification granularity settings are stored in Redis because losing them isn't the end of the world — you just set them again. Redis is plenty durable these days, but the mental model still helps when deciding where to put things.

Basecamp runs multiple Redis instances, assigning different features to different clusters via a `RedisConnectable` module that handles namespacing.

---

## The `send` Trade-off: Bypassing Privacy

The `Notifications` class keeps its Redis `user_key` private — it's an implementation detail that controllers shouldn't access. But the composed `Granularity` class needs it to build its own Redis key.

**Option A**: Use `send(:user_key)` to bypass privacy — feels wrong, violates encapsulation.
**Option B**: Make `user_key` public — exposes internals to all consumers.

DHH chooses `send` as the **lesser of two evils**. The `Granularity` class is within the notifications domain — it's almost like a `protected` method access, but Ruby's protection model doesn't support that outside inheritance hierarchies. In context, this is a deliberate, documented violation of the general rule.

---

## The Settings Controller

The notification settings screen updates five different things (granularity, schedule, snooze, platforms, etc.). The controller's `update` method is composed into five steps. For granularity:

```ruby
current.user.notifications.granularity.choice = params[:granularity]
```

Redis writes are immediate — no `save` call needed. The API reads naturally thanks to the concern → notifications → granularity composition chain.

---

## Key Themes

- **`app/models` is for domain objects** — Active Record models, concerns, AND plain Ruby classes all belong there
- **Concerns for API beauty, POROs for encapsulation** — use concerns to provide nice method access on host classes, then delegate real work to composed objects
- **Composition over inheritance** — the notifications system is a tree of composed objects, not an inheritance hierarchy
- **Trade-offs are context-dependent** — general rules (don't call private methods) can be broken when the specific context justifies it
- **A beautiful API is worth bending rules for** — `current.user.notifications.granularity.choice` is worth the extra concern and composition layers
- **Storage choices reflect criticality** — use the database for data you can't afford to lose, Redis for everything else
