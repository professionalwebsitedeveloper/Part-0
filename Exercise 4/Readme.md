# My Project

## Architecture

### Note Creation Flow

```mermaid
flowchart TD
    A["User submits form"] --> B["JS: e.preventDefault() Stop default form behavior"]
    B --> C["Create note object with content & timestamp"]
    C --> D["Send POST to /new_note_spa with JSON data"]
    D --> E["Server: Add note to array Return 201 Created"]
    E --> F["JS: Add note to local array"]
    F --> G["JS: Update DOM redrawNotes()"]
    G --> H["JS: Clear form field"]
    H --> I["User sees new note immediately No page reload"]
