# Architecture Diagram Template

System context and container diagrams using flowchart syntax (C4-inspired, renderer-safe).

## System context diagram (C4 Level 1)

Shows the system in relation to its users and external systems.

```mermaid
flowchart TD
    User([User])
    ExtSystemA([External System A])
    ExtSystemB([External System B])

    subgraph YourSystem
        Core[Core Service]
    end

    User -->|Uses| Core
    Core -->|Calls API| ExtSystemA
    Core -->|Reads data from| ExtSystemB
```

## Container diagram (C4 Level 2)

Shows the major containers (apps, services, stores) inside your system.

```mermaid
flowchart LR
    User([User])

    subgraph System
        WebApp[Web Application]
        API[API Service]
        Worker[Background Worker]
        DB[(Database)]
        Queue[(Message Queue)]
    end

    ExtService([External Service])

    User -->|HTTPS| WebApp
    WebApp -->|REST| API
    API --> DB
    API -->|Publish| Queue
    Worker -->|Subscribe| Queue
    Worker -->|Calls| ExtService
```

## Component diagram (C4 Level 3)

Shows the components inside one container.

```mermaid
flowchart TD
    subgraph APIService
        Router[Router]
        AuthMiddleware[Auth Middleware]
        Controller[Controller]
        Repository[Repository]
    end

    DB[(Database)]

    Router --> AuthMiddleware
    AuthMiddleware --> Controller
    Controller --> Repository
    Repository --> DB
```

## Placeholder legend

| Placeholder       | Replace with                             |
|-------------------|------------------------------------------|
| `YourSystem`      | Name of the system being documented      |
| `Core Service`    | Main processing component                |
| `External System` | Real name of the external dependency     |
| `User`            | Actual user type or persona              |
