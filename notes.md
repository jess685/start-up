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

### Start-up CSS
I created a new html page **others** to split the results of the quiz and other users results. I also linked all 10 questions of the quiz to the quiz html that automatically links to the results page after the 10th question

### Midterm
CS260 Midterm Topics/Questions Review

1. In the following code, what does the link element do?
The <link> element in HTML is used to link external resources to a document, typically stylesheets. It is commonly placed within the <head> section and is used to link to CSS files like this:
html
<link rel="stylesheet" href="styles.css">
This tells the browser to load and apply the styles.css file to the HTML page. <br/> 
2. In the following code,  what does a div tag do?  
The <div> element is a block-level container that is used to group other HTML elements. It doesn’t have any specific styling or semantic meaning by default but is often used with classes or IDs to style or organize sections of a page:
html
<div class="container">
  <p>This is some content inside a div.</p>
</div>  
3. In the following code, what is the difference between the #title and .grid selector?  
In CSS, #title is an ID selector, meaning it targets an element with the id attribute set to "title":
css
#title {
  color: blue;
}
.grid is a class selector, meaning it targets any element with the class attribute set to "grid":
css
.grid {
  display: grid;
}
IDs should be unique to a single element on a page, whereas classes can be applied to multiple elements.  
4. In the following code, what is the difference between padding and margin?  
padding is the space between the content of an element and its border, essentially the "inner" space.
margin is the space outside the element’s border, creating "outer" space between the element and other elements.
5. Given this HTML and this CSS how will the images be displayed using flex?  
6. What does the following padding CSS do?  
padding CSS sets space inside an element. For example:
padding: 10px 20px; 
This adds 10px of space on the top and bottom, and 20px on the left and right.
7. What does the following code using arrow syntax function declaration do?  
Arrow functions in JavaScript provide a shorter syntax for writing functions. For example:
javascript
const add = (a, b) => a + b;
This function takes two parameters a and b, and returns their sum.
8. What does the following code using map with an array output?  
Generally, map creates a new array by applying a function to each element of an original array.
9. What does the following code output using getElementByID and addEventListener?  
getElementById selects an element by its id
addEventListener is used to attach an event listener to that element.
10. What does the following line of Javascript do using a hashtag selector?  
A hashtag selector in JavaScript typically refers to selecting an element by its id using document.querySelector:
javascript
const element = document.querySelector('#myElement');
This selects the element with the id of "myElement".
11. Which of the following are true? (mark all that are true about the DOM)  
DOM (Document Object Model) involves knowing that it's a hierarchical structure representing HTML documents, allowing JavaScript to interact with and manipulate elements on a web page.
12. By default, the HTML span element has a default CSS display property value of:  
The default display value for a <span> is inline. This means it will not start on a new line and will only take up as much width as its content.
13. How would you use CSS to change all the div elements to have a background color of red?  
css
div {
  background-color: red;
}
This CSS selector targets all <div> elements and sets their background-color to red.
14. How would you display an image with a hyperlink in HTML?  
html
<a href="https://www.example.com">
  <img src="image.jpg" alt="Example Image">
</a>
This wraps the <img> tag with an <a> tag, so when the image is clicked, it directs the user to the URL specified in the href.
15. In the CSS box model, what is the ordering of the box layers starting at the inside and working out?  
The order is:
Content (the actual text or other content)
Padding (space between the content and the border)
Border (surrounds the padding and content)
Margin (space outside the border)
16. Given the following HTML, what CSS would you use to set the text "trouble" to green and leave the "double" text unaffected?  
Assuming the HTML looks like this:
	html
	<p><span class="trouble">trouble</span> double</p>
The CSS would be:
css
Copy code
.trouble {
  color: green;
}
This targets the span element with the class trouble and changes its text color to green.
17. What will the following code output when executed using a for loop and console.log?  
a for loop will iterate over a range or array, and console.log outputs each iteration to the browser's console.
18. How would you use JavaScript to select an element with the id of “byu” and change the text color of that element to green?  
document.getElementById("byu").style.color = "green";
19. What is the opening HTML tag for a paragraph, ordered list, unordered list, second level heading, first level heading, third level heading?   
Paragraph: <p>
Ordered List: <ol>
Unordered List: <ul>
Second Level Heading: <h2>
First Level Heading: <h1>
Third Level Heading: <h3>
20. How do you declare the document type to be html?  
	<!DOCTYPE html>
21. What is valid javascript syntax for if, else, for, while, switch statements?  
if statement:
if (condition) {
  // code to run if condition is true
} else {
  // code to run if condition is false
}
for loop:
	for (let i = 0; i < 5; i++) {
  console.log(i);
}
while loop:
	while (condition) {
  // code to run as long as condition is true
}
switch statement:
	switch (value) {
  case 1:
    // code for case 1
    break;
  case 2:
    // code for case 2
    break;
  default:
    // code if no cases match
}
22. What is the correct syntax for creating a javascript object?  
This creates an object person with properties name and age and a method greet.
const person = {
  name: "John",
  age: 30,
  greet: function() {
    console.log("Hello, " + this.name);
  }
};
23. Is it possible to add new properties to javascript objects?  
Yes, you can add new properties like this:
person.address = "123 Main St";
This adds an address property to the person object.
24. If you want to include JavaScript on an HTML page, which tag do you use?  
Use the <script> tag:
html
<script src="script.js"></script>
Or include JavaScript directly inside the tag:
html
<script>
  console.log("Hello, world!");
</script>
25. Given the following HTML, what JavaScript could you use to set the text "animal" to "crow" and leave the "fish" text unaffected?
Assuming the HTML looks like this:  
	html
	<p id="animal">animal</p>
<p id="fish">fish</p>
The JavaScript would be:
	javascript
	document.getElementById("animal").textContent = "crow";
This selects the element with the id of "animal" and sets its text content to "crow", while the element with the id "fish" remains unchanged.
26. Which of the following correctly describes JSON?  
JSON (JavaScript Object Notation) is a lightweight data-interchange format. It is easy for humans to read and write and easy for machines to parse and generate. JSON uses key-value pairs and is often used for transmitting data between a server and a web application. Example:
json
{
  "name": "John",
  "age": 30,
  "isStudent": false
}
27. What does the console command chmod, pwd, cd, ls, vim, nano, mkdir, mv, rm, man, ssh, ps, wget, sudo  do?  
chmod: Changes the permissions of a file or directory.
pwd: Prints the current working directory.
cd: Changes the current directory.
ls: Lists the files and directories in the current directory.
vim: Opens the Vim text editor.
nano: Opens the Nano text editor.
mkdir: Creates a new directory.
mv: Moves or renames files and directories.
rm: Removes (deletes) files or directories.
man: Displays the manual page for a command.
ssh: Starts an SSH (Secure Shell) session to a remote server.
ps: Displays the currently running processes.
wget: Downloads files from the web.
sudo: Executes a command with superuser (root) privileges.
28. Which of the following console command creates a remote shell session?  
The ssh command is used to create a secure shell session to a remote machine. It allows you to execute commands on the remote system as if you were physically present there. Example:
bash
ssh user@remote-server.com
29. Which of the following is true when the -la parameter is specified for the ls console command?  
Using ls -la will list all files and directories, including hidden ones (those starting with a .), in a detailed format that includes file permissions, owner, file size, and modification date.
30. Which of the following is true for the domain name banana.fruit.bozo.click, which is the top level domain, which is a subdomain, which is a root domain?  
	In the domain banana.fruit.bozo.click:
Top-Level Domain (TLD): click (the last part of the domain)
Root Domain: bozo.click (the main domain name combined with the TLD)
Subdomain: banana.fruit (anything that precedes the root domain)
31. Is a web certificate is necessary to use HTTPS.  
Yes, a web certificate (SSL/TLS certificate) is necessary to use HTTPS. It encrypts the communication between a web server and a client, ensuring secure data transmission.
32. Can a DNS A record can point to an IP address or another A record.  
A DNS A record can point directly to an IP address, but it cannot point to another A record. Instead, a CNAME record is used to alias one domain name to another.
33. Port 443, 80, 22 is reserved for which protocol?  
Port 443: Used for HTTPS (Hypertext Transfer Protocol Secure).
Port 80: Used for HTTP (Hypertext Transfer Protocol).
Port 22: Used for SSH (Secure Shell).
34. What will the following code using Promises output when executed?  
Generally, JavaScript promises handle asynchronous operations and their output depends on how the resolve or reject states are handled.

