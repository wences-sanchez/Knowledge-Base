# Terraform

deck:: [[O'Reilly-Learning::Terraform]]\
author:: [[Yevgeniy Brikman]]\
full-title:: "Terraform"\
category:: #books\
\
tags:: O'Reilly-Learning  

![](https://learning.oreilly.com/library/view/terraform-up/9781492046899/ibis_generated_cover_thumbnail.jpg)
## Highlights
### 1. Why Terraform
### 2. Getting Started with Terraform
- id:: 63639931-2875-48d3-9eee-038bdd419b62
  
  The goal of DevOps is to make software delivery vastly more efficient. #flashcard
-
- id:: 63639931-9f31-478f-bad6-cc3e9fa82e3a
   How could you add tags to a resource in Terraform (e.g. an AWS instance)? #flashcard 
    resource "aws_instance" "example" {
     ami = "ami-0c55b159cbfafe1f0"
     instance_type = "t2.micro"
     tags = {
     Name = "terraform-example"
     }
     }
-
- id:: 63639931-4262-4291-bd00-d169475c9a83
   The three (optional) parts of a variable’s declaration body. #flashcard 
    The body of the variable declaration can contain three parameters, all of them optional:
     description
     It’s always a good idea to use this parameter to document how a variable is used. Your teammates will not only be able to see this description while reading the code, but also when running the plan or apply commands (you’ll see an example of this shortly).
     default
     There are a number of ways to provide a value for the variable, including passing it in at the command line (using the -var option), via a file (using the -var-file option), or via an environment variable (Terraform looks for environment variables of the name TF_VAR_<variable_name>). If no value is passed in, the variable will fall back to this default value. If there is no default value, Terraform will interactively prompt the user for one.
     type
     This allows you enforce type constraints on the variables a user passes in. Terraform supports a number of type constraints, including string, number, bool, list, map, set, object, tuple, and any. If you don’t specify a type, Terraform assumes the type is any.
-
### A. Recommended Reading
- id:: 63639931-88fe-4ed8-8fa8-970bd8fc533b
   Which files and/or directories should I put in the .gitignore when using Terraform? #flashcard 
    You should also create a file called .gitignore that tells Git to ignore certain types of files so that you don’t accidentally check them in:
     .terraform
     *.tfstate
     *.tfstate.backup
-
- id:: 63639931-8e4a-48be-b1d8-59d4d727476f
   Example of a variable declaration. #flashcard 
    variable "list_example" {
     description = "An example of a list in Terraform"
     type = list
     default = ["a", "b", "c"]
     }
-
- id:: 63639931-54a6-4867-a829-b8d107cabd1c
  
  The following are some of the best resources I’ve found on DevOps and infrastructure as code, including books, blog posts, newsletters, and talks.
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
     Hello, Startup: A Programmer’s Guide to Building Products, Technologies, and Teams by Yevgeniy Brikman (O’Reilly) #flashcard
-
- id:: 63639931-7cb9-4382-9900-802c57542389
   Mention an example of a security group in AWS with Terraform. #flashcard 
    resource "aws_security_group" "instance" {
     name = "terraform-example-instance"
     ingress {
     from_port = 8080
     to_port = 8080
     protocol = "tcp"
     cidr_blocks = ["0.0.0.0/0"]
     }
     }
-
- id:: 63639931-dcf1-4b7f-802f-35c079622abc
  
  To use the value from an input variable in your Terraform code, you can use a new type of expression called a variable reference, which has the following syntax:
     var.<VARIABLE_NAME> #flashcard
-
- id:: 63639931-ea4c-425a-be4c-bfd3661ba6a7
  
  The idea behind immutable infrastructure is similar: once you’ve deployed a server, you never make changes to it again. If you need to update something, such as deploy a new version of your code, you create a new image from your server template and you deploy it on a new server. Because servers never change, it’s a lot easier to reason about what’s deployed. #flashcard
-
- id:: 63639931-8a53-4dc9-8059-0e4086dd8565
  
  An expression in Terraform is anything that returns a value. You’ve already seen the simplest type of expressions, literals, such as strings (e.g., "ami-0c55b159cbfafe1f0") and numbers (e.g., 5). Terraform supports many other types of expressions #flashcard
-
- id:: 63639931-7e48-40ed-8323-323a85c94dd8
   About output variables in Terraform. #flashcard 
    In addition to input variables, Terraform also allows you to define output variables by using the following syntax:
     output "<NAME>" {
     value = <VALUE>
     [CONFIG ...]
     }
     The NAME is the name of the output variable, and VALUE can be any Terraform expression that you would like to output. The CONFIG can contain two additional parameters, both optional:
     description
     It’s always a good idea to use this parameter to document what type of data is contained in the output variable.
     sensitive
     Set this parameter to true to instruct Terraform not to log this output at the end of terraform apply. This is useful if the output variable contains sensitive material or secrets such as passwords or private keys.
-
- id:: 63639931-715a-49ee-8dec-a861e507ae9b
   What does provisioning mean? #flashcard 
    Whereas configuration management, server templating, and orchestration tools define the code that runs on each server, provisioning tools such as Terraform, CloudFormation, and OpenStack Heat are responsible for creating the servers themselves. In fact, you can use provisioning tools to not only create servers, but also databases, caches, load balancers, queues, monitoring, subnet configurations, firewall settings, routing rules, Secure Sockets Layer (SSL) certificates, and almost every other aspect of your infrastructure
-
- id:: 63639931-c9e4-4bbc-94f8-b3d8c8962a10
   How can you use a reference of an attribute in Terraform? #flashcard 
    One particularly useful type of expression is a reference, which allows you to access values from other parts of your code. To access the ID of the security group resource, you are going to need to use a resource attribute reference, which uses the following syntax:
     <PROVIDER>_<TYPE>.<NAME>.<ATTRIBUTE>
     where PROVIDER is the name of the provider (e.g., aws), TYPE is the type of resource (e.g., security_group), NAME is the name of that resource (e.g., the security group is named "instance"), and ATTRIBUTE is either one of the arguments of that resource (e.g., name) or one of the attributes exported by the resource (you can find the list of available attributes in the documentation for each resource).
-
- id:: 63639931-ed03-4185-8b7a-38a8506bf37b
  
  output variables show up in the console after you run terraform apply, which users of your Terraform code might find useful (e.g., you now know what IP to test after the web server is deployed). You can also use the terraform output command to list all outputs without applying any changes:
     $ terraform output
     public_ip = 54.174.13.5 #flashcard
-
- id:: 63639931-e71c-4808-b8b5-cabc1dd9c7f9
  
  That said, if you’re not using server templating tools, a good alternative is to use a configuration management and provisioning tool together. For example, you might use Terraform to provision your servers and run Chef to configure each one. #flashcard
-
- id:: 63639931-0e7e-4a5f-9286-eaeb01ce8af9
  
  When you add a reference from one resource to another, you create an implicit dependency. Terraform parses these dependencies, builds a dependency graph from them, and uses that to automatically determine in which order it should create resources. For example, if you were deploying this code from scratch, Terraform would know that it needs to create the security group before the EC2 Instance, because the EC2 Instance references the ID of the security group. You can even get Terraform to show you the dependency graph by running the graph command: #flashcard
-
- id:: 63639931-a115-4dcd-86c3-34b4692970fb
  
  And you can run terraform output <OUTPUT_NAME> to see the value of a specific output called <OUTPUT_NAME>:
     $ terraform output public_ip
     54.174.13.5 #flashcard
-
- id:: 63639931-3619-4449-aea5-77c26dc650b9
  
  The -/+ in the plan output means “replace” #flashcard
-
- id:: 63639931-73a3-4704-a298-22864290f97e
   About how can AWS ease with automated scalability. #flashcard 
    Managing such a cluster manually is a lot of work. Fortunately, you can let AWS take care of it for by you using an Auto Scaling Group (ASG), as shown in Figure 2-9. An ASG takes care of a lot of tasks for you completely automatically, including launching a cluster of EC2 Instances, monitoring the health of each Instance, replacing failed Instances, and adjusting the size of the cluster in response to load.
-
- id:: 63639931-c899-4746-86d6-414944de8db3
  
  provider "aws" {
     region = "us-east-2"
     }
     This tells Terraform that you are going to be using AWS as your provider and that you want to deploy your infrastructure into the us-east-2 region. #flashcard
-
- id:: 63639931-0745-479d-b345-8c9dbcd0c53d
   What is the syntax for declaring a variable: #flashcard 
    variable "NAME" {
     [CONFIG ...]
     }
-
- id:: 63639931-8696-4e6d-90d9-a73b9307183c
  
  Note that the ASG uses a reference to fill in the launch configuration name. This leads to a problem: launch configurations are immutable, so if you change any parameter of your launch configuration, Terraform will try to replace it. Normally, when replacing a resource, Terraform deletes the old resource first and then creates its replacement, but because your ASG now has a reference to the old resource, Terraform won’t be able to delete it.
     To solve this problem, you can use a lifecycle setting. Every Terraform resource supports several lifecycle settings that configure how that resource is created, updated, and/or deleted. A particularly useful lifecycle setting is create_before_destroy. If you set create_before_destroy to true, Terraform will invert the order in which it replaces resources, creating the replacement resource first (including updating any references that were pointing at the old resource to point to the replacement) and then deleting the old resource. Add the lifecycle block to your aws_launch_configuration #flashcard
-
- id:: 63639931-4edb-4a7f-998a-15e77b096594
   What is the general syntax for creating a resource in Terraform? #flashcard 
    resource "<PROVIDER>_<TYPE>" "<NAME>" {
     [CONFIG ...]
     }
     where PROVIDER is the name of a provider (e.g., aws), TYPE is the type of resource to create in that provider (e.g., instance), NAME is an identifier you can use throughout the Terraform code to refer to this resource (e.g., my_instance), and CONFIG consists of one or more arguments that are specific to that resource.
-
- id:: 63639931-f50c-4c21-8bb0-835cfa9a4d61
   What is a data source in Terraform? #flashcard 
    A data source represents a piece of read-only information that is fetched from the provider (in this case, AWS) every time you run Terraform. Adding a data source to your Terraform configurations does not create anything new; it’s just a way to query the provider’s APIs for data and to make that data available to the rest of your Terraform code. Each Terraform provider exposes a variety of data sources. For example, the AWS provider includes data sources to look up VPC data, subnet data, AMI IDs, IP address ranges, the current user’s identity, and much more.
-
- id:: 63639931-4784-4765-a1fa-682ec8e946e1
   About referring to the documentation of Terraform. #flashcard 
    Terraform supports dozens of providers, each of which supports dozens of resources, and each resource has dozens of arguments. There is no way to remember them all. When you’re writing Terraform code, you should be regularly referring to the Terraform documentation to look up what resources are available and how to use each one. For example, here’s the documentation for the aws_instance resource. I’ve been using Terraform for years and I still refer to these docs multiple times per day!
-
- id:: 63639931-5074-4fe0-9f4a-656d6309f300
   Example of data source declaration in Terraform. #flashcard 
    data "aws_vpc" "default" {
     default = true
     }
-
- id:: 63639931-d483-4b56-900f-9ccadb4fd8fa
  
  The terraform binary contains the basic functionality for Terraform, but it does not come with the code for any of the providers (e.g., the AWS provider, Azure provider, GCP provider, etc.), so when you’re first starting to use Terraform, you need to run terraform init to tell Terraform to scan the code, figure out which providers you’re using, and download the code for them. By default, the provider code will be downloaded into a .terraform folder, which is Terraform’s scratch directory (you may want to add it to .gitignore). #flashcard
-
- id:: 63639931-65c6-4a1f-809e-a9bcba2e0df4
   Example of data source use in Terraform. #flashcard 
    data.<PROVIDER>_<TYPE>.<NAME>.<ATTRIBUTE>
     For example, to get the ID of the VPC from the aws_vpc data source, you would use the following:
     data.aws_vpc.default.id
-
- id:: 63639931-9505-45c0-b8ec-94b489e13a4e
  
  The plan command lets you see what Terraform will do before actually making any changes. #flashcard
-
- id:: 63639931-a344-4a99-932f-6e9e9ec17d0f
  
  When you’re done experimenting with Terraform, either at the end of this chapter, or at the end of future chapters, it’s a good idea to remove all of the resources you created so that AWS doesn’t charge you for them. Because Terraform keeps track of what resources you created, cleanup is simple. All you need to do is run the destroy command: #flashcard
-
- id:: 63639931-41a0-4db2-b5b6-292082d1b9b3
   How does the Terraform output specify the results? #flashcard 
    The output of the plan command is similar to the output of the diff command that is part of Unix, Linux, and git: anything with a plus sign (+) will be created, anything with a minus sign (–) will be deleted, and anything with a tilde sign (~) will be modified in place.
-
- id:: 63639931-69b9-42a1-9a38-e82a61503266
  
  Note that later in the book, you will continue to develop this example, so don’t delete the Terraform code! However, feel free to run destroy on the actual deployed resources whenever you want. After all, the beauty of infrastructure as code is that all of the information about those resources is captured in code, so you can re-create all of them at any time with a single command: terraform apply. In fact, you might want to commit your latest changes to Git so that you can keep track of the history of your infrastructure. #flashcard
-
- id:: 63639931-037f-4f97-955d-a75ac23948ad
  
  To actually create the Instance, run the terraform apply command: #flashcard
-
### 3. How to Manage Terraform State
- id:: 63639931-ad71-44b0-9600-4eba79d02bc9
  
  In other words, the output of the plan command is a diff between the code on your computer and the infrastructure deployed in the real world, as discovered via IDs in the state file. #flashcard
-
- id:: 63639931-b6cb-4b29-aca8-044cb6f7d43d
  
  Instead of using version control, the best way to manage shared storage for state files is to use Terraform’s built-in support for remote backends. A Terraform backend determines how Terraform loads and stores state. The default backend, which you’ve been using this entire time, is the local backend, which stores the state file on your local disk. Remote backends allow you to store the state file in a remote, shared store. A number of remote backends are supported, including Amazon S3; Azure Storage; Google Cloud Storage; and HashiCorp’s Terraform Cloud, Terraform Pro, and Terraform Enterprise. #flashcard
-
- id:: 63639931-eb92-4c78-a444-a1f6f67567f6
   About port numbers #flashcard 
    PORT NUMBERS
     The reason this example uses port 8080, rather than the default HTTP port 80, is that listening on any port less than 1024 requires root user privileges. This is a security risk, because any attacker who manages to compromise your server would get root privileges, too.
     Therefore, it’s a best practice to run your web server with a non-root user that has limited permissions. That means you have to listen on higher-numbered ports, but as you’ll see later in this chapter, you can configure a load balancer to listen on port 80 and route traffic to the high-numbered ports on your server(s).
-
- id:: 63639931-3e2f-44f4-afb4-db28862faa7f
   How do you interpolate a variable in Terraform? #flashcard 
    "${...}"
     You can put any valid reference within the curly braces, and Terraform will convert it to a string. For example, here’s how you can use var.server_port inside of the User Data string:
     user_data = <<-EOF
     #!/bin/bash
     echo "Hello, World" > index.html
     nohup busybox httpd -f -p ${var.server_port} &
     EOF
-
- id:: 63639931-abf5-46d8-8d99-ac91a026d1fc
   How do you interpolate a variable in Terraform? #flashcard 
    "${...}"
-