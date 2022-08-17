title:: Linux Fundamentals/User and Group Management and Permissions
tags:: Linux, O'Reilly-Learning, Videos

- #tags #O'Reilly-Learning #Linux #Videos
- ## Lesson 9: [[User and Group Management]]
	- ### 9.2 Understanding the Role of Ownership #spaced
		- When a user creates a file on Linux, that user becomes the file owner.
		- Every Linux user is a member of at least one group, and while creating a file on Linux, that group will become group owner.
		- Because of group ownership, every user must be a member of at least one group.
		- Tip: Use `$ useradd` with **-m**
			- For creating the home directory
		- `$sudo groupadd sales`
		- `$ sudo usermod -aG sales bill`
	- ### 9.5 Managing User and Group Properties
		- Users and their properties are stored in `/etc/passwd`
		- ![image.png](../assets/image_1660725345251_0.png)
		-
		- Groups are stored in `/etc/group`
		- Use **$ vigr** to edit `/etc/group`
	- ### 9.7 Managing Password Properties
		- `$ sudo chage <user>`
			- Asks for input about pasword configuration parameters of <user>
			- It changes password properties
	- ### 9.8 Managing Current Sessions
		- `$ who` and `$ w` show who is currenntly logged in
		- `$ loginctl` allows for current session management
		-
	-