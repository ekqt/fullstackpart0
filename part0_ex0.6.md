title Notes: SPA Sequence Diagram

note over browser:
User submits form and sends 
data as a HTTP POST request 
to the server address new_note_spa
end note

browser->server: HTTP POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa

server-->browser:application/json; new_note_spa

note over browser:
Javascript pushes note,
rerenders notes and
the server responds with 
HTTP status code 201 (created)
sending the new note to server
end note

Created on: https://www.websequencediagrams.com/