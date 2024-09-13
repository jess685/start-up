# start-up
## Specification Deliverable
### Elevator Pitch
### Design
### Key Features
- Secure login over HTTPS
- Display of questions that determine result
- Display of answers to choose from 
- Ability to select, and change, choice for each question
- Results from all users displayed in realtime
- Ability for a user to save and share their results
- Results are persistently stored

### Technologies
I am going to use the required technologies in the following ways.

HTML - Uses correct HTML structure for application. Two HTML pages. One for login and one for the quiz. Hyperlinks to choice artifact.
CSS - Application styling that looks good on different screen sizes, uses good whitespace, color choice and contrast.
JavaScript - Provides login, choice display, applying scores, display other users results, backend endpoint calls.
React - Provides login, question display, choice display, applying score, display other users results, and use of React for routing and components.
Service - Backend service with endpoints for:
- login
- retrieving choices
- submitting scores
- retrieving results
DB/Login - Store users, choices, and results in database. Register and login users. Credentials securely stored in database. Can't take quiz unless authenticated.
WebSocket - As each user takes the quiz, their results are broadcast to all other users.

## HTML
Uses correct HTML structure for application. Two HTML pages. One for login and one for the quiz. Hyperlinks to choice artifact.
  HTML pages - Two HTML page that represent the ability to login and vote.
   Links - The login page automatically links to the voter page. The voter page contains links for every voting choice.
   Text - Each of the voting choices is represented by a textual description.
   Images - I couldn't figure out how to include an image and so I didn't do this. 
   DB/Login - Input box and submit button for login. The voting choices represent data pulled from the database.
   WebSocket - The count of voting results represent the tally of realtime votes.
   
## CSS
Application styling that looks good on different screen sizes, uses good whitespace, color choice and contrast.
  For this deliverable I properly styled the application into its final appearance.
   Header, footer, and main content body
   Navigation elements - I dropped the underlines and changed the color for anchor elements.
   Responsive to window resizing - My app looks great on all window sizes and devices
   Application elements - Used good contrast and whitespace
   Application text content - Consistent fonts
   Application images - Still don't have images and so no styling here. 
   
## JavaScript
Provides login, choice display, applying scores, display other users results, backend endpoint calls.
  For this deliverable I used JavaScript and React so that the application completely works for a single user. I also added placeholders for future technology.

   Bundled and transpiled - done!
   Components - Login, voting list, vote are all components with mocks for login, WebSocket.
   login - When you press enter or the login button it takes you to the voting page.
   database - Displayed the voting counts. Currently this is stored and retrieved from local storage, but it will be replaced with the database data later.
   WebSocket - I used the setInterval function to periodically increase a random vote count. This will be replaced with WebSocket messages later.
   application logic - The highlight and ranking number change based up the user's selections.
   Router - Routing between login and voting components.
   Hooks - Vue uses class properties instead of UseState to track changes in vote state.
   
## React
Single page application with views componentized and reactive to user's actions.
## Service
Backend service with endpoints for:
- login
- retrieving choices
- submitting scores
- retrieving results

    For this deliverable I added backend endpoints that receives votes and returns the voting totals.
   Node.js/Express HTTP service - done!
   Static middleware for frontend - done!
   Calls to third party endpoints - I didn't have time to implement this. 
   Backend service endpoints - Placeholders for login that stores the current user on the server. Endpoints for voting.
   Frontend calls service endpoints - I did this using the fetch function.
## DB/Login
Store users, choices, and results in database. Register and login users. Credentials securely stored in database. Can't take quiz unless authenticated.
  For this deliverable I associate the votes with the logged in user. I stored the votes in the database.
  MongoDB Atlas database created - done!
   Stores data in MongoDB - done!
   User registration - Creates a new account in the database.
   existing user - Stores the votes under the same user if the user already exists.
   Use MongoDB to store credentials - Stores both user and their votes.
   Restricts functionality - You cannot vote until you have logged in. This is restricted on the frontend only. 
## WebSocket
As each user votes, their votes are broadcast to all other users.
  For this deliverable I used webSocket to update the votes on the frontend in realtime.
   Backend listens for WebSocket connection - done!
   Frontend makes WebSocket connection - done!
   Data sent over WebSocket connection - done!
   WebSocket data displayed - All user votes display in realtime.
