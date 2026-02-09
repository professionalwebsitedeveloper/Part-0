# My Project

## Architecture

### Note Creation Flow

```mermaid
flowchart TB
    A["User submits form"] --> B["JS: e.preventDefault()<br>Stop default form behavior"]
    B --> C["Create note object with<br>content & timestamp"]
    C --> D["Send POST to /new_note_spa<br>with JSON data"]
    D --> E["Server: Add note to array<br>Return 201 Created"]
    E --> F["JS: Add note to local array"]
    F --> G["JS: Update DOM<br>redrawNotes()"]
    G --> H["JS: Clear form field"]
    H --> I["User sees new note immediately<br>No page reload"]

    style A fill:#FF6D00,stroke:#00C853
    style B fill:#00C853
    style C fill:#00C853
    style D fill:#00C853
    style E fill:#00C853
    style F fill:#00C853
    style G fill:#00C853
    style H fill:#00C853,stroke:#00C853
    style I fill:#FF6D00,stroke:#00C853
