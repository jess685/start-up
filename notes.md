### GitHub
Git provides two things, 1) Version tracking in a repository, and 2) the ability to clone a copy of the repository to a different location.

GitHub is going to be used for three things:
1. Hosting all of this instruction. Because it is hosted on GitHub you can generate pull requests when you see things that need improvement.
2. Publicly hosting your project repositories. This creates a backup copy of your code, demonstrates your progress with your commit history, allows for reviews of your code, and makes it so you can collaborate with your peers. 
3. Keeping notes about what you have learned and things you want to remember

Pattern for development process:
- Pull the repository's latest changes from GitHub (git pull)
- Make changes to the code
- Commit the changes (git commit)
- Push the changes to GitHub (git push)

### SSH Console Program
IP Address = ssh -i ~/keys/cs260.pem ubuntu@52.55.234.221
Domain Name = ssh -i ~/keys/cs260.pem ubuntu@princess

### Technologies
- HTML - Basic structural and organizational elements
- CSS - Styling and animating
- JavaScript - Interactivity (e.g. What happens when a user presses a button)
- React - Reactivity, components, and routing using the React web framework.
- Web service - Remote functions that your application calls on your, and someone else's, web server (e.g. saveScores, getWeather, chatWithFriend).
⚠ Note that in addition to calling your own service, you must include at least one call to a service that you didn't write. You can view a list of APIs here: https://github.com/public-apis/public-apis.
- Authentication: An input for your user to create an account and login. You will want to display the user's name after they login.
- Database data: A rendering of application data that is stored in the database. For Simon, this is the high scores of all players.
- WebSocket data: A rendering of data that is received from your server. This may be realtime data sent from other users (e.g. chat or scoring data), or realtime data that your service is generating (e.g. stock prices or latest high scores). For Simon, this represents every time another user creates or ends a game.

### My Use of Technologies
- HTML - Uses correct HTML structure for application. Three HTML pages. One for login, one for the quiz, and one for results.   
- CSS - Application styling that looks good on different screen sizes, uses good whitespace, color choice and contrast.  
- JavaScript - Provides login, calculating princess match scores, backend endpoint calls.  
- React - Provides login form, question and choice display, display other users results.  
- Service - Backend service supports the following: login, retrieving choices, submitting scores, retrieving results   
- DB/Login - Store users, user's choices, and results in database. Register and login users. Credentials securely stored in database. Can't take quiz unless authenticated.  
- WebSocket - As each user takes the quiz, their results are broadcast to all other users.

### AWS - Route 53
- Now that you own a domain name you can use it to create DNS records that will map domain names to IP addresses (A records) or other domain names (CNAME records). For the purposes of this class, you want your root domain name, and any subdomain of your root domain, to map to the IP address of the web server you created previously.
- By defining both a record for your root domain and a wildcard record for any subdomain of your root domain you can now navigate to your server with either your domain name or a subdomain. I purchased the domain name princess260.click can could reach my server by navigating my browser to princess260.click, simon.princess260.click, or startup.princess260.click.

### Start-up HTML
To start I deployed the Simon HTML to my production environment (onto the link https://simon.princess260.click).

To deploy I had to cd into the cs260 folder I had and then cd into the start-up folder within that. To deploy my startup application to my production environment I used the following script: ./deployFiles.sh -k ~/downloads/cs260.pem -h princess260.click -s startup   

I used VS Code to clone the Simon HTML and change the script to fit my version. I created three different folders containing the index.html, quiz.html, and results.html. To view the live updates I made to my html I used the Live Server VS Code extension so I could open them on another tab. The final html application is now available from my production environment and I can open the website https://startup.princess260.click to see the index.html and the other two html pages by clicking on the links. I additionally linked my GitHub startup repository to display on my application's home page. 
