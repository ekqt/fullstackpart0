title Notes: AJAX Sequence Diagram

note over browser:
User submits form and sends 
data as a HTTP POST request 
to the server address new_note
end note

browser->server: HTTP POST https://studies.cs.helsinki.fi/exampleapp/new_note

server-->browser:text/html; new_note

note over browser:
The server responds with 
HTTP status code 302 (redirect) 
to /exampleapp/notes
end note

browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/notes
server-->browser: text/html; notes

browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.css
server-->browser: text/css; main.css

browser->server: https://studies.cs.helsinki.fi/exampleapp/main.js
server-->browser: application/javascript; main.js

note over browser:
browser starts executing javascript code 
that requests JSON data from server
end note

browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/data.json
server-->browser: HTTP application/json; data.json

note over browser:
browser executes the event handler
on readyState == 4 (DONE) && 
HTTP Status 200
end note

Created on: https://www.websequencediagrams.com/
