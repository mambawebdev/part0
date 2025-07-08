



## Part 0 - 0.6: New note in Single page app diagram
```mermaid

sequenceDiagram
participant browser
participant server
Note right of browser: Post request made after client has saved the input
browser-->server: POST REQUEST https://studies.cs.helsinki.fi/exampleapp/new_note
Note right of browser: POST request to the address new_note_spa notes contains the new note as JSON data 
Note right of browser: containing both note (content) and the timestamp(date)
activate server
    server-->>browser: HTTP Status Code: 201 Created, Content-Type: application/json
    Note left of server: Server replying with a Status Code 201 to create the note
    Note left of server: Without this header (Content-Type) the server would not know how to correctly parse the data.
deactivate server

```

