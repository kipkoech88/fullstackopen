```mermaid
    participant browser
    participant server

    browser->> server: POST https://studies.cs.helsinki.fi
    activate server
    server->> browser: 302 REDIRECT https://studies.cs.helsinki.fi/...
    deactivate server
    browser->> server: GET https://studies.cs.helsinki.fi/...
    activate server
    server->> browser: HTML-code
    deactivate server
    browser->> server: GET https://studies.cs.helsinki.fi/...
    activate server
    server->> browser: HTML-code
    deactivate server
    
```