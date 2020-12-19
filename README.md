# tinder-clone
Full tinder clone
Hosted on: https://tinder-clone-b1bdc.web.app/

To start off in my code I have comments that go into most functions in detail unless they are the usual obvious functions. So here I will be giving a basic overview of how and why I made the app. The reason behind creating this tinder clone was to learn how to connect the mongoDB when using visual studio code as all my previous projects had been made using either glitch or repl.it as they were incredibly easy to use and being the only two I had been taught to use. 


When choosing a project to make I decide on creating a M.E.R.N app as I have never done one in visual studio code. Then came across a Tinder clone M.E.R.N app that I thought would be perfect as It would also be great to learn how to use the swipe function and the database set up behind it. Although within creating this app I was also able to use react for the first time in visual studio code and now I can see why so many people love using react. Although there were a few other programmes I was able to learn for the first time like Postman for checking the connection, firebase for hosting the frontend, axios to secure the backend, express js with heroku to help build the backend as well as using nodemon.js.


To start off using npx create-react-app tinder-clone in the terminal of visual code to start off the initial front end folder. After this it was important to import npm i axios on the front end so that it will make HTTPS requests super simple and help create web requests like fetch which will also intern help with all the backend later on.

Then rather than designing everything in HTML I used the App.js file as this is common practice with react developers then rather than putting all the javascript in one file I created a javascript file for each section of the page.This included the Header what is a profile icon and chat icon from https://material-ui.com/ that are both click sensitive using IconButton div then added a png file from google images for the tinder picture. This was also used for the swipe buttons at the bottom of the page.


The Tinder cards were surprisingly simple to make as there is already a package that is for free online that you can just import npm install --save react-tinder-card.  First before any other function a used useEffect await axios to get the tinder cards. Then all I had to do after that was to create a few functions to remove the person at the front and let the program know that they had left. 

Once the front end was finished It was time to make the backend by creating a new tinder-backend react folder with a server.js file to create the server and a dbCards.js file to create the database structure. For creating the server I made a connected express then connected it on port 8001 to start to see if it was working while also connecting it to my mongoDB account. For the Middlewares I used express.json to recognize the incoming Request Object as a JSON Object and Cors for the headers. 

 

I set up my mongoDB using mongoose to connect up to it with downloading both then used mongoose.connect(connection_url,  with useNewParser: true, as I had a specific port. useCreateIndex: true, to avoid deprecation warnings from the MongoDB driver and finally useUnifiedTopology: true, for to opt in to using the MongoDB driver's new connection management engine. 

For the API endpoints I created I app.get with “Hello world” to first see if the server was working with testing it on the local server 8001 to first test if it’s running smoothly then. Set the proper app.post and app.get functions that are connected to the tinder cards so they can update when more are added. One way to add new cards was to do it manually through mongodb but that wouldn’t show how the connection is between the website and the database. From this I was able to learn how to use Postman to add the new cards to mongodb through /tinder/cards using the post json in Postman then manually checking if it was received on the mongodb. This is where I was stuck the longest as I was getting a response of 400 rather than 201 if it was okay or 500 if there was an error. Later I found that all I had to do was restart the terminal which redownloaded all the libraries which I naturally did next time I came on the computer. Once I had established the connection I was then able to transfer the backend to the frontend folder with axios but through the herokuapp to act as a service (PaaS) that enables developers to build, run, and operate applications entirely in the cloud.

With the backend up and running it was time to find a place to host the website and I was told to use FireBase which was amazing as I had never worked with it before. So I downloaded and connected up through the terminal with an account that I had created on their website.
