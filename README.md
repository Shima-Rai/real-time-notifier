# real-time-notifier
The Real-Time Event Notifier API is a backend service designed to help users manage and stay informed about important events, such as meetings, deadlines, and reminders. This API provides essential functionality for creating events, sending real-time notifications, handling event overlaps, and logging completed events for future reference. The system is optimized for real-time interaction and automated event tracking, making it ideal for use cases where users need timely reminders or alerts about their scheduled tasks.
Features:
- Create events: Allows users to create events with a title, description, start time, and end time.
- Real-time notifications: Sends real-time notifications 5 minutes before an event starts using WebSockets.
- Event overlap detection: Checks if a new event overlaps with any existing events.
- Logging: Logs completed events to a file asynchronously for future reference.
Requirements
- Node.js (v16 or later) – [Download Node.js](https://nodejs.org/)
- SQLite – Used for storing event data.
- WebSocket – For sending real-time notifications.
- node-cron– A Node.js package for scheduling tasks, such as sending notifications before events start.
1. Project Overview
  Description: A short explanation of what the API does (Real-Time Event Notifier).
  Features:
  Creating events with title, description, start and end times.
  Sending real-time notifications via WebSockets.
  Detecting event overlaps before adding new events.
  logging completed events for historical reference.
3. Requirements
  List of software required to run the project:
  Node.js (v16 or later)
  SQLite (for storing events)
  WebSocket (for real-time notifications)
4. Setup and Installation
  Instructions for setting up and running the project:
  Clone the repository.
  Install dependencies using npm install.
  Set up environment variables with .env (including PORT and DB_FILE).
  Run the application with npm start.
5. API Endpoints
  Descriptions and examples for the API endpoints:
  POST /events: Create a new event with details (title, description, start time, and end time).
  GET /events: Retrieve a list of all upcoming events.
  WebSocket notifications: Real-time notifications sent 5 minutes before an event starts.
  GET /completed-events: Fetch completed events from the log (if implemented).
  Example JSON responses for each endpoint, including:
  Successful creation of events.
  Overlapping event errors with details about the conflict.
6. Testing the API with Postman
  Detailed steps for testing the API using Postman:
  How to send a POST /events request to create a non-overlapping event.
  How to send a POST /events request to create an event with an overlap.
  Expected error response (409 Conflict) for overlapping events.
  How to retrieve events using GET /events.
  How to use WebSocket for receiving real-time notifications.
7. Logs and File Storage
  Information about logging completed events asynchronously to a file (completed_events.log).
  Example of a log entry format in the file.
8. Troubleshooting
  Common errors to look out for:
  Missing fields in the request body.
  Invalid date format.
Suggested solutions for these common issues.
9. Future Enhancements
A section outlining possible future improvements:
Better error handling.
More robust database solutions.
Enhanced WebSocket error handling and reconnection logic.
