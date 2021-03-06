# Crypto Mail


## HTTP Proxy (Client) features:
- Parse HTTP requests, including requests for binary data - sends back a response dynamically based on the nature of the request
- Manage state with sessions - keeps an open connection to the main server once a user makes a successful authentication request
- Full authentication for users
- Display inbox of received emails
- Read/Write emails - including writing to multiple recipients
- Read/Write encrypted emails - prompt recipient for Key upon opening of message
- Modern browser-based UI

## Server Changes:
- Database Implemented - All data (Users, Notifications, Emails) is now stored in a MySQL database, rather than saved within files
- Authentication optimized - better password hashing

## Other Details:
- HTTP Proxy - Received emails that are opened by a user are cached for the duration of the users session, allowing instant re-opening and no delay when decrypting message. Also lightens DB load
- HTML wrapping - Content is wrapped with HTML from standard .html files, allowing for easy customization of the UI


## Features in progress:
- Tags - Implementing tags which a user can add to their recieved messages to optimize searching
- Attachments - Implementing the ability to attach files from the browser, and subsequently store a reference to attachments within database
