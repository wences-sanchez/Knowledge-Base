title:: Readwise/How to Set Up TypeScript With Node.js and Express (highlights)
deck:: [[Across-the-Net]]
author:: [[Aman Mittal]]
full-title:: "How to Set Up TypeScript With Node.js and Express"
category:: #articles
url:: https://blog.logrocket.com/how-to-set-up-node-typescript-express/

- Highlights first synced by [[Readwise]] [[Tuesday, 14-02-2023]]
	- -
		- The [DefinitelyTyped GitHub repository](https://github.com/DefinitelyTyped/DefinitelyTyped) maintains the TypeScript type definitions for use directly in Node.js and other JavaScript projects, so you don’t have to define these types from scratch. To add these types or the declaration files related to a particular library or a module, you have to look for the packages that start with the `@types` namespace.
		  
		  Open the terminal window and install the packages described above with the following command:
		  
		  npm i -D typescript @types/express @types/node
		  
		  The `-D` flag, also known as the `--dev` flag, is a specification for the package manager to install these libraries as `devDependencies`. #flashcard
		- tags:: [[code]]
		- ([View Highlight](https://read.readwise.io/read/01gs7z7vammdh7p4e4aywaczjn))
	- -
- New highlights added [[Tuesday, 14-02-2023]] at 3:13 PM
	- -
		- After installing these dev dependencies, update the `scripts` in the `package.json` file:
		  
		  {
		  "scripts": {
		    "build": "npx tsc",
		    "start": "node dist/index.js",
		    "dev": "concurrently \"npx tsc --watch\" \"nodemon -q dist/index.js\""
		  }
		  }
		  
		  The `build` command will compile the code in JavaScript inside a `dist` directory. The `dev` command is used to run the Node.js server in development mode.
		  
		  Now, go back to the terminal window and run `npm run dev` to trigger the development server: #flashcard
		- ([View Highlight](https://read.readwise.io/read/01gs80z990gag7dr484gm0m8sz))
	- -