# start-up
## Specification Deliverable
### Elevator Pitch
### Design
### Key Features
Secure login over HTTPS
Ability to select the question to decide
Display of choices
Ability to select, and change, top three choices
Totals from all users displayed in realtime
Ability for a user to lock in their top three
Results are persistently stored
Ability for admin to create and delete questions

### Technologies
I am going to use the required technologies in the following ways.

HTML - Uses correct HTML structure for application. Two HTML pages. One for login and one for voting. Hyperlinks to choice artifact.
CSS - Application styling that looks good on different screen sizes, uses good whitespace, color choice and contrast.
React - Provides login, choice display, applying votes, display other users votes, and use of React for routing and components.
Service - Backend service with endpoints for:
login
retrieving choices
submitting votes
retrieving vote status
DB/Login - Store users, choices, and votes in database. Register and login users. Credentials securely stored in database. Can't vote unless authenticated.
WebSocket - As each user votes, their votes are broadcast to all other users.

## HTML
Uses correct HTML structure for application. Two HTML pages. One for login and one for voting. Hyperlinks to choice artifact.
## CSS
Application styling that looks good on different screen sizes, uses good whitespace, color choice and contrast.
## JavaScript
Provides login, choice display, applying votes, display other users votes, backend endpoint calls.
## React
Single page application with views componentized and reactive to user's actions.
## Service
Backend service with endpoints for:
## DB/Login
Store users, choices, and votes in database. Register and login users. Credentials securely stored in database. Can't vote unless authenticated.
## WebSocket
As each user votes, their votes are broadcast to all other users.
