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