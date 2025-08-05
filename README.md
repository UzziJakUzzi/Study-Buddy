# Study-Buddy
Jackson Happel-Walvatne
Microservice A – Pomodoro Timer

This microservice provides a Pomodoro session timer that starts a 25-minute countdown and returns both start and end timestamps.

- Communication Contract

- How to Programmatically REQUEST Data

Send a `POST` request to:

[http://localhost:3001/start-pomodoro](http://localhost:3001/start-pomodoro)

Example (JavaScript):
```js
fetch("http://localhost:3001/start-pomodoro", {
  method: "POST",
  headers: { "Content-Type": "application/json" }
})
.then(res => res.json())
.then(data => console.log(data));
```


Use .then(response => response.json()) to parse the JSON response from the server.
The server responds with a JSON object like:
```
{
  "message": "Pomodoro timer started for 25 minutes.",
  "start_time": "2025-08-04T20:00:00Z",
  "end_time": "2025-08-04T20:25:00Z"
}
```
This diagram illustrates the communication between the test program and the Pomodoro timer microservice:

![UML Sequence Diagram](./UML%20-%20Pomodoro%20Timer%20Session.png)

Dependencies

- CORS enabled (via cors package)
  
Run this to install dependencies:
- bash:
  npm install express cors



