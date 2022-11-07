# Kubernetes in Action

deck:: [[O'Reilly-Learning::Kubernetes in Action]]\
author:: [[Marko Luksa]]\
full-title:: "Kubernetes in Action"\
category:: #books\
\
tags:: O'Reilly-Learning  

![](https://learning.oreilly.com/library/view/kubernetes-in-action/9781617293726/ibis_generated_cover_thumbnail.jpg)
## Highlights
### Chapter 1. Introducing Kubernetes
### Chapter 5. Services: enabling clients to discover and talk to pods
### Chapter 6. Volumes: attaching disk storage to containers
- id:: 6363991f-2597-409e-9abb-b2807cdf8ac3
  
  Figure 1.1. Components inside a monolithic application vs. standalone microservices #flashcard
-
- id:: 6363991f-8865-4503-b61f-9f2e83706e25
   [Figure 5.10](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781617293726/files/Images/05fig10_alt.jpg) #flashcard 
    Figure 5.10 shows how the client connected to one of the pods through the Ingress controller. The client first performed a DNS lookup of kubia.example.com, and the DNS server (or the local operating system) returned the IP of the Ingress controller. The client then sent an HTTP request to the Ingress controller and specified kubia.example.com in the Host header. From that header, the controller determined which service the client is trying to access, looked up the pod IPs through the Endpoints object associated with the service, and forwarded the client’s request to one of the pods.
-
- id:: 6363991f-d122-427a-8e61-b1ce5263b212
   Use case examples of a volume inside a pod in Kubernetes
   [Figure 6.1](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781617293726/files/Images/06fig01.jpg) #flashcard 
    Imagine you have a pod with three containers (shown in figure 6.1). One container runs a web server that serves HTML pages from the /var/htdocs directory and stores the access log to /var/logs. The second container runs an agent that creates HTML files and stores them in /var/html. The third container processes the logs it finds in the /var/logs directory (rotates them, compresses them, analyzes them, or whatever).
-
- id:: 6363991f-47dc-4848-8005-83ab46bac771
  
  Here’s a list of several of the available volume types:
     emptyDir—A simple empty directory used for storing transient data.
     hostPath—Used for mounting directories from the worker node’s filesystem into the pod.
     gitRepo—A volume initialized by checking out the contents of a Git repository.
     nfs—An NFS share mounted into the pod.
     gcePersistentDisk (Google Compute Engine Persistent Disk), awsElasticBlockStore (Amazon Web Services Elastic Block Store Volume), azureDisk (Microsoft Azure Disk Volume)—Used for mounting cloud provider-specific storage.
     cinder, cephfs, iscsi, flocker, glusterfs, quobyte, rbd, flexVolume, vsphere-Volume, photonPersistentDisk, scaleIO—Used for mounting other types of network storage.
     configMap, secret, downwardAPI—Special types of volumes used to expose certain Kubernetes resources and cluster information to the pod.
     persistentVolumeClaim—A way to use a pre- or dynamically provisioned persistent storage. (We’ll talk about them in the last section of this chapter.) #flashcard
-
- id:: 6363991f-a61f-450f-9d17-83795b4f6019
  
  Microservices communicate through synchronous protocols such as HTTP, over which they usually expose RESTful (REpresentational State Transfer) APIs, or through asynchronous protocols such as AMQP (Advanced Message Queueing Protocol). These protocols are simple, well understood by most developers, and not tied to any specific programming language. Each microservice can be written in the language that’s most appropriate for implementing that specific microservice. #flashcard
-
- id:: 6363991f-7304-4808-b102-2a3a11801c9e
   What is the _readiness probe_ in Kubernetes? #flashcard 
    The readiness probe is invoked periodically and determines whether the specific pod should receive client requests or not. When a container’s readiness probe returns success, it’s signaling that the container is ready to accept requests.
     This notion of being ready is obviously something that’s specific to each container. Kubernetes can merely check if the app running in the container responds to a simple GET / request or it can hit a specific URL path, which causes the app to perform a whole list of checks to determine if it’s ready. Such a detailed readiness probe, which takes the app’s specifics into account, is the app developer’s responsibility.
-
### Chapter 9. Deployments: updating applications declaratively
- id:: 6363991f-649a-44f1-9989-accfbbd7231e
   What is NoOps? #flashcard 
    Ideally, you want the developers to deploy applications themselves without knowing anything about the hardware infrastructure and without dealing with the ops team. This is referred to as NoOps. Obviously, you still need someone to take care of the hardware infrastructure, but ideally, without having to deal with peculiarities of each application running on it.
-
- id:: 6363991f-bd8f-4835-8086-f041c79c810a
   **Liveness probes** VS **Readiness probes** #flashcard 
    Unlike liveness probes, if a container fails the readiness check, it won’t be killed or restarted. This is an important distinction between liveness and readiness probes. Liveness probes keep pods healthy by killing off unhealthy containers and replacing them with new, healthy ones, whereas readiness probes make sure that only pods that are ready to serve requests receive them. This is mostly necessary during container start up, but it’s also useful after the container has been running for a while.
-
- id:: 6363991f-b63d-4a53-97f7-21b4f07cf5df
   How could you undo a deployment in Kubernetes if something goes wrong? #flashcard 
    Luckily, Deployments make it easy to roll back to the previously deployed version by telling Kubernetes to undo the last rollout of a Deployment:
     $ kubectl rollout undo deployment kubia
     deployment "kubia" rolled back
-
- id:: 6363991f-f534-4459-9952-d17021bbe644
  
  Kubernetes uses Linux container technologies to provide isolation of running applications #flashcard
-
- id:: 6363991f-c28e-4c09-8b12-106bf11d2e1a
   About containers and Linux #flashcard 
    Instead of using virtual machines to isolate the environments of each microservice (or software processes in general), developers are turning to Linux container technologies. They allow you to run multiple services on the same host machine, while not only exposing a different environment to each of them, but also isolating them from each other, similarly to VMs, but with much less overhead.
     A process running in a container runs inside the host’s operating system, like all the other processes (unlike VMs, where processes run in separate operating systems). But the process in the container is still isolated from other processes. To the process itself, it looks like it’s the only one running on the machine and in its operating system.
-
- id:: 6363991f-a419-4eab-9320-78bb0983a198
  
  Figure 1.4. Using VMs to isolate groups of applications vs. isolating individual apps with containers #flashcard
-
- id:: 6363991f-c045-4346-9f78-c84c44b21430
   Types of hypervisors #flashcard 
    Note
     Two types of hypervisors exist. Type 1 hypervisors don’t use a host OS, while Type 2 do.
-
- id:: 6363991f-2c94-47fb-90e4-5931bf790439
   https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781617293726/files/Images/01fig05.jpg #flashcard 
    Containers, on the other hand, all perform system calls on the exact same kernel running in the host OS. This single kernel is the only one performing x86 instructions on the host’s CPU. The CPU doesn’t need to do any kind of virtualization the way it does with VMs (see figure 1.5).
-
- id:: 6363991f-2bb5-4b7c-9a60-f54f2e583b8a
  
  By this point, you’re probably wondering how exactly containers can isolate processes if they’re running on the same operating system. Two mechanisms make this possible. The first one, Linux Namespaces, makes sure each process sees its own personal view of the system (files, processes, network interfaces, hostname, and so on). The second one is Linux Control Groups (cgroups), which limit the amount of resources the process can consume (CPU, memory, network bandwidth, and so on). #flashcard
-
- id:: 6363991f-0a61-4ed6-ba50-65e93ed81ea8
   What is an image in Docker? #flashcard 
    Images—A Docker-based container image is something you package your application and its environment into. It contains the filesystem that will be available to the application and other metadata, such as the path to the executable that should be executed when the image is run.
-
- id:: 6363991f-056d-449f-88e1-fd333d992bf0
   What is a registy in Docker? #flashcard 
    Registries—A Docker Registry is a repository that stores your Docker images and facilitates easy sharing of those images between different people and computers. When you build your image, you can either run it on the computer you’ve built it on, or you can push (upload) the image to a registry and then pull (download) it on another computer and run it there. Certain registries are public, allowing anyone to pull images from it, while others are private, only accessible to certain people or machines.
-
- id:: 6363991f-8684-48cc-a444-1c70f91f1b3f
  
  Containers—A Docker-based container is a regular Linux container created from a Docker-based container image. A running container is a process running on the host running Docker, but it’s completely isolated from both the host and all other processes running on it. The process is also resource-constrained, meaning it can only access and use the amount of resources (CPU, RAM, and so on) that are allocated to it. #flashcard
-
- id:: 6363991f-381e-4305-bbdb-72b1a66ca78a
   https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781617293726/files/Images/01fig08_alt.jpg #flashcard 
    Figure 1.8 shows the simplest possible view of a Kubernetes system. The system is composed of a master node and any number of worker nodes. When the developer submits a list of apps to the master, Kubernetes deploys them to the cluster of worker nodes. What node a component lands on doesn’t (and shouldn’t) matter—neither to the developer nor to the system administrator.
     Figure 1.8. Kubernetes exposes the whole datacenter as a single deployment platform.
-
- id:: 6363991f-5c2b-4386-a385-3fe67dc77d05
   https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781617293726/files/Images/01fig09_alt.jpg #flashcard 
    At the hardware level, a Kubernetes cluster is composed of many nodes, which can be split into two types:
     The master node, which hosts the Kubernetes Control Plane that controls and manages the whole Kubernetes system
     Worker nodes that run the actual applications you deploy
     Figure 1.9 shows the components running on these two sets of nodes. I’ll explain them next.
     Figure 1.9. The components that make up a Kubernetes cluster
-
- id:: 6363991f-29d1-41fe-8d5e-94dc2fca9ad9
   About the Kubernetes Control Plane #flashcard 
    The Control Plane
     The Control Plane is what controls the cluster and makes it function. It consists of multiple components that can run on a single master node or be split across multiple nodes and replicated to ensure high availability. These components are
     The Kubernetes API Server, which you and the other Control Plane components communicate with
     The Scheduler, which schedules your apps (assigns a worker node to each deployable component of your application)
     The Controller Manager, which performs cluster-level functions, such as replicating components, keeping track of worker nodes, handling node failures, and so on
     etcd, a reliable distributed data store that persistently stores the cluster configuration.
     The components of the Control Plane hold and control the state of the cluster, but they don’t run your applications. This is done by the (worker) nodes.
-
- id:: 6363991f-b445-4ebd-94fe-a4a18384f73f
   About the nodes in Kubernetes #flashcard 
    The nodes
     The worker nodes are the machines that run your containerized applications. The task of running, monitoring, and providing services to your applications is done by the following components:
     Docker, rkt, or another container runtime, which runs your containers
     The Kubelet, which talks to the API server and manages containers on its node
     The Kubernetes Service Proxy (kube-proxy), which load-balances network traffic between application components
-
- id:: 6363991f-1f57-49a7-beb2-60266afe77f4
  
  Figure 1.10. A basic overview of the Kubernetes architecture and an application running on top of it #flashcard
-
### Chapter 2. First steps with Docker and Kubernetes
- id:: 6363991f-4b75-4147-bf5e-08b503e7e3fd
  
  All software packages get updated, so more than a single version of a package usually exists. Docker supports having multiple versions or variants of the same image under the same name. Each variant must have a unique tag. When referring to images without explicitly specifying the tag, Docker will assume you’re referring to the so-called latest tag. #flashcard
-
- id:: 6363991f-c1c0-43f6-afe9-09d81b596716
  
  You could now download and install Node.js and test your app directly, but this isn’t necessary, because you’ll use Docker to package the app into a container image and enable it to be run anywhere without having to download or install anything (except Docker, which does need to be installed on the machine you want to run the image on). #flashcard
-
- id:: 6363991f-23d1-47b8-8d23-eb90e6608d70
  
  Choosing a base image
     You may wonder why we chose this specific image as your base. Because your app is a Node.js app, you need your image to contain the node binary executable to run the app. You could have used any image that contains that binary, or you could have even used a Linux distro base image such as fedora or ubuntu and installed Node.js into the container at image build time. But because the node image is made specifically for running Node.js apps, and includes everything you need to run your app, you’ll use that as the base image. #flashcard
-
- id:: 6363991f-b16a-4281-aa9d-93c16121beb9
  
  You may think that each Dockerfile creates only a single new layer, but that’s not the case. When building an image, a new layer is created for each individual command in the Dockerfile. During the build of your image, after pulling all the layers of the base image, Docker will create a new layer on top of them and add the app.js file into it. Then it will create yet another layer that will specify the command that should be executed when the image is run. This last layer will then be tagged as kubia:latest. This is shown in figure 2.3, which also shows how a different image called other:latest would use the same layers of the Node.js image as your own image does.
     Figure 2.3. Container images are composed of layers that can be shared among different images.
     W #flashcard
-
- id:: 6363991f-d58c-4d3c-a425-3bfff163028d
  
  Understanding that processes in a container run in the host operating system
     If you now open another terminal and list the processes on the host OS itself, you will, among all other host processes, also see the processes running in the container, as shown in listing 2.7.
     Note
     If you’re using a Mac or Windows, you’ll need to log into the VM where the Docker daemon is running to see these processes.
     Listing 2.7. A container’s processes run in the host OS
     $ ps aux | grep app.js
     USER PID %CPU %MEM VSZ RSS TTY STAT START TIME COMMAND
     root 382 0.0 0.1 676380 16504 ? Sl 12:31 0:00 node app.js
     This proves that processes running in the container are running in the host OS. If you have a keen eye, you may have noticed that the processes have different IDs inside the container vs. on the host. The container is using its own PID Linux namespace and has a completely isolated process tree, with its own sequence of numbers. #flashcard
-
- id:: 6363991f-2f97-43b7-b000-2dccd06db103
   What is a pod in Kubernetes? #flashcard 
    You may be wondering if you can see your container in a list showing all the running containers. Maybe something such as kubectl get containers? Well, that’s not exactly how Kubernetes works. It doesn’t deal with individual containers directly. Instead, it uses the concept of multiple co-located containers. This group of containers is called a Pod.
     A pod is a group of one or more tightly related containers that will always run together on the same worker node and in the same Linux namespace(s). Each pod is like a separate logical machine with its own IP, hostname, processes, and so on, running a single application.
-
- id:: 6363991f-2afd-4187-86c3-1659ed8acb6b
  
  Figure 2.6. Running the luksa/kubia container image in Kubernetes
     When you ran the kubectl command, it created a new ReplicationController object in the cluster by sending a REST HTTP request to the Kubernetes API server. The ReplicationController then created a new pod, which was then scheduled to one of the worker nodes by the Scheduler. The Kubelet on that node saw that the pod was scheduled to it and instructed Docker to pull the specified image from the registry because the image wasn’t available locally. After downloading the image, Docker created and ran the container. #flashcard
-
- id:: 6363991f-2e8b-45ad-9357-2cde2bea6ecc
  
  Definition
     The term scheduling means assigning the pod to a node. The pod is run immediately, not at a time in the future as the term might lead you to believe. #flashcard
-
- id:: 6363991f-2427-4f3e-b87e-cbe29e88a8df
   Why do we need services in Kubernetes? #flashcard 
    To understand why you need services, you need to learn a key detail about pods. They’re ephemeral. A pod may disappear at any time—because the node it’s running on has failed, because someone deleted the pod, or because the pod was evicted from an otherwise healthy node. When any of those occurs, a missing pod is replaced with a new one by the Replication-Controller, as described
-
### Chapter 3. Pods: running containers in Kubernetes
- id:: 6363991f-6886-48a3-b300-ed76e3886b74
   We need only one process in each container because (among other reasons) we won’t be able to identify properly each one. 
   Furthermore, we need a **pod** just for that reason. #flashcard 
    Understanding why multiple containers are better than one contain- ner running multiple processes
-
- id:: 6363991f-5f30-4def-a23e-da5f9d80a74e
   About pods and IPs. #flashcard 
    Like a computer on a LAN, each pod gets its own IP address and is accessible from all other pods through this network established specifically for pods.
-
- id:: 6363991f-f90c-4065-b7a2-52054aada0ab
   Parts of a pod definition #flashcard 
    The pod definition consists of a few parts. First, there’s the Kubernetes API version used in the YAML and the type of resource the YAML is describing. Then, three important sections are found in almost all Kubernetes resources:
     Metadata includes the name, namespace, labels, and other information about the pod.
     Spec contains the actual description of the pod’s contents, such as the pod’s containers, volumes, and other data.
     Status contains the current information about the running pod, such as what condition the pod is in, the description and status of each container, and the pod’s internal IP and other basic info.
-
- id:: 6363991f-5178-48ed-a2da-5e968cd60c1f
  
  When preparing a manifest, you can either turn to the Kubernetes reference documentation at http://kubernetes.io/docs/api to see which attributes are supported by each API object, or you can use the kubectl explain command. #flashcard
-
- id:: 6363991f-5b65-4003-8a04-2c6ad64a2f7d
   How can you **remove** the Kubernetes resources? #flashcard 
    You can delete the ReplicationController and the pods, as well as all the Services you’ve created, by deleting all resources in the current namespace with a single command:
     $ kubectl delete all --all
     pod "kubia-09as0" deleted
     replicationcontroller "kubia" deleted
     service "kubernetes" deleted
     service "kubia-http" deleted
     The first all in the command specifies that you’re deleting resources of all types, and the --all option specifies that you’re deleting all resource instances instead of specifying them by name
-
- id:: 6363991f-4221-4502-8ba8-6e3c8c9b7cac
   Which is the purpose of a ReplicationController in Kubernetes? #flashcard 
    ReplicationController. It makes sure there’s always exactly one instance of your pod running. Generally, ReplicationControllers are used to replicate pods (that is, create multiple copies of a pod) and keep them running. In your case, you didn’t specify how many pod replicas you want, so the Replication-Controller created a single one. If your pod were to disappear for any reason, the Replication-Controller would create a new pod to replace the missing one.
-
### Chapter 4. Replication and other controllers: deploying managed pods
- id:: 6363991f-a399-448c-a436-5797dd03e286
   Mention the purpose of a **liveness probe** in *Kubernetes* #flashcard 
    Kubernetes can check if a container is still alive through liveness probes. You can specify a liveness probe for each container in the pod’s specification. Kubernetes will periodically execute the probe and restart the container if the probe fails.
-
- id:: 6363991f-3e14-452b-9576-4f8b8f9c7b76
   About liveness probe's terms #flashcard 
    kubectl describe also displays additional information about the liveness probe:
     Liveness: http-get http://:8080/ delay=0s timeout=1s period=10s #success=1
     ➥ #failure=3
     Beside the liveness probe options you specified explicitly, you can also see additional properties, such as delay, timeout, period, and so on. The delay=0s part shows that the probing begins immediately after the container is started. The timeout is set to only 1 second, so the container must return a response in 1 second or the probe is counted as failed. The container is probed every 10 seconds (period=10s) and the container is restarted after the probe fails three consecutive times (#failure=3).
-
- id:: 6363991f-4a37-483f-bb3d-1823dc2f87dd
   [Figure 4.1](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781617293726/files/Images/04fig01_alt.jpg) #flashcard 
    Figure 4.1. When a node fails, only pods backed by a ReplicationController are recreated.
-
- id:: 6363991f-d519-4c6f-83b0-4aff2618e53a
   How many parts has a **ReplicationController** ? [Figure](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781617293726/files/Images/04fig03.jpg) #flashcard 
    A ReplicationController has three essential parts (also shown in figure 4.3):
     A label selector, which determines what pods are in the ReplicationController’s scope
     A replica count, which specifies the desired number of pods that should be running
     A pod template, which is used when creating new pod replicas
     Figure 4.3. The three key parts of a ReplicationController (pod selector, replica count, and pod template)
-
- id:: 6363991f-349e-4a80-b942-d1d7f4c27ac1
  
  Tip
     Don’t specify a pod selector when defining a ReplicationController. Let Kubernetes extract it from the pod template. This will keep your YAML shorter and simpler. #flashcard
-
- id:: 6363991f-d9b0-4c41-946f-855c9582ca3f
  
  If a node fails in the non-Kubernetes world, the ops team would need to migrate the applications running on that node to other machines manually. Kubernetes, on the other hand, does that automatically. Soon after the ReplicationController detects that its pods are down, it will spin up new pods to replace them. #flashcard
-
- id:: 6363991f-4a2f-4985-aa89-d28edea1ed92
  
  When deleting a ReplicationController with kubectl delete, you can keep its pods running by passing the --cascade=false option to the command. Try that now:
     $ kubectl delete rc kubia --cascade=false
     replicationcontroller "kubia" deleted
     You’ve deleted the ReplicationController so the pods are on their own. They are no longer managed. But you can always create a new ReplicationController with the proper label selector and make them managed again. #flashcard
-
- id:: 6363991f-e593-4344-8468-2c05b8ef6544
  
  a single ReplicationController can’t match pods with the label env=production and those with the label env=devel at the same time. It can only match either pods with the env=production label or pods with the env=devel label. But a single ReplicaSet can match both sets of pods and treat them as a single group. #flashcard
-
- id:: 6363991f-0628-461f-b099-ef10a693a7e0
   Example of **matchExpressions** selector in Kubernetes #flashcard 
    Listing 4.9. A matchExpressions selector: kubia-replicaset-matchexpressions.yaml
     selector:
     matchExpressions:
	- key: app ❶
	       operator: In ❷
	       values: ❷
	- kubia ❷
	       ❶ This selector requires the pod to contain a label with the “app” key.
	       ❷ The label’s value must be “kubia”.
	       Note
	       Only the selector is shown. You’ll find the whole ReplicaSet definition in the book’s code archive.
	       You can add additional expressions to the selector. As in the example, each expression must contain a key, an operator, and possibly (depending on the operator) a list of values. You’ll see four valid operators:
	       In—Label’s value must match one of the specified values.
	       NotIn—Label’s value must not match any of the specified values.
	       Exists—Pod must include a label with the specified key (the value isn’t important). When using this operator, you shouldn’t specify the values field.
	       DoesNotExist—Pod must not include a label with the specified key. The values property must not be specified.
-
- id:: 6363991f-097f-4095-87ff-626105f3bfb0
   [Figure 4.8](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781617293726/files/Images/04fig08_alt.jpg) #flashcard 
    Both ReplicationControllers and ReplicaSets are used for running a specific number of pods deployed anywhere in the Kubernetes cluster. But certain cases exist when you want a pod to run on each and every node in the cluster (and each node needs to run exactly one instance of the pod, as shown in figure 4.8).
     Figure 4.8. DaemonSets run only a single pod replica on each node, whereas ReplicaSets scatter them around the whole cluster randomly.
-
- id:: 6363991f-d307-4169-9755-f7b7bb3cc08d
   Example of a Service YAML definition #flashcard 
    Listing 5.1. A definition of a service: kubia-svc.yaml
     apiVersion: v1
     kind: Service
     metadata:
     name: kubia
     spec:
     ports:
	- port: 80 ❶
	       targetPort: 8080 ❷
	       selector: ❸
	       app: kubia ❸
	       ❶ The port this service will be available on
	       ❷ The container port the service will forward to
	       ❸ All pods with the app=kubia label will be part of this service.
-
- id:: 6363991f-712d-4a5f-aa80-0254cb2333da
  
  If you later decide to migrate the external service to pods running inside Kubernetes, you can add a selector to the service, thereby making its Endpoints managed automatically. The same is also true in reverse—by removing the selector from a Service, Kubernetes stops updating its Endpoints. This means a service IP address can remain constant while the actual implementation of the service is changed. #flashcard
-
- id:: 6363991f-9244-4899-9231-4d6147d10623
   About NodePort in Kubernetes #flashcard 
    The first method of exposing a set of pods to external clients is by creating a service and setting its type to NodePort. By creating a NodePort service, you make Kubernetes reserve a port on all its nodes (the same port number is used across all of them) and forward incoming connections to the pods that are part of the service.
     This is similar to a regular service (their actual type is ClusterIP), but a NodePort service can be accessed not only through the service’s internal cluster IP, but also through any node’s IP and the reserved node port.
     This will make more sense when you try interacting with a NodePort service.
-
- id:: 6363991f-ff1d-4215-ada5-dfced26913aa
   [Figure 5.9](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9781617293726/files/Images/05fig09_alt.jpg) #flashcard 
    One important reason is that each LoadBalancer service requires its own load balancer with its own public IP address, whereas an Ingress only requires one, even when providing access to dozens of services. When a client sends an HTTP request to the Ingress, the host and path in the request determine which service the request is forwarded to, as shown in figure 5.9.
-