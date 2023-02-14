title:: Readwise/Conventions for app.js, index.js, and server.js in node.js? (highlights)
deck:: [[Across-the-Net]]
author:: [[Stack Overflow]]
full-title:: "Conventions for app.js, index.js, and server.js in node.js?"
category:: #articles
url:: https://stackoverflow.com/questions/36002413/conventions-for-app-js-index-js-and-server-js-in-node-js

- Highlights first synced by [[Readwise]] [[Tuesday, 14-02-2023]]
	- -
		- What is the difference between index.js, server.js and app.js? #flashcard
			- Even though you can call the files anything you want, there's an advantage to calling the entry point index.js or server.js
			  
			  **Why index.js:** When you issue `npm init` it will set the main entry point of the module to index.js. Some people don't change it, so they end up naming their main entry point index.js. It means there's one less thing to do.
			  
			  **Why server.js:** If your node package is not going to be consumed by another package, but rather is a stand-alone app, then if you call your main entry point server.js, then you can issue `npm start` and start your app. `npm start` will run your server.js file by default. To change this behavior, supply a `start` script in package.json. If a `start` script exists, `npm start` will run that script instead.
			  
			  app.js is just a convention -- the only advantage to it is that some IDEs, such as Visual Studio Code will default to app.js as the entry point of a program you debug. That way when using the most common framework, Express, which creates an app.js file, "it just works"
		- tags:: [[coding knowledge]]
		- ([View Highlight](https://read.readwise.io/read/01gs7zxq8qtnd0d49swffq7s7y))
	- -