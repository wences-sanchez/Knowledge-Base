tags:: Udacity, Cloud Development
deck:: [[Cloud Development Nanodegree::Full Stack Apps on AWS]]

-
- ## 1. Understanding Persistence #flashcard
  id:: 63de521e-3f5d-408d-8e73-4803639a0a2b
	- ### Difficulties of Persistent Data
		- {{video https://www.youtube.com/watch?v=FudZpoYYJBI}}
		  collapsed:: true
			- {{youtube-timestamp 0}} within this lesson we're going to answer the question where can we store data within our stack we've explored some of how to interface with different systems how to respond to requests and now we'll understand how can our request actually contain those valuable pieces of data that we were that we're looking for to refresh your memory our stack is expanding and we're now looking at these two parts on the right side of our diagram our file system and our database these will have different use cases and our specialized pieces of equipment to help us to store specific types of data let's look at our example of cars we have a list of different types of cars that all contain different payloads and different information that we'll be accessing this is a simple example but it helps to motivate our point one approach would be to simply add this data as an instance variable within our server this data would now live in the RAM or non persistent volatile memory
			- {{youtube-timestamp 58}} within the server whenever the server resets we know that this information will also reset with it if we add a car or remove a car or edit any of this data that information will not continue past the server's reset cycle now you might be thinking I think this is a terrible idea why do we ever implement this this is not something that will ever work but you'd be surprised to hear me say this actually might be a good idea sometimes we talked about technical debt and building things that are difficult to manage and maintain this is related to another concept called time to test versus time to build often the data store and the persistent nature of data making sure we can access things quickly takes a lot of time to design an architect properly but if we're trying to test the concept of is this image filter even worth building we might not want to invest time and energy into building that data store day one instead we can hack together solutions
			- {{youtube-timestamp 118}} to fake or make persistence easy in this case we'll be keeping this information in a temporary location and we won't necessarily be interacting with it long term but it helps us to stand up the architecture and stub the type of system that we would implement later to improve this part of the stack if we do things well here our interfaces for interacting with our cars models won't really change that much once we migrate to a proper database system but you might be asking now I can probably continue to hack I can take that data that we have in our cars instance variable and just dump it into a file at random times or when the server is about to shut down now instead of living in memory we can have a cars JSON file that lives somewhere on a hard drive on that computer and this is where this becomes a terrible idea as soon as we start introducing more complexity we start introducing more complexity and that's going to cause problems downstream as we do migrate to
			- {{youtube-timestamp 187}} more complicated systems for example we now have to deal with consistency will this data continue to be identical in memory and on disk as we begin to scale our stack we also will begin adding new instances of servers that will interact with this data and remember our stack is asynchronous meaning we can handle multiple inbound requests making things like adding records changing records or deleting records if we're trying to roll our own solution for storing data persistently we will probably have issues where one record was changed on one server but not on the other or one server is trying to delete a record that another server already deleted these race conditions are a nightmare and are really things we don't want to have to deal with ourselves additionally we have more problems to think about when we are scaling our system if we're storing information as a simple list we'll need to find a record in that list if it's a string like record we might iterate
			- {{youtube-timestamp 247}} through each item of the list looking for that record this would take Big O of N or linear time where we're looking at each record until we find a hit if we're looking for all things that match we might have to go through the entire list search speed is extremely difficult to master and why would we do it ourselves additionally reading from these records will take time as well if our list grows to a size that is outside of our memory constraints remember if we're storing our cars as an instance variable we need to have that entire variable in our RAM if our list gets too big we need to start paging that data from a hard drive and that will be slow that is not something we want to do right speed is also important now writing to ram is probably the simplest operation in terms of time complexity but we don't necessarily want that this early on finally we're going to have more complicated models as we begin to build out more features and more complexity
			- {{youtube-timestamp 309}} things will start to interact cars will have make IDs which correspond to some other data that exists somewhere else on some other list and I don't want to think about implementing any of this myself we need something better and there's a reason one of the first things we did to uncouple our system was pull out our database databases have been designed and developed over decades to optimize performance for optimal readwrite concurrency all of these types of issues that we've been discussing
		- **RAM (Random Access Memory)**: Data can be accessed quickly, but is erased once the server restarts. It may be okay to use RAM when prototyping, and later replace it with a database.
		- **Hard Drive Disk**: Data remains after server restarts, but is specific to that server (not shared across servers).
		- **Race Condition**: When an application’s behavior is dependent on other uncontrollable events. This is an issue with storing data on disks or RAM of multiple servers.
		- **Relational Database**: can store at scale, improve search runtime, and maintain relationships between data fields. We recommend using a database for storing data.
		-
	-
		- But it's very important to be aware that those data should never be in json files, but in memory.
		- As soon as we have a bunch of servers that have to be consistent amongst them, the importance of keeping data as just one unit becomes obvious.
			- Additionally, if we have so much amount of data, it's slow.
			- We strongly need a way of treating our data correctly ==> databases
		- Databases allow us to uncouple our systems.
-
- ## 2. Database Basics #flashcard
  id:: 63de569d-092b-4bc6-bf67-0686fbd92d39
	- ### Indexing Our Data for Better Recall
		- {{video https://www.youtube.com/watch?v=u1waVHPqR-Q}}
		  collapsed:: true
			- {{youtube-timestamp 0}} so now that we understand why persistent data is difficult let's talk about specifically how we can store this kind of data using modern systems we'll be looking closely first at databases we've discussed some problems like concurrency read speed write speed & databases start to solve these problems by adding valuable structure if we had a simple list of items we know we'd have to iterate through each item to find the one thing we're looking for databases start to add some structure on top of these lists so that we can find things more efficiently most databases use a structure like a b-tree this is similar to a binary search tree but we might have more than one branch we'd call these types of structures that sit on top of data indexes and they can include things like numbers or strings or hashes essentially when we start to find a request we look down the tree to find where that request lies this reduces the complexity from Big O of n to something
			- {{youtube-timestamp 61}} like Big O of log n databases also are very good at this many databases store a different data structure within some of these nodes called bloom filters which allow these systems to probabilistically have early stopping criteria let's say we're looking for a record that doesn't exist in our data set we can look down a tree realize oh this probably doesn't exist below and we can stop our search now bloom filters and B trees are complicated data structures and I'd encourage you to study them on your own but they're really beyond the scope of what we're interested in we want to learn how can we use these systems and design systems that will index automatically for us
		-
	- ### NoSQL - Simple Key:Value Stores
		- {{video https://www.youtube.com/watch?v=aGvQpNG-Zus}}
		  collapsed:: true
			- {{youtube-timestamp 0}} one type of database is called no sequel or no SQL will learn what SQL means in a minute but no sequel databases are pretty trendy and popular and there's something you should be aware of at their core they're a key value store essentially all they do is store a specific key to a specific type of data by having our data as a key value pair we can quickly index our key and allow us to find a single record now this is very familiar if you know JavaScript and how objects are stored objects in JavaScript are key value pairs we have a key and then we have a corresponding piece of data no sequel databases act fairly similarly and provide JavaScript interfaces for you to interact with no sequel databases are very easy to scale out we can have data on multiple instances of a machine that allow us to add more computers and more servers as we have more concurrency more users accessing the system at one time or just more data they're also really good if
			- {{youtube-timestamp 67}} you're trying to design a system in a really scrappy way let's say you don't exactly know what your data model will contain when you start building your system day one you might forget you have an interior or you might forget that cars have specific colors since you're storing a key value pair all you have to do in this instance is change your data model and continue using your database as you go but I want to emphasize and stress this is probably a bad idea changing your data models will probably introduce a lot of technical debt later on because you need to be able to parse an interface with all of these data models when you are continuing to design and build your system
		-
		- They're very popular
		- They have our data as a key-value pair, so they can quickly get our searches.
		- They're very easy to scale out.
		- And they allow us to change our data model (something that SQL-based can't)
			- Although this is not a very good idea and leads to technical debt.
	- ### Relational Databases - Structured and Queryable Datastores
		- {{video https://www.youtube.com/watch?v=WFk2Ng5fHig&t=1s}}
		  collapsed:: true
			- {{youtube-timestamp 0}} an alternative type of database is called sequel or relational databases here sequel stands for a structured query language essentially these types of databases have been around for decades very common systems are my sequel or Postgres or Oracle all rely on some type of structured query language to interface with data which is stored in tables this is still a very good skill to know despite how old it is these systems are seasoned well designed and well supported and allow you to build out very complicated queries to find specific types of data looking at our data structures from before we have our objects with lots of information which map directly to columns within our sequel database our ID field is generally referred to as a primary key in this case we have our ID as auto incrementing integers when a new record is introduced to the database will automatically add a new row and assign an ID that's next in line IDs become
			- {{youtube-timestamp 65}} very useful within relational databases because we can relate data by their IDs here we have our make ID which corresponds to a specific make of car this is called a foreign key within our cars table we have the ID 1 which will correspond to ID 1 in this case Tesla within our other table will see this primary key and foreign key concept show up a lot as we begin to build larger data models let's take a look at why this is called a structured query language simply put we have structure to our query and are writing it in a language a simple query might be to select specific columns from a database table this would give us a result that has all of the information within that table and all of the columns that we requested we can add more complexity to our query by doing things like joins we discussed foreign keys by adding an inner join with a table on a specific foreign key column we're able to combine the different columns from those two
			- {{youtube-timestamp 132}} Abel's in this case we're looking for make dot meek we can also add additional parameters to our query to allow us to sort and limit our results here we're ordering by the cost column in a descending order and we're limiting our results to two and we're offsetting by zero we only want to records and we want the first two records if we change this to two we'd be asking for the next two records we can add more complexity by adding we're statements which essentially will act as a filter for specific columns in this case make will be Toyota sequel databases are easiest to scale up as opposed to no sequel databases that are easiest to scale out if we recall scaling out means we can add more instances more computers to support more data needs and more concurrency scaling up means we can make that one computer bigger we can add more hard drives or more RAM or more powerful CPU to support more concurrent users and more data remember sequel databases are storing a
			- {{youtube-timestamp 202}} lot of types of indexes and we want to store as much of that information in RAM so that we can easily and quickly access those indexes when we are looking for records sequel databases are also slower to write information to since we have more indexes to maintain every time we try to insert records we need to make sure our indexes are up-to-date as we get more and more data we'll have more and more indexes that we need to add and maintain and make sure that they are balanced now most databases will reindex and deal with this for you but it's something to keep in mind as you are supporting and deploying your systems
		-
		- **SQL** stands for *Structured Query Languange*
		- They're are easier to scale up than NoSQL
		- They're lower when grow
		-
		- **B-Tree**: a generalization of a binary search tree, which stores sorted data, but can have more than 2 child nodes.
		- **Bloom Filters**: a data structure that is useful for determining if an item is probably in a data set, or definitely not in the data set. Bloom filters don’t actually store the data themselves.
		- **primary key and foreign key**: The primary consists of one or more column in a table that are unique to each record (each row). A foreign key in a table contains the primary key of another table.
		-
		-
- ## 3. Provisioning a Cloud Database
	- We use the *postbird* tool to interact with our RDS (PostgreSQL) Database
		- **Postbird** is used to interact with a PostgreSQL database
	- ### Follow Along!
		- We'll be using this provisioned cloud resource within our project!
	- ### Configuring Amazon Web Services' Relational Database Service
		- {{video https://www.youtube.com/watch?v=2ydzbZjoB-Q&t=1s}}
		- > *NOTE**: Gabe misspoke and mentioned ***Postman*** which we are using for HTTP querying when he meant ***Postbird*** which is used to interface directly with the Postgres database.*
		- {{video https://www.youtube.com/watch?v=JEh35M7LGbo}}
	- ### Allowing Public Traffic to RDS
		- {{video https://www.youtube.com/watch?v=4PnjHumSNA0}}
	- ### Interfacing with our Database using Postbird
		- #### Installing Postbird
			- Download and install Postbird by following the following README instructions: [https://github.com/Paxa/postbird](https://github.com/Paxa/postbird)
	- ### Connecting to RDS with Postbird
		- {{video https://www.youtube.com/watch?v=SFoI65eGENk}}
		  collapsed:: true
			- {{youtube-timestamp 0}} it might take a little bit of time for your RDS instance to spin up what it's doing under the hood is creating a new computer instance a new server instance installing the software and instantiating the database once this completes we can now interface with that system let's go back to our management console and search for RDS to access that service we can now click on our databases either by accessing our resources here or clicking databases on the left we now see our u2 Graham database which we can click on to bring us into our main panel we now have some new information that allows us to connect we have an endpoint and we have a port let's copy that endpoint and we're going to open a new piece of software called post bird will be using post bird to interface with our database it's important to not confuse post bird and postman post bird is to interface with Postgres post man is to create things like post requests they're both
			- {{youtube-timestamp 66}} really useful tools and sometimes you might confuse the two because the names are so similar okay so opening post bird we see a few options in the center we have a GUI that will allow us to connect to our database we'll copy and paste our endpoint from our database our port is the default port for Postgres five four three two and our username and database name is what we entered before while creating our system we can paste this in enter our password and paste in that same information into our database and let's go ahead and test this connection if all goes well we'll see successfully connected if things don't go well don't panic sometimes the creation and instantiation of your RDS instance might not work if that happens usually the first step will fix it and it's turning it off and turning it back on again in our s3 console we can click actions and reboot which I do not want to do right now but clicking reboot would basically just shut it down and turn it
			- {{youtube-timestamp 134}} for a first-time clean install if there are any problems that we'll probably fix it now that we have our credentials entered in and tested let's go ahead and save and connect which will store this record within our post bird
	- ### Creating Tables in RDS with Postbird
		- {{video https://www.youtube.com/watch?v=9vus2aEFzNs}}
		  collapsed:: true
			- {{youtube-timestamp 0}} we're now connected to our you to Gram database and it's completely empty this is a fresh instance and there's no information that is stored in there yet this little checkbox at the bottom is something for power users databases have their own structure that needs to be stored somewhere and they store them in their own database so this information contains some of the way that Postgres knows how to interpret your data we're not going to cover this this is very complicated but it might be fun for you to poke around and maybe try to break something instead let's use the GUI to create a table if we recall we had a set of information called cars we can create a table for cars by clicking the green plus at the bottom left of the screen and typing in a table called cars we can create this table it'll generate some boilerplate structure and now we have a single empty table by default Postgres will create a few columns and indexes automatically for you we already
			- {{youtube-timestamp 63}} have an ID column which is an integer so a number and it auto increments it'll add a new number in order as we get new data this is also a primary key and the primary way we'll find that record within our database we can see that primary key within our indexes this tells us that it's unique it's using the b-tree algorithm to try to find it and it takes up about a thousand bytes of space let's go ahead and use the GUI to add a column to our database by clicking add column we can add things like type we can select a data type since Postgres is a type database in our case our type is text and we will leave our default value and our maximum length empty and we will not allow null fields we can now add this column
	- ### Making SQL Commands with Postbird
		- {{video https://www.youtube.com/watch?v=WFPW_dSq48w}}
	- ### SQL Walkthrough
		- {{video https://www.youtube.com/watch?v=5PZIuHBC7wY}}
			- {{youtube-timestamp 0}} if you've added the sequel correctly your sequel should look something like this to add a table for me will have an ID and a name and we'll create that table similar to before we can also insert into that table the last concept we'll talk about our views select queries are ways for us to filter items within our database table we talked a bit about these in the concept slides so let's go ahead and try copy and pasting some of those into our query and saving them as views the one key difference here is we add create view with a view name as which we'll use the information from this query to create those views view show up in post bird as blue tables then will show us the result of that select query our joint table will show us joins on our foreign primary key looking at the content we can see instead of an ID field we have our completed name field as expected similarly we have our view for filtering where we have our make is Toyota and
			- {{youtube-timestamp 65}} looking at that content we see only records from Toyota go ahead and play with some of these queries try to break the system have fun with it and don't stress out if you're not following on completely there are some great resources we'll include that have more detail on how to write sequel but keep in mind we will be using an ORM a system within our JavaScript framework to complete these tasks automatically for us
		-
		- ```sql
		  CREATE TABLE "public"."make" (
		    id SERIAL PRIMARY KEY,
		    name TEXT
		  );
		  
		  INSERT INTO "public"."cars" ("type", "model", "cost", "make_id") VALUES 
		  	('sedan', 'roadster', '33', '2'),
		  	('sedan', 'prius', '22', '1'),
		  	('sedan', 'focus', '18', '3'),
		  	('suv', 'highlander', '40', '1');
		  
		  INSERT INTO "public"."make" ("id", "name") VALUES
		  	(1, 'Tesla'),
		  	(2, 'Chevrolet'),
		  	(3, 'Ford');
		    
		  SELECT cars.model, cars.type, make.name 
		  	FROM cars, make 
		  	WHERE cars.make_id = make.id AND make.name = 'Tesla';
		  ```
		-
		-
- ## 4. Filestore Basics #flashcard
  id:: 63de7626-d495-4c4a-96bb-321698ebcf54
	- ### Benefits of Cloud Filestores
		- {{video https://www.youtube.com/watch?v=Gs0adcq6WF4}}
		  collapsed:: true
			- {{youtube-timestamp 0}} we've just learned that databases are great for structured data with small fields and things that we need to search for complex types of queries we might be looking for some type of subset of items with multiple parameters that help us find that item this type of data is expensive to store we have to not only store the data itself but we also have to store the indexes and all of the overhead associated with finding that information file stores allow us to store larger bits of information with lower cost things like images videos or documents where we're not necessarily looking within the content of that information but looking for the document itself should be stored in a file store this will save us in cost and also in speed to deliver that kind of resource
		- {{video https://www.youtube.com/watch?v=FOkDh5p6Pok}}
			- {{youtube-timestamp 0}} databases are great for storing complex data with some kind of information and structure but for larger things like images or videos it's going to be cost prohibitive to dump that information into a table. Database hard drive space is precious and we really don't want to store large blob like data which is really anything that's just loosely structured information within that table instead we want a solution that is less expensive for us to be able to store data for long periods of time we're now talking about file stores this is a specialized piece of infrastructure that allows us to store these larger types of data file stores also provide additional capabilities that are useful for our longer-term needs for example we can archive information will be using s3 as our main file store s3 is quick and scalable for our immediate file storing needs but as we start to have older data that we're not accessing very quickly they offer a cheaper solution called
			- {{youtube-timestamp 62}} glacial storage this offers a very similar interface to s3 but allows us to essentially keep our data in a place where it'll be slower to read from but cheaper to store in fact they just released an even more cost-effective solution for older data modern file stores also give us the ability to add more complexity to our infrastructure to allow us to support things like content delivery networks this will clone our data into smaller file stores closer to our end customer since large data takes a longer amount of time to transmit over long distances this is a concept called latency and we'll cover this in more depth later we want our data to reside very close to where our final use will be CD ends were traditionally used for data storage but we're seeing more and more types of edge compute so that we can actually make use of data very close to our users we can move our data stores close but we can also move our compute systems closer to our customers so we
			- {{youtube-timestamp 123}} don't even need to move that data across the world in order for us to process it we also have some really interesting capabilities by using s3 and other of cloud file stores in particular remember our server is still a finite resource we have a certain amount of concurrent requests we can support and we will need to scale that system to support more requests scaling costs money with systems like s3 and other cloud file stores we don't have to take our large files from our client pass it through our server and dump it into our file system instead we are going to be using a design pattern called signed URLs which will save us tremendous amounts of bandwidth we'll have our client make a simple request to our server saying I have data I want to deliver our server will make a quick handshake with our file store it will then return back a URL that the client can directly upload data to by passing our infrastructure completely once this whole process is done we can
			- {{youtube-timestamp 189}} notify our server and move on with whatever processing we need to make not only will this save us bandwidth but it will also be quicker for our customers and users instead of having to wait for our server to proxy that request we can directly stream that information into those buckets and buckets is a useful piece of terminology that's what we call a simple directory like system a simple place where we're going to be dumping data s3 we call that a bucket this type of pattern also gives us a little bit of extra security for free if we only allow our server to interface with our file system no one else from the outside world can access it in any other way the only vector of attack for our file store would be through our server or through the AWS cloud which as good developers we will keep secure the only way to upload or download information from our file store will be by asking for that signed URL through our server our server will ensure that we have the
			- {{youtube-timestamp 249}} authentication required an authorization required to access that information and then provide that information to our end client just to recap because this can be a little bit confusing the signed URL pattern composes of three parts of our system in our sequence diagram we have our client our server and our file store this could be Google Chrome and our web application our management server our REST API and Amazon s3 with one of our buckets for our media walking through one more time our client requests a resource from our server our server can perform some additional processing and authorization to make sure we can indeed serve that request if we can't we can reject it if we can we can request that signed URL from our file store saying we've specifically want one resource for a specific amount of time and then we can retrieve that signed URL from the file store and send that URL back to our client this is a very light low overhead
			- {{youtube-timestamp 313}} process and all of the real bandwidth comes in after that signed URL is made use of in this case we're loading the side URL this could be a get request for let's say an image but it could just as easily be a post signed URL a user can post data which can be posted directly to the file store bypassing the server completely
		-
	- **Filestores** allow us to store big amounts of data (like images, videos and documents) that are too expensive to save them in databases.
	- We don't want to store any big file nor object nor image nor document in our database
	- ![image.png](../assets/image_1675524090543_0.png)
	- ### S3 is a filestore
	- Buckets are a simple directory-like system in which to store data.
	- We can access our buckets (which are filestores) directly bypassing the server. That's great!
	- ![image.png](../assets/image_1675524484058_0.png)
	- CORS (Cross-Origin Resource Sharing) allows clients in web applications to talk which one another and reject certain requests from outsiders.
		- By default, your S3 bucket will not allow requests from just any old domain.
		- Instead, we have to add a course policy to allow certain hosts from accessing this type of information
		- ![image.png](../assets/image_1675525432939_0.png)
		- This is for consuming this bucket in our application with our signedURL pattern
	-
- Could you briefly explain what CORS is? #flashcard
  id:: 63de811f-054b-4995-9d1a-98d0d867d92f
	- CORS (Cross Origin Resource Sharing o **Uso compartido de recursos entre orígenes**): defines how a client can interact with a resource, and what the client can and cannot do with that resource. Setting the CORS policy of our S3 bucket allows our client to communicate with the S3 bucket using the SignedURL pattern.
		-
- ## 5.Creating an S3 Filestore Bucket in AWS
- ## 6.Understanding Secrets
	- It's better to use environment variables instead of text fields
	- We can connect **resources** (Servers with Services) within a **VPC** using IAM **roles**
		- IAM service role: an IAM role gives a service a set of permissions to access one or more services.
	- We can connect **developers** with a Service using IAM **Users**
		- IAM user role: an IAM role can give a user a set of permissions to access one or more services.
	-
	-
	-
	-