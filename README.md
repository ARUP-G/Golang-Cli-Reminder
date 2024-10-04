# Golang CLI Reminder

This is a simple command-line reminder application written in Go. It allows users to set a reminder for a specific time and will display an alert message when the time is reached.

## Features

- Parse human-readable time strings (e.g., `14:30` for 2:30 PM).
- Display a desktop notification (using `beeep` library).
- Set reminders to alert with a custom message.
- Prevents setting reminders in the past.
  
## Prerequisites

Before running this application, make sure you have the following installed:

- [Go](https://golang.org/dl/) version 1.23 or above.
- [beeep](https://github.com/gen2brain/beeep) library for desktop notifications.
- [when](https://github.com/olebedev/when) library for parsing time.

To install the required libraries, use:

```bash
go get github.com/gen2brain/beeep
go get github.com/olebedev/when
```
## Usage
To run the application, use the following command:

```bash
Copy code
go run main.go <hh:mm> <reminder message>
Example
Set a reminder for 2:30 PM with a message "Meeting with client":
```

```bash
Copy code
go run main.go 14:30 "Meeting with client"
```
The reminder will trigger a desktop notification at 2:30 PM with the message "Meeting with client."

### Notes
- The time should be in 24-hour format.
- The program prevents reminders from being set in the past.
- The reminder is displayed using the system's notification system (works on macOS, Windows, and Linux).

## File Structure
- *main.go*: The main Go file with the reminder logic.
- *assets/*: This folder should contain the icons or images for notifications. (Optional)

## How It Works
- The application takes a time string and message as input.
- It parses the time using the when library.
- If the time is valid and in the future, it calculates the time difference.
- The reminder is scheduled to show a notification using the beeep library after the specified duration.
- If you attempt to set a reminder for the past, the application will notify you.

## Error Handling
- If the time cannot be parsed, or the time is in the past, the application will exit with an appropriate message and error code.
- The application gracefully handles errors related to executing the reminder command or displaying notifications.

## License
This project is open-source and available under the MIT License.
