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
	- ### Intro to Object-Relational Maps (ORM)
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
		- {{video https://www.youtube.com/watch?v=4W9f0h_KVUQ&t=227s}}
		  collapsed:: true
			- {{youtube-timestamp 0}} Oh RMS can also handle the connections to our database our server instance needs to be able to communicate directly to our data store and we can either do this ourselves and make sure that our communication back and forth is working with our request response cycles that we've learned but our ms will usually make this process much simpler we also might need more than one connection if we have high concurrency on our server we'll need to have multiple connections open to our data store to support the connections and the traffic that we will be needing to serve those requests Oh our ms will usually handle this for us when we instantiate our sequel eyes object within our server we can provide some of our parameters we can provide our username password database and the host on which we're running on we can also select a dialect and storage this will tell sequel eyes what type of data store we're using in our case Postgres but we can migrate between databases
			- {{youtube-timestamp 62}} pretty easily let's say we wanted to switch to my sequel instead of Postgres while sequel eyes can handle that under the hood and provide the same interfaces within our code this again uncouples a major component from our code base allowing us to have freedom and flexibility to support different systems but as the name implies sequel eyes is a relational RM and won't really allow us to very easily migrate to a no sequel type database ORM s can also help us to manage database state when we create a new database we'll have a certain set of columns and a certain set of initial seed data potentially this is the state in which the database exists for example our car example will have a make ID a type a model a cost and an ID and we might want to start our database with some records so we have some information the records that we're inserting into a new table are called seeds and we're not going to cover that in depth but can provide some additional texts for you to
			- {{youtube-timestamp 128}} understand that a bit deeper when we're adding or changing table or inserting or removing columns Oh RMS can handle this using a concept called migrations migrations could be a bit complicated but generally there's some terminology that's consistent an up migration is adding or going to the next state a down migration is going back to a prior state it's generally a good idea to have both up and down migrations in case you do something wrong and want to go back in time to an older version of your system if all you have is an up migration you would have to probably manually reverse some of those changes to your database in order for your code to be compatible here we have a create table migration which will create a table with feed item and we'll have a few columns that we're adding we will add a few parameters to specify what kinds of what kind of column that is with in Postgres we won't allow null we want this to auto increment our ID so
			- {{youtube-timestamp 193}} when we add new records it will be the largest ID there will have a primary key and this will be an integer our URL is simpler it's just a string and if we need to go backwards in time we're just going to drop this table migrations can include creating new tables but also modifying existing tables like adding columns changing column types and get more complicated like mapping data from one place to another so RMS provide a whole bunch of benefits for us from managing connections to the database to managing data and accessing things like finding create updating and deleting objects for us let's now take a look at how we can implement ORM s within our node Express environment for this we're going to be using the the database we provision in a prior exercise and post bird to make sure that our database state is actually existing the way we expect it to
		- #### Transcript
		  collapsed:: true
			- Oh RMS can also handle the connections to our database our server instance needs to be able to communicate directly to our data store and we can either do this ourselves and make sure that our communication back and forth is working with our request response cycles that we've learned but our ms will usually make this process much simpler we also might need more than one connection if we have high concurrency on our server we'll need to have multiple connections open to our data store to support the connections and the traffic that we will be needing to serve those requests Oh our ms will usually handle this for us when we instantiate our sequel eyes object within our server we can provide some of our parameters we can provide our username password database and the host on which we're running on we can also select a dialect and storage this will tell sequel eyes what type of data store we're using in our case Postgres but we can migrate between databases pretty easily let's say we wanted to switch to my sequel instead of Postgres while sequel eyes can handle that under the hood and provide the same interfaces within our code this again uncouples a major component from our code base allowing us to have freedom and flexibility to support different systems but as the name implies sequel eyes is a relational RM and won't really allow us to very easily migrate to a no sequel type database ORM s can also help us to manage database state when we create a new database we'll have a certain set of columns and a certain set of initial seed data potentially this is the state in which the database exists for example our car example will have a make ID a type a model a cost and an ID and we might want to start our database with some records so we have some information the records that we're inserting into a new table are called seeds and we're not going to cover that in depth but can provide some additional texts for you to understand that a bit deeper when we're adding or changing table or inserting or removing columns Oh RMS can handle this using a concept called migrations migrations could be a bit complicated but generally there's some terminology that's consistent an up migration is adding or going to the next state a down migration is going back to a prior state it's generally a good idea to have both up and down migrations in case you do something wrong and want to go back in time to an older version of your system if all you have is an up migration you would have to probably manually reverse some of those changes to your database in order for your code to be compatible here we have a create table migration which will create a table with feed item and we'll have a few columns that we're adding we will add a few parameters to specify what kinds of what kind of column that is with in Postgres we won't allow null we want this to auto increment our ID so when we add new records it will be the largest ID there will have a primary key and this will be an integer our URL is simpler it's just a string and if we need to go backwards in time we're just going to drop this table migrations can include creating new tables but also modifying existing tables like adding columns changing column types and get more complicated like mapping data from one place to another so RMS provide a whole bunch of benefits for us from managing connections to the database to managing data and accessing things like finding create updating and deleting objects for us let's now take a look at how we can implement ORM s within our node Express environment for this we're going to be using the the database we provision in a prior exercise and post bird to make sure that our database state is actually existing the way we expect it to
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
	- ### Using Sequelize in our Node RestAPI Source Code
		- {{video https://www.youtube.com/watch?v=AHUp7GJh5ko}}
		- #### Decorators
			- The Decorators (also known as Annotations) mentioned in this video are a feature of the sequelize-typescript package which allows us to link database features with our models. We exemplify this using the `@CreatedAt` and `@UpdatedAt`. This will set the option in the Postgres database to automatically set the date when any row is created, or updated and is useful when sorting and filtering our data.
			- [Read more and view complete details on the model definition in the sequelize-typescript docs](https://www.npmjs.com/package/sequelize-typescript#model-definition)
		- {{video https://www.youtube.com/watch?v=1FnTTG07Oxk}}
		  collapsed:: true
			- {{youtube-timestamp 0}} the one other thing we should take a quick look at is within our next line on our server dot es si equalise dot sync this will allow us to make sure that our database is in sync with our expected models within sequel eyes.if sequel eyes and our data stores are not currently aligned then we'll have some issues when we're trying to provide that interface between what our data looks like on the table and what our data looks like within our objects so this line will make sure that everything is on the same level of updates it does that by applying our migrations taking a look at our migrations folder within our source folder we can see two migrations migrations work in order of time so generally there'll be some kind of date sometimes down to a second level of creation and will apply from oldest to newest to make sure that they're all up-to-date now sometimes you'll see a lot of migrations it's common sometimes to combine these migrations into a single migration file that brings you to a certain state of the system because migrations take time and if you're taking a table and keep adding columns adding columns that's going to be expensive instead what we'd like to do is just try to create the state in its most recent form looking at these we can see we're creating two tables the oldest migration is creating our feed item table with its corresponding columns and column properties and our user table is created in the newer migration in a similar way now that we understand how our sequel eyes is structured within our node Express environment we can run NPM run dev to start our server now we see a whole bunch of new things that we didn't see before when we started our server this is sequel eyes outputting what it's trying to do within sequel you can see generally this is sequel commands so you're creating a table for feed item or doing some other fun stuff and then finally once this is all completed we'll have our server running on localhost 8080 we can now open up post bird which should maintain that connection click this little refresh button and we'll see some new tables here we have our user and here we have our feed item and this has the structure we expected our RM kept our database up-to-date with our models within our system now we can begin to consume data within our server let's take a look at how we can do that within our controllers we're going to be looking at our feed item will open up controllers v-0 feed routes and open our feed router now we'll get into some of this AWS stuff in a future concept but for now let's quickly look at how we're collecting feed items here we're saying we'd like a new feed item here we're declaring a variable for items locally and we're using our interface from sequel eyes to find and count all ordering by ID descending we'll be mapping and manipulating our URL we'll learn about this soon and then we are going to be sending those items back to our client let's also take a quick look at post here we're doing the same thing now you'll also see this require off which is in post this is going to be important and we will be covering this soon as well but for now you can ignore it we're doing the same thing that we were doing for validating our inputs are valid by pulling them out of our body and doing some quick checks just to make sure that they are valid they exist in our case and finally we're instantiate our new feed item and then we're using our sequel eyes interface to save that item
		- Enter `npm run dev` in terminal to start the server
		- {{video https://www.youtube.com/watch?v=XFHB26f_JyY&t=2s}}
		-
		- #### Exercise
			- 1. Create a new GET endpoint that gets a specific record from the database using the **id** field
				- i. Use the *sequelize* interface to find that record
				- ii. Make some validation to make sure there's an id present
				- iii. Return that to the user in a send data payload.
				- iv. Use Postman to try it out
			- 2. Create a PATCH endpoint that updates an existing record that it's in a database with some kind of body
		-
		- {{video https://www.youtube.com/watch?v=OJs3eMhKIZc}}
			-
		- #### Associations
			- Associations allow our models to reference other models. For example, consider people and dog relationships. We might represent this as a person table and dog table.
			  
			  *person table*
			  
			  | id | name |
			  | ---- | ---- | ---- |
			  | 1 | Sally |
			  | 2 | James |
			  
			  *dog table*
			  
			  | id | name |
			  | ---- | ---- | ---- |
			  | a | Ruffles |
			  | b | Noodles |
			  | c | Xander |
		- #### One-To-One Association
			- If the person has only one dog, we can use a foreign key column in the person table to reference a single row in the dog table. This is known as a One-To-One association.
			  
			  *person table (extended)*
			  
			  | id | name | dogId |
			  | ---- | ---- | ---- |
			  | 1 | Sally | a |
			  | 2 | James | c |
		- #### One-To-Many Association
			- However, a person may have many dogs. In SQL we might represent this using a new separate table known as a Join table. This is essentially a table of two foreign key columns, one for person table and one for dog table. We can then find all dog foreign keys for a given person foreign key to find the relationship.
			  
			  *person-dog join table*
			  
			  | personId | dogId |
			  | ---- | ---- | ---- |
			  | 1 | a |
			  | 1 | b |
			  | 2 | c |
		- #### Associations In Sequelize
			- Check out the Sequelize documentation on associations to understand how to implement this pattern: [http://docs.sequelizejs.com/manual/associations.html](https://sequelize.org/master/manual/assocs.html)
- ## 4. Connecting our S3 Filestore in Node
	- ### SignedURL Refresher and Intro to AWS SDK
		- We'll be using the Amazon Web Services (AWS) Javascript Software Development Kit (SDK) to implement the SignedURL pattern within our Node server.
		- {{video https://www.youtube.com/watch?v=b89Tlx8rAho&t=1s}}
		- ![image.png](../assets/image_1676893104366_0.png)
		- ![image.png](../assets/image_1676893191231_0.png)
		- > *tip*: AWS SDK dependencies are included in the project's `package.json` file. If you're starting a new project, you will need to install these dependencies using NPM. AWS offers clear instructions for setting it up in a new project: [https://docs.aws.amazon.com/sdk-for-javascript/v2/developer-guide/installing-jssdk.html](https://docs.aws.amazon.com/sdk-for-javascript/v2/developer-guide/installing-jssdk.html).
	- ## Implementing the AWS S3 SDK in our Node Server
		- ### Understanding the Stubbed Code
			- {{video https://www.youtube.com/watch?v=OeNqid8icYA}}
		- ### Unstubbing with AWS SDK
			- {{video https://www.youtube.com/watch?v=WkvBe0D0YlE}}
		- ### Using Postman to Test The Image Upload
			- {{video https://www.youtube.com/watch?v=91Xi2-RQzp8}}
			-
-
- ## 5.Handling Secrets with Environment Variables
	- ### Handling Secrets with Environment Variables
		- {{video https://www.youtube.com/watch?v=YvSJGpoNtdE}}
	- ### Glossary
	  collapsed:: true
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
		- #### 3. Environment Variables - Windows Users
			- Windows has the same concept of variable stored at the OS level to use within and across applications. Windows has two types of Environment Variables:
			- **User Environment Variables** which are accessible only to the currently logged in user
			- **System Environment Variables** which are available *all* users on the machine
			- #### Setting Windows Environment Variables
			- Environment variables are set on Windows using a GUI (Graphical User Interface). On Windows 10, this can be found by:
			- From the start menu, right-click the `Computer` icon
			- Select `Properties`
			- Select `Advanced System Settings` on the left
			- In the new window, click `Environment Variables`
			- Use the `New...` and `Edit...` buttons to set and modify your variables
			- You can follow [this handy guide](https://www.computerhope.com/issues/ch000549.htm) for your flavor of Windows.
			-
		- #### 4. Run Linux Environment on Windows
			- Windows OS also has a concept of the shell. The default shell in Windows is the command-line tool **Cmd.exe**. There is another shell available in Windows 7 SP1and above, [PowerShell](https://docs.microsoft.com/en-us/powershell/scripting/windows-powershell/install/installing-windows-powershell?view=powershell-7). PowerShell is primarily used for Windows system administration. Neither CMD nor PowerShell can run bash, ssh, git, apt, or any Linux commands by default.
			  
			  The solution is to use *either* of the options below:
			- #### Option 1 - Windows Subsystem for Linux
				- [Windows Subsystem for Linux](https://docs.microsoft.com/en-us/windows/wsl/about) (WSL) - WSL allows us to run Linux environment, including most command-line tools, utilities, and applications, from the Windows Command Prompt (CMD). You can even mix the Linux and Windows commands after installing WSL. Refer to the installation instructions [here](https://docs.microsoft.com/en-us/windows/wsl/install-win10) to install WSL on Windows.
				  
				  The next step is to install and run a Linux distribution parallelly on WSL. There are multiple choices for installing - Ubuntu, OpenSUSE, Debian, and many more. If you have no preference, you can install [Ubuntu on Windows](https://www.microsoft.com/en-us/p/ubuntu/9nblggh4msv6?activetab=pivot:overviewtab) App, and proceed as mentioned in the installation instructions above.
			- #### Option 2 - Git Bash on Windows
				- Git is an open-source distributed Version Control System (VCS). Github is a repository hosting and version control service, where you can store, share, or download the repository content in collaboration with multiple contributors. Git provides a Unix style command-line tool called [Git for Windows](https://git-scm.com/download/win) to help users work with Github repositories. Once you download and install Git for Windows, it can be run either in CMD or a GUI.
				- [Git Bash](https://www.atlassian.com/git/tutorials/git-bash) is a command-line tool by default included in Git for Windows. Besides running Git commands, Git Bash allows users to run Linux/Bash commands as well.
-
- ## 6.Permissions for Elastic Beanstalk
	- {{video https://www.youtube.com/watch?v=aa1DH7eClIc&t=4s}}
	-
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
- ## 7. Deploying Our Server to the Cloud
	- ### Basic AWS Architecture
		- {{video https://www.youtube.com/watch?v=JTp-2V2V5Ps}}
		  collapsed:: true
			- {{youtube-timestamp 0}} now that we understand and have provisioned our resources in the cloud for our data store and our file system and we've integrated it with a larger node Express framework we want our node Express framework to also be living in the cloud there are a few ways we can do this but we'll be using AWS elastic beanstalk to make our lives a little bit easier so AWS ec2 or elastic cloud compute cloud compute 2 sees easy 2 is a service offered by Amazon to provide computational platforms in their cloud these are but you can think of these as just servers that are running on AWS infrastructure there's some complicated stuff like virtualization and how they're provisioning these systems that you don't have to really worry about that's the beauty of using a managed cloud service like EC to EC to s run operating systems in the form of Amazon machine images these are snapshots of the OS at a particular state which makes it extremely convenient to stand up infrastructure for whatever environment you really need to run there are certain flavors of Linux or Windows or whatever you really need to get your system stood up elastic Beanstalk actually has a specific image designed for node and heavily optimized for node and we'll be using that within our deployments this takes a lot of the engineering of infrastructure development out of the mix and makes it really nice for us to be able to quickly stand up systems within these kinds of services we've developed our server locally running on our local machines we're running our node Express server by running NPM run dev which is directly using our typescript files to run our server on our machines wouldn't be awesome if we could take that and deploy it to another server for public consumption on a production like environment so that other people can use our server well that's what we'll be doing now but as with most things in the cloud it's really not that simple instead there's a bunch of extra stuff that needs to happen in order for things to be stable and scalable and make everyone happier also if you're sharp and paying attention we haven't done authentication yet don't worry we'll get there this is a really important step and we'll have an entire lesson dedicated to adding authentication to our server but for now let's let's continue let's simplify our diagram a bit so we only have our server and our data stores again our servers running locally we're using elastic Beanstalk to deploy our application to a cloud environment elastic Beanstalk is a service offered by Amazon to make our deployments easier while standing up really good equipment and infrastructure starting at the basics our code will be running on an AWS ec2 instance ec2 is elastic cloud compute cloud compute being the two C's which is a type of server type of computer virtualized within their environment there'll be different classes of computers different classes of servers but we'll be using some basic equipment for our deployment within this system you can think of it as a computer like your local environment where you'll be running code our node application will be running within this ec2 instance but we don't want traffic from the internet connecting directly to that node application this won't be efficient this won't be secure this won't necessarily be scalable instead we want some kind of reverse proxy or proxy server that sits in front of our application within this instance elastic Beanstalk automatically adds this infrastructure to our server in the form of an engine X proxy this will take external traffic and route it internally within that instance to a running node application this will be really helpful for us as we start to add things like SSL or TLS encryption as well as having more traffic it will simply route multiple concurrent requests q1q requests that we can't necessarily handle out at a given time and just make our lives easier while we have more concurrent users our node application will be managed by the AWS service as well so we don't have to worry about whether about state and certain types of concerns that we would have to normally aforehand provisioning this system elastic Beanstalk also provisions a load balancer that sits in front of our ec2 and since this doesn't necessarily make sense if we only have one instance but elastic Beanstalk allows us to auto scale our group simplifying this diagram and adding more ec2 instances demonstrates what scaling our system out looks like as one server becomes inundated with requests if we have thousands of users trying to access data all at once we'll need to scale out by adding more instances to support that load we'll have auto scaling policies that we'll explore later which will automatically spin up new instances make sure they're healthy and direct traffic to them through our load balancer all of our external web traffic comes to our load balancer and it intelligently routes this traffic to an instance that is capable of supporting it if we have too much traffic coming in at one time the server will become overwhelmed and will start rejecting requests and we really don't want that with our cloud system this is a common type of attack that you might have heard of called a dedicated denial of service attack where tons of traffic will swarm a specific website and take it down having an auto scaling group and a load balancer doesn't necessarily mitigate against that attack because we'll just be spinning up a lot more instances and we should probably have an upper bound to that or else we'll spend a lot of money but in a normal use case where we have legitimate requests we don't want those legitimate requests blocked this also demonstrates why we wanted to pull out our file stores and databases from within this stack we can implement an additional layer between our ec2 instances and our data stores called a cache which will allow us to quickly access this kind of information within multiple instances now before we can deploy our code our code needs to be in a state which Amazon can make sense of while installing it on our instance we'll be introducing a concept called a build process that will allow us to do this quickly and automatically
		- ### Flashcards
		  collapsed:: true
			- Q: What is elastic beanstalk? #flashcard
				- A: Elastic Beanstalk is a service offered by Amazon to make our deployments easier while standing up really good equipment and infrastructure.
			- Q: What is EC2? #flashcard
				- A: EC2 is elastic cloud compute cloud compute 2 sees easy 2 is a service offered by Amazon to provide computational platforms in their cloud, these are servers running on AWS infrastructure.
			- Q: What is Amazon machine images? #flashcard
				- A: Amazon machine images are snapshots of the OS at a particular state which makes it extremely convenient to stand up infrastructure for whatever environment you really need to run.
			- Q: What does elastic Beanstalk do? #flashcard
				- A: Elastic Beanstalk automatically adds an engine X proxy which will take external traffic and route it internally within that instance to a running node application.
			- Q: What is a cache? #flashcard
				- A: A cache is an additional layer between our EC2 instances and our data stores which allows us to quickly access information within multiple instances.
		- ![image.png](../assets/image_1676896984151_0.png)
		-
		- Elastic Beanstalk has images already prepared to our Node projects.
		- Our Node applications run inside the above EC2 instance.
			- But we don't want traffic from the internet be able to access to our EC2 instance!
			- So we run a NGINX Proxy which routes internally to the server
			- Elastic Beanstalk also provides a load balancer
			-
	- ### Using AWS Elastic Beanstalk
		- Elastic Beanstalk is a powerful Development Operations tool (Dev Ops) to deploy your code to AWS services and infrastructure with minimal effort. #flashcard
		- #### EB CLI
			- We'll be using the Command Line Interface to work with Elastic Beanstalk. This will provide us with a set of commands to create new applications and deploy code to these systems. Before continuing, you must install the EB CLI by reading the [AWS Doc Instructions for Install](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/eb-cli3-install.html) for your platform.
		-
		- {{video https://www.youtube.com/watch?v=Sfzgp_4wlhI}}
		-
		- After running the `eb init` command and following the guided setup will create a new directory in our project named `.elasticbeanstalk`. Within this configuration file, there is a configuration file named `config.yml`. This is the set of instructions Elastic Beanstalk will follow when provisioning your AWS infrastructure and deploying your code.
		-
		- #### Generating SSH Keypairs
			- Public-Key Cryptography is a method to encrypt and decrypt authentication information for connecting to your resources in the cloud. The keys you generate replace your password, but they should be treated as sensitive data that would grant anyone who holds them access to your running instance. AWS offers a great guide on how to create [Key Pairs for your EC2 Instances](https://docs.aws.amazon.com/AWSEC2/latest/UserGuide/ec2-key-pairs.html).
		-
		- #### Creating Deployable Build Archives and Deploying
			- Now that you have a running Beanstalk instance, we must package our code into a format that is usable by Elastic Beanstalk. We do this by transpiring our typescript into javascript and then zipping the contents into a single file which we can upload. NPM allows us to define simple script commands in the `package.json` file. As described in the video, we've included the `build` command to perform these steps for us.
				- > Note for Windows Users
				  Unlike Unix (Linux and Mac), The Windows Environment does not have a native CLI command for `zip`. Instead, you must install a utility called [UnixUtils](https://sourceforge.net/projects/unxutils/) to support this functionality. For more information and detailed instructions to install [UnixUtils](https://sourceforge.net/projects/unxutils/) refer to the prereq section in the [AWS Nodejs Tutorial](https://docs.aws.amazon.com/elasticbeanstalk/latest/dg/nodejs-dynamodb-tutorial.html#nodejs-dynamodb-tutorial-prereqs).
			- {{video https://www.youtube.com/watch?v=4Tmx2ZUxwMw}}
			- After running `npm run build` to transpile and package our code into a zip, we need to configure Elastic Beanstalk to use this build archive. This is accomplished with the following addition to the .easticbeanstalk/config.yml configuration file:
			-
			- ```yaml
			  deploy:
			      artifact: ./www/Archive.zip
			  ```
			-
	- ### Setting Environment Variables in Elastic Beanstalk
		- Just like our local code, we'll need to access certain variables from our system within our Node server. We can set these variables through the AWS Console.
		- {{video https://www.youtube.com/watch?v=GnFd-a0dAyI}}
		-
-
-
-
-
-
-
-
-