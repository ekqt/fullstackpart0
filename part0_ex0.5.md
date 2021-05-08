title Notes: SPA Sequence Diagram

browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/spa
server-->browser: text/html; spa

browser->server: HTTP GET https://studies.cs.helsinki.fi/exampleapp/main.css
server-->browser: text/css; main.css

browser->server: https://studies.cs.helsinki.fi/exampleapp/spa.js
server-->browser: application/javascript; spa.js

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