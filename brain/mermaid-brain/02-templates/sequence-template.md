# Sequence Diagram Template

Actor interaction sequence. Copy and adapt.

## Basic request-response

```mermaid
sequenceDiagram
    participant Client
    participant Service
    participant Store

    Client->>Service: Request(data)
    Service->>Store: Query(key)
    Store-->>Service: Result
    Service-->>Client: Response(result)
```

## With activation and notes

```mermaid
sequenceDiagram
    participant User
    participant API
    participant Auth
    participant DB

    User->>+API: POST /login
    API->>+Auth: Validate credentials
    Auth->>DB: Lookup user
    DB-->>Auth: User record
    Auth-->>-API: Token
    API-->>-User: 200 OK + Token

    Note over User,API: Token is short-lived
```

## With loop and alt blocks

```mermaid
sequenceDiagram
    participant Producer
    participant Queue
    participant Consumer

    loop Every 5 seconds
        Producer->>Queue: Publish(event)
    end

    Queue->>Consumer: Deliver(event)

    alt Success
        Consumer-->>Queue: Ack
    else Failure
        Consumer-->>Queue: Nack
        Queue->>Consumer: Redeliver(event)
    end
```

## Placeholder legend

| Placeholder | Replace with                        |
|-------------|-------------------------------------|
| `Client`    | Initiating actor (user, service)    |
| `Service`   | Processing actor                    |
| `Store`     | Storage or downstream dependency    |
| `Request()` | Actual operation name and payload   |
| `Result`    | Actual return value or status       |
