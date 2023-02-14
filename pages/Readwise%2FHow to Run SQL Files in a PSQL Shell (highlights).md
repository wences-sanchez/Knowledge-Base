title:: Readwise/How to Run SQL Files in a PSQL Shell (highlights)
deck:: [[Across-the-Net]]
author:: [[Educative Enterprise]]
full-title:: "How to Run SQL Files in a PSQL Shell"
category:: #articles
url:: https://www.educative.io/answers/how-to-run-sql-files-in-a-psql-shell

- Highlights first synced by [[Readwise]] [[Tuesday, 14-02-2023]]
	- -
		- ¿Cómo ejecutarías un script de PostgreSQL en la shell? #flashcard
			- Step 1: Locate the SQL file
			  
			  Locate the SQL file you want to run and copy its location. See the following example.
			  
			    /home/me/projects/run-sql-tut/list-databases.sql
			  
			  `me` is the current user’s username. Replace it with your username.
			  
			  Step 2: Log into the `psql` shell
			  
			    sudo -iu postgres psql
			  
			  Step 3: Execute the SQL file
			  
			    \i /home/me/projects/run-sql-tut/list-databases.sql
			  
			  This should give an output similar to:
			  
			                                   List of databases    Name     |  Owner   | Encoding | Collate |  Ctype  |   Access privileges-------------+----------+----------+---------+---------+----------------------- postgres    | postgres | UTF8     | C.UTF-8 | C.UTF-8 | template0   | postgres | UTF8     | C.UTF-8 | C.UTF-8 | =c/postgres          +             |          |          |         |         | postgres=CTc/postgres template1   | postgres | UTF8     | C.UTF-8 | C.UTF-8 | =c/postgres          +             |          |          |         |         | postgres=CTc/postgres(3 rows)
		- ([View Highlight](https://read.readwise.io/read/01gs8b44fexbagrfsjr4fy9b8m))
	- -