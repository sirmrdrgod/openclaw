# Flowchart Template

Generic process flowchart. Copy and adapt.

## Top-down process flow

```mermaid
flowchart TD
    A([Start]) --> B[Step One]
    B --> C{Decision?}
    C -->|Yes| D[Step Two A]
    C -->|No| E[Step Two B]
    D --> F[Step Three]
    E --> F
    F --> G([End])
```

## Left-to-right pipeline flow

```mermaid
flowchart LR
    A([Input]) --> B[Stage One]
    B --> C[Stage Two]
    C --> D{Gate}
    D -->|Pass| E[Stage Three]
    D -->|Fail| F[Rework]
    F --> B
    E --> G([Output])
```

## With subgraphs

```mermaid
flowchart TD
    subgraph Phase1
        A[Task A] --> B[Task B]
    end
    subgraph Phase2
        C[Task C] --> D[Task D]
    end
    Phase1 --> Phase2
```

## Placeholder legend

| Placeholder | Replace with                              |
|-------------|-------------------------------------------|
| `Start`     | Name of the trigger event or entry point  |
| `Step One`  | First action or process step              |
| `Decision?` | The question at the branch point          |
| `Yes` / `No`| Actual condition labels                   |
| `End`       | Outcome or exit point                     |
