# Single Page Application (SPA)

## Architecture Overview

```mermaid
flowchart TD
    A[User navigates to /spa] --> B[Browser GETs spa.html]
    B --> C[Browser GETs main.css]
    C --> D[Browser GETs spa.js]
    D --> E[Browser executes spa.js]
    E --> F[spa.js fetches data.json]
    F --> G[Server returns JSON]
    G --> H[JS renders notes with DOM]
    H --> I[Page is ready<br/>No further reloads needed]
