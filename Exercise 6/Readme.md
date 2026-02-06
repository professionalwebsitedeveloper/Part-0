# Project Documentation

## Flowchart

```mermaid
flowchart TD
    A[User submits form] --> B[Browser sends POST to /new_note]
    B -->|becomes| C[s2b]
    C --> D[The browser follows the redirect and GETs /notes]
    D --> E[HTML returned by server]
    E --> F[CSS is retrieved by the browser]
    F --> G[JavaScript is retrieved by the browser]
    G --> H[Browser GETs /data.json, runs JS]
    H --> I[The server responds with JSON containing the new note]
    I --> J[Browser displays notes]
