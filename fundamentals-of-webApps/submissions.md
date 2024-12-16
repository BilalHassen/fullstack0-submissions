# 0.4

Button is clicked browser sends the text input by the user to the server at the “/new_note”
The submission causes 5 HTTP requests
Form submit event is POST request to address new_note
Server responds with 302 URL redirect
Server asks browser new HTTP GET request to the address in the defined in the headers location
Browser reloads the notes page and causes 3 more HTTP requests for the fetching the css js file and the notes data
Form tag has the action attribute and method which explains that submitting the form is done using the HTTP POST to the address in the in the action attribute
Code on the server handles adding the new note by creating a new object with the data of the note and the the date of creation

# 0.5

Form tag has no action or method attributes
Creating a new note browser only sends one request to the server
The Post request payload to new_note_spa contains the new note as JSON data with the note content and the timestamp
Content-type header of the request tells the server that the included data is on JSON format
Server responds with 201 created server does not ask for a redirect and does not send anymore HTTP requests
This version does not send the form data but it uses the javascript code it fetches form the server to handle the process
By using the DOM and selecting an the notes_form element reference and applying and event handler to handle the submit event of the form the event handler calls the method to prevent the default submission which causes a refresh
The event handler creates a new note, adds it to the notes list and rerenders the note list on the page and sends the new note to the server.
