```mermaid
    sequenceDiagram
    participant browser
    participant server

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server

    Note right of server: The server saves the note

    server-->>browser: 201 Created {"message":"note created"}
    deactivate server

    Note right of browser: The browser renders the notes

```