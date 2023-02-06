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
-
-