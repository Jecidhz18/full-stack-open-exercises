sequenceDiagram
    participant User
    participant Browser
    participant Server

    Note over User: Escribe una nueva nota "Hello Hn"
    User->>Browser: Hace click en el input type submit "Save" 
    Note over Browser: En el documento spa.js el controlador de eventos <br> crea una nueva nota, la agrega a la lista de notas <br> y vuelve a renderizar la lista en la página y <br> envía la nueva nota al servidor
    Browser->>Server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    Server-->>Browser: Responde con un código de estado HTTP 201 Created