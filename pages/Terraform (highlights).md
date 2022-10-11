title:: Terraform (highlights)
author:: [[Yevgeniy Brikman]]
full-title:: "Terraform"
category:: #books

tags:: #[[O'Reilly-Learning]]

- #tags #[[O'Reilly-Learning]]
- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- 1. Why Terraform
	- 2. Getting Started with Terraform
		- -
		- The goal of DevOps is to make software delivery vastly more efficient. #ñspace
		- -
		- -
		- How could you add tags to a resource in Terraform (e.g. an AWS instance)? #car
		  id:: 63401535-670b-49ab-89c2-1b7417d40b22
			- resource "aws_instance" "example" {
			  ami           = "ami-0c55b159cbfafe1f0"
			  instance_type = "t2.micro"
			  
			  tags = {
			    Name = "terraform-example"
			  }
			  }
		- -
		- -
		- The three (optional) parts of a variable’s declaration body. #car
			- The body of the variable declaration can contain three parameters, all of them optional:
			  
			  description
			  It’s always a good idea to use this parameter to document how a variable is used. Your teammates will not only be able to see this description while reading the code, but also when running the plan or apply commands (you’ll see an example of this shortly).
			  
			  default
			  There are a number of ways to provide a value for the variable, including passing it in at the command line (using the -var option), via a file (using the -var-file option), or via an environment variable (Terraform looks for environment variables of the name TF_VAR_<variable_name>). If no value is passed in, the variable will fall back to this default value. If there is no default value, Terraform will interactively prompt the user for one.
			  
			  type
			  This allows you enforce type constraints on the variables a user passes in. Terraform supports a number of type constraints, including string, number, bool, list, map, set, object, tuple, and any. If you don’t specify a type, Terraform assumes the type is any.
		- -
	- A. Recommended Reading
		- -
		- Which files and/or directories should I put in the .gitignore when using Terraform? #car
			- You should also create a file called .gitignore that tells Git to ignore certain types of files so that you don’t accidentally check them in:
			  
			  .terraform
			  *.tfstate
			  *.tfstate.backup
		- -
		- -
		- Example of a variable declaration. #car
			- variable "list_example" {
			  description = "An example of a list in Terraform"
			  type        = list
			  default     = ["a", "b", "c"]
			  }
		- -
		- -
		- The following are some of the best resources I’ve found on DevOps and infrastructure as code, including books, blog posts, newsletters, and talks.
		  
		  Books
		  Infrastructure as Code: Managing Servers in the Cloud by Kief Morris (O’Reilly)
		  
		  Site Reliability Engineering: How Google Runs Production Systems by Betsy Beyer, Chris Jones, Jennifer Petoff, and Niall Richard Murphy (O’Reilly)
		  
		  The DevOps Handbook: How To Create World-Class Agility, Reliability, & Security in Technology Organizations by Gene Kim, Jez Humble, Patrick Debois, and John Willis (IT Revolution Press)
		  
		  Designing Data Intensive Applications by Martin Kleppmann (O’Reilly)
		  
		  Continuous Delivery: Reliable Software Releases through Build, Test, and Deployment Automation by Jez Humble and David Farley (Addison-Wesley Professional)
		  
		  Release It! Design and Deploy Production-Ready Software by Michael T. Nygard (The Pragmatic Bookshelf)
		  
		  Kubernetes In Action by Marko Luksa (Manning)
		  
		  Leading the Transformation: Applying Agile and DevOps Principles at Scale by Gary Gruver and Tommy Mouser (IT Revolution Press)
		  
		  Visible Ops Handbook by by Kevin Behr, Gene Kim, and George Spafford (Information Technology Process Institute)
		  
		  Effective DevOps by Jennifer Davis and Katherine Daniels (O’Reilly)
		  
		  Lean Enterprise by Jez Humble, Joanne Molesky, Barry O’Reilly (O’Reilly)
		  
		  Hello, Startup: A Programmer’s Guide to Building Products, Technologies, and Teams by Yevgeniy Brikman (O’Reilly) #ñspace
		- -
		- -
		- Mention an example of a security group in AWS with Terraform. #car
		  id:: 63401535-dcfe-4895-9656-4058cb86e34b
			- resource "aws_security_group" "instance" {
			  name = "terraform-example-instance"
			  
			  ingress {
			    from_port   = 8080
			    to_port     = 8080
			    protocol    = "tcp"
			    cidr_blocks = ["0.0.0.0/0"]
			  }
			  }
		- -
		- -
		- To use the value from an input variable in your Terraform code, you can use a new type of expression called a variable reference, which has the following syntax:
		  
		  var.<VARIABLE_NAME> #ñspace
		- -
		- -
		- The idea behind immutable infrastructure is similar: once you’ve deployed a server, you never make changes to it again. If you need to update something, such as deploy a new version of your code, you create a new image from your server template and you deploy it on a new server. Because servers never change, it’s a lot easier to reason about what’s deployed. #ñspace
		- -
		- -
		- An expression in Terraform is anything that returns a value. You’ve already seen the simplest type of expressions, literals, such as strings (e.g., "ami-0c55b159cbfafe1f0") and numbers (e.g., 5). Terraform supports many other types of expressions #ñspace
		- -
		- -
		- About output variables in Terraform. #car
		  id:: 63401535-54e0-4ba2-bcc1-a4efc1983ae8
			- In addition to input variables, Terraform also allows you to define output variables by using the following syntax:
			  
			  output "<NAME>" {
			  value = <VALUE>
			  [CONFIG ...]
			  }
			  The NAME is the name of the output variable, and VALUE can be any Terraform expression that you would like to output. The CONFIG can contain two additional parameters, both optional:
			  
			  description
			  It’s always a good idea to use this parameter to document what type of data is contained in the output variable.
			  
			  sensitive
			  Set this parameter to true to instruct Terraform not to log this output at the end of terraform apply. This is useful if the output variable contains sensitive material or secrets such as passwords or private keys.
		- -
		- -
		- What does provisioning mean? #car
		  id:: 63401535-54fd-4eeb-9a29-c456968c351d
			- Whereas configuration management, server templating, and orchestration tools define the code that runs on each server, provisioning tools such as Terraform, CloudFormation, and OpenStack Heat are responsible for creating the servers themselves. In fact, you can use provisioning tools to not only create servers, but also databases, caches, load balancers, queues, monitoring, subnet configurations, firewall settings, routing rules, Secure Sockets Layer (SSL) certificates, and almost every other aspect of your infrastructure
		- -
		- -
		- How can you use a reference of an attribute in Terraform? #car
			- One particularly useful type of expression is a reference, which allows you to access values from other parts of your code. To access the ID of the security group resource, you are going to need to use a resource attribute reference, which uses the following syntax:
			  
			  <PROVIDER>_<TYPE>.<NAME>.<ATTRIBUTE>
			  where PROVIDER is the name of the provider (e.g., aws), TYPE is the type of resource (e.g., security_group), NAME is the name of that resource (e.g., the security group is named "instance"), and ATTRIBUTE is either one of the arguments of that resource (e.g., name) or one of the attributes exported by the resource (you can find the list of available attributes in the documentation for each resource).
		- -
		- -
		- output variables show up in the console after you run terraform apply, which users of your Terraform code might find useful (e.g., you now know what IP to test after the web server is deployed). You can also use the terraform output command to list all outputs without applying any changes:
		  
		  $ terraform output
		  public_ip = 54.174.13.5 #ñspace
		- -
		- -
		- That said, if you’re not using server templating tools, a good alternative is to use a configuration management and provisioning tool together. For example, you might use Terraform to provision your servers and run Chef to configure each one. #ñspace
		- -
		- -
		- When you add a reference from one resource to another, you create an implicit dependency. Terraform parses these dependencies, builds a dependency graph from them, and uses that to automatically determine in which order it should create resources. For example, if you were deploying this code from scratch, Terraform would know that it needs to create the security group before the EC2 Instance, because the EC2 Instance references the ID of the security group. You can even get Terraform to show you the dependency graph by running the graph command: #ñspace
		- -
		- -
		- And you can run terraform output <OUTPUT_NAME> to see the value of a specific output called <OUTPUT_NAME>:
		  
		  $ terraform output public_ip
		  54.174.13.5 #ñspace
		- -
		- -
		- The -/+ in the plan output means “replace” #ñspace
		- -
		- -
		- About how can AWS ease with automated scalability. #car
			- Managing such a cluster manually is a lot of work. Fortunately, you can let AWS take care of it for by you using an Auto Scaling Group (ASG), as shown in Figure 2-9. An ASG takes care of a lot of tasks for you completely automatically, including launching a cluster of EC2 Instances, monitoring the health of each Instance, replacing failed Instances, and adjusting the size of the cluster in response to load.
		- -
		- -
		- provider "aws" {
		  region = "us-east-2"
		  }
		  This tells Terraform that you are going to be using AWS as your provider and that you want to deploy your infrastructure into the us-east-2 region. #ñspace
		- -
		- -
		- What is the syntax for declaring a variable: #car
		  id:: 63401535-b494-401c-8649-44cef8d13c86
			- variable "NAME" {
			  [CONFIG ...]
			  }
		- -
		- -
		- Note that the ASG uses a reference to fill in the launch configuration name. This leads to a problem: launch configurations are immutable, so if you change any parameter of your launch configuration, Terraform will try to replace it. Normally, when replacing a resource, Terraform deletes the old resource first and then creates its replacement, but because your ASG now has a reference to the old resource, Terraform won’t be able to delete it.
		  
		  To solve this problem, you can use a lifecycle setting. Every Terraform resource supports several lifecycle settings that configure how that resource is created, updated, and/or deleted. A particularly useful lifecycle setting is create_before_destroy. If you set create_before_destroy to true, Terraform will invert the order in which it replaces resources, creating the replacement resource first (including updating any references that were pointing at the old resource to point to the replacement) and then deleting the old resource. Add the lifecycle block to your aws_launch_configuration #ñspace
		- -
		- -
		- What is the general syntax for creating a resource in Terraform? #car
		  id:: 63401535-cb48-49e4-83c1-820802d3cc80
			- resource "<PROVIDER>_<TYPE>" "<NAME>" {
			  [CONFIG ...]
			  }
			  where PROVIDER is the name of a provider (e.g., aws), TYPE is the type of resource to create in that provider (e.g., instance), NAME is an identifier you can use throughout the Terraform code to refer to this resource (e.g., my_instance), and CONFIG consists of one or more arguments that are specific to that resource.
		- -
		- -
		- What is a data source in Terraform? #car
			- A data source represents a piece of read-only information that is fetched from the provider (in this case, AWS) every time you run Terraform. Adding a data source to your Terraform configurations does not create anything new; it’s just a way to query the provider’s APIs for data and to make that data available to the rest of your Terraform code. Each Terraform provider exposes a variety of data sources. For example, the AWS provider includes data sources to look up VPC data, subnet data, AMI IDs, IP address ranges, the current user’s identity, and much more.
		- -
		- -
		- About referring to the documentation of Terraform. #car
		  id:: 63401535-c596-4f28-808e-cbc0b47e6821
			- Terraform supports dozens of providers, each of which supports dozens of resources, and each resource has dozens of arguments. There is no way to remember them all. When you’re writing Terraform code, you should be regularly referring to the Terraform documentation to look up what resources are available and how to use each one. For example, here’s the documentation for the aws_instance resource. I’ve been using Terraform for years and I still refer to these docs multiple times per day!
		- -
		- -
		- Example of data source declaration in Terraform. #car
		  id:: 63401535-95d0-42e2-8e9d-6e9743996bcc
			- data "aws_vpc" "default" {
			  default = true
			  }
		- -
		- -
		- The terraform binary contains the basic functionality for Terraform, but it does not come with the code for any of the providers (e.g., the AWS provider, Azure provider, GCP provider, etc.), so when you’re first starting to use Terraform, you need to run terraform init to tell Terraform to scan the code, figure out which providers you’re using, and download the code for them. By default, the provider code will be downloaded into a .terraform folder, which is Terraform’s scratch directory (you may want to add it to .gitignore). #ñspace
		- -
		- -
		- Example of data source use in Terraform. #car
			- data.<PROVIDER>_<TYPE>.<NAME>.<ATTRIBUTE>
			  For example, to get the ID of the VPC from the aws_vpc data source, you would use the following:
			  
			  data.aws_vpc.default.id
		- -
		- -
		- The plan command lets you see what Terraform will do before actually making any changes. #ñspace
		- -
		- -
		- When you’re done experimenting with Terraform, either at the end of this chapter, or at the end of future chapters, it’s a good idea to remove all of the resources you created so that AWS doesn’t charge you for them. Because Terraform keeps track of what resources you created, cleanup is simple. All you need to do is run the destroy command: #ñspace
		- -
		- -
		- How does the Terraform output specify the results? #car
		  id:: 63401535-1e3a-4a86-8607-2652f2466d88
			- The output of the plan command is similar to the output of the diff command that is part of Unix, Linux, and git: anything with a plus sign (+) will be created, anything with a minus sign (–) will be deleted, and anything with a tilde sign (~) will be modified in place.
		- -
		- -
		- Note that later in the book, you will continue to develop this example, so don’t delete the Terraform code! However, feel free to run destroy on the actual deployed resources whenever you want. After all, the beauty of infrastructure as code is that all of the information about those resources is captured in code, so you can re-create all of them at any time with a single command: terraform apply. In fact, you might want to commit your latest changes to Git so that you can keep track of the history of your infrastructure. #ñspace
		- -
		- -
		- To actually create the Instance, run the terraform apply command: #ñspace
		- -
	- 3. How to Manage Terraform State
		- -
		- In other words, the output of the plan command is a diff between the code on your computer and the infrastructure deployed in the real world, as discovered via IDs in the state file. #ñspace
		- -
		- -
		- Instead of using version control, the best way to manage shared storage for state files is to use Terraform’s built-in support for remote backends. A Terraform backend determines how Terraform loads and stores state. The default backend, which you’ve been using this entire time, is the local backend, which stores the state file on your local disk. Remote backends allow you to store the state file in a remote, shared store. A number of remote backends are supported, including Amazon S3; Azure Storage; Google Cloud Storage; and HashiCorp’s Terraform Cloud, Terraform Pro, and Terraform Enterprise. #ñspace
		- -
		- -
		- About port numbers #car
			- PORT NUMBERS
			  The reason this example uses port 8080, rather than the default HTTP port 80, is that listening on any port less than 1024 requires root user privileges. This is a security risk, because any attacker who manages to compromise your server would get root privileges, too.
			  
			  Therefore, it’s a best practice to run your web server with a non-root user that has limited permissions. That means you have to listen on higher-numbered ports, but as you’ll see later in this chapter, you can configure a load balancer to listen on port 80 and route traffic to the high-numbered ports on your server(s).
		- -
		- -
		- How do you interpolate a variable in Terraform? #car
			- "${...}"
			  You can put any valid reference within the curly braces, and Terraform will convert it to a string. For example, here’s how you can use var.server_port inside of the User Data string:
			- ```
			  #!/bin/bash
			  user_data = <<-EOF
			  echo "Hello, World" > index.html
			  nohup busybox httpd -f -p ${var.server_port} &
			  EOF
			  ```
			-
		- -
		- -
		- How do you interpolate a variable in Terraform? #car
			- "${...}"
		- -