# 37signals Developer Blog - Article Summaries

A comprehensive reference guide to 56 technical articles from dev.37signals.com, organized chronologically. Use this guide to quickly find relevant information about Rails architecture, Hotwire, infrastructure, performance, and 37signals engineering practices.

---

## 2022

### Domain-Driven Boldness
**Date:** June 13, 2022
**Author:** Jeremy Daer
**Domain:** Rails Architecture, Domain Modeling

**Key Concepts:**
- Domain-driven design in Rails applications
- Balancing pragmatism with architectural patterns
- Model organization and responsibility assignment

**Technologies/Tools:**
- Ruby on Rails
- Active Record
- Domain modeling patterns

**Summary:**
Explores how 37signals applies domain-driven design principles pragmatically in Rails applications. The article discusses finding the right balance between pure DDD and Rails conventions, focusing on creating models that reflect business domains while maintaining Rails' simplicity and productivity.

**Use Cases/Patterns:**
- Organizing complex business logic in Rails applications
- Creating domain-focused models beyond simple CRUD
- Refactoring toward clearer domain boundaries

**Developer Relevance:**
Reference when architecting complex Rails applications that need clear domain modeling. Useful for understanding when to introduce domain patterns versus sticking with vanilla Rails.

---

### Fractal Journeys
**Date:** September 18, 2022
**Author:** Jeremy Daer
**Domain:** Rails Architecture, Code Organization

**Key Concepts:**
- Fractal organization patterns in codebases
- Nested modules and namespacing
- Code locality and discoverability

**Technologies/Tools:**
- Ruby on Rails
- Module organization
- Namespace patterns

**Summary:**
Discusses fractal code organization where similar structures repeat at different scales of the application. Advocates for keeping related code close together using nested modules and namespaces, making code more discoverable and maintainable.

**Use Cases/Patterns:**
- Organizing large Rails applications
- Creating self-contained feature modules
- Improving code discoverability

**Developer Relevance:**
Consult when scaling Rails applications and deciding how to organize growing codebases. Helps understand 37signals' approach to code organization beyond MVC.

---

### Good Concerns
**Date:** October 10, 2022
**Author:** Jorge Manrubia
**Domain:** Rails Architecture, Code Reuse

**Key Concepts:**
- ActiveSupport::Concern best practices
- Code extraction and reuse
- Avoiding concern anti-patterns

**Technologies/Tools:**
- Ruby on Rails
- ActiveSupport::Concern
- Mixins and modules

**Summary:**
Provides guidance on using Rails concerns effectively, distinguishing between good and bad uses. Emphasizes that concerns should extract meaningful, cohesive behavior rather than becoming dumping grounds for miscellaneous methods.

**Use Cases/Patterns:**
- Extracting shared behavior across models or controllers
- Organizing cross-cutting concerns
- Avoiding god objects through proper extraction

**Developer Relevance:**
Essential reference when considering whether to extract code into a concern. Helps avoid common pitfalls that lead to hard-to-maintain code.

---

### Faster Paging in HEY
**Date:** November 7, 2022
**Author:** Jorge Manrubia
**Domain:** Performance, Database Optimization

**Key Concepts:**
- Pagination performance optimization
- Database query efficiency
- Cursor-based pagination

**Technologies/Tools:**
- Ruby on Rails
- MySQL
- ActiveRecord query optimization

**Summary:**
Details how HEY improved pagination performance from slow offset-based queries to efficient cursor-based pagination. The optimization dramatically reduced query times for large datasets by avoiding expensive OFFSET operations.

**Use Cases/Patterns:**
- Paginating large datasets efficiently
- Cursor-based vs offset-based pagination
- Optimizing queries on tables with millions of rows

**Developer Relevance:**
Critical reference when implementing pagination for large datasets. Shows practical performance gains from switching pagination strategies.

---

### Vanilla Rails is Plenty
**Date:** November 8, 2022
**Author:** David Heinemeier Hansson
**Domain:** Rails Architecture, Philosophy

**Key Concepts:**
- Minimal dependencies approach
- Embracing Rails defaults
- Fighting feature bloat

**Technologies/Tools:**
- Ruby on Rails
- Standard Rails stack
- Convention over configuration

**Summary:**
Advocates for sticking with vanilla Rails and default conventions rather than adding numerous gems and frameworks. Emphasizes that Rails' built-in features are sufficient for most needs and that added dependencies create long-term maintenance burden.

**Use Cases/Patterns:**
- Starting new Rails applications
- Evaluating whether to add new dependencies
- Simplifying existing Rails applications

**Developer Relevance:**
Essential philosophy piece when starting new projects or evaluating dependency additions. Explains 37signals' minimalist approach to Rails development.

---

### Making Export Jobs More Reliable
**Date:** November 15, 2022
**Author:** Rosa Gutiérrez
**Domain:** Background Jobs, Reliability

**Key Concepts:**
- Job reliability patterns
- Idempotent job design
- Error handling in background jobs

**Technologies/Tools:**
- Ruby on Rails
- ActiveJob
- Background job processing

**Summary:**
Explains patterns for making background export jobs more reliable through idempotency, proper error handling, and graceful degradation. Focuses on ensuring exports complete successfully even when interrupted.

**Use Cases/Patterns:**
- Designing reliable background jobs
- Implementing idempotent operations
- Handling job failures gracefully

**Developer Relevance:**
Reference when implementing background jobs that must be reliable, especially for long-running exports or data processing tasks.

---

### A Week in the Life of a Product Designer
**Date:** November 18, 2022
**Author:** Scott Upton
**Domain:** Design Process, Workflow

**Key Concepts:**
- Design workflow at 37signals
- Shape Up methodology in practice
- Designer-developer collaboration

**Technologies/Tools:**
- Basecamp
- Figma
- Design tools

**Summary:**
Provides insight into how product designers work at 37signals within the Shape Up framework. Shows the daily rhythm of design work, prototyping, and collaboration with programmers.

**Use Cases/Patterns:**
- Product design workflows
- Shape Up design cycles
- Cross-functional collaboration

**Developer Relevance:**
Useful for developers to understand the design process and how designers work within Shape Up cycles. Helps improve designer-developer collaboration.

---

### The 10x Development Environment
**Date:** November 29, 2022
**Author:** Jorge Manrubia
**Domain:** Developer Experience, Tooling

**Key Concepts:**
- Development environment optimization
- Fast feedback loops
- Developer productivity

**Technologies/Tools:**
- Ruby on Rails
- Development tooling
- Editor configuration

**Summary:**
Argues that optimizing the development environment for fast feedback loops can provide 10x productivity gains. Emphasizes the importance of quick test runs, fast server restarts, and efficient workflows.

**Use Cases/Patterns:**
- Optimizing development workflows
- Reducing feedback loop time
- Improving developer experience

**Developer Relevance:**
Reference when setting up development environments or identifying productivity bottlenecks. Shows how small optimizations compound into major productivity gains.

---

### Better Navigation in HEY
**Date:** December 1, 2022
**Author:** Javan Makhmali
**Domain:** Frontend, User Experience

**Key Concepts:**
- Navigation patterns
- Progressive enhancement
- Turbo navigation

**Technologies/Tools:**
- Turbo Drive
- Hotwire
- JavaScript

**Summary:**
Details improvements to HEY's navigation system using Turbo, making page transitions faster and smoother. Demonstrates progressive enhancement principles where JavaScript enhances but doesn't require complete rewrites.

**Use Cases/Patterns:**
- Implementing fast navigation in web apps
- Using Turbo Drive effectively
- Progressive enhancement strategies

**Developer Relevance:**
Consult when implementing navigation improvements with Turbo or understanding how to make page transitions feel instant.

---

### Compared to What?
**Date:** December 13, 2022
**Author:** David Heinemeier Hansson
**Domain:** Philosophy, Decision Making

**Key Concepts:**
- Comparative analysis in technical decisions
- Cost-benefit evaluation
- Alternative consideration

**Technologies/Tools:**
- Decision-making frameworks
- Technical evaluation

**Summary:**
Emphasizes the importance of asking "compared to what?" when evaluating technologies or approaches. Argues that decisions should be made relative to realistic alternatives, not theoretical perfection.

**Use Cases/Patterns:**
- Evaluating new technologies
- Making architectural decisions
- Comparing implementation approaches

**Developer Relevance:**
Apply when evaluating whether to adopt new tools, frameworks, or patterns. Helps avoid perfectionism and focus on practical improvements.

---

### Active Record Nice and Blended
**Date:** December 16, 2022
**Author:** Jorge Manrubia
**Domain:** Rails Architecture, Active Record

**Key Concepts:**
- Active Record pattern usage
- Balancing simplicity and complexity
- Model responsibility

**Technologies/Tools:**
- Ruby on Rails
- Active Record
- Database interactions

**Summary:**
Discusses how to use Active Record effectively by keeping models focused but not anemic. Shows how to blend database concerns with business logic appropriately without creating god objects.

**Use Cases/Patterns:**
- Organizing model logic
- Balancing Active Record with domain models
- Avoiding anemic or bloated models

**Developer Relevance:**
Reference when deciding where to place business logic in Rails applications. Helps find the right balance between thin and fat models.

---

## 2023

### Our Cloud Spend in 2022
**Date:** January 13, 2023
**Author:** David Heinemeier Hansson
**Domain:** Infrastructure, Cost Analysis

**Key Concepts:**
- Cloud infrastructure costs
- Cost analysis and optimization
- Cloud vs on-premise economics

**Technologies/Tools:**
- AWS
- Cloud infrastructure
- Cost analysis

**Summary:**
Reveals 37signals' cloud infrastructure costs for 2022, totaling millions of dollars. Provides detailed breakdown of spending across different AWS services, foreshadowing the eventual cloud exit.

**Use Cases/Patterns:**
- Understanding cloud cost structures
- Analyzing infrastructure spending
- Evaluating cloud economics

**Developer Relevance:**
Important context for understanding infrastructure costs at scale and the economics that drove 37signals' eventual cloud exit.

---

### Bringing Card Table to the Small Screen
**Date:** February 15, 2023
**Author:** Jay Ohms
**Domain:** Mobile, Responsive Design

**Key Concepts:**
- Mobile-first design adaptation
- Touch interactions
- Responsive layout patterns

**Technologies/Tools:**
- Hotwire Native
- Mobile web development
- Touch interfaces

**Summary:**
Describes the challenges and solutions for adapting Basecamp's Card Table (Kanban board) feature to mobile screens. Focuses on maintaining usability while adapting complex desktop interactions to touch interfaces.

**Use Cases/Patterns:**
- Adapting complex desktop UIs to mobile
- Implementing touch-friendly interactions
- Responsive design for data-heavy interfaces

**Developer Relevance:**
Consult when adapting complex desktop features to mobile or building touch-friendly interfaces for data manipulation.

---

### Pending Tests
**Date:** March 1, 2023
**Author:** Jorge Manrubia
**Domain:** Testing, Development Process

**Key Concepts:**
- Test-driven development workflow
- Pending test pattern
- Progressive implementation

**Technologies/Tools:**
- Minitest
- TDD practices
- Ruby testing

**Summary:**
Advocates for using pending tests as a workflow tool to outline implementation plans before writing code. Pending tests serve as a checklist and design tool, helping structure development.

**Use Cases/Patterns:**
- Test-driven development workflow
- Planning implementation with tests
- Breaking down complex features

**Developer Relevance:**
Useful when practicing TDD or planning complex feature implementations. Shows how tests can guide development beyond just verification.

---

### Bringing Our Apps Back Home
**Date:** March 21, 2023
**Author:** David Heinemeier Hansson
**Domain:** Infrastructure, Cloud Exit

**Key Concepts:**
- Cloud repatriation strategy
- On-premise infrastructure
- Cost optimization at scale

**Technologies/Tools:**
- AWS (exiting from)
- Bare metal servers
- Datacenter infrastructure

**Summary:**
Announces 37signals' decision to exit the cloud and move applications back to owned hardware. Details the economic rationale and expected multi-million dollar savings over five years.

**Use Cases/Patterns:**
- Evaluating cloud vs on-premise
- Large-scale infrastructure migration
- Cost optimization strategies

**Developer Relevance:**
Critical for understanding modern infrastructure decisions and when cloud might not be the optimal choice. Challenges the cloud-first orthodoxy.

---

### A Friday Email Incident
**Date:** May 29, 2023
**Author:** Matthew Kent
**Domain:** Incident Response, Reliability

**Key Concepts:**
- Incident management
- Post-mortem analysis
- System reliability

**Technologies/Tools:**
- Email infrastructure
- Monitoring systems
- Incident response procedures

**Summary:**
Detailed post-mortem of an email delivery incident in HEY, covering detection, response, and resolution. Emphasizes transparent communication and systematic incident handling.

**Use Cases/Patterns:**
- Incident response procedures
- Post-mortem documentation
- Root cause analysis

**Developer Relevance:**
Reference for incident response best practices and writing effective post-mortems. Shows how 37signals handles production incidents.

---

### Globals, Callbacks, and Other Sacrileges
**Date:** July 31, 2023
**Author:** David Heinemeier Hansson
**Domain:** Programming Philosophy, Rails Architecture

**Key Concepts:**
- Pragmatic programming choices
- Breaking conventional rules
- Context-appropriate solutions

**Technologies/Tools:**
- Ruby on Rails
- Global state
- Callbacks

**Summary:**
Defends the pragmatic use of globals, callbacks, and other typically-discouraged patterns when appropriate. Argues that dogmatic avoidance of certain patterns can lead to worse solutions than thoughtful application.

**Use Cases/Patterns:**
- When to use globals appropriately
- Effective callback usage
- Pragmatic vs dogmatic programming

**Developer Relevance:**
Important for understanding when to break rules pragmatically. Helps developers think critically about programming advice rather than following it blindly.

---

### 37signals Datacenter Overview
**Date:** August 10, 2023
**Author:** Ops Team
**Domain:** Infrastructure, Hardware

**Key Concepts:**
- Datacenter architecture
- Hardware provisioning
- Physical infrastructure

**Technologies/Tools:**
- Dell servers
- Networking equipment
- Datacenter facilities

**Summary:**
Provides detailed overview of 37signals' datacenter infrastructure after cloud exit, including hardware specifications, network topology, and facility details. Shows the physical infrastructure supporting their applications.

**Use Cases/Patterns:**
- Datacenter design and setup
- Hardware selection criteria
- Infrastructure redundancy

**Developer Relevance:**
Reference for understanding physical infrastructure requirements when moving off cloud. Shows what's needed to run applications on owned hardware.

---

### Prometheus Metrics at 37signals
**Date:** August 14, 2023
**Author:** Troy Rosenberg
**Domain:** Monitoring, Observability

**Key Concepts:**
- Metrics collection and monitoring
- Prometheus setup and usage
- Application instrumentation

**Technologies/Tools:**
- Prometheus
- Grafana
- Yabeda gem
- Ruby metrics instrumentation

**Summary:**
Details how 37signals uses Prometheus for metrics collection and monitoring across their infrastructure. Covers instrumentation patterns, metric types, and integration with Rails applications.

**Use Cases/Patterns:**
- Application metrics instrumentation
- Setting up Prometheus monitoring
- Creating meaningful metrics

**Developer Relevance:**
Essential reference for implementing Prometheus monitoring in Rails applications. Shows practical patterns for collecting and visualizing metrics.

---

### Minding the Small Stuff in PR Reviews
**Date:** August 30, 2023
**Author:** Jeremy Daer
**Domain:** Code Review, Team Process

**Key Concepts:**
- Code review best practices
- Attention to detail
- Constructive feedback

**Technologies/Tools:**
- GitHub
- Pull requests
- Code review process

**Summary:**
Advocates for paying attention to small details in code reviews, arguing that small improvements compound over time. Emphasizes that caring about code quality in reviews shapes overall codebase health.

**Use Cases/Patterns:**
- Effective code review practices
- Giving constructive feedback
- Maintaining code quality

**Developer Relevance:**
Apply when conducting or receiving code reviews. Helps establish standards for what matters in reviews and how to communicate feedback.

---

### Web Programming Internship
**Date:** August 31, 2023
**Author:** Jay Ohms
**Domain:** Hiring, Learning

**Key Concepts:**
- Internship program design
- Teaching web development
- Onboarding practices

**Technologies/Tools:**
- Ruby on Rails
- Web development fundamentals
- Mentorship

**Summary:**
Describes 37signals' web programming internship program, including curriculum, mentorship approach, and learning objectives. Shows how they train new developers in their practices and values.

**Use Cases/Patterns:**
- Designing internship programs
- Teaching Rails development
- Effective onboarding

**Developer Relevance:**
Useful for teams creating internship programs or onboarding processes. Shows how to structure learning experiences for new developers.

---

### Leaning Imperative
**Date:** September 5, 2023
**Author:** Jorge Manrubia
**Domain:** Programming Style, JavaScript

**Key Concepts:**
- Imperative vs declarative programming
- JavaScript style choices
- Code clarity and directness

**Technologies/Tools:**
- JavaScript
- Stimulus
- Frontend development

**Summary:**
Advocates for imperative programming style in JavaScript where it improves clarity, challenging the trend toward purely declarative or functional approaches. Argues that directness and obviousness trump abstraction.

**Use Cases/Patterns:**
- Writing clear JavaScript code
- Choosing between imperative and declarative styles
- Balancing abstraction and clarity

**Developer Relevance:**
Reference when writing JavaScript, especially with Stimulus. Helps make style decisions that prioritize readability and maintainability.

---

### 2023 Summer Interns
**Date:** September 15, 2023
**Author:** Jay Ohms
**Domain:** Team Culture, Learning

**Key Concepts:**
- Internship outcomes
- Real-world project experience
- Team integration

**Technologies/Tools:**
- Ruby on Rails
- Basecamp
- Real product work

**Summary:**
Showcases projects completed by summer interns, highlighting how they contributed real features to production applications. Demonstrates the effectiveness of hands-on learning with production code.

**Use Cases/Patterns:**
- Intern project selection
- Integrating interns into teams
- Measuring internship success

**Developer Relevance:**
Shows the kinds of projects interns can tackle and how to structure meaningful learning experiences that benefit both intern and company.

---

### Announcing Strada
**Date:** September 20, 2023
**Author:** Jay Ohms
**Domain:** Mobile, Hotwire

**Key Concepts:**
- Native bridge components
- Hybrid mobile development
- Progressive enhancement for mobile

**Technologies/Tools:**
- Strada
- Turbo Native
- JavaScript-to-native bridges
- iOS and Android

**Summary:**
Introduces Strada, the third piece of Hotwire for building high-fidelity native features in hybrid mobile apps. Strada enables web screens to trigger native UI components for better mobile experiences.

**Use Cases/Patterns:**
- Enhancing hybrid apps with native features
- Progressive enhancement for mobile
- Web-to-native communication

**Developer Relevance:**
Essential when building hybrid mobile apps that need native UI elements. Shows how to progressively enhance web views with platform-specific features.

---

### Navigating Personal Information with Care
**Date:** September 24, 2023
**Author:** Abraham Kuri
**Domain:** Security, Privacy

**Key Concepts:**
- Personal data handling
- Privacy-by-design
- Secure data practices

**Technologies/Tools:**
- Rails encryption
- Data protection patterns
- Privacy tools

**Summary:**
Discusses how 37signals handles personal information with care, including encryption strategies, data minimization, and privacy-conscious design. Emphasizes building privacy into systems from the start.

**Use Cases/Patterns:**
- Implementing data encryption
- Privacy-conscious architecture
- Secure data handling

**Developer Relevance:**
Critical reference when handling personal or sensitive data. Shows practical privacy and security patterns for Rails applications.

---

### Solid Cache
**Date:** October 3, 2023
**Author:** Donal McBreen
**Domain:** Performance, Caching

**Key Concepts:**
- Database-backed caching
- Cache implementation
- Removing Redis dependency

**Technologies/Tools:**
- Solid Cache gem
- MySQL/PostgreSQL
- Rails caching

**Summary:**
Introduces Solid Cache, a database-backed cache store for Rails that eliminates the need for Redis or Memcached. Uses efficient database techniques to provide fast caching without additional infrastructure.

**Use Cases/Patterns:**
- Implementing application caching
- Reducing infrastructure dependencies
- Database-backed caching strategies

**Developer Relevance:**
Reference when choosing caching strategies or simplifying infrastructure. Shows how to use relational databases effectively for caching.

---

### A Happier Happy Path in Turbo with Morphing
**Date:** October 9, 2023
**Author:** Jorge Manrubia
**Domain:** Frontend, Hotwire

**Key Concepts:**
- DOM morphing
- Turbo enhancements
- Smooth page updates

**Technologies/Tools:**
- Turbo
- Page morphing
- idiomorph algorithm

**Summary:**
Introduces morphing to Turbo, which updates pages by intelligently morphing the DOM rather than replacing it entirely. This preserves scroll position, form state, and other ephemeral UI state during updates.

**Use Cases/Patterns:**
- Implementing smooth page refreshes
- Preserving UI state during updates
- Progressive enhancement with Turbo

**Developer Relevance:**
Essential for building smooth, app-like experiences with Turbo. Shows how to update content without jarring page replacements.

---

### Exploring Server-Side Diffing in Turbo
**Date:** October 24, 2023
**Author:** Jorge Manrubia
**Domain:** Frontend, Hotwire

**Key Concepts:**
- Server-side rendering optimization
- Efficient DOM updates
- Diffing algorithms

**Technologies/Tools:**
- Turbo
- Server-side rendering
- DOM diffing

**Summary:**
Explores techniques for server-side diffing to send minimal updates to the browser. Discusses trade-offs between server-side and client-side diffing for optimal performance.

**Use Cases/Patterns:**
- Optimizing page update performance
- Reducing bandwidth for updates
- Server-side rendering strategies

**Developer Relevance:**
Reference when optimizing Turbo applications for minimal data transfer. Helps understand diffing strategies and their trade-offs.

---

### Building Basecamp Project Stacks with Hotwire
**Date:** November 7, 2023
**Author:** Jay Ohms
**Domain:** Frontend, Hotwire

**Key Concepts:**
- Complex UI with Hotwire
- Navigation stacks
- Progressive disclosure

**Technologies/Tools:**
- Turbo Frames
- Turbo Streams
- Stimulus
- Navigation patterns

**Summary:**
Details how Basecamp's project stacks feature was built entirely with Hotwire, demonstrating that complex, app-like UIs don't require heavy JavaScript frameworks. Shows navigation and state management patterns.

**Use Cases/Patterns:**
- Building complex UIs with Hotwire
- Navigation stack implementation
- Progressive disclosure patterns

**Developer Relevance:**
Essential case study for building sophisticated interfaces with Hotwire. Demonstrates that Hotwire can handle complex, stateful UIs.

---

### The Radiating Programmer
**Date:** November 19, 2023
**Author:** Jorge Manrubia
**Domain:** Communication, Team Culture

**Key Concepts:**
- Asynchronous communication
- Radiating information
- Remote work practices

**Technologies/Tools:**
- Basecamp
- Asynchronous communication
- Written communication

**Summary:**
Advocates for "radiating" information through clear, proactive communication rather than waiting to be asked. Emphasizes that remote work requires intentional information sharing.

**Use Cases/Patterns:**
- Effective remote communication
- Proactive status updates
- Asynchronous collaboration

**Developer Relevance:**
Critical for remote developers to understand how to communicate effectively. Shows how to work asynchronously while keeping teams aligned.

---

### Page Refreshes with Morphing Demo
**Date:** November 27, 2023
**Author:** Jorge Manrubia
**Domain:** Frontend, Hotwire

**Key Concepts:**
- Live demos of morphing
- Visual comparisons
- User experience improvements

**Technologies/Tools:**
- Turbo morphing
- Live demos
- Before/after comparisons

**Summary:**
Provides visual demonstrations of Turbo morphing in action, showing the difference between traditional page refreshes and morphing. Illustrates the UX improvements morphing provides.

**Use Cases/Patterns:**
- Demonstrating morphing benefits
- Understanding morphing behavior
- Visual learning

**Developer Relevance:**
Useful for understanding morphing behavior visually. Helps explain morphing benefits to stakeholders or team members.

---

### YJIT is Fast
**Date:** December 1, 2023
**Author:** Rosa Gutiérrez
**Domain:** Performance, Ruby

**Key Concepts:**
- Ruby performance optimization
- JIT compilation
- Production performance gains

**Technologies/Tools:**
- YJIT
- Ruby 3.x
- Performance profiling

**Summary:**
Reports significant performance improvements from enabling YJIT in production at 37signals. Shows measurable speed increases across HEY and Basecamp with minimal configuration.

**Use Cases/Patterns:**
- Enabling YJIT in production
- Measuring Ruby performance
- Easy performance wins

**Developer Relevance:**
Important for Ruby developers looking for performance improvements. Shows real-world YJIT benefits with production metrics.

---

### Introducing Solid Queue
**Date:** December 18, 2023
**Author:** Rosa Gutiérrez
**Domain:** Background Jobs, Infrastructure

**Key Concepts:**
- Database-backed job queue
- Removing Redis dependency
- Job processing reliability

**Technologies/Tools:**
- Solid Queue gem
- ActiveJob
- MySQL/PostgreSQL
- Job processing

**Summary:**
Introduces Solid Queue, a database-backed job processing system that eliminates the need for Redis. Provides reliable, persistent job queuing using the application database.

**Use Cases/Patterns:**
- Implementing background jobs
- Reliable job processing
- Simplifying infrastructure

**Developer Relevance:**
Essential reference for background job processing without Redis. Shows how to build reliable job systems on database storage.

---

## 2024

### Mission Control Jobs
**Date:** January 30, 2024
**Author:** Pablo Crivella
**Domain:** Operations, Job Management

**Key Concepts:**
- Job queue monitoring
- Operations dashboard
- Job management UI

**Technologies/Tools:**
- Mission Control - Jobs
- Solid Queue
- Web-based dashboard

**Summary:**
Introduces Mission Control - Jobs, a dashboard for monitoring and managing background jobs. Provides visibility into job queues, failures, and performance across different job backends.

**Use Cases/Patterns:**
- Monitoring background jobs
- Managing job queues
- Debugging job failures

**Developer Relevance:**
Critical tool for operating applications with background jobs. Reference when needing visibility into job processing.

---

### Turbo 8 Released
**Date:** February 7, 2024
**Author:** Jorge Manrubia
**Domain:** Frontend, Hotwire

**Key Concepts:**
- Turbo major version release
- Morphing by default
- View transitions API

**Technologies/Tools:**
- Turbo 8
- Page morphing
- View Transitions API
- Instant clicks

**Summary:**
Announces Turbo 8 with morphing as the default refresh method, bringing smooth page updates to all Turbo applications. Includes View Transitions API support and instant click responses.

**Use Cases/Patterns:**
- Upgrading to Turbo 8
- Using page morphing
- Smooth page transitions

**Developer Relevance:**
Important for Hotwire developers to understand new default behaviors and upgrade considerations. Shows evolution of Turbo's approach to page updates.

---

### Speeding Up Mobile Development with Turbo
**Date:** February 22, 2024
**Author:** Jay Ohms
**Domain:** Mobile, Development Workflow

**Key Concepts:**
- Mobile development workflow
- Hybrid app development speed
- Shared web code

**Technologies/Tools:**
- Turbo Native
- iOS development
- Android development
- Web views

**Summary:**
Explains how using Turbo Native dramatically speeds up mobile development by sharing most code with the web application. Shows how web-first development reduces platform-specific work.

**Use Cases/Patterns:**
- Accelerating mobile development
- Sharing code across platforms
- Hybrid app development

**Developer Relevance:**
Essential for teams considering mobile app development. Shows how to leverage web skills for mobile without sacrificing quality.

---

### Adventures Hunting Down a Ruby Memory Leak
**Date:** March 7, 2024
**Author:** Jorge Manrubia
**Domain:** Debugging, Performance

**Key Concepts:**
- Memory leak investigation
- Ruby debugging techniques
- Production troubleshooting

**Technologies/Tools:**
- Ruby memory profiling
- Heap dumps
- ObjectSpace
- Production debugging

**Summary:**
Chronicles the investigation and resolution of a subtle memory leak in a Rails application. Demonstrates debugging techniques, profiling tools, and systematic problem-solving approaches.

**Use Cases/Patterns:**
- Debugging memory leaks
- Using Ruby profiling tools
- Production troubleshooting

**Developer Relevance:**
Critical reference when investigating memory issues in Ruby applications. Shows systematic debugging approach and useful tools.

---

### Thruster Released
**Date:** March 7, 2024
**Author:** Kevin McConnell
**Domain:** Infrastructure, Deployment

**Key Concepts:**
- HTTP/2 proxy
- Asset caching
- X-Sendfile support

**Technologies/Tools:**
- Thruster
- HTTP/2
- Asset serving
- Deployment

**Summary:**
Introduces Thruster, a lightweight HTTP/2 proxy for Rails applications that handles asset caching, compression, and X-Sendfile. Simplifies deployment by providing essential proxy features.

**Use Cases/Patterns:**
- Deploying Rails applications
- Asset serving optimization
- Simple HTTP/2 setup

**Developer Relevance:**
Reference when deploying Rails applications and needing a simple proxy solution. Alternative to nginx for basic needs.

---

### Modern CSS Patterns and Techniques in Campfire
**Date:** April 4, 2024
**Author:** Daniel Loder
**Domain:** Frontend, CSS

**Key Concepts:**
- Modern CSS features
- Container queries
- CSS Grid and Flexbox
- No-build CSS

**Technologies/Tools:**
- CSS Grid
- Container Queries
- CSS Variables
- Modern CSS

**Summary:**
Showcases modern CSS techniques used in Campfire, demonstrating that contemporary CSS can replace many JavaScript-heavy solutions. Emphasizes using native CSS features over build tools.

**Use Cases/Patterns:**
- Modern CSS layout techniques
- Responsive design without media queries
- No-build CSS approaches

**Developer Relevance:**
Important for frontend developers wanting to use modern CSS effectively. Shows what's possible with CSS alone.

---

### Mission Control Web
**Date:** May 9, 2024
**Author:** Jorge Manrubia
**Domain:** Operations, Monitoring

**Key Concepts:**
- Web console for Rails
- Production debugging
- Safe production access

**Technologies/Tools:**
- Mission Control - Web
- Rails console
- Web-based tools

**Summary:**
Introduces Mission Control - Web, providing web-based access to Rails console and other operational tools. Enables safe production debugging through a web interface.

**Use Cases/Patterns:**
- Safe production console access
- Web-based debugging
- Operations tooling

**Developer Relevance:**
Useful when needing to access production console safely. Shows how to provide operational tools without SSH access.

---

### Kamal Prometheus
**Date:** May 23, 2024
**Author:** Kevin McConnell
**Domain:** Monitoring, Deployment

**Key Concepts:**
- Kamal integration with Prometheus
- Automated metrics setup
- Container monitoring

**Technologies/Tools:**
- Kamal
- Prometheus
- Docker metrics
- Grafana

**Summary:**
Details how to integrate Prometheus monitoring with Kamal deployments for automatic container and application metrics. Simplifies monitoring setup for Kamal-deployed applications.

**Use Cases/Patterns:**
- Monitoring Kamal deployments
- Setting up Prometheus automatically
- Container metrics collection

**Developer Relevance:**
Essential when deploying with Kamal and needing monitoring. Shows automated setup patterns for observability.

---

### Homographic Spoofing
**Date:** June 25, 2024
**Author:** Abraham Kuri
**Domain:** Security, Email

**Key Concepts:**
- Email security
- Unicode homograph attacks
- User protection

**Technologies/Tools:**
- Email parsing
- Unicode normalization
- Security defenses

**Summary:**
Explains homographic spoofing attacks where visually similar characters deceive users, and how HEY defends against them. Shows practical security measures for email applications.

**Use Cases/Patterns:**
- Defending against spoofing attacks
- Email security measures
- Unicode handling

**Developer Relevance:**
Important for applications dealing with email or user-submitted content. Shows how to detect and prevent homograph attacks.

---

### The Gift of Constraints
**Date:** September 9, 2024
**Author:** Jorge Manrubia
**Domain:** Product Development, Philosophy

**Key Concepts:**
- Constraints as enablers
- Timeboxing
- Fixed time, variable scope
- Team size and productivity

**Technologies/Tools:**
- Shape Up methodology
- Basecamp workflow
- Project management

**Summary:**
Argues that constraints like timeboxing and small teams are gifts that force good decision-making rather than obstacles. Explains how 37signals uses constraints to maintain quality while shipping quickly.

**Use Cases/Patterns:**
- Setting project constraints
- Timeboxing work
- Small team organization

**Developer Relevance:**
Essential philosophy for understanding how to make trade-offs and prioritize. Shows how constraints improve rather than hinder shipping.

---

### Announcing Hotwire Native
**Date:** September 25, 2024
**Author:** Jay Ohms
**Domain:** Mobile, Hotwire

**Key Concepts:**
- Turbo Native evolution
- Strada integration
- Unified mobile framework

**Technologies/Tools:**
- Hotwire Native (iOS & Android)
- Bridge Components
- Path Configuration
- Native screens

**Summary:**
Announces Hotwire Native, consolidating Turbo Native and Strada into a unified framework for iOS and Android. Includes improved navigation, better defaults, and comprehensive documentation.

**Use Cases/Patterns:**
- Building hybrid mobile apps
- Progressive enhancement for mobile
- Web-to-native integration

**Developer Relevance:**
Critical for anyone building mobile apps with Hotwire. Shows the current recommended approach for hybrid mobile development.

---

### Kamal 2.0 Released
**Date:** September 26, 2024
**Author:** Donal McBreen
**Domain:** Deployment, Infrastructure

**Key Concepts:**
- Deployment simplification
- Custom proxy (kamal-proxy)
- Automatic HTTPS
- Multi-app single server

**Technologies/Tools:**
- Kamal 2.0
- kamal-proxy
- Let's Encrypt
- Docker deployments

**Summary:**
Announces Kamal 2.0 with custom-built proxy replacing Traefik, automatic HTTPS, and ability to deploy multiple apps to one server. Simplifies deployments for all scales.

**Use Cases/Patterns:**
- Deploying Rails applications
- Zero-downtime deployments
- Multi-app hosting

**Developer Relevance:**
Essential for modern Rails deployment. Shows how to deploy applications simply and efficiently without complex orchestration.

---

### Solid Queue 1.0 Released
**Date:** September 26, 2024
**Author:** Rosa Gutiérrez
**Domain:** Background Jobs, Infrastructure

**Key Concepts:**
- Production-ready job processing
- Database-backed queues
- Recurring jobs
- Mission Control integration

**Technologies/Tools:**
- Solid Queue 1.0
- PostgreSQL/MySQL
- ActiveJob
- Mission Control - Jobs

**Summary:**
Announces Solid Queue 1.0 after extensive production use at 37signals processing 20 million jobs daily. Includes recurring jobs, bulk operations, and comprehensive instrumentation.

**Use Cases/Patterns:**
- Production job processing
- Replacing Redis-based queues
- Recurring job scheduling

**Developer Relevance:**
Reference implementation for database-backed job processing. Shows production-proven patterns for reliable job handling.

---

### All About QA
**Date:** October 15, 2024
**Authors:** Michael Berger, Gabriel Monette
**Domain:** Quality Assurance, Testing

**Key Concepts:**
- Manual testing approach
- Shape Up integration
- Accessibility testing
- Holistic QA

**Technologies/Tools:**
- Basecamp Card Table
- BackstopJS
- Screen readers (NVDA, axe)
- Manual testing

**Summary:**
Describes 37signals' QA process with a two-person team testing across all products. Emphasizes manual testing, accessibility, and integration with Shape Up cycles rather than automated test suites.

**Use Cases/Patterns:**
- QA in agile/Shape Up workflows
- Manual testing strategies
- Accessibility testing

**Developer Relevance:**
Shows how small teams can maintain quality without extensive automation. Useful for understanding QA collaboration and accessibility testing.

---

### Mission Control Jobs 1.0 Released
**Date:** December 4, 2024
**Author:** Rosa Gutiérrez
**Domain:** Operations, Job Management

**Key Concepts:**
- Job queue dashboard maturity
- Production job management
- Recurring task support

**Technologies/Tools:**
- Mission Control - Jobs 1.0
- Solid Queue integration
- Resque support
- Basic HTTP authentication

**Summary:**
Announces version 1.0 of Mission Control - Jobs with support for recurring tasks, API-only apps, and improved security defaults. Used daily at 37signals for HEY and Basecamp.

**Use Cases/Patterns:**
- Managing production jobs
- Monitoring job queues
- Operating recurring tasks

**Developer Relevance:**
Essential tool for operating applications with Solid Queue or Resque. Shows mature patterns for job queue management.

---

### A Vanilla Rails Stack is Plenty
**Date:** December 12, 2024
**Author:** Jorge Manrubia
**Domain:** Rails Architecture, Philosophy

**Key Concepts:**
- Minimal dependencies
- Standard Rails stack
- Hotwire for frontend
- No-build approach

**Technologies/Tools:**
- Rails 8
- Hotwire
- Import maps
- Propshaft
- Solid libraries (cache, queue, cable)
- Minitest

**Summary:**
Advocates strongly for vanilla Rails with minimal dependencies as the optimal stack. Recommends Hotwire, import maps, Solid libraries, and avoiding front-end frameworks or excessive gems for maximum productivity.

**Use Cases/Patterns:**
- Starting new Rails applications
- Simplifying existing applications
- Choosing the Rails stack

**Developer Relevance:**
Foundational philosophy piece for Rails development. Essential reference when evaluating technology choices or starting projects.

---

### Announcing Hotwire Spark
**Date:** December 18, 2024
**Author:** Jorge Manrubia
**Domain:** Developer Experience, Hotwire

**Key Concepts:**
- Live reloading
- Hot module replacement
- Fast feedback loops
- No-build tooling

**Technologies/Tools:**
- Hotwire Spark
- Live reloading
- HTML morphing
- Stimulus HMR

**Summary:**
Introduces Hotwire Spark for smooth live reloading without build tools. Morphs HTML changes, hot-swaps Stimulus controllers, and reloads CSS instantly for fast development feedback.

**Use Cases/Patterns:**
- Development workflow optimization
- Live reloading setup
- No-build development

**Developer Relevance:**
Improves development experience dramatically. Shows how to get modern DX without complex build tooling.

---

## 2025

### Pure Storage Monitoring
**Date:** January 2, 2025
**Author:** Victor Bogo
**Domain:** Infrastructure, Monitoring

**Key Concepts:**
- Storage infrastructure monitoring
- Prometheus setup for storage
- On-premise observability

**Technologies/Tools:**
- Pure Storage FlashBlade
- Prometheus
- Pure OpenMetrics exporter
- Grafana

**Summary:**
Details monitoring setup for 10 petabytes of Pure Storage infrastructure, including Prometheus configuration, alert setup, and performance monitoring. Part of cloud exit infrastructure.

**Use Cases/Patterns:**
- Storage monitoring
- Infrastructure observability
- Alert configuration for storage

**Developer Relevance:**
Reference for monitoring large-scale storage infrastructure. Shows production monitoring patterns for on-premise systems.

---

### Announcing Hotwire Native 1.2
**Date:** April 23, 2025
**Author:** Jay Ohms
**Domain:** Mobile, Hotwire

**Key Concepts:**
- Route decision handlers
- Server-driven navigation
- Bottom tab navigation
- Mobile UX patterns

**Technologies/Tools:**
- Hotwire Native 1.2 (iOS & Android)
- Route decision handlers
- Historical location routes
- Tab bar controllers

**Summary:**
Major update to Hotwire Native with route decision handlers for flexible URL routing, server-driven navigation improvements, and built-in bottom tab support. Includes comprehensive new demo apps.

**Use Cases/Patterns:**
- Customizing mobile app routing
- Server-driven navigation
- Bottom tab navigation

**Developer Relevance:**
Important update for Hotwire Native developers. Shows evolved patterns for mobile app architecture and navigation.

---

### Introducing Action Push Native
**Date:** August 18, 2025
**Author:** Jacopo Beschi
**Domain:** Mobile, Infrastructure

**Key Concepts:**
- Push notification infrastructure
- Cloud exit for push services
- HTTP/2 persistent connections

**Technologies/Tools:**
- Action Push Native gem
- APNs (Apple Push Notifications)
- FCM (Firebase Cloud Messaging)
- HTTP/2

**Summary:**
Introduces Action Push Native gem for sending push notifications directly to Apple and Google services, replacing AWS SNS/Pinpoint. Uses HTTP/2 for significant performance improvements in job duration.

**Use Cases/Patterns:**
- Sending mobile push notifications
- Replacing cloud notification services
- High-volume notification sending

**Developer Relevance:**
Essential for Rails apps sending push notifications. Shows how to bypass cloud services for direct, faster notification delivery.

---

### Running Docker Registry On-Prem with Harbor
**Date:** August 24, 2025
**Author:** Farah Schüller
**Domain:** Infrastructure, DevOps

**Key Concepts:**
- Container registry migration
- Harbor setup and configuration
- Multi-datacenter replication
- Cost optimization

**Technologies/Tools:**
- Harbor
- Docker registry
- Pure Storage S3
- Terraform
- Chef

**Summary:**
Details migration from DockerHub and AWS ECR to self-hosted Harbor registry, achieving 25-second reduction in pull times and $5k annual savings. Includes comprehensive setup, replication, and migration scripts.

**Use Cases/Patterns:**
- Self-hosted container registry
- Multi-site replication
- Migrating from cloud registries

**Developer Relevance:**
Critical for teams considering registry self-hosting. Shows complete migration approach with performance improvements and cost savings.

---

### Announcing Lexxy: A New Rich Text Editor for Rails
**Date:** September 4, 2025
**Author:** Jorge Manrubia
**Domain:** Frontend, Text Editing

**Key Concepts:**
- Modern text editing
- Lexical framework integration
- Action Text improvement
- Markdown support

**Technologies/Tools:**
- Lexxy
- Lexical (Meta)
- Action Text
- Active Storage
- Markdown

**Summary:**
Introduces Lexxy, a new rich text editor for Rails based on Meta's Lexical framework. Brings better HTML semantics, Markdown support, syntax highlighting, and improved editing experience to Action Text.

**Use Cases/Patterns:**
- Rich text editing in Rails
- Markdown integration
- Modern editor implementation

**Developer Relevance:**
Important for applications needing rich text editing. Shows evolution beyond Trix with modern features and better foundation.

---

### The Rails Delegated Type Pattern
**Date:** December 19, 2025
**Authors:** Kimberly Rhodes, Fernando Olivares, Jeffrey Hardy
**Domain:** Rails Architecture, Design Patterns

**Key Concepts:**
- Delegated types pattern
- Recordings and recordables
- Immutable content models
- Tree-based organization
- Event sourcing patterns

**Technologies/Tools:**
- ActiveRecord::DelegatedType
- Rails polymorphic associations
- Event modeling
- Basecamp/HEY architecture

**Summary:**
Comprehensive explanation of the delegated type pattern powering Basecamp and HEY, where a main "recording" table delegates to specific "recordable" types. Includes immutability, version history, and efficient copying/moving.

**Use Cases/Patterns:**
- Modeling polymorphic content
- Version history implementation
- Efficient content copying
- Timeline/feed implementations
- Type-agnostic operations

**Developer Relevance:**
Foundational pattern for building scalable Rails applications with diverse content types. Essential for understanding 37signals architecture and when delegated types solve problems better than STI or polymorphic associations.

---

## Quick Reference by Topic

### Rails Architecture
- Domain-Driven Boldness (2022-06-13)
- Fractal Journeys (2022-09-18)
- Good Concerns (2022-10-10)
- Vanilla Rails is Plenty (2022-11-08)
- Active Record Nice and Blended (2022-12-16)
- Globals, Callbacks, and Other Sacrileges (2023-07-31)
- A Vanilla Rails Stack is Plenty (2024-12-12)
- The Rails Delegated Type Pattern (2025-12-19)

### Hotwire & Frontend
- Better Navigation in HEY (2022-12-01)
- A Happier Happy Path in Turbo with Morphing (2023-10-09)
- Exploring Server-Side Diffing in Turbo (2023-10-24)
- Building Basecamp Project Stacks with Hotwire (2023-11-07)
- Page Refreshes with Morphing Demo (2023-11-27)
- Turbo 8 Released (2024-02-07)
- Modern CSS Patterns and Techniques in Campfire (2024-04-04)
- Announcing Hotwire Spark (2024-12-18)
- Leaning Imperative (2023-09-05)
- Announcing Lexxy (2025-09-04)

### Mobile Development
- Bringing Card Table to the Small Screen (2023-02-15)
- Announcing Strada (2023-09-20)
- Speeding Up Mobile Development with Turbo (2024-02-22)
- Announcing Hotwire Native (2024-09-25)
- Announcing Hotwire Native 1.2 (2025-04-23)
- Introducing Action Push Native (2025-08-18)

### Infrastructure & Cloud Exit
- Our Cloud Spend in 2022 (2023-01-13)
- Bringing Our Apps Back Home (2023-03-21)
- 37signals Datacenter Overview (2023-08-10)
- Pure Storage Monitoring (2025-01-02)
- Running Docker Registry On-Prem with Harbor (2025-08-24)

### Performance & Optimization
- Faster Paging in HEY (2022-11-07)
- YJIT is Fast (2023-12-01)
- Adventures Hunting Down a Ruby Memory Leak (2024-03-07)
- Solid Cache (2023-10-03)

### Background Jobs & Operations
- Making Export Jobs More Reliable (2022-11-15)
- Introducing Solid Queue (2023-12-18)
- Mission Control Jobs (2024-01-30)
- Solid Queue 1.0 Released (2024-09-26)
- Mission Control Jobs 1.0 Released (2024-12-04)

### Deployment & DevOps
- Kamal 2.0 Released (2024-09-26)
- Thruster Released (2024-03-07)
- Kamal Prometheus (2024-05-23)

### Monitoring & Observability
- Prometheus Metrics at 37signals (2023-08-14)
- Mission Control Web (2024-05-09)
- Pure Storage Monitoring (2025-01-02)

### Security & Privacy
- Navigating Personal Information with Care (2023-09-24)
- Homographic Spoofing (2024-06-25)

### Testing & Quality
- Pending Tests (2023-03-01)
- All About QA (2024-10-15)

### Team & Process
- A Week in the Life of a Product Designer (2022-11-18)
- Minding the Small Stuff in PR Reviews (2023-08-30)
- Web Programming Internship (2023-08-31)
- 2023 Summer Interns (2023-09-15)
- The Radiating Programmer (2023-11-19)
- The Gift of Constraints (2024-09-09)

### Philosophy & Decision Making
- Compared to What? (2022-12-13)
- The 10x Development Environment (2022-11-29)
- Globals, Callbacks, and Other Sacrileges (2023-07-31)
- The Gift of Constraints (2024-09-09)
- A Vanilla Rails Stack is Plenty (2024-12-12)

### Incident Response
- A Friday Email Incident (2023-05-29)

---

## Technology Index

### Languages & Frameworks
- **Ruby on Rails**: Referenced in nearly all articles
- **JavaScript/Stimulus**: Modern CSS Patterns, Leaning Imperative, Hotwire articles
- **Swift/Kotlin**: Mobile development articles

### Hotwire Stack
- **Turbo**: Multiple articles on Turbo Drive, Frames, Streams, morphing
- **Stimulus**: Referenced in frontend articles
- **Strada/Hotwire Native**: Mobile enhancement articles

### Infrastructure
- **Kamal**: Deployment articles
- **Docker/Harbor**: Container registry article
- **Pure Storage**: Storage infrastructure
- **Prometheus/Grafana**: Monitoring articles

### Solid* Libraries
- **Solid Cache**: Caching without Redis
- **Solid Queue**: Job processing without Redis
- **Solid Cable**: Action Cable without Redis

### Tools & Gems
- **Thruster**: HTTP/2 proxy
- **Mission Control - Jobs**: Job queue dashboard
- **Mission Control - Web**: Web console
- **Action Push Native**: Push notifications
- **Lexxy**: Rich text editor
- **Hotwire Spark**: Live reloading

### Testing & QA
- **Minitest**: Testing framework
- **BackstopJS**: Visual regression testing
- **Accessibility tools**: axe, NVDA, Headings Map

---

## Pattern Quick Reference

### Architectural Patterns
- **Delegated Types**: The Rails Delegated Type Pattern
- **Concerns**: Good Concerns
- **Domain Modeling**: Domain-Driven Boldness
- **Event Sourcing**: The Rails Delegated Type Pattern (events)

### Performance Patterns
- **Cursor Pagination**: Faster Paging in HEY
- **Page Morphing**: Turbo morphing articles
- **Caching**: Russian doll caching, Solid Cache
- **YJIT**: Performance improvements

### Frontend Patterns
- **Progressive Enhancement**: Multiple Hotwire articles
- **Turbo Frames**: Component-based updates
- **Turbo Streams**: Real-time updates
- **No-build**: Import maps, Propshaft

### Mobile Patterns
- **Hybrid Apps**: Hotwire Native articles
- **Bridge Components**: Strada/Hotwire Native
- **Progressive Enhancement**: Native features on demand

### Infrastructure Patterns
- **Database-backed Services**: Solid Cache, Solid Queue, Solid Cable
- **Multi-datacenter**: Harbor replication
- **Monitoring**: Prometheus patterns

---

This comprehensive guide covers all 56 articles and serves as a quick reference for developers working with Rails, Hotwire, infrastructure, or following 37signals practices. Use the topic and technology indexes to find relevant articles quickly.
