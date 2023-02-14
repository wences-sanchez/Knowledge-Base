tags:: Udacity, Cloud Development
deck:: [[Cloud Development Nanodegree::Full Stack Apps on AWS]]

-
- ## 2.Organizing our Code & Working with Larger Systems
	- ![image.png](../assets/image_1675530476287_0.png)
	- In larger projects, we use:
	- In server.ts:
		- ```typescript
		  import { IndexRouter } from "./controllers/v0/index.router"
		  
		  //...
		  app.use("/api/v0/", IndexRouter);
		  ```
	- In controllers/v0/index.router.ts:
		- ```typescript
		  const router: Router = Router()
		  
		  router.use("/feed", FeedRouter);
		  ```
	- In controllers/v0/feed/routes/feed.router.ts:
		- ```TypeScript
		  const router: Router = Router()
		  
		  router.get("/", ) //...) ...;
		  // THIS IS NOT THE ROOT BUT THE SUB-FOLDER ROOT
		  ```
	- In the file controllers/v0/feed/routes/feed.router.ts, the root directory `router.get('/',...` is not the server root directory. The root in this case is based on where the server is entering from, which in this case, is `api/v0/feed/routes`.
-
- ## 3. Connecting our RDS Database in Node
	- We'll use **Sequelize**, which is a framework of Javascript that runs with Node.
	- ORM works in both directions.
	- ![image.png](../assets/image_1675675006851_0.png)
	- ![image.png](../assets/image_1675675157977_0.png)
	- #### Models
		- A model is the data representation of some group of data. In object-oriented programing terms, a model is an object and is represented by a new class. It should usually represent a noun such as a user, a feed item, an order, etc. We use the `@Table` decorator and extend the base sequelize `Model` class to link our model to our database table.
	- #### Parameters
		- The model contains instance parameters. These can be other models or primitive fields. We use the `@Column` decorator to link our parameters to the table columns. The bang symbol `!` specifies if the field in the table can be null. Sequelize handles the datatype mappings from TypeScript types to Postgres column datatypes.
		- Read more at the [Sequelize docs entry on models](http://docs.sequelizejs.com/class/lib/model.js~Model.html).
	-
	-
	- Sequelize is not for NoSQL databases.
	- ![image.png](../assets/image_1675675537984_0.png)
	- ORMS allow us to easily switch to a different dialect of SQL (e.g. PostgreSQL, MySQL), without having to modify the code that interacts with the database. If we were to write SQL queries directly, instead of using an ORM, we would have to modify our SQL statements to be compatible with the dialect of the database that we are using.
	- ### Migrations
		- Migration refers to modifying the database (by adding or removing tables or columns, for instance, or switching to a different dialect of SQL) to a newer version (usually based on new business requirements).
			- Up migration is the process of modifying the database to a newer state.
			- Down migration is the process of reversing an up migration, to a prior state.
		- Read more at the [Sequelize docs on migrations](http://docs.sequelizejs.com/manual/migrations.html)
			- > **Note** Migrations is a loaded term. We most commonly refer to migrations when changing database table states (new columns, adding tables, etc). However, it can also refer to migrating infrastructure - for examples Postgres to MySQL.
	- ### Seeding
		- Seeds are default rows of data that will be inserted upon database formation. This may be helpful when provisioning databases frequently for specific applications and having welcome data populated, or when running tests on staging systems to simulate real-world conditions.
			- Read more at the [Sequelize docs on seeding](http://docs.sequelizejs.com/manual/migrations.html#creating-first-seed)
-
- ## 5.Handling Secrets with Environment Variables
	- ### 1. Shell - Linux/Mac Users
		- For Unix/Linux/Mac operating systems, a shell is a command-line program that accepts users' commands and executes those commands on the underlying kernel. Each command has a specific job to perform.
		  
		  There are multiple shells available. The default shell for (most) Linux systems is the `bash` shell. Other examples are `ksh`, `tcsh`, and `zsh`. The default shell for macOS 10+ is `.zsh`.
		  
		  Your default shell boots when you open a terminal, which allows you to execute commands.
	- ### 2. Environment Variables - Linux/Mac Users
		- Assume you store the user-specific secrets, such as username, password, or private key, into a simple file. It might not be a safe approach because all the sensitive information may become public if you put that information on Github/any other Version Control System. User-specific secrets, visible publicly, are never a good thing.
		  
		  Here comes the role of Environment variables in this scenario. Environment variables are pretty much like standard variables, in that they have a name and hold value. The environment variables only belong to your local system and won't be visible when you push your code to a different environment like Github.
		- #### a. The   `.env`   file
			- The `.env` file is one of the *hidden* files in which you can store your choice of environment variables. The variables stored in this file are your individual working environment variables. ***Note that the environment variables that are stored in the `.env` file override the variables set in the `/etc/environment` file, that is shared by all users of that computer. ***You will need to follow the steps below to configure environment variables in a `.env` file:
			- **Install environment variables package** -
			  
			  ```
			  npm **install** dotenv *--save*
			  ```
			  
			  This will allow you to use the environment variables that you'll set in a new file.
			- **Create a new `.env` file** in the root of your project. Fill the `.env` file with your new variables, and their corresponding values. For example:
			  
			  ```
			  POSTGRES_USERNAME = yourUsername
			  POSTGRES_PASSWORD = yourpassword
			  AWS_REGION = yourAWSRegion
			  AWS_PROFILE=awsProfileName
			  ```
			- **Require the package in your server** - Add the following code on top of the `server.ts` file
			  
			  ```
			  require('dotenv').config();
			  ```
			- **Use your environment variables** - If you want to refer the environment variables that you just saved in the `.env` file, anywhere in the code, try putting a prefix `process.env.` in front of the variable name. For example, `process.env.POSTGRES_USERNAME` will fetch you the value stored in it.
			- **Add `.env` to your `.gitignore`** - You wouldn't want your `.env` file to be available publicly in the project Github repository. For this reason, go to the `.gitignore` file in the project root, and add and entry `.env` to it. It will make sure that you don't push our environment variables to Github!
		- #### b. The   `process.env`   file
			- The `process.env` file is a default file that stores the variables for the current terminal environment. When you run the following command, it will store the `POSTGRES_USERNAME` to the current terminal environment:
			  
			  ```
			  export POSTGRES_USERNAME = yourUsername
			  ```
			  
			  By default, the Node is accessing the same set of variables that are defined in your `process.env` file.
		- #### c. Bash Profile -   `.profile`   file
			- You won't want to export the user-specific variables *every time* you'll log in to your system, and do not want to override the variables set in the root level `/etc/environment` file. The solution is to store the new variables *either* in `.profile`,`.bashrc` or `.zshrc` file, depending on your shell. These are the files that the shell executes even before you type your first command to it. ***Note that every user of the computer has its own `.profile` file.***
			  
			  When you put
			  
			  ```
			  export AWS_PROFILE=awsProfileName
			  ```
			  
			  inside the `.profile` file, it will run this command before you start firing commands in your shell.
			  
			  Usually, the bash profile is found at `~/.profile`, where `~` represents your current logged in user's home directory. Keep in mind the `.` preceding profile means this file will be hidden.
			  
			  If you wish to instruct your Node to execute the `.profile` file anytime, you can run the following command:
			  
			  ```
			  source ~/.profile
			  ```
		- #### d. Using the Manual Page -   `man`   command
			- Most Bash commands in the terminal give you instructions on how to use them when you type `man <command>` where `<command>` could be any CLI command. For example, typing `man bash` into the terminal will give you the manual page for `bash`.
			  
			  The *INVOCATION* section of this man page will give you some hints to where bash looks for profiles when starting.
	- ### 3. Environment Variables - Windows Users
		- Windows has the same concept of variable stored at the OS level to use within and across applications. Windows has two types of Environment Variables:
		- **User Environment Variables** which are accessible only to the currently logged in user
		- **System Environment Variables** which are available *all* users on the machine
		- ##### Setting Windows Environment Variables
		  
		  Environment variables are set on Windows using a GUI (Graphical User Interface). On Windows 10, this can be found by:
		- From the start menu, right-click the `Computer` icon
		- Select `Properties`
		- Select `Advanced System Settings` on the left
		- In the new window, click `Environment Variables`
		- Use the `New...` and `Edit...` buttons to set and modify your variables
		  
		  You can follow [this handy guide](https://www.computerhope.com/issues/ch000549.htm) for your flavor of Windows.
-
- ## 6.Permissions for Elastic Beanstalk
	- ### Clarifying Profiles
		- When we're working locally, we need to specify which AWS profile to use (a refresher on named profiles can be found [here](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-profiles.html)). When we're deploying to an AWS ElasticBeanstalk instance, the profile will be implicitly set by the instance. We can use the logic control to implicitly not specify these AWS credentials in this deployed state.
		- ```
		  # ./src/aws.ts
		  //Configure AWS
		  if(c.aws_profile !== "DEPLOYED") {
		  var credentials = new AWS.SharedIniFileCredentials({profile: 'default'});
		  AWS.config.credentials = credentials;
		  }
		  ```
-