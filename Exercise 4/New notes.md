sequenceDiagram
    participant User
    participant Browser
    participant Server

    Note left of User: User types note and clicks Save
    
    Browser->>Server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
    Note over Browser,Server: Request body: note=[new_note_content]
    activate Server
    Server-->>Browser: HTTP 302 Redirect to /notes
    deactivate Server
    
    Note over Browser: Browser follows redirect
    
    Browser->>Server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    activate Server
    Server-->>Browser: HTML document
    deactivate Server
    
    Browser->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    activate Server
    Server-->>Browser: CSS file
    deactivate Server
    
    Browser->>Server: GET https://studies.cs.helsinki.fi/exampleapp/main.js
    activate Server
    Server-->>Browser: JavaScript file
    deactivate Server
    
    Note over Browser: Browser executes JS which fetches JSON data
    
    Browser->>Server: GET https://studies.cs.helsinki.fi/exampleapp/data.json
    activate Server
    Server-->>Browser: JSON array including new note
    deactivate Server
    
    Note over Browser: Browser renders notes including the new note
    Note left of User: User sees their note appear in the list
