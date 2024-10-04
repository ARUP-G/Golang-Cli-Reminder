# Golang CLI Reminder

This is a simple command-line reminder application written in Go. It allows users to set a reminder for a specific time and will display an alert message when the time is reached.

## Features

- Parse human-readable time strings (e.g., `14:30` for 2:30 PM).
- Display a desktop notification (using `beeep` library).
- Set reminders to alert with a custom message.
- Prevents setting reminders in the past.
  
## Prerequisites

Before running this application, make sure you have the following installed:

- [Go](https://golang.org/dl/) version 1.16 or above.
- [beeep](https://github.com/gen2brain/beeep) library for desktop notifications.
- [when](https://github.com/olebedev/when) library for parsing time.

To install the required libraries, use:

```bash
go get github.com/gen2brain/beeep
go get github.com/olebedev/when
```

