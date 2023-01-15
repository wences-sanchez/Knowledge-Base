title:: Readwise/Kubernetes in Action (highlights)
deck:: [[O'Reilly-Learning::Kubernetes in Action]]
author:: [[Marko Lukša]]
full-title:: "Kubernetes in Action"
category:: #books

tags:: DevOps O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Sunday, 15-01-2023]]
	- Chapter 1. Introducing Kubernetes
		- 1.1. Understanding the need for a system like Kubernetes
			- 1.1.3. Moving to continuous delivery: DevOps and NoOps
				- -
					- What is NoOps? #flashcard
						- Ideally, you want the developers to deploy applications themselves without knowing anything about the hardware infrastructure and without dealing with the ops team. This is referred to as *NoOps*. Obviously, you still need someone to take care of the hardware infrastructure, but ideally, without having to deal with peculiarities of each application running on it.
					- ([View Highlight](https://read.readwise.io/read/01gpnmzk5ze0c7ttt4nwjc8b1s))
				- -
			- 1.2. Introducing container technologies
				- -
					- Figure 1.4. Using VMs to isolate groups of applications vs. isolating individual apps with containers
					  
					  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added8-01fig04_alt_1eMwdte.jpg) #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpnnc5gef3x2qjscgce6jsnm))
				- -
				- -
					- Which two mechanisms make containers possible? #flashcard
						- Two mechanisms make this possible. The first one, *Linux Namespaces*, makes sure each process sees its own personal view of the system (files, processes, network interfaces, hostname, and so on). The second one is *Linux Control Groups (cgroups)*, which limit the amount of resources the process can consume (CPU, memory, network bandwidth, and so on).
					- ([View Highlight](https://read.readwise.io/read/01gpnnh2ms2a3mspna0w7mkkgr))
				- -
				- -
					- Building, distributing, and running a Docker image
					  
					  [Figure 1.6](https://readwise.io/reader/document_raw_content/26339439#ch01fig06) shows all three concepts and how they relate to each other. The developer first builds an image and then pushes it to a registry. The image is thus available to anyone who can access the registry. They can then pull the image to any other machine running Docker and run the image. Docker creates an isolated container based on the image and runs the binary executable specified as part of the image.
					  
					  Figure 1.6. Docker images, registries, and containers
					  
					  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added10-01fig06_alt_MqDxmEi.jpg) #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpnx8nx5drvpdzsj2tctq1g0))
				- -
				- -
					- Understanding image layers
					  
					  I’ve already said that Docker images are composed of layers. Different images can contain the exact same layers because every Docker image is built on top of another image and two different images can both use the same parent image as their base. This speeds up the distribution of images across the network, because layers that have already been transferred as part of the first image don’t need to be transferred again when transferring the other image.
					  
					  But layers don’t only make distribution more efficient, they also help reduce the storage footprint of images. Each layer is only stored once. Two containers created from two images based on the same base layers can therefore read the same files, but if one of them writes over those files, the other one doesn’t see those changes. Therefore, even if they share files, they’re still isolated from each other. This works because container image layers are read-only. When a container is run, a new writable layer is created on top of the layers in the image. When the process in the container writes to a file located in one of the underlying layers, a copy of the whole file is created in the top-most layer and the process writes to the copy. #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpnxp8wmrextgjhdc0ne5cbd))
				- -
				- -
					- Docker was the first container platform that made containers mainstream. I hope I’ve made it clear that Docker itself doesn’t provide process isolation. The actual isolation of containers is done at the Linux kernel level using kernel features such as Linux Namespaces and cgroups. Docker only makes it easy to use those features. #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpnxtx2t3ef8xzzatqd55n46))
				- -
			- 1.3. Introducing Kubernetes
				- -
					- Define Kubernetes and highlight its relationship with cloud providers: #flashcard
						- Kubernetes is a software system that allows you to easily deploy and manage containerized applications on top of it. It relies on the features of Linux containers to run heterogeneous applications without having to know any internal details of these applications and without having to manually deploy these applications on each host. Because these apps run in containers, they don’t affect other apps running on the same server, which is critical when you run applications for completely different organizations on the same hardware. This is of paramount importance for cloud providers, because they strive for the best possible utilization of their hardware while still having to maintain complete isolation of hosted applications.
					- ([View Highlight](https://read.readwise.io/read/01gpnydhp4h0zksrpw1a63y3p6))
				- -
				- -
					- [Figure 1.8](https://readwise.io/reader/document_raw_content/26339439#ch01fig08) shows the simplest possible view of a Kubernetes system. The system is composed of a master node and any number of worker nodes. When the developer submits a list of apps to the master, Kubernetes deploys them to the cluster of worker nodes. What node a component lands on doesn’t (and shouldn’t) matter—neither to the developer nor to the system administrator.
					  
					  Figure 1.8. Kubernetes exposes the whole datacenter as a single deployment platform.
					  
					  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added12-01fig08_alt_Zn8B1S0.jpg) #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpnykwz10084w0v4xxrdjfvw))
				- -
				- -
					- Because your application doesn’t care which node it’s running on, Kubernetes can relocate the app at any time, and by mixing and matching apps, achieve far better resource utilization than is possible with manual scheduling. #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpnyq9k9kynwasqse3kneke9))
				- -
				- -
					- What are the two main types of Kubernetes nodes? #flashcard
						- At the hardware level, a Kubernetes cluster is composed of many nodes, which can be split into two types:
						  
						  •   The *master* node, which hosts the *Kubernetes Control Plane* that controls and manages the whole Kubernetes system
						  •   Worker *nodes* that run the actual applications you deploy
					- ([View Highlight](https://read.readwise.io/read/01gpnytbej5x95d8v0hqzyx5n2))
				- -
				- -
					- Explain the elements of Kubernetes #flashcard
						- The components that make up a Kubernetes cluster
						  
						  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added13-01fig09_alt_rPLZigU.jpg)
						  
						  The Control Plane
						  
						  The Control Plane is what controls the cluster and makes it function. It consists of multiple components that can run on a single master node or be split across multiple nodes and replicated to ensure high availability. These components are
						  
						  •   The *Kubernetes API Server*, which you and the other Control Plane components communicate with
						  •   The *Scheduler*, which schedules your apps (assigns a worker node to each deployable component of your application)
						  •   The *Controller Manager*, which performs cluster-level functions, such as replicating components, keeping track of worker nodes, handling node failures, and so on
						  •   *etcd*, a reliable distributed data store that persistently stores the cluster configuration.
						  
						  The components of the Control Plane hold and control the state of the cluster, but they don’t run your applications. This is done by the (worker) nodes.
						  
						  The nodes
						  
						  The worker nodes are the machines that run your containerized applications. The task of running, monitoring, and providing services to your applications is done by the following components:
						  
						  •   Docker, rkt, or another *container runtime*, which runs your containers
						  •   The *Kubelet*, which talks to the API server and manages containers on its node
						  •   The *Kubernetes Service Proxy (kube-proxy)*, which load-balances network traffic between application components
					- ([View Highlight](https://read.readwise.io/read/01gpnz17wbphdazj8fhmbe7h8j))
				- -