```mermaid
sequenceDiagram
    participant user as User
    participant browser as Browser
    participant server as Server

    user->>browser: Types a note and clicks "Save" on https://studies.cs.helsinki.fi/exampleapp/spa
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/spa/new_note
    activate server
    server-->>browser: 201 Created or Updated Notes Data
    deactivate server
    Note right of browser: The SPA dynamically adds the new note to the list.
```