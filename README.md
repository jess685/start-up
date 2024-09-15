# Which Disney Princess Are You?
## Specification Deliverable
### Elevator Pitch
Have you ever had countless debates with friends, family, and even co-workers on the debilitating question of which Disney Princess truly represents you? It is now time to find out once and for all: which Disney Princess are you? Each user will be presented with a series of questions and can choose the answer that fits them best. The results will be automatically calculated and displayed at the end of the quiz. You are given the option to save and share your results with other users. I can guarentee your life will be permanently after this moment. Your Welcome. 

If you don't agree with your results, just take the quiz again! What truly defines a princess is persuing your own personal happily ever after.

### Design
<img width="782" alt="Screenshot 2024-09-14 at 6 02 23 PM" src="https://github.com/user-attachments/assets/944962aa-4f0c-4235-8e8c-78b61f489293">
<img width="779" alt="Screenshot 2024-09-14 at 11 19 33 PM" src="https://github.com/user-attachments/assets/ad4f68a0-84a0-4a4d-860e-e9fed0365498">

### Key Features
- Secure login over HTTPS
- Display of questions that determine result
- Display of answers to choose from 
- Ability to select, and change, choice for each question
- Results from most recent users displayed 
- Ability for a user to save and share their results
- Results are persistently stored

### Technologies
I am going to use the required technologies in the following ways.

HTML - Uses correct HTML structure for application. Three HTML pages. One for login, one for the quiz, and one for results. 
CSS - Application styling that looks good on different screen sizes, uses good whitespace, color choice and contrast.
JavaScript - Provides login, calculating princess match scores, backend endpoint calls.
React - Provides login form, question and choice display, display other users results.
Service - Backend service supports the following:
- login
- retrieving choices
- submitting scores
- retrieving results
DB/Login - Store users, user's choices, and results in database. Register and login users. Credentials securely stored in database. Can't take quiz unless authenticated.
WebSocket - As each user takes the quiz, their results are broadcast to all other users.

## HTML
Uses correct HTML structure for application. Three HTML pages. One for login, one for the quiz, and one for results. 
   HTML pages - Three HTML page that represent the ability to login, take the quiz, and view results as well as other user's results.
   Links - The login page automatically links to the quiz page which in turn links to the results page
   Text - Each of the choices for the questions and results is represented by a textual description.
   Images - An image of each princess will be linked to the result of the quiz. 
   DB/Login - Input box and submit button for login. The quiz results represent data pulled from the database.
   WebSocket - The quiz results are represented to other users.
   
## CSS
Application styling that looks good on different screen sizes, uses good whitespace, color choice and contrast.
   For this deliverable I properly styled the application into its final appearance.
   Header, footer, and main content body
   Navigation elements - I dropped the underlines and changed the color for anchor elements.
   Responsive to window resizing - My app looks great on all window sizes and devices
   Application elements - Used good contrast and whitespace
   Application text content - Consistent fonts
   Application images - Images are linked to results. 
   
## React
Provides login, question and choice display, calculating princess match scores, display other users results, backend endpoint calls.
   For this deliverable I will use JavaScript and React so that the application completely works for a single user. 
   Components - Login and calculating similarity scores.
   Login - When you press enter or the login button it takes you to the quiz page. 
   Database - Displayed the questions, choice, results, and other user's results.
   Application logic - The results will be calculated by the similarity between the user's score with the princesses scores.
   Router - Routing between login and quiz components

## Service
Backend service with endpoints for:
- login
- retrieving choices
- submitting scores
- retrieving results
   For this deliverable I will add backend endpoints that receives scores and returns the results.
   Backend service endpoints - Placeholders for login that stores the current user on the server. Endpoints for results.
  
## DB/Login
Store users, user's choices, and results in database. Register and login users. Credentials securely stored in database. Can't take quiz unless authenticated.
   For this deliverable I associate the results with the logged in user. I stored the results in the database.
   User registration - Creates a new account in the database.
   Existing user - Stores the results under the same user if the user already exists.
   Use MongoDB to store credentials - Stores both user and their votes.
   Restricts functionality - You cannot take the quiz until you have logged in. 
   
## WebSocket
As each user takes the quiz, their results are broadcast to all other users.
   For this deliverable I used webSocket to update the results on the frontend in realtime.
   Backend listens for WebSocket connection 
   Frontend makes WebSocket connection 
   Data sent over WebSocket connection 
   WebSocket data displayed - Recent user results display in realtime.
