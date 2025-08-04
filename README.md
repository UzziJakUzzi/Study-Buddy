# Study-Buddy
Communication Contract

// JavaScript example
fetch("http://localhost:3001/start-pomodoro", {
  method: "POST",
  headers: { "Content-Type": "application/json" },
})
.then(res => res.json())
.then(data => console.log(data));

{
  "message": "Pomodoro timer started for 25 minutes.",
  "start_time": "2025-08-04T20:00:00Z",
  "end_time": "2025-08-04T20:25:00Z"
}

![UML Sequence Diagram](./uml-pomodoro.png)
