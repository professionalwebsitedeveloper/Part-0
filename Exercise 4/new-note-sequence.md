flowchart TD
    A[User submits form] --> B[JS: e.preventDefault()<br/>Stop default form behavior]
    B --> C[Create note object<br/>with content & timestamp]
    C --> D[Send POST to /new_note_spa<br/>with JSON data]
    D --> E[Server: Add note to array<br/>Return 201 Created]
    E --> F[JS: Add note to local array]
    F --> G[JS: Update DOM<br/>redrawNotes()]
    G --> H[JS: Clear form field]
    H --> I[User sees new note immediately<br/>No page reload]
