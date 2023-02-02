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
					  id:: 3692ca3b-b714-4bd2-803c-b8639ee54337
						- Ideally, you want the developers to deploy applications themselves without knowing anything about the hardware infrastructure and without dealing with the ops team. This is referred to as *NoOps*. Obviously, you still need someone to take care of the hardware infrastructure, but ideally, without having to deal with peculiarities of each application running on it.
					- ([View Highlight](https://read.readwise.io/read/01gpnmzk5ze0c7ttt4nwjc8b1s))
				- -
			- 1.2. Introducing container technologies
				- -
					- Figure 1.4. Using VMs to isolate groups of applications vs. isolating individual apps with containers
					  id:: 9f711f97-0e6f-4dea-a1f1-50c36ba30c45
					  
					  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added8-01fig04_alt_1eMwdte.jpg) #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpnnc5gef3x2qjscgce6jsnm))
				- -
				- -
					- Which two mechanisms make containers possible? #flashcard
					  id:: 8e0517c9-25af-4310-9e88-2f29c24c3321
						- Two mechanisms make this possible. The first one, *Linux Namespaces*, makes sure each process sees its own personal view of the system (files, processes, network interfaces, hostname, and so on). The second one is *Linux Control Groups (cgroups)*, which limit the amount of resources the process can consume (CPU, memory, network bandwidth, and so on).
					- ([View Highlight](https://read.readwise.io/read/01gpnnh2ms2a3mspna0w7mkkgr))
				- -
				- -
					- Building, distributing, and running a Docker image
					  id:: a2205bc6-e6e4-4479-b3eb-adcb8b59d061
					  
					  [Figure 1.6](https://readwise.io/reader/document_raw_content/26339439#ch01fig06) shows all three concepts and how they relate to each other. The developer first builds an image and then pushes it to a registry. The image is thus available to anyone who can access the registry. They can then pull the image to any other machine running Docker and run the image. Docker creates an isolated container based on the image and runs the binary executable specified as part of the image.
					  
					  Figure 1.6. Docker images, registries, and containers
					  
					  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added10-01fig06_alt_MqDxmEi.jpg) #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpnx8nx5drvpdzsj2tctq1g0))
				- -
				- -
					- Understanding image layers
					  id:: 0aa58801-9830-422b-823d-87b0dfe024a5
					  
					  I’ve already said that Docker images are composed of layers. Different images can contain the exact same layers because every Docker image is built on top of another image and two different images can both use the same parent image as their base. This speeds up the distribution of images across the network, because layers that have already been transferred as part of the first image don’t need to be transferred again when transferring the other image.
					  
					  But layers don’t only make distribution more efficient, they also help reduce the storage footprint of images. Each layer is only stored once. Two containers created from two images based on the same base layers can therefore read the same files, but if one of them writes over those files, the other one doesn’t see those changes. Therefore, even if they share files, they’re still isolated from each other. This works because container image layers are read-only. When a container is run, a new writable layer is created on top of the layers in the image. When the process in the container writes to a file located in one of the underlying layers, a copy of the whole file is created in the top-most layer and the process writes to the copy. #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpnxp8wmrextgjhdc0ne5cbd))
				- -
				- -
					- Docker was the first container platform that made containers mainstream. I hope I’ve made it clear that Docker itself doesn’t provide process isolation. The actual isolation of containers is done at the Linux kernel level using kernel features such as Linux Namespaces and cgroups. Docker only makes it easy to use those features. #flashcard
					  id:: 867dc26c-2bda-4784-b88f-75a71bf06002
					- ([View Highlight](https://read.readwise.io/read/01gpnxtx2t3ef8xzzatqd55n46))
				- -
			- 1.3. Introducing Kubernetes
				- -
					- Define Kubernetes and highlight its relationship with cloud providers: #flashcard
					  id:: 75f0e826-9745-4814-bee3-eb4b6516ed18
						- Kubernetes is a software system that allows you to easily deploy and manage containerized applications on top of it. It relies on the features of Linux containers to run heterogeneous applications without having to know any internal details of these applications and without having to manually deploy these applications on each host. Because these apps run in containers, they don’t affect other apps running on the same server, which is critical when you run applications for completely different organizations on the same hardware. This is of paramount importance for cloud providers, because they strive for the best possible utilization of their hardware while still having to maintain complete isolation of hosted applications.
					- ([View Highlight](https://read.readwise.io/read/01gpnydhp4h0zksrpw1a63y3p6))
				- -
				- -
					- [Figure 1.8](https://readwise.io/reader/document_raw_content/26339439#ch01fig08) shows the simplest possible view of a Kubernetes system. The system is composed of a master node and any number of worker nodes. When the developer submits a list of apps to the master, Kubernetes deploys them to the cluster of worker nodes. What node a component lands on doesn’t (and shouldn’t) matter—neither to the developer nor to the system administrator.
					  id:: a0c879bc-0ab0-4633-90ee-526330cf0a67
					  
					  Figure 1.8. Kubernetes exposes the whole datacenter as a single deployment platform.
					  
					  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added12-01fig08_alt_Zn8B1S0.jpg) #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpnykwz10084w0v4xxrdjfvw))
				- -
				- -
					- Because your application doesn’t care which node it’s running on, Kubernetes can relocate the app at any time, and by mixing and matching apps, achieve far better resource utilization than is possible with manual scheduling. #flashcard
					  id:: 365ed82d-cc71-46c2-b680-a40737e0950f
					- ([View Highlight](https://read.readwise.io/read/01gpnyq9k9kynwasqse3kneke9))
				- -
				- -
					- What are the two main types of Kubernetes nodes? #flashcard
					  id:: 4184ea83-3c3a-40cd-bd63-14353ca010e6
						- At the hardware level, a Kubernetes cluster is composed of many nodes, which can be split into two types:
						  
						  •   The *master* node, which hosts the *Kubernetes Control Plane* that controls and manages the whole Kubernetes system
						  •   Worker *nodes* that run the actual applications you deploy
					- ([View Highlight](https://read.readwise.io/read/01gpnytbej5x95d8v0hqzyx5n2))
				- -
				- -
					- Explain the elements of Kubernetes #flashcard
					  id:: 0a9b7a6d-19a1-4e32-9636-698c89690594
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
- New highlights added [[Tuesday, 17-01-2023]] at 10:26 AM
	- -
		- How can we find a specific service between the whole number of containers, in Kubernetes? #flashcard
		  id:: 12c2aed4-f32a-45cf-9830-29b06b54ea71
			- To allow clients to easily find containers that provide a specific service, you can tell Kubernetes which containers provide the same service and Kubernetes will expose all of them at a single static IP address and expose that address to all applications running in the cluster. This is done through environment variables, but clients can also look up the service IP through good old DNS. The kube-proxy will make sure connections to the service are load balanced across all the containers that provide the service. The IP address of the service stays constant, so clients can always connect to its containers, even when they’re moved around the cluster.
		- ([View Highlight](https://read.readwise.io/read/01gpwtsnzczqdsgb08xw04rscy))
	- -
	- -
		- How “fault resilient” works #flashcard
		  id:: a5beab8c-b53f-4bc5-8d5d-66ae9a7577d6
			- Having a system that allows moving an application across the cluster at any time is also valuable in the event of server failures. As your cluster size increases, you’ll deal with failing computer components ever more frequently.
			  
			  Kubernetes monitors your app components and the nodes they run on and automatically reschedules them to other nodes in the event of a node failure. This frees the ops team from having to migrate app components manually and allows the team to immediately focus on fixing the node itself and returning it to the pool of available hardware resources instead of focusing on relocating the app.
		- ([View Highlight](https://read.readwise.io/read/01gpwvf8ep5qngmwh6t21yggvx))
	- -
	- Chapter 2. First steps with Docker and Kubernetes
		- 2.1. Creating, running, and sharing a container image
			- -
				- Kubernetes in different OS than Linux #flashcard
				  id:: 95fd489d-2ad2-4f31-bfb8-e0ce2ae2aed7
					- If you don’t use Linux, you’ll need to start a Linux virtual machine (VM) and run Docker inside that VM. If you’re using a Mac or Windows and install Docker per instructions, Docker will set up a VM for you and run the Docker daemon inside that VM. The Docker client executable will be available on your host OS, and will communicate with the daemon inside the VM.
				- ([View Highlight](https://read.readwise.io/read/01gpwvwehq2kbswt9sytsnsd68))
			- -
			- -
				- $ docker run busybox echo "Hello world" #flashcard
				  id:: f5f4fee1-3774-4177-80fb-92b0b5b65de5
				- ([View Highlight](https://read.readwise.io/read/01gpww3tjr48ph4gb6yk4ms9c1))
			- -
			- -
				- How do you execute an instance of an image n
				  id:: c3735e9c-9c0f-49e8-be9d-383a3b444fac
				  Docker? #flashcard
					- $ docker run <imagen>
				- tags:: [[code]]
				- ([View Highlight](https://read.readwise.io/read/01gpww7ssebv6qnc5qsw02d6qg))
			- -
			- -
				- How can you execute a specific version of an image in Docker? #flashcard
				  id:: 519bc56a-2ae5-46b6-a339-39f3bda48bcd
					- $ docker run <image>:<tag>
				- tags:: [[code]]
				- ([View Highlight](https://read.readwise.io/read/01gpwwdw67j7h959rzz895dj2t))
			- -
			- -
				- Example of a Dockerfile #flashcard
				  id:: 68faa16e-cba5-4571-b805-422f9918cacd
					- A Dockerfile for building a container image for your app
					  
					  FROM node:7
					  ADD app.js /app.js
					  ENTRYPOINT ["node", "app.js"]
					  
					  The FROM line defines the container image you’ll use as a starting point (the base image you’re building on top of). In your case, you’re using the node container image, tag 7. In the second line, you’re adding your app.js file from your local directory into the root directory in the image, under the same name (app.js). Finally, in the third line, you’re defining what command should be executed when somebody runs the image. In your case, the command is node app.js.
				- ([View Highlight](https://read.readwise.io/read/01gpwwq0c2vpb3mzcvabshb4a0))
			- -
			- -
				- How do you make an image from a Dockerfile? #flashcard
				  id:: c1ea8a51-1392-42a3-9010-3911c9fcfd05
					- $ docker build -t kubia .
				- tags:: [[code]]
				- ([View Highlight](https://read.readwise.io/read/01gpwws2rhkbdawp06hwpgk5fh))
			- -
			- -
				- An image isn’t a single, big, binary blob, but is composed of multiple layers, which you may have already noticed when running the busybox example (there were multiple Pull complete lines—one for each layer). Different images may share several layers, which makes storing and transferring images much more efficient. For example, if you create multiple images based on the same base image (such as node:7 in the example), all the layers comprising the base image will be stored only once. Also, when pulling an image, Docker will download each layer individually. Several layers may already be stored on your machine, so Docker will only download those that aren’t. #flashcard
				  id:: 72f691e0-62f3-4ab3-8eb8-3073e29285a6
				- ([View Highlight](https://read.readwise.io/read/01gpwx105kdg7r1rwdbdc8fskn))
			- -
			- -
				- You may think that each Dockerfile creates only a single new layer, but that’s not the case. When building an image, a new layer is created for each individual command in the Dockerfile. During the build of your image, after pulling all the layers of the base image, Docker will create a new layer on top of them and add the app.js file into it. Then it will create yet another layer that will specify the command that should be executed when the image is run. This last layer will then be tagged as kubia:latest. This is shown in [figure 2.3](https://readwise.io/reader/document_raw_content/26339439#ch02fig03), which also shows how a different image called other:latest would use the same layers of the Node.js image as your own image does.
				  id:: ed60b7aa-5ec8-492c-aa37-9f301ac59e61
				  
				  Figure 2.3. Container images are composed of layers that can be shared among different images.
				  
				  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added17-02fig03_alt_1oz7GTY.jpg) #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gpwx7c0gwfxj8tbcwrx6w4kh))
			- -
			- -
				- How do you list your locally stored images in Docker? #flashcard
				  id:: 0d8faca6-cf28-42b7-9cad-77e1fca6ed3a
					- **$ docker images** REPOSITORY TAG IMAGE ID CREATED VIRTUAL SIZE kubia latest d30ecc7419e7 1 minute ago 637.1 MB ...
				- tags:: [[code]]
				- ([View Highlight](https://read.readwise.io/read/01gpwx91tjrd9y3d19p1t37s2b))
			- -
			- -
				- You can now run your image with the following command:
				  id:: 63c0bdba-8433-4b04-b2fb-4386c1cbb655
				  
				  **$ docker run --name kubia-container -p 8080:8080 -d kubia**
				  
				  This tells Docker to run a new container called kubia-container from the kubia image. The container will be detached from the console (-d flag), which means it will run in the background. Port 8080 on the local machine will be mapped to port 8080 inside the container (-p 8080:8080 option), so you can access the app through http://localhost:8080.
				  
				  If you’re not running the Docker daemon on your local machine (if you’re using a Mac or Windows, the daemon is running inside a VM), you’ll need to use the hostname or IP of the VM running the daemon instead of localhost. You can look it up through the DOCKER_HOST environment variable. #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gpwxcx13b22jazw75jn2c01e))
			- -
			- -
				- How do you list your running containers in Docker? #flashcard
				  id:: 752ea8dc-ee02-44aa-87bf-b171517f5187
					- **$ docker ps** CONTAINER ID IMAGE COMMAND CREATED ... 44d76963e8e1 kubia:latest "/bin/sh -c 'node ap 6 minutes ago ... ... STATUS PORTS NAMES ... Up 6 minutes 0.0.0.0:8080->8080/tcp kubia-container
				- tags:: [[code]]
				- ([View Highlight](https://read.readwise.io/read/01gpwxg0npbpd8c25jwmewxydy))
			- -
			- -
				- The docker ps command only shows the most basic information about the containers. To see additional information, you can use docker inspect:
				  id:: 2e334d87-779b-49d4-8b48-b76b4bf162e6
				  
				  **$ docker inspect kubia-container**
				  
				  Docker will print out a long JSON containing low-level information about the container. #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gpwxjmp9annfbrbhphqdmr61))
			- -
			- -
				- The Node.js image on which you’ve based your image contains the bash shell, so you can run the shell inside the container like this:
				  id:: ec122c3a-f936-4ebf-8d16-17bf0609db2a
				  
				  **$ docker exec -it kubia-container bash**
				  
				  This will run bash inside the existing kubia-container container. The bash process will have the same Linux namespaces as the main container process. This allows you to explore the container from within and see how Node.js and your app see the system when running inside the container. The -it option is shorthand for two options:
				  
				  •   -i, which makes sure STDIN is kept open. You need this for entering commands into the shell.
				  •   -t, which allocates a pseudo terminal (TTY).
				  
				  You need both if you want the use the shell like you’re used to. (If you leave out the first one, you can’t type any commands, and if you leave out the second one, the command prompt won’t be displayed and some commands will complain about the TERM variable not being set.) #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gpwxpaacxrs5cbvsesghgh6j))
			- -
			- -
				- Stopping and removing a Docker container #flashcard
				  id:: 43da8072-b2fb-4aa2-be26-59feb8018784
					- To stop your app, you tell Docker to stop the kubia-container container:
					  
					  **$ docker stop kubia-container**
					  
					  This will stop the main process running in the container and consequently stop the container, because no other processes are running inside the container. The container itself still exists and you can see it with docker ps -a. The -a option prints out all the containers, those running and those that have been stopped. To truly remove a container, you need to remove it with the docker rm command:
					  
					  **$ docker rm kubia-container**
					  
					  This deletes the container. All its contents are removed and it can’t be started again.
				- ([View Highlight](https://read.readwise.io/read/01gpwxt97t19c68f14kfz5zccd))
			- -
			- -
				- Tagging an image under an additional tag in Docker #flashcard
				  id:: e28869a4-2b85-48ef-b734-c6dee75e5fb6
					- Once you know your ID, you’re ready to rename your image, currently tagged as kubia, to luksa/kubia (replace luksa with your own Docker Hub ID):
					  
					  **$ docker tag kubia luksa/kubia**
					  
					  This doesn’t rename the tag; it creates an additional tag for the same image. You can confirm this by listing the images stored on your system with the docker images command, as shown in the following listing.
				- ([View Highlight](https://read.readwise.io/read/01gpwxyz24722bdqnnwzmwr27w))
			- -
			- -
				- Pushing an image to Docker Hub #flashcard
				  id:: ad548352-e64a-4ab1-8b80-0e11f043f785
					- Before you can push the image to Docker Hub, you need to log in under your user ID with the docker login command. Once you’re logged in, you can finally push the yourid/kubia image to Docker Hub like this:
					  
					  **$ docker push luksa/kubia**
				- ([View Highlight](https://read.readwise.io/read/01gpwy0nqddhp4mnzq12cgkr74))
			- -
			- 2.2. Setting up a Kubernetes cluster
				- -
					- You’ll use kubectl often. You’ll soon realize that having to type the full command every time is a real pain. Before you continue, take a minute to make your life easier by setting up an alias and tab completion for kubectl.
					  id:: 15be2821-d2d8-4cf8-9bca-72ab1d551edd
					  
					  Creating an alias
					  
					  Throughout the book, I’ll always be using the full name of the kubectl executable, but you may want to add a short alias such as k, so you won’t have to type kubectl every time. If you haven’t used aliases yet, here’s how you define one. Add the following line to your ~/.bashrc or equivalent file:
					  
					  **alias k=kubectl** #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpwyx96dk30g25q59mt07ymb))
				- -
				- -
					- For example, instead of having to write the whole node name in the previous example, all you’d need to type is
					  id:: 11f171e4-3fd2-4e4e-928b-b00d0053ddcb
					  
					  **$ kubectl desc<TAB> no<TAB> gke-ku<TAB>**
					  
					  To enable tab completion in bash, you’ll first need to install a package called bash-completion and then run the following command (you’ll probably also want to add it to ~/.bashrc or equivalent):
					  
					  **$ source <(kubectl completion bash)**
					  
					  But there’s one caveat. When you run the preceding command, tab completion will only work when you use the full kubectl name (it won’t work when you use the k alias). To fix this, you need to transform the output of the kubectl completion command a bit:
					  
					  **$ source <(kubectl completion bash | sed s/kubectl/k/g)** #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpwz028pyghve8mb2p4dzsfe))
				- -
			- 2.3. Running your first app on Kubernetes
				- -
					- Explain what is a pod in Kubernetes #flashcard
					  id:: cf0eb154-5e93-4933-90ac-53d049844e83
						- Each pod is like a separate logical machine with its own IP, hostname, processes, and so on, running a single application. The application can be a single process, running in a single container, or it can be a main application process and additional supporting processes, each running in its own container. All the containers in a pod will appear to be running on the same logical machine, whereas containers in other pods, even if they’re running on the same worker node, will appear to be running on a different one.
						  
						  To better understand the relationship between containers, pods, and nodes, examine [figure 2.5](https://readwise.io/reader/document_raw_content/26339439#ch02fig05). As you can see, each pod has its own IP and contains one or more containers, each running an application process. Pods are spread out across different worker nodes.
						  
						  Figure 2.5. The relationship between containers, pods, and physical worker nodes
						  
						  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added19-02fig05_alt_FkmyoIt.jpg)
					- ([View Highlight](https://read.readwise.io/read/01gpwza3s1v8w93vr62qspk53w))
				- -
				- -
					- How can you list your pods in Kubernetes? #flashcard
					  id:: 8c4d408a-be26-491e-8929-c3a8a8a9c0ab
						- **$ kubectl get pods**
						  NAME          READY     STATUS    RESTARTS   AGE
						  kubia-4jfyf   0/1       Pending   0          1m
						  
						  This is your pod. Its status is still Pending and the pod’s single container is shown as not ready yet (this is what the 0/1 in the READY column means). The reason why the pod isn’t running yet is because the worker node the pod has been assigned to is downloading the container image before it can run it. When the download is finished, the pod’s container will be created and then the pod will transition to the Running state, as shown in the following listing.
						  
						  Listing 2.15. Listing pods again to see if the pod’s status has changed
						  
						  **$ kubectl get pods**
						  NAME          READY     STATUS    RESTARTS   AGE
						  kubia-4jfyf   1/1       Running   0          5m
					- tags:: [[code]]
					- ([View Highlight](https://read.readwise.io/read/01gpwzdw0anhwve0r3x9r65c5m))
				- -
				- -
					- Figure 2.6. Running the luksa/kubia container image in Kubernetes
					  id:: 5fa2f695-47be-4aba-837d-53657e10aa70
					  
					  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added20-02fig06_alt_ImS54Qd.jpg)
					  
					  When you ran the kubectl command, it created a new ReplicationController object in the cluster by sending a REST HTTP request to the Kubernetes API server. The ReplicationController then created a new pod, which was then scheduled to one of the worker nodes by the Scheduler. The Kubelet on that node saw that the pod was scheduled to it and instructed Docker to pull the specified image from the registry because the image wasn’t available locally. After downloading the image, Docker created and ran the container.
					  
					  The other two nodes are displayed to show context. They didn’t play any role in the process, because the pod wasn’t scheduled to them. #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpwzpzp2k5fnzst3mgb55zx3))
				- -
				- -
					- How can you list your services in
					  id:: 84cc1563-59ce-433d-a1b6-3b752ee61733
					  Kubernetes? #flashcard
						- you can see the newly created Service object by running the kubectl get services command, as shown in the following listing.
						  
						  Listing 2.16. Listing Services
						  
						  **$ kubectl get services**
						  NAME         CLUSTER-IP     EXTERNAL-IP   PORT(S)         AGE
						  kubernetes   10.3.240.1     <none>        443/TCP         34m
						  kubia-http   10.3.246.185   <pending>     8080:31348/TCP  4s
					- tags:: [[code]]
					- ([View Highlight](https://read.readwise.io/read/01gpx058svtxa7ryceyq650629))
				- -
				- -
					- Understanding the role of the ReplicationController #flashcard
					  id:: e70c213d-2a18-45a2-971e-eca0088803e3
						- The next component is the kubia ReplicationController. It makes sure there’s always exactly one instance of your pod running. Generally, ReplicationControllers are used to replicate pods (that is, create multiple copies of a pod) and keep them running. In your case, you didn’t specify how many pod replicas you want, so the Replication-Controller created a single one. If your pod were to disappear for any reason, the Replication-Controller would create a new pod to replace the missing one.
					- ([View Highlight](https://read.readwise.io/read/01gpx0k72tkngw0vfgv240fkds))
				- -
		- Chapter 3. Pods: running containers in Kubernetes
			- 3.1. Introducing pods
				- -
					- Understanding why multiple containers are better than one contain- ner running multiple processes
					  id:: 08283eda-10db-466e-a402-f9af55ae14ab
					  
					  Imagine an app consisting of multiple processes that either communicate through *IPC* (Inter-Process Communication) or through locally stored files, which requires them to run on the same machine. Because in Kubernetes you always run processes in containers and each container is much like an isolated machine, you may think it makes sense to run multiple processes in a single container, but you shouldn’t do that.
					  
					  Containers are designed to run only a single process per container (unless the process itself spawns child processes). If you run multiple unrelated processes in a single container, it is your responsibility to keep all those processes running, manage their logs, and so on. For example, you’d have to include a mechanism for automatically restarting individual processes if they crash. Also, all those processes would log to the same standard output, so you’d have a hard time figuring out what process logged what.
					  
					  Therefore, you need to run each process in its own container. That’s how Docker and Kubernetes are meant to be used.
					  
					  3.1.2. Understanding pods
					  
					  Because you’re not supposed to group multiple processes into a single container, it’s obvious you need another higher-level construct that will allow you to bind containers together and manage them as a single unit. This is the reasoning behind pods.
					  
					  A pod of containers allows you to run closely related processes together and provide them with (almost) the same environment as if they were all running in a single container, while keeping them somewhat isolated. This way, you get the best of both worlds. You can take advantage of all the features containers provide, while at the same time giving the processes the illusion of running together. #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpx1s7187cras2ct1x1xbpfw))
				- -
				- -
					- Understanding the partial isolation between containers of the same pod
					  id:: f638eb82-96ca-4d59-a7ec-804cc7fd686b
					  
					  In the previous chapter, you learned that containers are completely isolated from each other, but now you see that you want to isolate groups of containers instead of individual ones. You want containers inside each group to share certain resources, although not all, so that they’re not fully isolated. Kubernetes achieves this by configuring Docker to have all containers of a pod share the same set of Linux namespaces instead of each container having its own set. #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpx1ywr6y5mmfpn58r9cr78j))
				- -
				- -
					- About ports, IPs and pods in Kubernetes #flashcard
					  id:: 92104050-2126-463f-9025-b01517e6a477
						- One thing to stress here is that because containers in a pod run in the same Network namespace, they share the same IP address and port space. This means processes running in containers of the same pod need to take care not to bind to the same port numbers or they’ll run into port conflicts. But this only concerns containers in the same pod. Containers of different pods can never run into port conflicts, because each pod has a separate port space. All the containers in a pod also have the same loopback network interface, so a container can communicate with other containers in the same pod through localhost.
					- ([View Highlight](https://read.readwise.io/read/01gpx25c9wsysn10zf8pgpxgzp))
				- -
				- -
					- Another reason why you shouldn’t put them both into a single pod is scaling. A pod is also the basic unit of scaling. Kubernetes can’t horizontally scale individual containers; instead, it scales whole pods. #flashcard
					  id:: 152e10ba-bdbb-4124-bb08-8d85f2fdcac0
					- ([View Highlight](https://read.readwise.io/read/01gpx2hy22vhzv07xc1svbxf34))
				- -
				- -
					- The main reason to put multiple containers into a single pod is when the application consists of one main process and one or more complementary processes, as shown in [figure 3.3](https://readwise.io/reader/document_raw_content/26339439#ch03fig03).
					  id:: 6536d8ef-a9ae-4ec3-bc2b-04f8edadb460
					  
					  Figure 3.3. Pods should contain tightly coupled containers, usually a main container and containers that support the main one.
					  
					  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added26-03fig03_u5cSE3x.jpg)
					  
					  For example, the main container in a pod could be a web server that serves files from a certain file directory, while an additional container (a sidecar container) periodically downloads content from an external source and stores it in the web server’s directory. #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpx2q09sfbezjctvfasrgmp4))
				- -
				- -
					- Figure 3.4. A container shouldn’t run multiple processes. A pod shouldn’t contain multiple containers if they don’t need to run on the same machine.
					  id:: 5dc0b5a3-6cee-4a20-acf0-02c84e61f887
					  
					  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added27-03fig04_alt_4vv8G8J.jpg) #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpx3fxn7136wsje5w9yzfb6v))
				- -
				- -
					- you should also refer to the Kubernetes API reference documentation at [http://kubernetes.io/docs/reference/](http://kubernetes.io/docs/reference/) when creating objects #flashcard
					  id:: 37bb9d0c-2a36-4a90-b3a4-982fc28a3e5c
					- ([View Highlight](https://read.readwise.io/read/01gpx3mmtgnwryj5fn7gbdh2y0))
				- -
				- -
					- three important sections are found in almost all Kubernetes resources:
					  id:: 491418f1-49cc-4d8b-b07d-c15ba1627d21
					  
					  •   *Metadata* includes the name, namespace, labels, and other information about the pod.
					  •   *Spec* contains the actual description of the pod’s contents, such as the pod’s containers, volumes, and other data.
					  •   *Status* contains the current information about the running pod, such as what condition the pod is in, the description and status of each container, and the pod’s internal IP and other basic info. #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpx432zzab41kqpg938qz45d))
				- -
				- -
					- Listing 3.2. A basic pod manifest: kubia-manual.yaml
					  
					  apiVersion: v1               ❶
					  kind: Pod                    ❷
					  metadata:
					  name: kubia-manual         ❸
					  spec:
					  containers:
					- ([View Highlight](https://read.readwise.io/read/01gpx460zpe4jt0tzq8wmn9aqk))
				- -
				- -
					- When preparing a manifest, you can either turn to the Kubernetes reference documentation at [http://kubernetes.io/docs/api](http://kubernetes.io/docs/api) to see which attributes are supported by each API object, or you can use the kubectl explain command. #flashcard
					  id:: 57e29d25-20d7-440a-ab93-ea982256c6a9
					- ([View Highlight](https://read.readwise.io/read/01gpx49fk1wmxf58jx01n97r1z))
				- -
				- -
					- How can you create a pod from your YAML file in Kubernetes? #flashcard
					  id:: 5455839d-1f32-4e15-9886-0a15db1cd5c2
						- **$ kubectl create -f kubia-manual.yaml**
						  pod "kubia-manual" created
						  
						  The kubectl create -f command is used for creating any resource (not only pods) from a YAML or JSON file.
					- tags:: [[code]]
					- ([View Highlight](https://read.readwise.io/read/01gpx4dbr5e67hx0e22369eh5n))
				- -
				- -
					- Let’s list pods to see their statuses:
					  id:: bb727f25-cae1-4749-a797-9f2b4e8b1c6a
					  
					  **$ kubectl get pods**
					  NAME            READY   STATUS    RESTARTS   AGE
					  kubia-manual    1/1     Running   0          32s
					  kubia-zxzij     1/1     Running   0          1d #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpx4gq9n2s4xm3nhzwa0394v))
				- -
				- -
					- To see your pod’s log (more precisely, the container’s log) you run the following command on your local machine (no need to ssh anywhere):
					  id:: d49011c7-4cc1-46cb-a322-dea788fb7bbc
					  
					  **$ kubectl logs kubia-manual**
					  Kubia server starting... #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpx4jwgm1bm5fh2b5mq505ga))
				- -
				- -
					- If your pod includes multiple containers, you have to explicitly specify the container name by including the -c <container name> option when running kubectl logs. In your kubia-manual pod, you set the container’s name to kubia, so if additional containers exist in the pod, you’d have to get its logs like this:
					  id:: 4142c4d6-9abc-4057-98b4-ec54dcc41553
					  
					  **$ kubectl logs kubia-manual -c kubia**
					  Kubia server starting... #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpx4vpa2134wj2gfe5ttgxsk))
				- -
				- -
					- Forwarding a local network port to a port in the pod
					  id:: cb6ebf67-7246-45bc-be67-248445339128
					  
					  When you want to talk to a specific pod without going through a service (for debugging or other reasons), Kubernetes allows you to configure port forwarding to the pod. This is done through the kubectl port-forward command. The following command will forward your machine’s local port 8888 to port 8080 of your kubia-manual pod:
					  
					  **$ kubectl port-forward kubia-manual 8888:8080**
					  ... Forwarding from 127.0.0.1:8888 -> 8080
					  ... Forwarding from [::1]:8888 -> 8080
					  
					  The port forwarder is running and you can now connect to your pod through the local port. #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpx4z68q7xckrxtgjkz0jkhn))
				- -
			- 3.3. Organizing pods with labels
				- -
					- Figure 3.7. Organizing pods in a microservices architecture with pod labels
					  id:: a7a45d30-8c91-404b-88fa-707d64132ca2
					  
					  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added30-03fig07_alt_fLxDYX9.jpg) #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpx5tteqxp40vef0np2acjh6))
				- -
				- -
					- The kubectl get pods command doesn’t list any labels by default, but you can see them by using the --show-labels switch:
					  id:: 771d567a-c4c8-482b-bb97-e4d0d82bb061
					  
					  **$ kubectl get po --show-labels**
					  NAME            READY  STATUS   RESTARTS  AGE LABELS
					  kubia-manual    1/1    Running  0         16m <none>
					  kubia-manual-v2 1/1    Running  0         2m  creat_method=manual,env=prod
					  kubia-zxzij     1/1    Running  0         1d  run=kubia
					  
					  Instead of listing all labels, if you’re only interested in certain labels, you can specify them with the -L switch and have each displayed in its own column. List pods again and show the columns for the two labels you’ve attached to your kubia-manual-v2 pod:
					  
					  **$ kubectl get po -L creation_method,env**
					  NAME            READY   STATUS    RESTARTS   AGE   CREATION_METHOD   ENV
					  kubia-manual    1/1     Running   0          16m   <none>            <none>
					  kubia-manual-v2 1/1     Running   0          2m    manual            prod #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpx62aa0zfejh70hxbhyr8me))
				- -
				- -
					- Listing pods using a label selector
					  id:: dd10bbc7-0a35-476a-a743-342cf7cdb53c
					  
					  Let’s use label selectors on the pods you’ve created so far. To see all pods you created manually (you labeled them with creation_method=manual), do the following:
					  
					  **$ kubectl get po -l creation_method=manual**
					  NAME              READY     STATUS    RESTARTS   AGE
					  kubia-manual      1/1       Running   0          51m
					  kubia-manual-v2   1/1       Running   0          37m
					  
					  To list all pods that include the env label, whatever its value is:
					  
					  **$ kubectl get po -l env**
					  NAME              READY     STATUS    RESTARTS   AGE
					  kubia-manual-v2   1/1       Running   0          37m
					  
					  And those that don’t have the env label:
					  
					  **$ kubectl get po -l '!env'**
					  NAME           READY     STATUS    RESTARTS   AGE
					  kubia-manual   1/1       Running   0          51m
					  kubia-zxzij    1/1       Running   0          10d #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpx69d2xghxxj5f1ke3bvyce))
				- -
				- -
					- Similarly, you could also match pods with the following label selectors:
					  id:: 5720fd62-3662-4c57-8dc3-977f637ba460
					  
					  •   creation_method!=manual to select pods with the creation_method label with any value other than manual
					  •   env in (prod,devel) to select pods with the env label set to either prod or devel
					  •   env notin (prod,devel) to select pods with the env label set to any value other than prod or devel
					  
					  Turning back to the pods in the microservices-oriented architecture example, you could select all pods that are part of the product catalog microservice by using the app=pc label selector (shown in the following figure).
					  
					  Figure 3.8. Selecting the product catalog microservice pods using the “app=pc” label selector
					  
					  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added31-03fig08_alt_T6AT8OB.jpg)
					  
					  3.4.2. Using multiple conditions in a label selector
					  
					  A selector can also include multiple comma-separated criteria. Resources need to match all of them to match the selector. If, for example, you want to select only pods running the beta release of the product catalog microservice, you’d use the following selector: app=pc,rel=beta (visualized in [figure 3.9](https://readwise.io/reader/document_raw_content/26339439#ch03fig09)).
					  
					  Figure 3.9. Selecting pods with multiple label selectors
					  
					  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added32-03fig09_alt_cgR7Km4.jpg) #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpx6bw078k5bytkps5qp2dq9))
				- -
				- -
					- Using a label selector to schedule a pod to a specific node: kubia-gpu.yaml
					  
					  apiVersion: v1
					  kind: Pod
					  metadata:
					  name: kubia-gpu
					  spec:
					  nodeSelector:               ❶
					    gpu: "true"               ❶
					  containers:
					- ([View Highlight](https://read.readwise.io/read/01gpx6vvkysp86nky9p481n2tq))
				- -
				- -
					- A YAML definition of a namespace: custom-namespace.yaml
					  id:: 503b4108-ef15-4b35-a635-86a81b2d7cca
					  
					  apiVersion: v1
					  kind: Namespace                  ❶
					  metadata:
					  name: custom-namespace         ❷
					  
					  •   ❶ **This says you’re defining a namespace.**
					  •   ❷ **This is the name of the namespace.**
					  
					  Now, use kubectl to post the file to the Kubernetes API server:
					  
					  **$ kubectl create -f custom-namespace.yaml**
					  namespace "custom-namespace" created
					  
					  Creating a namespace with kubectl create namespace
					  
					  Although writing a file like the previous one isn’t a big deal, it’s still a hassle. Luckily, you can also create namespaces with the dedicated kubectl create namespace command, which is quicker than writing a YAML file. By having you create a YAML manifest for the namespace, I wanted to reinforce the idea that everything in Kubernetes has a corresponding API object that you can create, read, update, and delete by posting a YAML manifest to the API server.
					  
					  You could have created the namespace like this:
					  
					  **$ kubectl create namespace custom-namespace**
					  namespace "custom-namespace" created #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpx7vr2sdsj5efam5p0b86yk))
				- -
				- -
					- Wait, what!?! The kubia-zxzij pod is terminating, but a new pod called kubia-09as0, which wasn’t there before, has appeared. No matter how many times you delete all pods, a new pod called *kubia-something* will emerge.
					  id:: 684f96b0-25b3-4d2a-875c-92e7179d09df
					  
					  You may remember you created your first pod with the kubectl run command. In [chapter 2](https://readwise.io/reader/document_raw_content/26339439#ch02), I mentioned that this doesn’t create a pod directly, but instead creates a ReplicationController, which then creates the pod. As soon as you delete a pod created by the ReplicationController, it immediately creates a new one. To delete the pod, you also need to delete the ReplicationController. #flashcard
					- ([View Highlight](https://read.readwise.io/read/01gpx88fwsfw01yfxjc7bzjma0))
				- -
		- Chapter 4. Replication and other controllers: deploying managed pods
- New highlights added [[Monday, 23-01-2023]] at 9:23 AM
	- 4.1. Keeping pods healthy
		- -
			- 4.1.1. Introducing liveness probes #flashcard
			  id:: 6cabc5c8-0207-4e2a-a5b2-cf510da6c983
			- tags:: [[h4]]
			- ([View Highlight](https://read.readwise.io/read/01gpzrpgqjj0344k8xgj835a60))
		- -
		- -
			- What is a liveness probe in Kubernetes? #flashcard
			  id:: 5688f667-e832-4370-bcaa-e9b4862bf713
				- Kubernetes can check if a container is still alive through *liveness probes*. You can specify a liveness probe for each container in the pod’s specification. Kubernetes will periodically execute the probe and restart the container if the probe fails.
			- ([View Highlight](https://read.readwise.io/read/01gpzrqekskctqdy05zwh4jpkv))
		- -
		- -
			- What are the 3 ways of liveness probes in Kubernetes? #flashcard
			  id:: f59c6bcd-b407-44e6-9483-0ce9e7acbbb3
				- Kubernetes can probe a container using one of the three mechanisms:
				  
				  •   An *HTTP GET* probe performs an HTTP GET request on the container’s IP address, a port and path you specify. If the probe receives a response, and the response code doesn’t represent an error (in other words, if the HTTP response code is 2xx or 3xx), the probe is considered successful. If the server returns an error response code or if it doesn’t respond at all, the probe is considered a failure and the container will be restarted as a result.
				  •   A *TCP Socket* probe tries to open a TCP connection to the specified port of the container. If the connection is established successfully, the probe is successful. Otherwise, the container is restarted.
				  •   An *Exec* probe executes an arbitrary command inside the container and checks the command’s exit status code. If the status code is 0, the probe is successful. All other codes are considered failures.
			- ([View Highlight](https://read.readwise.io/read/01gpzrv0m85qzv5642rb5ybb4e))
		- -
		- -
			- Example of a liveness probe in Kubernetes #flashcard
			  id:: 17267409-881d-4035-85a9-b0ba84d11363
				- Adding a liveness probe to a pod: kubia-liveness-probe.yaml
				  
				  apiVersion: v1
				  kind: Pod
				  metadata:
				  name: kubia-liveness
				  spec:
				  containers:
			- tags:: [[code]]
			- ([View Highlight](https://read.readwise.io/read/01gpzrzatry7qewv8hc4tftdkj))
		- -
		- -
			- When you want to figure out why the previous container terminated, you’ll want to see those logs instead of the current container’s logs. This can be done by using the --previous option:
			  id:: 49d42e02-2182-4a10-bbce-5fc5d3e986f4
			  
			  $ kubectl logs mypod --previous #flashcard
			- ([View Highlight](https://read.readwise.io/read/01gpzs4n4chtpkghdjc7aa5d0m))
		- -
		- -
			- A liveness probe with an initial delay: kubia-liveness-probe-initial-delay.yaml
			  id:: 136facb6-3d7b-48d2-8b49-a59348307d99
			  
			   livenessProbe:
			     httpGet:
			       path: /
			       port: 8080
			     initialDelaySeconds: 15              ❶
			  
			  •   ❶ Kubernetes will wait 15 seconds before executing the first probe.
			  
			  If you don’t set the initial delay, the prober will start probing the container as soon as it starts, which usually leads to the probe failing, because the app isn’t ready to start receiving requests. If the number of failures exceeds the failure threshold, the container is restarted before it’s even able to start responding to requests properly. #flashcard
			- ([View Highlight](https://read.readwise.io/read/01gpzsc4pex5csg814jjp6j2nt))
		- -
		- -
			- The ReplicationController in the figure manages only a single pod, but Replication-Controllers, in general, are meant to create and manage multiple copies (replicas) of a pod. That’s where ReplicationControllers got their name from. #flashcard
			  id:: 5ad52fc2-7bb3-48a1-a88d-1bff5ff7eaa9
			- ([View Highlight](https://read.readwise.io/read/01gpztts6aqargx1cnrw5nk417))
		- -
		- -
			- Understanding the three parts of a ReplicationController
			  id:: 8d82461d-653e-4fca-9542-70470de9ac1e
			  
			  A ReplicationController has three essential parts (also shown in [figure 4.3](#ch04fig03)):
			  
			  •   A *label selector*, which determines what pods are in the ReplicationController’s scope
			  •   A *replica count*, which specifies the desired number of pods that should be running
			  •   A *pod template*, which is used when creating new pod replicas
			  
			  Figure 4.3. The three key parts of a ReplicationController (pod selector, replica count, and pod template)
			  
			  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added36-04fig03_N6TiNzd.jpg) #flashcard
			- ([View Highlight](https://read.readwise.io/read/01gpzv2kdvd2jb9rmbke4wsj6m))
		- -
		- -
			- Changes to the label selector and the pod template have no effect on existing pods. Changing the label selector makes the existing pods fall out of the scope of the Replication-Controller, so the controller stops caring about them. ReplicationControllers also don’t care about the actual “contents” of its pods (the container images, environment variables, and other things) after they create the pod. The template therefore only affects new pods created by this ReplicationController. You can think of it as a cookie cutter for cutting out new pods. #flashcard
			  id:: f09ddef3-ee1e-4c72-90be-b9e2d755b46b
			- ([View Highlight](https://read.readwise.io/read/01gpzv4aekaph09qwkwhg1yfzj))
		- -
		- -
			- Example of ReplicationController in Kubernetes #flashcard
			  id:: b7901a1d-a60d-4c56-bec3-a8788b36b912
				- A YAML definition of a ReplicationController: kubia-rc.yaml
				  
				  apiVersion: v1
				  kind: ReplicationController        ❶
				  metadata:
				  name: kubia                      ❷
				  spec:
				  replicas: 3                      ❸
				  selector:                        ❹
				    app: kubia                     ❹
				  template:                        ❺
				    metadata:                      ❺
				      labels:                      ❺
				        app: kubia                 ❺
				    spec:                          ❺
				      containers:                  ❺
			- tags:: [[code]]
			- ([View Highlight](https://read.readwise.io/read/01gpzv975cs3hwqq0p5dgdcvbd))
		- -
		- -
			- If a node fails in the non-Kubernetes world, the ops team would need to migrate the applications running on that node to other machines manually. Kubernetes, on the other hand, does that automatically. Soon after the ReplicationController detects that its pods are down, it will spin up new pods to replace them. #flashcard
			  id:: 0f2e7b5e-4e0a-46f5-8f40-6ecf642b9246
			- ([View Highlight](https://read.readwise.io/read/01gpzw0w03j1qemf7p0a2e0tva))
		- -
		- -
			- You’re using the -L app option to display the app label in a column. #flashcard
			  id:: 56657e0f-735d-4506-b3aa-3f5ca713bf6b
			- ([View Highlight](https://read.readwise.io/read/01gpzwmsjqjaf31j9sr4570c32))
		- -
		- -
			- You can edit the ReplicationController with the following command:
			  id:: a5a39a50-8202-4d60-8bb8-71e53bae4521
			  
			  **$ kubectl edit rc kubia**
			  
			  This will open the ReplicationController’s YAML definition in your default text editor. Find the pod template section and add an additional label to the metadata. After you save your changes and exit the editor, kubectl will update the ReplicationController and print the following message:
			  
			  replicationcontroller "kubia" edited #flashcard
			- ([View Highlight](https://read.readwise.io/read/01gpzww06pyt5ak0162jhw3szp))
		- -
		- -
			- When you delete a ReplicationController through kubectl delete, the pods are also deleted. But because pods created by a ReplicationController aren’t an integral part of the ReplicationController, and are only managed by it, you can delete only the ReplicationController and leave the pods running, as shown in [figure 4.7](#ch04fig07).
			  id:: e006d56a-132b-40b7-93de-e472d92457da
			  
			  Figure 4.7. Deleting a replication controller with --cascade=false leaves pods unmanaged.
			  
			  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added40-04fig07_alt_k1fWUme.jpg) #flashcard
			- ([View Highlight](https://read.readwise.io/read/01gpzx2g3snsr28d9r14bzrj99))
		- -
- New highlights added [[Wednesday, 01-02-2023]] at 10:04 AM
	- -
		- Mention the four valid operators for selecting pods in Kubernetes #flashcard
		  id:: 63dc0fdb-f579-4727-9a98-771b14b0d42f
			- You can add additional expressions to the selector. As in the example, each expression must contain a key, an operator, and possibly (depending on the operator) a list of values. You’ll see four valid operators:
			  
			  •   In—Label’s value must match one of the specified values.
			  •   NotIn—Label’s value must not match any of the specified values.
			  •   Exists—Pod must include a label with the specified key (the value isn’t important). When using this operator, you shouldn’t specify the values field.
			  •   DoesNotExist—Pod must not include a label with the specified key. The values property must not be specified.
		- ([View Highlight](https://read.readwise.io/read/01gqyz30fch1rg98v7bwng57cf))
	- -
	- -
		- Both ReplicationControllers and ReplicaSets are used for running a specific number of pods deployed anywhere in the Kubernetes cluster. But certain cases exist when you want a pod to run on each and every node in the cluster (and each node needs to run exactly one instance of the pod, as shown in [figure 4.8](https://readwise.io/reader/document_raw_content/26339439#ch04fig08)).
		  id:: 63dc0fdb-4dbc-4ab0-b189-b5baa2df4a4a
		  
		  Figure 4.8. DaemonSets run only a single pod replica on each node, whereas ReplicaSets scatter them around the whole cluster randomly.
		  
		  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added41-04fig08_alt_YyBfnOB.jpg)
		  
		  Those cases include infrastructure-related pods that perform system-level operations. For example, you’ll want to run a log collector and a resource monitor on every node. Another good example is Kubernetes’ own kube-proxy process, which needs to run on all nodes to make services work.
		  
		  Outside of Kubernetes, such processes would usually be started through system init scripts or the systemd daemon during node boot up. On Kubernetes nodes, you can still use systemd to run your system processes, but then you can’t take advantage of all the features Kubernetes provides. #flashcard
		- ([View Highlight](https://read.readwise.io/read/01gqyz9s5kymdhzfc8dhyfjc6f))
	- -
	- -
		- To run a pod on all cluster nodes, you create a DaemonSet object, which is much like a ReplicationController or a ReplicaSet, except that pods created by a DaemonSet already have a target node specified and skip the Kubernetes Scheduler. They aren’t scattered around the cluster randomly.
		  id:: 63dc0fdb-e390-4f94-a27c-1f5e9e44786b
		  
		  A DaemonSet makes sure it creates as many pods as there are nodes and deploys each one on its own node, as shown in [figure 4.8](https://readwise.io/reader/document_raw_content/26339439#ch04fig08). #flashcard
		- ([View Highlight](https://read.readwise.io/read/01gqyzapyykjphkzbh6ed7azf6))
	- -
	- -
		- Let’s imagine having a daemon called ssd-monitor that needs to run on all nodes that contain a solid-state drive (SSD). You’ll create a DaemonSet that runs this daemon on all nodes that are marked as having an SSD. The cluster administrators have added the disk=ssd label to all such nodes, so you’ll create the DaemonSet with a node selector that only selects nodes with that label, as shown in [figure 4.9](https://readwise.io/reader/document_raw_content/26339439#ch04fig09).
		  id:: 63dc0fdb-3473-40be-8c55-713ee4e0b32f
		  
		  Figure 4.9. Using a DaemonSet with a node selector to deploy system pods only on certain nodes
		  
		  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added42-04fig09_alt_DdNtgIC.jpg) #flashcard
		- ([View Highlight](https://read.readwise.io/read/01gqyzhpeqez7gxmkkzxh4ey8b))
	- -
	- -
		- Up to now, we’ve only talked about pods than need to run continuously. You’ll have cases where you only want to run a task that terminates after completing its work. ReplicationControllers, ReplicaSets, and DaemonSets run continuous tasks that are never considered completed. Processes in such pods are restarted when they exit. But in a completable task, after its process terminates, it should not be restarted again.
		  id:: 63dc0fdb-ac5e-4fad-a1ca-625bd873bd32
		  
		  4.5.1. Introducing the Job resource
		  
		  Kubernetes includes support for this through the Job resource, which is similar to the other resources we’ve discussed in this chapter, but it allows you to run a pod whose container isn’t restarted when the process running inside finishes successfully. Once it does, the pod is considered complete.
		  
		  In the event of a node failure, the pods on that node that are managed by a Job will be rescheduled to other nodes the way ReplicaSet pods are. In the event of a failure of the process itself (when the process returns an error exit code), the Job can be configured to either restart the container or not. #flashcard
		- ([View Highlight](https://read.readwise.io/read/01gqyzr572860k5thys5x0y12m))
	- -
	- -
		- A YAML definition of a Job: exporter.yaml
		  
		  apiVersion: batch/v1                  ❶
		  kind: Job                             ❶
		  metadata:
		  name: batch-job
		  spec:                                 ❷
		  template:
		    metadata:
		      labels:                         ❷
		        app: batch-job                ❷
		    spec:
		      restartPolicy: OnFailure        ❸
		      containers:
		- ([View Highlight](https://read.readwise.io/read/01gqz00rw8v67emfxk53ejby24))
	- -
	- -
		- Running job pods sequentially
		  id:: 63dc0fdb-bea7-4bc0-95b0-60f4aff005fd
		  
		  If you need a Job to run more than once, you set completions to how many times you want the Job’s pod to run. The following listing shows an example.
		  
		  Listing 4.12. A Job requiring multiple completions: multi-completion-batch-job.yaml
		  
		  apiVersion: batch/v1
		  kind: Job
		  metadata:
		  name: multi-completion-batch-job
		  spec:
		  completions: 5                                ❶
		  template:
		    <template is the same as in listing 4.11>
		  
		  •   ❶ **Setting completions to 5 makes this Job run five pods sequentially.** #flashcard
		- ([View Highlight](https://read.readwise.io/read/01gqz082rvy1wz8dxc571b38ef))
	- -
	- -
		- Running job pods in parallel
		  id:: 63dc0fdb-ff34-4c91-b9cf-9d4d3fbd00d9
		  
		  Instead of running single Job pods one after the other, you can also make the Job run multiple pods in parallel. You specify how many pods are allowed to run in parallel with the parallelism Job spec property, as shown in the following listing.
		  
		  Listing 4.13. Running Job pods in parallel: multi-completion-parallel-batch-job.yaml
		  
		  apiVersion: batch/v1
		  kind: Job
		  metadata:
		  name: multi-completion-batch-job
		  spec:
		  completions: 5                      ❶
		  parallelism: 2                      ❷
		  template:
		    <same as in listing 4.11>
		  
		  •   ❶ **This job must ensure five pods complete successfully.**
		  •   ❷ **Up to two pods can run in parallel.** #flashcard
		- ([View Highlight](https://read.readwise.io/read/01gqz08q1kmete2p7mkt2asv84))
	- -
	- -
		- It may happen that the Job or pod is created and run relatively late. You may have a hard requirement for the job to not be started too far over the scheduled time. In that case, you can specify a deadline by specifying the startingDeadlineSeconds field in the CronJob specification as shown in the following listing.
		  id:: 63dc0fdb-4eee-458b-be7d-92caf4ba1b64
		  
		  Listing 4.15. Specifying a startingDeadlineSeconds for a CronJob
		  
		  apiVersion: batch/v1beta1
		  kind: CronJob
		  spec:
		  schedule: "0,15,30,45 * * * *"
		  startingDeadlineSeconds: 15           ❶
		  ...
		  
		  •   ❶ At the latest, the pod must start running at 15 seconds past the scheduled time.
		  
		  In the example in [listing 4.15](https://readwise.io/reader/document_raw_content/26339439#ch04ex15), one of the times the job is supposed to run is 10:30:00. If it doesn’t start by 10:30:15 for whatever reason, the job will not run and will be shown as Failed. #flashcard
		- ([View Highlight](https://read.readwise.io/read/01gqz0j7amext8bqzzc6k5yky2))
	- -
	- Chapter 5. Services: enabling clients to discover and talk to pods
		- -
			- A Kubernetes Service is a resource you create to make a single, constant point of entry to a group of pods providing the same service. Each service has an IP address and port that never change while the service exists. Clients can open connections to that IP and port, and those connections are then routed to one of the pods backing that service. This way, clients of a service don’t need to know the location of individual pods providing the service, allowing those pods to be moved around the cluster at any time. #flashcard
			  id:: 63dc0fdb-c35c-4258-bb23-c67b04443277
			- ([View Highlight](https://read.readwise.io/read/01gqz1376pe44ypqbacm7ch2w7))
		- -
		- -
			- Both internal and external clients usually connect to pods through services.
			  id:: 63dc0fdb-62a5-4e6f-a47d-ae4db6f6824c
			  
			  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added44-05fig01_alt_XYLW9ph.jpg) #flashcard
			- ([View Highlight](https://read.readwise.io/read/01gqz17v184376xty7ky4742ky))
		- -
		- -
			- Creating a service through a YAML descriptor
			  
			  Create a file called kubia-svc.yaml with the following listing’s contents.
			  
			  Listing 5.1. A definition of a service: kubia-svc.yaml
			  
			  apiVersion: v1
			  kind: Service
			  metadata:
			  name: kubia
			  spec:
			  ports:
			- ([View Highlight](https://read.readwise.io/read/01gqz1d70ch8mw87zsq4atenxk))
		- -
		- -
			- Connecting to the service through its FQDN
			  id:: 63dc0fdb-65ed-4aa7-934a-1e39be32a4c5
			  
			  To revisit the frontend-backend example, a frontend pod can connect to the backend-database service by opening a connection to the following FQDN:
			  
			  backend-database.default.svc.cluster.local
			  
			  backend-database corresponds to the service name, default stands for the namespace the service is defined in, and svc.cluster.local is a configurable cluster domain suffix used in all cluster local service names. #flashcard
			- ([View Highlight](https://read.readwise.io/read/01gr13w7bh1e2srq9sfhefg5q5))
		- -
		- -
			- You can use the curl command to access the kubia service in any of the following ways:
			  id:: 63dc0fdb-f739-44e9-a0be-00100b9e4fd7
			  
			  **root@kubia-3inly:/# curl http://kubia.default.svc.cluster.local**
			  You've hit kubia-5asi2
			  
			  **root@kubia-3inly:/# curl http://kubia.default**
			  You've hit kubia-3inly
			  
			  **root@kubia-3inly:/# curl http://kubia**
			  You've hit kubia-8awf3 #flashcard
			- ([View Highlight](https://read.readwise.io/read/01gr141sssk89790k7rgf9gmxq))
		- -
		- -
			- Pods consuming a service with two external endpoints.
			  id:: 63dc0fdb-63d7-4d68-8f88-f45cf9a6d99b
			  
			  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added47-05fig04_alt_lLFW7t0.jpg) #flashcard
			- ([View Highlight](https://read.readwise.io/read/01gr14stqc9jx13sv3b47z7evr))
		- -
		- -
			- Creating an ExternalName service
			  
			  To create a service that serves as an alias for an external service, you create a Service resource with the type field set to ExternalName. For example, let’s imagine there’s a public API available at [api.somecompany.com](http://api.somecompany.com). You can define a service that points to it as shown in the following listing.
			  
			  Listing 5.10. An ExternalName-type service: external-service-externalname.yaml
			  
			  apiVersion: v1
			  kind: Service
			  metadata:
			  name: external-service
			  spec:
			  type: ExternalName                         ❶
			  externalName: someapi.somecompany.com      ❷
			  ports:
			- ([View Highlight](https://read.readwise.io/read/01gr1503yf7j8mnm13xphmrwej))
		- -
		- -
			- Exposing a service to external clients
			  id:: 63dc0fdb-f1f3-4e88-8da6-95485b6e5727
			  
			  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added48-05fig05_alt_xJOpVxg.jpg)
			  
			  You have a few ways to make a service accessible externally:
			  
			  •   *Setting the service type to* *NodePort*—For a NodePort service, each cluster node opens a port on the node itself (hence the name) and redirects traffic received on that port to the underlying service. The service isn’t accessible only at the internal cluster IP and port, but also through a dedicated port on all nodes.
			  •   *Setting the service type to* *LoadBalancer*, *an extension of the* *NodePort* *type*—This makes the service accessible through a dedicated load balancer, provisioned from the cloud infrastructure Kubernetes is running on. The load balancer redirects traffic to the node port across all the nodes. Clients connect to the service through the load balancer’s IP.
			  •   *Creating an Ingress resource, a radically different mechanism for exposing multiple services through a single IP address*—It operates at the HTTP level (network layer 7) and can thus offer more features than layer 4 services can. #flashcard
			- ([View Highlight](https://read.readwise.io/read/01gr1547mnpzp0732v7q2vrncq))
		- -
		- -
			- Creating a NodePort service
			  
			  You’ll now create a NodePort service to see how you can use it. The following listing shows the YAML for the service.
			  
			  Listing 5.11. A NodePort service definition: kubia-svc-nodeport.yaml
			  
			  apiVersion: v1
			  kind: Service
			  metadata:
			  name: kubia-nodeport
			  spec:
			  type: NodePort             ❶
			  ports:
			- ([View Highlight](https://read.readwise.io/read/01gr1579hkn5nkt1nehp95y0hj))
		- -
		- -
			- Creating a LoadBalancer service
			  
			  To create a service with a load balancer in front, create the service from the following YAML manifest, as shown in the following listing.
			  
			  Listing 5.12. A LoadBalancer-type service: kubia-svc-loadbalancer.yaml
			  
			  apiVersion: v1
			  kind: Service
			  metadata:
			  name: kubia-loadbalancer
			  spec:
			  type: LoadBalancer                ❶
			  ports:
			- ([View Highlight](https://read.readwise.io/read/01gr15mb6fwf1eyr5vnf0wkndf))
		- -
		- -
			- See [figure 5.7](https://readwise.io/reader/document_raw_content/26339439#ch05fig07) to see how HTTP requests are delivered to the pod. External clients (curl in your case) connect to port 80 of the load balancer and get routed to the implicitly assigned node port on one of the nodes. From there, the connection is forwarded to one of the pod instances.
			  id:: 63dc0fdb-ade4-406d-9890-096fd16b606f
			  
			  Figure 5.7. An external client connecting to a LoadBalancer service
			  
			  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added50-05fig07_alt_6c0nkJ4.jpg) #flashcard
			- ([View Highlight](https://read.readwise.io/read/01gr15r8er36w79qrh8qx38b86))
		- -
		- -
			- Understanding why Ingresses are needed
			  id:: 63dc0fdb-9908-4d05-bcc1-fcfcdfa35e07
			  
			  One important reason is that each LoadBalancer service requires its own load balancer with its own public IP address, whereas an Ingress only requires one, even when providing access to dozens of services. When a client sends an HTTP request to the Ingress, the host and path in the request determine which service the request is forwarded to, as shown in [figure 5.9](https://readwise.io/reader/document_raw_content/26339439#ch05fig09).
			  
			  Figure 5.9. Multiple services can be exposed through a single Ingress.
			  
			  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added52-05fig09_alt_8dyTLSx.jpg) #flashcard
			- ([View Highlight](https://read.readwise.io/read/01gr16541d7rwr9py3ak5as2q9))
		- -
		- -
			- You’ve confirmed there’s an Ingress controller running in your cluster, so you can now create an Ingress resource. The following listing shows what the YAML manifest for the Ingress looks like.
			  
			  Listing 5.13. An Ingress resource definition: kubia-ingress.yaml
			  
			  apiVersion: extensions/v1beta1
			  kind: Ingress
			  metadata:
			  name: kubia
			  spec:
			  rules:
			- ([View Highlight](https://read.readwise.io/read/01gr16hqkg32y7d7e0f3y3kpqg))
		- -
		- -
			- Understanding how Ingresses work
			  id:: 63dc0fdb-9a6d-4687-9860-7590da25607d
			  
			  [Figure 5.10](https://readwise.io/reader/document_raw_content/26339439#ch05fig10) shows how the client connected to one of the pods through the Ingress controller. The client first performed a DNS lookup of kubia.example.com, and the DNS server (or the local operating system) returned the IP of the Ingress controller. The client then sent an HTTP request to the Ingress controller and specified kubia.example.com in the Host header. From that header, the controller determined which service the client is trying to access, looked up the pod IPs through the Endpoints object associated with the service, and forwarded the client’s request to one of the pods.
			  
			  Figure 5.10. Accessing pods through an Ingress
			  
			  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added53-05fig10_alt_RNKLZ5I.jpg)
			  
			  As you can see, the Ingress controller didn’t forward the request to the service. It only used it to select a pod. Most, if not all, controllers work like this. #flashcard
			- ([View Highlight](https://read.readwise.io/read/01gr16thbqf9566x7p2haqafbk))
		- -
		- -
			- Mapping different services to different paths of the same host
			  
			  You can map multiple paths on the same host to different services, as shown in the following listing.
			  
			  Listing 5.14. Ingress exposing multiple services on same host, but different paths
			  
			  ...
			- ([View Highlight](https://read.readwise.io/read/01gr1715jbhvnpqnr2qyfb8c8c))
		- -
		- -
			- The readiness probe is invoked periodically and determines whether the specific pod should receive client requests or not. When a container’s readiness probe returns success, it’s signaling that the container is ready to accept requests.
			  id:: 63dc0fdb-66cb-4086-8f50-1dcff369a7b4
			  
			  This notion of being ready is obviously something that’s specific to each container. Kubernetes can merely check if the app running in the container responds to a simple GET / request or it can hit a specific URL path, which causes the app to perform a whole list of checks to determine if it’s ready. Such a detailed readiness probe, which takes the app’s specifics into account, is the app developer’s responsibility.
			  
			  Types of readiness probes
			  
			  Like liveness probes, three types of readiness probes exist:
			  
			  •   An *Exec* probe, where a process is executed. The container’s status is determined by the process’ exit status code.
			  •   An *HTTP GET* probe, which sends an HTTP GET request to the container and the HTTP status code of the response determines whether the container is ready or not.
			  •   A *TCP Socket* probe, which opens a TCP connection to a specified port of the container. If the connection is established, the container is considered ready.
			  
			  Understanding the operation of readiness probes
			  
			  When a container is started, Kubernetes can be configured to wait for a configurable amount of time to pass before performing the first readiness check. After that, it invokes the probe periodically and acts based on the result of the readiness probe. If a pod reports that it’s not ready, it’s removed from the service. If the pod then becomes ready again, it’s re-added.
			  
			  Unlike liveness probes, if a container fails the readiness check, it won’t be killed or restarted. This is an important distinction between liveness and readiness probes. Liveness probes keep pods healthy by killing off unhealthy containers and replacing them with new, healthy ones, whereas readiness probes make sure that only pods that are ready to serve requests receive them. This is mostly necessary during container start up, but it’s also useful after the container has been running for a while.
			  
			  As you can see in [figure 5.11](https://readwise.io/reader/document_raw_content/26339439#ch05fig11), if a pod’s readiness probe fails, the pod is removed from the Endpoints object. Clients connecting to the service will not be redirected to the pod. The effect is the same as when the pod doesn’t match the service’s label selector at all.
			  
			  Figure 5.11. A pod whose readiness probe fails is removed as an endpoint of a service.
			  
			  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added54-05fig11_alt_4BaTm00.jpg) #flashcard
			- ([View Highlight](https://read.readwise.io/read/01gr17fwfxxta026p80dgrnpdg))
		- -
		- -
			- Tip
			  id:: 63dc0fdb-7b28-4e25-bc44-08afa8524c94
			  
			  If you want to add or remove a pod from a service manually, add enabled=true as a label to your pod and to the label selector of your service. Remove the label when you want to remove the pod from the service. #flashcard
			- ([View Highlight](https://read.readwise.io/read/01gr17sva7zpwmmhrftfgr7ztr))
		- -
		- -
			- Always define a readiness probe
			  id:: 63dc0fdb-bdf6-498f-8e9c-961145fd170c
			  
			  Before we conclude this section, there are two final notes about readiness probes that I need to emphasize. First, if you don’t add a readiness probe to your pods, they’ll become service endpoints almost immediately. If your application takes too long to start listening for incoming connections, client requests hitting the service will be forwarded to the pod while it’s still starting up and not ready to accept incoming connections. Clients will therefore see “Connection refused” types of errors.
			  
			  * * *
			  
			  Tip
			  
			  You should always define a readiness probe, even if it’s as simple as sending an HTTP request to the base URL. #flashcard
			- ([View Highlight](https://read.readwise.io/read/01gr17vqp7bbrmyca8s6zpbwnj))
		- -
		- -
			- Let’s use the newly created pod to perform a DNS lookup:
			  id:: 63dc0fdb-009c-4233-bea5-1ee5be9a149d
			  
			  **$ kubectl exec dnsutils nslookup kubia-headless**
			  ...
			  Name:    kubia-headless.default.svc.cluster.local
			  Address: 10.108.1.4
			  Name:    kubia-headless.default.svc.cluster.local
			  Address: 10.108.2.5
			  
			  The DNS server returns two different IPs for the kubia-headless.default.svc.cluster.local FQDN. Those are the IPs of the two pods that are reporting being ready. You can confirm this by listing pods with kubectl get pods -o wide, which shows the pods’ IPs.
			  
			  This is different from what DNS returns for regular (non-headless) services, such as for your kubia service, where the returned IP is the service’s cluster IP:
			  
			  **$ kubectl exec dnsutils nslookup kubia**
			  ...
			  Name:    kubia.default.svc.cluster.local
			  Address: 10.111.249.153
			  
			  Although headless services may seem different from regular services, they aren’t that different from the clients’ perspective. Even with a headless service, clients can connect to its pods by connecting to the service’s DNS name, as they can with regular services. But with headless services, because DNS returns the pods’ IPs, clients connect directly to the pods, instead of through the service proxy. #flashcard
			- ([View Highlight](https://read.readwise.io/read/01gr18e8fcp0qha27ehqf1q2wt))
		- -
		- Chapter 6. Volumes: attaching disk storage to containers
			- -
				- Kubernetes provides this by defining storage *volumes*. They aren’t top-level resources like pods, but are instead defined as a part of a pod and share the same lifecycle as the pod. This means a volume is created when the pod is started and is destroyed when the pod is deleted. Because of this, a volume’s contents will persist across container restarts. After a container is restarted, the new container can see all the files that were written to the volume by the previous container. Also, if a pod contains multiple containers, the volume can be used by all of them at once. #flashcard
				  id:: 63dc0fdb-cbe9-4ece-acbc-66f21fc66ef5
				- ([View Highlight](https://read.readwise.io/read/01gr1pz02fqdyryg3fcppfnf57))
			- -
			- -
				- Linux allows you to mount a filesystem at arbitrary locations in the file tree. When you do that, the contents of the mounted filesystem are accessible in the directory it’s mounted into. By mounting the same volume into two containers, they can operate on the same files. In your case, you’re mounting two volumes in three containers. By doing this, your three containers can work together and do something useful. Let me explain how.
				  id:: 63dc0fdb-18a8-4478-b1a4-64590a920479
				  
				  Figure 6.2. Three containers sharing two volumes mounted at various mount paths
				  
				  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added56-06fig02_S38UUd5.jpg)
				  
				  First, the pod has a volume called publicHtml. This volume is mounted in the WebServer container at /var/htdocs, because that’s the directory the web server serves files from. The same volume is also mounted in the ContentAgent container, but at /var/html, because that’s where the agent writes the files to. By mounting this single volume like that, the web server will now serve the content generated by the content agent. #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr1qa9vrwrx69s205zsmf5wc))
			- -
			- -
				- A pod with two containers sharing the same volume: fortune-pod.yaml
				  
				  apiVersion: v1
				  kind: Pod
				  metadata:
				  name: fortune
				  spec:
				  containers:
				- ([View Highlight](https://read.readwise.io/read/01gr1r8fnj1a4rp9b3h7ksmc1b))
			- -
			- -
				- A pod using a gitRepo volume: gitrepo-volume-pod.yaml
				  
				  apiVersion: v1
				  kind: Pod
				  metadata:
				  name: gitrepo-volume-pod
				  spec:
				  containers:
				- ([View Highlight](https://read.readwise.io/read/01gr1rvkbf79wz51d7bszce0eg))
			- -
			- -
				- A hostPath volume points to a specific file or directory on the node’s filesystem (see [figure 6.4](https://readwise.io/reader/document_raw_content/26339439#ch06fig04)). Pods running on the same node and using the same path in their hostPath volume see the same files.
				  id:: 63dc0fdb-f515-461b-a228-0c82532642f9
				  
				  Figure 6.4. A hostPath volume mounts a file or directory on the worker node into the container’s filesystem.
				  
				  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added58-06fig04_alt_gDdEBb8.jpg)
				  
				  hostPath volumes are the first type of persistent storage we’re introducing, because both the gitRepo and emptyDir volumes’ contents get deleted when a pod is torn down, whereas a hostPath volume’s contents don’t. If a pod is deleted and the next pod uses a hostPath volume pointing to the same path on the host, the new pod will see whatever was left behind by the previous pod, but only if it’s scheduled to the same node as the first pod.
				  
				  If you’re thinking of using a hostPath volume as the place to store a database’s data directory, think again. Because the volume’s contents are stored on a specific node’s filesystem, when the database pod gets rescheduled to another node, it will no longer see the data. This explains why it’s not a good idea to use a hostPath volume for regular pods, because it makes the pod sensitive to what node it’s scheduled to. #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr1sdbkdjvgsjqy6krchc2em))
			- -
			- -
				- The reason you created the GCE Persistent Disk volume is because your Kubernetes cluster runs on Google Kubernetes Engine. When you run your cluster elsewhere, you should use other types of volumes, depending on the underlying infrastructure.
				  
				  If your Kubernetes cluster is running on Amazon’s AWS EC2, for example, you can use an awsElasticBlockStore volume to provide persistent storage for your pods. If your cluster runs on Microsoft Azure, you can use the azureFile or the azureDisk volume. We won’t go into detail on how to do that here, but it’s virtually the same as in the previous example. First, you need to create the actual underlying storage, and then set the appropriate properties in the volume definition.
				  
				  Using an AWS Elastic Block Store volume
				  
				  For example, to use an AWS elastic block store instead of the GCE Persistent Disk, you’d only need to change the volume definition as shown in the following listing (see those lines printed in bold).
				  
				  Listing 6.7. A pod using an awsElasticBlockStore volume: mongodb-pod-aws.yaml
				  
				  apiVersion: v1
				  kind: Pod
				  metadata:
				  name: mongodb
				  spec:
				  volumes:
				- ([View Highlight](https://read.readwise.io/read/01gr1t8ecknva7xg6j79wxmm0b))
			- -
			- -
				- To enable apps to request storage in a Kubernetes cluster without having to deal with infrastructure specifics, two new resources were introduced. They are Persistent-Volumes and PersistentVolumeClaims. The names may be a bit misleading, because as you’ve seen in the previous few sections, even regular Kubernetes volumes can be used to store persistent data.
				  id:: 63dc0fdb-ce0a-4286-87b5-d6204f90159f
				  
				  Using a PersistentVolume inside a pod is a little more complex than using a regular pod volume, so let’s illustrate how pods, PersistentVolumeClaims, PersistentVolumes, and the actual underlying storage relate to each other in [figure 6.6](https://readwise.io/reader/document_raw_content/26339439#ch06fig06).
				  
				  Figure 6.6. PersistentVolumes are provisioned by cluster admins and consumed by pods through PersistentVolumeClaims.
				  
				  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added60-06fig06_alt_J9F1TQI.jpg)
				  
				  Instead of the developer adding a technology-specific volume to their pod, it’s the cluster administrator who sets up the underlying storage and then registers it in Kubernetes by creating a PersistentVolume resource through the Kubernetes API server. When creating the PersistentVolume, the admin specifies its size and the access modes it supports.
				  
				  When a cluster user needs to use persistent storage in one of their pods, they first create a PersistentVolumeClaim manifest, specifying the minimum size and the access mode they require. The user then submits the PersistentVolumeClaim manifest to the Kubernetes API server, and Kubernetes finds the appropriate PersistentVolume and binds the volume to the claim.
				  
				  The PersistentVolumeClaim can then be used as one of the volumes inside a pod. Other users cannot use the same PersistentVolume until it has been released by deleting the bound PersistentVolumeClaim #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr1tr6cbnkd583jn27z5a2cr))
			- -
			- -
				- A gcePersistentDisk PersistentVolume: mongodb-pv-gcepd.yaml
				  
				  apiVersion: v1
				  kind: PersistentVolume
				  metadata:
				  name: mongodb-pv
				  spec:
				  capacity:                                 ❶
				    storage: 1Gi                            ❶
				  accessModes:                              ❷
				- ([View Highlight](https://read.readwise.io/read/01gr1twt8cmrr2qp51d2fad6n3))
			- -
			- -
				- A PersistentVolumeClaim: mongodb-pvc.yaml
				  
				  apiVersion: v1
				  kind: PersistentVolumeClaim
				  metadata:
				  name: mongodb-pvc              ❶
				  spec:
				  resources:
				    requests:                    ❷
				      storage: 1Gi               ❷
				  accessModes:                   ❸
				- ([View Highlight](https://read.readwise.io/read/01gr1v8jhzq8et5vgf8wheq67m))
			- -
			- -
				- Note the abbreviations used for the access modes:
				  id:: 63dc0fdb-d536-48fc-83f7-0d5ad66c9aca
				  
				  •   RWO—ReadWriteOnce—Only a single node can mount the volume for reading and writing.
				  •   ROX—ReadOnlyMany—Multiple nodes can mount the volume for reading.
				  •   RWX—ReadWriteMany—Multiple nodes can mount the volume for both reading and writing.
				  
				  * * *
				  
				  Note
				  
				  RWO, ROX, and RWX pertain to the number of worker nodes that can use the volume at the same time, not to the number of pods! #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr1va6vnsbcxs5y2q3wjbvhm))
			- -
			- -
				- Using a PersistentVolumeClaim in a pod
				  
				  The PersistentVolume is now yours to use. Nobody else can claim the same volume until you release it. To use it inside a pod, you need to reference the PersistentVolumeClaim by name inside the pod’s volume (yes, the PersistentVolumeClaim, not the PersistentVolume directly!), as shown in the following listing.
				  
				  Listing 6.12. A pod using a PersistentVolumeClaim volume: mongodb-pod-pvc.yaml
				  
				  apiVersion: v1
				  kind: Pod
				  metadata:
				  name: mongodb
				  spec:
				  containers:
				- ([View Highlight](https://read.readwise.io/read/01gr1vhbgkcsant7d87aqmwtxt))
			- -
			- -
				- Using the GCE Persistent Disk directly or through a PVC and PV
				  id:: 63dc0fdb-09ee-44ef-9bda-8f5805cfb3aa
				  
				  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added62-06fig08_alt_wmZQAw9.jpg)
				  
				  Consider how using this indirect method of obtaining storage from the infrastructure is much simpler for the application developer (or cluster user). Yes, it does require the additional steps of creating the PersistentVolume and the Persistent-VolumeClaim, but the developer doesn’t have to know anything about the actual storage technology used underneath. #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr1vmvzb2sm7wsh2jz9jy2k3))
			- -
			- -
				- You’ve seen how using PersistentVolumes and PersistentVolumeClaims makes it easy to obtain persistent storage without the developer having to deal with the actual storage technology used underneath. But this still requires a cluster administrator to provision the actual storage up front. Luckily, Kubernetes can also perform this job automatically through dynamic provisioning of PersistentVolumes.
				  id:: 63dc0fdb-28bd-4e41-ad60-8352a45d50de
				  
				  The cluster admin, instead of creating PersistentVolumes, can deploy a PersistentVolume provisioner and define one or more StorageClass objects to let users choose what type of PersistentVolume they want. The users can refer to the StorageClass in their PersistentVolumeClaims and the provisioner will take that into account when provisioning the persistent storage.
				  
				  * * *
				  
				  Note
				  
				  Similar to PersistentVolumes, StorageClass resources aren’t namespaced.
				  
				  * * *
				  
				  Kubernetes includes provisioners for the most popular cloud providers, so the administrator doesn’t always need to deploy a provisioner. But if Kubernetes is deployed on-premises, a custom provisioner needs to be deployed.
				  
				  Instead of the administrator pre-provisioning a bunch of PersistentVolumes, they need to define one or two (or more) StorageClasses and let the system create a new PersistentVolume each time one is requested through a PersistentVolumeClaim. The great thing about this is that it’s impossible to run out of PersistentVolumes (obviously, you can run out of storage space).
				  
				  6.6.1. Defining the available storage types through StorageClass resources
				  
				  Before a user can create a PersistentVolumeClaim, which will result in a new Persistent-Volume being provisioned, an admin needs to create one or more StorageClass resources. Let’s look at an example of one in the following listing.
				  
				  Listing 6.14. A StorageClass definition: storageclass-fast-gcepd.yaml
				  
				  apiVersion: storage.k8s.io/v1
				  kind: StorageClass
				  metadata:
				  name: fast
				  provisioner: kubernetes.io/gce-pd        ❶
				  parameters:
				  type: pd-ssd                           ❷
				  zone: europe-west1-b                   ❷
				  
				  •   ❶ The volume plugin to use for provisioning the PersistentVolume
				  •   ❷ **The parameters passed to the provisioner** #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr1wanxbg8e8hrh216fpg40e))
			- -
			- -
				- To summarize, the best way to attach persistent storage to a pod is to only create the PVC (with an explicitly specified storageClassName if necessary) and the pod (which refers to the PVC by name). Everything else is taken care of by the dynamic PersistentVolume provisioner.
				  id:: 63dc0fdb-6404-4419-aea8-b28f6815e439
				  
				  To get a complete picture of the steps involved in getting a dynamically provisioned PersistentVolume, examine [figure 6.10](https://readwise.io/reader/document_raw_content/26339439#ch06fig10).
				  
				  Figure 6.10. The complete picture of dynamic provisioning of PersistentVolumes
				  
				  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added64-06fig10_alt_lbJce8p.jpg) #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr1x0wn3dj010fa188thstxp))
			- -
		- Chapter 7. ConfigMaps and Secrets: configuring applications
			- -
				- In a Dockerfile, two instructions define the two parts:
				  id:: 63dc0fdb-edf4-4ba5-877f-bf3800152e37
				  
				  •   ENTRYPOINT defines the executable invoked when the container is started.
				  •   CMD specifies the arguments that get passed to the ENTRYPOINT.
				  
				  Although you can use the CMD instruction to specify the command you want to execute when the image is run, the correct way is to do it through the ENTRYPOINT instruction and to only specify the CMD if you want to define the default arguments. The image can then be run without specifying any arguments
				  
				  **$ docker run <image>**
				  
				  or with additional arguments, which override whatever’s set under CMD in the Dockerfile:
				  
				  **$ docker run <image> <arguments>** #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr3gd78rhntvg9g23tq652jf))
			- -
			- -
				- Specifying the executable and its arguments in Docker vs Kubernetes
				  id:: 63dc0fdb-e904-4046-8f34-68bb31142c70
				  
				  
				  
				  Docker
				  
				  Kubernetes
				  
				  Description
				  
				  ENTRYPOINT
				  
				  command
				  
				  The executable that’s executed inside the container
				  
				  CMD
				  
				  args
				  
				  The arguments passed to the executable #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr3gmrgt6pe2fzqbvb5bs9pd))
			- -
			- -
				- Defining an environment variable in a pod: fortune-pod-env.yaml
				  
				  kind: Pod
				  spec:
				   containers:
				- ([View Highlight](https://read.readwise.io/read/01gr3gytx2vqx0btv0fhbet635))
			- -
			- -
				- Pods use ConfigMaps through environment variables and configMap volumes.
				  id:: 63dc0fdb-beba-4c91-a97e-484ef76bf636
				  
				  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added66-07fig02_OehCTBm.jpg) #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr3h94m57a501te75a3d165t))
			- -
			- -
				- You can define the map’s entries by passing literals to the kubectl command or you can create the ConfigMap from files stored on your disk. Use a simple literal first:
				  id:: 63dc0fdb-90a3-4583-bb88-6a41165129e8
				  
				  **$ kubectl create configmap fortune-config --from-literal=sleep-interval=25**
				  configmap "fortune-config" created #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr3hgs3b1z1zczk33ykzk3tt))
			- -
			- -
				- Pod with env var from a config map: fortune-pod-env-configmap.yaml
				  
				  apiVersion: v1
				  kind: Pod
				  metadata:
				  name: fortune-env-from-configmap
				  spec:
				  containers:
				- ([View Highlight](https://read.readwise.io/read/01gr3ja28s92frkhz2xfh4cnwp))
			- -
			- -
				- Imagine having a ConfigMap with three keys called FOO, BAR, and FOO-BAR. You can expose them all as environment variables by using the envFrom attribute, instead of env the way you did in previous examples. The following listing shows an example.
				  
				  Listing 7.10. Pod with env vars from all entries of a ConfigMap
				  
				  spec:
				  containers:
				- ([View Highlight](https://read.readwise.io/read/01gr3jefb13qg0ycqjntb95krk))
			- -
			- -
				- A pod with ConfigMap entries mounted as files: fortune-pod-configmap-volume.yaml
				  
				  apiVersion: v1
				  kind: Pod
				  metadata:
				  name: fortune-configmap-volume
				  spec:
				  containers:
				- ([View Highlight](https://read.readwise.io/read/01gr3jyra3nwdr8ch1tn8th5cj))
			- -
			- -
				- Luckily, you can populate a configMap volume with only part of the ConfigMap’s entries—in your case, only the my-nginx-config.conf entry. This won’t affect the fortuneloop container, because you’re passing the sleep-interval entry to it through an environment variable and not through the volume.
				  
				  To define which entries should be exposed as files in a configMap volume, use the volume’s items attribute as shown in the following listing.
				  
				  Listing 7.16. A pod with a specific ConfigMap entry mounted into a file directory: fortune-pod-configmap-volume-with-items.yaml
				  
				  volumes:
				- ([View Highlight](https://read.readwise.io/read/01gr3k2xvstbeet2xbwx8ehp2s))
			- -
			- -
				- We’ve said that one of the drawbacks of using environment variables or command-line arguments as a configuration source is the inability to update them while the process is running. Using a ConfigMap and exposing it through a volume brings the ability to update the configuration without having to recreate the pod or even restart the container.
				  id:: 63dc0fdb-f406-4054-96b9-fca3dca65b20
				  
				  When you update a ConfigMap, the files in all the volumes referencing it are updated. It’s then up to the process to detect that they’ve been changed and reload them. But Kubernetes will most likely eventually also support sending a signal to the container after updating the files. #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr3mx6v3zk2zj4twh9zap6xf))
			- -
			- -
				- YAML definition of the fortune-https pod: fortune-pod-https.yaml
				  
				  apiVersion: v1
				  kind: Pod
				  metadata:
				  name: fortune-https
				  spec:
				  containers:
				- ([View Highlight](https://read.readwise.io/read/01gr3nxa4gv97kcw2kp9kg9s2t))
			- -
			- -
				- Creating a Secret for authenticating with a Docker registry
				  
				  Creating a Secret holding the credentials for authenticating with a Docker registry isn’t that different from creating the generic Secret you created in [section 7.5.3](https://readwise.io/reader/document_raw_content/26339439#ch07lev2sec16). You use the same kubectl create secret command, but with a different type and options:
				  
				  **$ kubectl create secret docker-registry mydockerhubsecret \**
				  **--docker-username=myusername --docker-password=mypassword \**
				  **--docker-email=my.email@provider.com**
				  
				  Rather than create a generic secret, you’re creating a docker-registry Secret called mydockerhubsecret. You’re specifying your Docker Hub username, password, and email. If you inspect the contents of the newly created Secret with kubectl describe, you’ll see that it includes a single entry called .dockercfg. This is equivalent to the .dockercfg file in your home directory, which is created by Docker when you run the docker login command.
				  
				  Using the docker-registry Secret in a pod definition
				  
				  To have Kubernetes use the Secret when pulling images from your private Docker Hub repository, all you need to do is specify the Secret’s name in the pod spec, as shown in the following listing.
				  
				  Listing 7.28. A pod definition using an image pull Secret: pod-with-private-image.yaml
				  
				  apiVersion: v1
				  kind: Pod
				  metadata:
				  name: private-pod
				  spec:
				  imagePullSecrets:                 ❶
				- ([View Highlight](https://read.readwise.io/read/01gr3p97ctgn20fexxrhgvw8hv))
			- -
		- Chapter 8. Accessing pod metadata and other resources from applications
			- -
				- the Kubernetes Downward API. It allows you to pass metadata about the pod and its environment through environment variables or files (in a downwardAPI volume). Don’t be confused by the name. The Downward API isn’t like a REST endpoint that your app needs to hit so it can get the data. It’s a way of having environment variables or files populated with values from the pod’s specification or status, as shown in [figure 8.1](https://readwise.io/reader/document_raw_content/26339439#ch08fig01).
				  id:: 63dc0fdb-297e-41c2-a538-d672f19ef8fd
				  
				  Figure 8.1. The Downward API exposes pod metadata through environment variables or files.
				  
				  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added77-08fig01_alt_IVRd6GK.jpg)
				  
				  8.1.1. Understanding the available metadata
				  
				  The Downward API enables you to expose the pod’s own metadata to the processes running inside that pod. Currently, it allows you to pass the following information to your containers:
				  
				  •   The pod’s name
				  •   The pod’s IP address
				  •   The namespace the pod belongs to
				  •   The name of the node the pod is running on
				  •   The name of the service account the pod is running under
				  •   The CPU and memory requests for each container
				  •   The CPU and memory limits for each container
				  •   The pod’s labels
				  •   The pod’s annotations #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr3sc6x3bm243mk4fc9nh5nb))
			- -
			- -
				- Pod with a downwardAPI volume: downward-api-volume.yaml
				  
				  apiVersion: v1
				  kind: Pod
				  metadata:
				  name: downward
				  labels:                                     ❶
				    foo: bar                                  ❶
				  annotations:                                ❶
				    key1: value1                              ❶
				    key2: |                                   ❶
				      multi                                   ❶
				      line                                    ❶
				      value                                   ❶
				  spec:
				  containers:
				- ([View Highlight](https://read.readwise.io/read/01gr3ssrq1vgw4qkqdg0zdg8et))
			- -
		- Chapter 9. Deployments: updating applications declaratively
			- -
				- Deleting old pods and replacing them with new ones
				  id:: 63dc0fdb-10f7-4621-a40d-274287f020dd
				  
				  You already know how to get a ReplicationController to replace all its pod instances with pods running a new version. You probably remember the pod template of a ReplicationController can be updated at any time. When the ReplicationController creates new instances, it uses the updated pod template to create them.
				  
				  If you have a ReplicationController managing a set of v1 pods, you can easily replace them by modifying the pod template so it refers to version v2 of the image and then deleting the old pod instances. The ReplicationController will notice that no pods match its label selector and it will spin up new instances. The whole process is shown in [figure 9.2](https://readwise.io/reader/document_raw_content/26339439#ch09fig02).
				  
				  Figure 9.2. Updating pods by changing a ReplicationController’s pod template and deleting old Pods
				  
				  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added85-09fig02_alt_atmHVbl.jpg)
				  
				  This is the simplest way to update a set of pods, if you can accept the short downtime between the time the old pods are deleted and new ones are started. #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr3w1paw7gqhwjdpj5vc69tj))
			- -
			- -
				- If you don’t want to see any downtime and your app supports running multiple versions at once, you can turn the process around and first spin up all the new pods and only then delete the old ones. This will require more hardware resources, because you’ll have double the number of pods running at the same time for a short while.
				  id:: 63dc0fdb-f9e7-47a0-a32b-5da05443d23b
				  
				  This is a slightly more complex method compared to the previous one, but you should be able to do it by combining what you’ve learned about ReplicationControllers and Services so far.
				  
				  Switching from the old to the new version at once
				  
				  Pods are usually fronted by a Service. It’s possible to have the Service front only the initial version of the pods while you bring up the pods running the new version. Then, once all the new pods are up, you can change the Service’s label selector and have the Service switch over to the new pods, as shown in [figure 9.3](https://readwise.io/reader/document_raw_content/26339439#ch09fig03). This is called a *blue-green deployment*. After switching over, and once you’re sure the new version functions correctly, you’re free to delete the old pods by deleting the old ReplicationController.
				  
				  * * *
				  
				  Note
				  
				  You can change a Service’s pod selector with the kubectl set selector command.
				  
				  * * *
				  
				  Figure 9.3. Switching a Service from the old pods to the new ones
				  
				  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added86-09fig03_alt_yTCbKZe.jpg) #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr3w5zqz0srmt8qe2wn74n7m))
			- -
			- -
				- Performing a rolling update
				  id:: 63dc0fdb-f04c-4cc8-b067-e6ab00573cc4
				  
				  Instead of bringing up all the new pods and deleting the old pods at once, you can also perform a rolling update, which replaces pods step by step. You do this by slowly scaling down the previous ReplicationController and scaling up the new one. In this case, you’ll want the Service’s pod selector to include both the old and the new pods, so it directs requests toward both sets of pods. See [figure 9.4](https://readwise.io/reader/document_raw_content/26339439#ch09fig04).
				  
				  Figure 9.4. A rolling update of pods using two ReplicationControllers
				  
				  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added87-09fig04_alt_fRehAeD.jpg) #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr3wat3j7wf1sk8qmzktteym))
			- -
			- -
				- A Deployment definition: kubia-deployment-v1.yaml
				  
				  apiVersion: apps/v1beta1          ❶
				  kind: Deployment                  ❷
				  metadata:
				  name: kubia                     ❸
				  spec:
				  replicas: 3
				  template:
				    metadata:
				      name: kubia
				      labels:
				        app: kubia
				    spec:
				      containers:
				- ([View Highlight](https://read.readwise.io/read/01gr3x7t9frgn6qd7t0w9g7ydx))
			- -
			- -
				- You’re now ready to create the Deployment:
				  id:: 63dc0fdb-4d9d-416b-889a-56627b1cb0e9
				  
				  **$ kubectl create -f kubia-deployment-v1.yaml --record**
				  deployment "kubia" created
				  
				  * * *
				  
				  Tip
				  
				  Be sure to include the --record command-line option when creating it. This records the command in the revision history, which will be useful later. #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr3y4b5wcqbtbj87zqt60h20))
			- -
			- -
				- Displaying the status of the deployment rollout
				  id:: 63dc0fdb-92a1-42fd-9a3d-7b4a5f66e63b
				  
				  You can use the usual kubectl get deployment and the kubectl describe deployment commands to see details of the Deployment, but let me point you to an additional command, which is made specifically for checking a Deployment’s status:
				  
				  **$ kubectl rollout status deployment kubia**
				  deployment kubia successfully rolled out
				  
				  According to this, the Deployment has been successfully rolled out, so you should see the three pod replicas up and running. Let’s see:
				  
				  **$ kubectl get po**
				  NAME                     READY     STATUS    RESTARTS   AGE
				  kubia-1506449474-otnnh   1/1       Running   0          14s
				  kubia-1506449474-vmn7s   1/1       Running   0          14s
				  kubia-1506449474-xis6m   1/1       Running   0          14s #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr3xb2bswj1ajvrvwjp59nat))
			- -
			- -
				- Understanding the awesomeness of Deployments
				  id:: 63dc0fdb-4dfe-43ae-8459-4ce0b9f1e79a
				  
				  Let’s think about what has happened. By changing the pod template in your Deployment resource, you’ve updated your app to a newer version—by changing a single field!
				  
				  The controllers running as part of the Kubernetes control plane then performed the update. The process wasn’t performed by the kubectl client, like it was when you used kubectl rolling-update. I don’t know about you, but I think that’s simpler than having to run a special command telling Kubernetes what to do and then waiting around for the process to be completed. #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr3xvaf5h5fjn7f24a527fp3))
			- -
			- -
				- The events that occurred below the Deployment’s surface during the update are similar to what happened during the kubectl rolling-update. An additional ReplicaSet was created and it was then scaled up slowly, while the previous ReplicaSet was scaled down to zero (the initial and final states are shown in [figure 9.10](https://readwise.io/reader/document_raw_content/26339439#ch09fig10)).
				  id:: 63dc0fdb-6d06-4b04-ad6b-f1e706ac4fb2
				  
				  Figure 9.10. A Deployment at the start and end of a rolling update
				  
				  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added93-09fig10_alt_cDksNJT.jpg) #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr3xy3v1ww2v5grntaef27jx))
			- -
			- -
				- You can’t have your users experiencing internal server errors, so you need to do something about it fast. In [section 9.3.6](https://readwise.io/reader/document_raw_content/26339439#ch09lev2sec11) you’ll see how to block bad rollouts automatically, but for now, let’s see what you can do about your bad rollout manually. Luckily, Deployments make it easy to roll back to the previously deployed version by telling Kubernetes to undo the last rollout of a Deployment:
				  id:: 63dc0fdb-4f28-42c0-b1f2-51c309d8a9c9
				  
				  **$ kubectl rollout undo deployment kubia**
				  deployment "kubia" rolled back
				  
				  This rolls the Deployment back to the previous revision. #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr3y1eyjaam0314ge96hz63h))
			- -
			- -
				- The revision history can be displayed with the kubectl rollout history command:
				  id:: 63dc0fdb-6a87-4355-8511-e8e861bde18c
				  
				  **$ kubectl rollout history deployment kubia**
				  deployments "kubia":
				  REVISION    CHANGE-CAUSE
				  2           kubectl set image deployment kubia nodejs=luksa/kubia:v2
				  3           kubectl set image deployment kubia nodejs=luksa/kubia:v3
				  
				  Remember the --record command-line option you used when creating the Deployment? Without it, the CHANGE-CAUSE column in the revision history would be empty, making it much harder to figure out what’s behind each revision.
				  
				  Rolling back to a specific Deployment revision
				  
				  You can roll back to a specific revision by specifying the revision in the undo command. For example, if you want to roll back to the first version, you’d execute the following command:
				  
				  **$ kubectl rollout undo deployment kubia --to-revision=1** #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr3y6e1qnw23hj2g9azvxgym))
			- -
			- -
				- Remember the inactive ReplicaSet left over when you modified the Deployment the first time? The ReplicaSet represents the first revision of your Deployment. All Replica-Sets created by a Deployment represent the complete revision history, as shown in [figure 9.11](https://readwise.io/reader/document_raw_content/26339439#ch09fig11). Each ReplicaSet stores the complete information of the Deployment at that specific revision, so you shouldn’t delete it manually. If you do, you’ll lose that specific revision from the Deployment’s history, preventing you from rolling back to it.
				  id:: 63dc0fdb-844b-438a-b5ee-e8057a271445
				  
				  Figure 9.11. A Deployment’s ReplicaSets also act as its revision history.
				  
				  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added94-09fig11_alt_ct0Opmo.jpg)
				  
				  But having old ReplicaSets cluttering your ReplicaSet list is not ideal, so the length of the revision history is limited by the revisionHistoryLimit property on the Deployment resource. It defaults to two, so normally only the current and the previous revision are shown in the history (and only the current and the previous ReplicaSet are preserved). Older ReplicaSets are deleted automatically. #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr3y8kawxwy23jt1xd9ybp07))
			- -
			- -
				- Specifying parameters for the rollingUpdate strategy
				  id:: 63dc0fdb-7c80-47bf-a926-bf35fcdd1800
				  
				  spec:
				  strategy:
				    rollingUpdate:
				      maxSurge: 1
				      maxUnavailable: 0
				    type: RollingUpdate
				  
				  What these properties do is explained in [table 9.2](https://readwise.io/reader/document_raw_content/26339439#ch09table02).
				  
				  Table 9.2. Properties for configuring the rate of the rolling update
				  
				  
				  
				  Property
				  
				  What it does
				  
				  maxSurge
				  
				  Determines how many pod instances you allow to exist above the desired replica count configured on the Deployment. It defaults to 25%, so there can be at most 25% more pod instances than the desired count. If the desired replica count is set to four, there will never be more than five pod instances running at the same time during an update. When converting a percentage to an absolute number, the number is rounded up. Instead of a percentage, the value can also be an absolute value (for example, one or two additional pods can be allowed).
				  
				  maxUnavailable
				  
				  Determines how many pod instances can be unavailable relative to the desired replica count during the update. It also defaults to 25%, so the number of available pod instances must never fall below 75% of the desired replica count. Here, when converting a percentage to an absolute number, the number is rounded down. If the desired replica count is set to four and the percentage is 25%, only one pod can be unavailable. There will always be at least three pod instances available to serve requests during the whole rollout. As with maxSurge, you can also specify an absolute value instead of a percentage. #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr3ydykmz43yfkag1nvwzqta))
			- -
			- -
				- Rolling update of a Deployment with three replicas and default maxSurge and maxUnavailable
				  id:: 63dc0fdb-d877-497c-95a3-d5b41bae91ee
				  
				  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added95-09fig12_alt_VXLD4xs.jpg)
				  
				  Understanding the maxUnavailable property
				  
				  The extensions/v1beta1 version of Deployments uses different defaults—it sets both maxSurge and maxUnavailable to 1 instead of 25%. In the case of three replicas, maxSurge is the same as before, but maxUnavailable is different (1 instead of 0). This makes the rollout process unwind a bit differently, as shown in [figure 9.13](https://readwise.io/reader/document_raw_content/26339439#ch09fig13).
				  
				  Figure 9.13. Rolling update of a Deployment with the maxSurge=1 and maxUnavailable=1
				  
				  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added96-09fig13_alt_TfvOUw5.jpg)
				  
				  In this case, one replica can be unavailable, so if the desired replica count is three, only two of them need to be available. That’s why the rollout process immediately deletes one pod and creates two new ones. This ensures two pods are available and that the maximum number of pods isn’t exceeded (the maximum is four in this case—three plus one from maxSurge). As soon as the two new pods are available, the two remaining old pods are deleted. #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr3yjym7kd6zb2v1x0kr2pw2))
			- -
			- -
				- Deployment with a readiness probe: kubia-deployment-v3-with-readinesscheck.yaml
				  
				  apiVersion: apps/v1beta1
				  kind: Deployment
				  metadata:
				  name: kubia
				  spec:
				  replicas: 3
				  minReadySeconds: 10                 ❶
				  strategy:
				    rollingUpdate:
				      maxSurge: 1
				      maxUnavailable: 0               ❷
				    type: RollingUpdate
				  template:
				    metadata:
				      name: kubia
				      labels:
				        app: kubia
				    spec:
				      containers:
				- tags:: [[code]]
				- ([View Highlight](https://read.readwise.io/read/01gr3z4rhh6yryz3c6d6r1q2fd))
			- -
			- -
				- Aha! There’s your problem (or as you’ll learn soon, your blessing)! The pod is shown as not ready, but I guess you’ve been expecting that, right? What has happened?
				  id:: 63dc0fdb-d7e1-41a9-912d-8f560b6b9668
				  
				  Understanding how a readiness probe prevents bad versions from being rolled out
				  
				  As soon as your new pod starts, the readiness probe starts being hit every second (you set the probe’s interval to one second in the pod spec). On the fifth request the readiness probe began failing, because your app starts returning HTTP status code 500 from the fifth request onward.
				  
				  As a result, the pod is removed as an endpoint from the service (see [figure 9.14](https://readwise.io/reader/document_raw_content/26339439#ch09fig14)). By the time you start hitting the service in the curl loop, the pod has already been marked as not ready. This explains why you never hit the new pod with curl. And that’s exactly what you want, because you don’t want clients to hit a pod that’s not functioning properly.
				  
				  Figure 9.14. Deployment blocked by a failing readiness probe in the new pod
				  
				  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added97-09fig14_alt_ER2oR2U.jpg) #flashcard
				- ([View Highlight](https://read.readwise.io/read/01gr3z8t58c20drxnyyvk25e2j))
			- -
		- Chapter 10. StatefulSets: deploying replicated stateful applications
- New highlights added [[Thursday, 02-02-2023]] at 12:48 PM
	- -
		- Instead of using a ReplicaSet to run these types of pods, you create a StatefulSet resource, which is specifically tailored to applications where instances of the application must be treated as non-fungible individuals, with each one having a stable name and state.
		  id:: 63dc0fdb-ecee-4911-80c7-f069cf500b57
		  
		  10.2.1. Comparing StatefulSets with ReplicaSets
		  
		  To understand the purpose of StatefulSets, it’s best to compare them to ReplicaSets or ReplicationControllers. But first let me explain them with a little analogy that’s widely used in the field.
		  
		  Understanding stateful pods with the pets vs. cattle analogy
		  
		  You may have already heard of the pets vs. cattle analogy. If not, let me explain it. We can treat our apps either as pets or as cattle. #flashcard
		- ([View Highlight](https://read.readwise.io/read/01gr4asp5wfnt5f8txpnzpeyss))
	- -
	- -
		- But in contrast to ReplicaSets, the replacement pod gets the same name and hostname as the pod that has disappeared (this distinction between ReplicaSets and StatefulSets is illustrated in [figure 10.6](https://readwise.io/reader/document_raw_content/26339439#ch10fig06)).
		  id:: 63dc0fdb-879f-46b7-a9a1-cb77dbe99bb1
		  
		  Figure 10.6. A StatefulSet replaces a lost pod with a new one with the same identity, whereas a ReplicaSet replaces it with a completely new unrelated pod.
		  
		  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added103-10fig06_alt_3WjALxq.jpg)
		  
		  The new pod isn’t necessarily scheduled to the same node, but as you learned early on, what node a pod runs on shouldn’t matter. This holds true even for stateful pods. Even if the pod is scheduled to a different node, it will still be available and reachable under the same hostname as before. #flashcard
		- ([View Highlight](https://read.readwise.io/read/01gr4bb4s0j7pf2hh8bzxht0zt))
	- -
	- -
		- The StatefulSet has to create the PersistentVolumeClaims as well, the same way it’s creating the pods. For this reason, a StatefulSet can also have one or more volume claim templates, which enable it to stamp out PersistentVolumeClaims along with each pod instance (see [figure 10.8](https://readwise.io/reader/document_raw_content/26339439#ch10fig08)).
		  id:: 63dc0fdb-2bb4-4d90-aae5-850c7ae5512a
		  
		  Figure 10.8. A StatefulSet creates both pods and PersistentVolumeClaims.
		  
		  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added105-10fig08_alt_3fbTlAn.jpg)
		  
		  The PersistentVolumes for the claims can either be provisioned up-front by an administrator or just in time through dynamic provisioning of PersistentVolumes, as explained at the end of [chapter 6](https://readwise.io/reader/document_raw_content/26339439#ch06).
		  
		  Understanding the creation and deletion of PersistentVolumeClaims
		  
		  Scaling up a StatefulSet by one creates two or more API objects (the pod and one or more PersistentVolumeClaims referenced by the pod). Scaling down, however, deletes only the pod, leaving the claims alone. The reason for this is obvious, if you consider what happens when a claim is deleted. After a claim is deleted, the PersistentVolume it was bound to gets recycled or deleted and its contents are lost.
		  
		  Because stateful pods are meant to run stateful applications, which implies that the data they store in the volume is important, deleting the claim on scale-down of a Stateful-Set could be catastrophic—especially since triggering a scale-down is as simple as decreasing the replicas field of the StatefulSet. For this reason, you’re required to delete PersistentVolumeClaims manually to release the underlying PersistentVolume. #flashcard
		- ([View Highlight](https://read.readwise.io/read/01gr4bmsa0b2dc02favhxdv1wf))
	- -
	- -
		- StatefulSets don’t delete PersistentVolumeClaims when scaling down; then they reattach them when scaling back up.
		  id:: 63dc0fdb-31c9-4c79-8ae3-3bff386cbd0a
		  
		  ![](https://readwise-assets.s3.amazonaws.com/media/reader/parsed_document_assets/26339439/added106-10fig09_alt_gPs7iV2.jpg) #flashcard
		- ([View Highlight](https://read.readwise.io/read/01gr4bp3zkgkr1c821sf7phhr6))
	- -
	- -
		- StatefulSet manifest: kubia-statefulset.yaml
		  
		  apiVersion: apps/v1beta1
		  kind: StatefulSet
		  metadata:
		  name: kubia
		  spec:
		  serviceName: kubia
		  replicas: 2
		  template:
		    metadata:
		      labels:                        ❶
		        app: kubia                   ❶
		    spec:
		      containers:
		- ([View Highlight](https://read.readwise.io/read/01gr4cg0c53jntharg9ewtbwy7))
	- -