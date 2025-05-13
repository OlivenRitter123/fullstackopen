sequenceDiagram

    participant user
    participant browser
    participant server

    user->>browser: Write note and click 'Save'

    Note right of browser: JavaScript captures input and prepares POST request

    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa (with note content)
    activate server
    server-->>browser: 201 Created (or similar response)
    deactivate server

    Note right of browser: JavaScript updates the note list and renders it dynamically
