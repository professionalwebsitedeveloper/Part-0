# My Project

## Architecture

### Note Creation Flow

```mermaid
sequenceDiagram
    participant User
    participant Browser
    participant Server
    
    Note left of User: User types note and clicks Save
    Browser->>Server: POST /new_note
    activate Server
    Server-->>Browser: HTTP 302 Redirect
    deactivate Server
    Browser->>Server: GET /notes
    activate Server
    Server-->>Browser: HTML document
    deactivate Server
