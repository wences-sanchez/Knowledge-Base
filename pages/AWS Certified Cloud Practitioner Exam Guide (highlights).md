title:: AWS Certified Cloud Practitioner Exam Guide (highlights)
deck:: [[O'Reilly-Learning::AWS Certified Cloud Practitioner Exam Guide]]

- author:: [[]]
  full-title:: "AWS Certified Cloud Practitioner Exam Guide"
  category:: #books
  
  tags:: AWS O'Reilly-Learning
- Highlights first synced by [[Readwise]] [[Thursday, 27-10-2022]]
	- Chapter 7: AWS Compute Services
		- -
		- -
		- Under Availability Zone, select us-east-1a – this is the same zone where we placed Public Subnet One. This way, any frontend web resources in Public Subnet One can access any backend resources in Private Subnet One, allowing those resources to be in the same Availability Zone. #flashcard
		  id:: daa5043f-f059-4da3-8380-9452467d307a
		- -
	- Chapter 8: AWS Database Services
		- -
		- About relational and non-relational databases #flashcard
		  id:: 1de5e3ee-b967-4da6-a11c-49897176696f
			- they have certain restrictions, such as the fact that you need to define the database schema (its structure) before you can add data, and changing this later can be difficult. Non-relational databases offer a lot more flexibility and are used for many modern-day web and mobile applications.
		- -
		- -
		- Let's look at the core components of a DynamoDB database:
		  id:: edb074d8-e232-4770-abb3-b5ece8659803
		  
		  Tables: Like Amazon RDS databases, your data is stored in tables. So, you can have a customers table that will host information about your customers and their orders. Each table will also have a unique primary key, which is crucial for uniquely identifying every record in the table. Records are known as items in DynamoDB Tables.
		  Items: Items are like records in Amazon RDS databases. A table can have one or more items, and each item will be a unique combination of attributes that define that item. Items can be up to 400 KB in size and can contain key-value pairs called attributes.
		  Attributes: An attribute is like a column heading or a field in an Amazon RDS database. Attributes help define the items in your table. So, in a Customers Table, the attributes could be First-Name or Last-Name and so on. #flashcard
		- -
		- -
		- Amazon Neptune is a fully managed graph database service and a type of NoSQL database. #flashcard
		  id:: 2664e41d-e167-452f-af81-5b05db4c7506
		- -