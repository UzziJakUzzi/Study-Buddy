# Study-Buddy

This microservice provides a Pomodoro session timer that starts a 25-minute countdown and returns both start and end timestamps.

- Communication Contract

- How to Programmatically REQUEST Data

Send a `POST` request to: http://localhost:3001/start-pomodoro


- Example (JavaScript)

fetch("http://localhost:3001/start-pomodoro", {
  method: "POST",
  headers: {
    "Content-Type": "application/json"
  }
})
  .then(res => res.json())
  .then(data => console.log(data));

The server responds with a JSON object that includes:
- A confirmation message
- The timer's start_time (ISO 8601 format)
- The end_time (25 minutes later)

{
  "message": "Pomodoro timer started for 25 minutes.",
  "start_time": "2025-08-04T20:00:00Z",
  "end_time": "2025-08-04T20:25:00Z"
}

This diagram illustrates the communication between the test program and the Pomodoro timer microservice:
![UML Sequence Diagram](./uml-pomodoro.png)


- CORS enabled (via cors package)
- Run npm install to install dependencies:

bash
npm install express cors


Jackson Happel-Walvatne
Microservice A – Pomodoro Timer
Summer 2025 CS361



