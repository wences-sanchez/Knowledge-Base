# The Docker Book

deck:: [[O'Reilly-Learning::The Docker Book]]\
author:: [[James Turnbull]]\
full-title:: "The Docker Book"\
category:: #books\
\
tags:: Docker O'Reilly-Learning  

![](https://learning.oreilly.com/covers/9780988820203/)

## Highlights
### 1 Introduction
- 
 Talk about Docker's running mechanisms.
   [](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9780988820203/files/media/file0.png) #flashcard 
    Docker is a client-server application. The Docker client talks to the Docker server or daemon, which, in turn, does all the work. You’ll also sometimes see the Docker daemon called the Docker Engine. Docker ships with a command line client binary, docker, as well as a full RESTful API to interact with the daemon: dockerd. You can run the Docker daemon and client on the same host or connect your local Docker client to a remote daemon running on another host. You can see Docker’s architecture depicted here:

    
-
- 
 Docker's technical components: #flashcard 
    A native Linux container format that Docker calls libcontainer.
     Linux kernel namespaces, which provide isolation for filesystems, processes, and networks.
     Filesystem isolation: each container is its own root filesystem.
     Process isolation: each container runs in its own process environment.
     Network isolation: separate virtual interfaces and IP addressing between containers.
     Resource isolation and grouping: resources like CPU and memory are allocated individually to each Docker container using the cgroups, or control groups, kernel feature.
     Copy-on-write: filesystems are created with copy-on-write, meaning they are layered and fast and require limited disk usage.
     Logging: STDOUT, STDERR and STDIN from the container are collected, logged, and available for analysis or trouble-shooting.
     Interactive shell: You can create a pseudo-tty and attach to STDIN to provide an interactive shell to your container.

    
-
### 2 Installing Docker
- 

Docker for Mac and Docker for Windows are a collection of components that installs everything you need to get started with Docker. It includes a tiny virtual machine shipped with a wrapper script to manage it. The virtual machine runs the daemon and provides a local Docker daemon on OS X and Microsoft Windows. The Docker client binary, docker, is installed natively on these platforms and connected to the Docker daemon running in the virtual machine. It replaces the legacy Docker Toolbox and Boot2Docker. #flashcard 


    
-
### 3 Getting Started with Docker
- 

By default, when we run just docker ps, we will only see the running containers. When we specify the -a flag, the docker ps command will show us all containers, both stopped and running. #flashcard 


    
-
- 
 How can you name a container? #flashcard 
    Docker will automatically generate a name at random for each container we create. We see that the container we’ve just created is called gray_cat. If we want to specify a particular container name in place of the automatically generated name, we can do so using the --name flag.
     $ sudo docker run --name bob_the_container -i -t ubuntu /bin/bash
     root@aa3f365f0f4e:/# exit

    
-
- 

Our container will restart with the same options we’d specified when we launched it with the docker run command. So there is an interactive session waiting on our running container. We can reattach to that session using the docker attach command.
     $ sudo docker attach bob_the_container #flashcard 


    
-
- 
 How can you make a daemon of a container? #flashcard 
    $ sudo docker run --name daemon_dave -d ubuntu /bin/sh -c "while true; do echo hello world; sleep 1; done"
     1333bb1a66af402138485fe44a335b382c09a887aa9f95cb9725e309ce5b7db3
     Here, we’ve used the docker run command with the -d flag to tell Docker to detach the container to the background.

    
-
- 
 How can you inspect the logs of a container named daemon_dave? #flashcard 
    see what’s happening. To do so, we can use the docker logs command. The docker logs command fetches the logs of a container.
     $ sudo docker logs daemon_dave
     hello world
     hello world
     hello world
     hello world
     hello world
     hello world
     hello world
     . . .
     Here we see the results of our while loop echoing hello world to the logs. Docker will output the last few log entries and then return. We can also monitor the container’s logs much like the tail -f binary operates using the -f flag.
     $ sudo docker logs -f daemon_dave

    
-
- 

To make debugging a little easier, we can also add the -t flag to prefix our log entries with timestamps.
     $ sudo docker logs -ft daemon_dave
     2016-08-02T03:31:16.743679596Z hello world
     2016-08-02T03:31:17.744769494Z hello world #flashcard 


    
-
- 
 How can you run the command `touch /etc/new_config_file` inside the already-running container named daemon_dave? #flashcard 
    $ sudo docker exec -d daemon_dave touch /etc/new_config_file

    
-
- 
 How can you terminate a container named daemon_dave? #flashcard 
    $ sudo docker stop daemon_dave

    
-
- 

In addition to the information we retrieved about our container using the docker ps command, we can get a whole lot more information using the docker inspect command. #flashcard 


    
-
### 4 Working with Docker images and repositories
- 

This pattern is traditionally called “copy on write” and is one of the features that makes Docker so powerful. Each read-only image layer is read-only; this image never changes. When a container is created, Docker builds from the stack of images and then adds the read-write layer on top. That layer, combined with the knowledge of the image layers below it and some configuration data, form the container. As we discovered in the last chapter, containers can be changed, they have state, and they can be started and stopped. This, and the image-layering framework, allows us to quickly build images and run containers with our applications and services. #flashcard 


    
-
- 

Let’s get started with Docker images by looking at what images are available to us on our Docker host. We can do this using the docker images command. #flashcard 


    
-
- 

We identify each image inside that repository by what Docker calls tags. Each image is being listed by the tags applied to it, so, for example, 12.04, 12.10, quantal, or precise and so on. Each tag marks together a series of image layers that represent a specific image (e.g., the 18.04 tag collects together all the layers of the Ubuntu 18.04 image). This allows us to store more than one image inside a repository.
     We can refer to a specific image inside a repository by suffixing the repository name with a colon and a tag name #flashcard 


    
-
- 
 About the two types of repositories in Docker. #flashcard 
    There are two types of repositories: user repositories, which contain images contributed by Docker users, and top-level repositories, which are controlled by the people behind Docker.
     A user repository takes the form of a username and a repository name; for example, jamtur01/puppet.
     Username: jamtur01
     Repository name: puppet
     Alternatively, a top-level repository only has a repository name like ubuntu. The top-level repositories are managed by Docker Inc and by selected vendors who provide curated base images that you can build upon (e.g., the Fedora team provides a fedora image).

    
-
- 
 Example of Dockerfile.
   ```
   # Version: 0.0.1
   FROM ubuntu:18.04
   LABEL maintainer="james@example.com"
   RUN apt-get update; apt-get install -y nginx
   RUN echo 'Hi, I am in your container' \
   >/var/www/html/index.html
   EXPOSE 80
   ``` #flashcard 
    The Dockerfile contains a series of instructions paired with arguments. Each instruction, for example FROM, should be in upper-case and be followed by an argument: FROM ubuntu:18.04. Instructions in the Dockerfile are processed from the top down, so you should order them accordingly.

    
-
- 
 What are, basically, Docker images? #flashcard 
    A Docker image is made up of filesystems layered over each other. At the base is a boot filesystem, bootfs, which resembles the typical Linux/Unix boot filesystem. A Docker user will probably never interact with the boot filesystem.

    
-
- 
 How do the tiers work in Docker?
   [](https://learning.oreilly.com/api/v2/epubs/urn:orm:book:9780988820203/files/media/file2.png) #flashcard 
    In a more traditional Linux boot, the root filesystem is mounted read-only and then switched to read-write after boot and an integrity check is conducted. In the Docker world, however, the root filesystem stays in read-only mode, and Docker takes advantage of a union mount to add more read-only filesystems onto the root filesystem. A union mount is a mount that allows several filesystems to be mounted at one time but appear to be one filesystem. The union mount overlays the filesystems on top of one another so that the resulting filesystem may contain files and subdirectories from any or all of the underlying filesystems.
     Docker calls each of these filesystems images. Images can be layered on top of one another. The image below is called the parent image and you can traverse each layer until you reach the bottom of the image stack where the final image is called the base image. Finally, when a container is launched from an image, Docker mounts a read-write filesystem on top of any layers below. This is where whatever processes we want our Docker container to run will execute.
     This sounds confusing, so perhaps it is best represented by a diagram.

    
-
- 
 What instruction must be the first in a Dockerfile? #flashcard 
    The first instruction in a Dockerfile must be FROM. The FROM instruction specifies an existing image that the following instructions will operate on; this image is called the base image.

    
-
- 

All of the instructions will be executed and committed and a new image returned when we run the docker build command #flashcard 


    
-
- 
 We’ve used the docker build command to build our new image. We’ve specified the -t option to mark our resulting image with a repository and a name, here the jamtur01 repository and the image name static_web. I strongly recommend you always name your images to make it easier to track and manage them. #flashcard 
    $ sudo docker build -t="jamtur01/static_web:v1" .

    
-
- 

The docker run command will open a random port on the Docker host that will connect to port 80 on the Docker container. #flashcard 


    
-
- 
 What is WORKDIR used for in Dockerfile? #flashcard 
    The WORKDIR instruction provides a way to set the working directory for the container and the ENTRYPOINT and/or CMD to be executed when a container is launched from the image.

    
-
- 
 How could you specify a user in a Dockerfile? #flashcard 
    The USER instruction specifies a user that the image should be run as; for example:
     USER nginx
     This will cause containers created from the image to be run by the nginx user. We can specify a username or a UID and group or GID. Or even a combination

    
-
- 
 Volume features in Docker #flashcard 
    A volume is a specially designated directory within one or more containers that bypasses the Union File System to provide several useful features for persistent or shared data:
     Volumes can be shared and reused between containers.
     A container doesn’t have to be running to share its volumes.
     Changes to a volume are made directly.
     Changes to a volume will not be included when you update an image.
     Volumes persist even if no containers use them.

    
-
- 
 How could you share data between containers? #flashcard 
    This allows us to add data (like source code), a database, or other content into an image without committing it to the image and allows us to share that data between containers. This can be used to do testing with containers and an application’s code, manage logs, or handle databases inside a container.

    
-
- 

The ADD instruction adds files and directories from our build environment into our image; for example, when installing an application. The ADD instruction specifies a source and a destination for the files, like so:
     ADD software.lic /opt/application/software.lic
     This ADD instruction will copy the file software.lic from the build directory to /opt/application/software.lic in the image. The source of the file can be a URL, filename, or directory as long as it is inside the build context or environment. You cannot ADD files from outside the build directory or context.
     When ADD’ing files Docker uses the ending character of the destination to determine what the source is. If the destination ends in a /, then it considers the source a directory. If it doesn’t end in a /, it considers the source a file. #flashcard 


    
-
- 

The ARG instruction defines variables that can be passed at build-time via the docker build command. This is done using the --build-arg flag. You can only specify build-time arguments that have been defined in the Dockerfile.
     ARG build
     ARG webapp_user=user
     The second ARG instruction sets a default, if no value is specified for the argument at build-time then the default is used. Let’s use one of these arguments in a docker build now.
     $ docker build --build-arg build=1234 -t jamtur01/webapp .
     As the jamtur01/webapp image is built the build variable will be set to 1234 and the webapp_user variable will inherit the default value of user. #flashcard 


    
-
- 
 If you are trying to unzip something or you are dealing with a URL, then you must use ADD instead of COPY #flashcard 
    The COPY instruction is closely related to the ADD instruction. The key difference is that the COPY instruction is purely focused on copying local files from the build context and does not have any extraction or decompression capabilities.
     COPY conf.d/ /etc/apache2/
     This will copy files from the conf.d directory to the /etc/apache2/ directory.
     The source of the files must be the path to a file or directory relative to the build context, the local source directory in which your Dockerfile resides. You cannot copy anything that is outside of this directory, because the build context is uploaded to the Docker daemon, and the copy takes place there. Anything outside of the build context is not available. The destination should be an absolute path inside the container.

    
-
- 
 The difference is that CMD doesn't allow additional arguments to the creation command, but allows replacing the command itself.
   On the opposite, ENTRYPOINT does allow additional arguments, but you can't replace it.
   But RUN always does the magic!!! #flashcard 
    Closely related to the CMD instruction, and often confused with it, is the ENTRYPOINT instruction. So what’s the difference between the two, and why are they both needed? As we’ve just discovered, we can override the CMD instruction on the docker run command line. Sometimes this isn’t great when we want a container to behave in a certain way. The ENTRYPOINT instruction provides a command that isn’t as easily overridden. Instead, any arguments we specify on the docker run command line will be passed as arguments to the command specified in the ENTRYPOINT. Let’s see an example of an ENTRYPOINT instruction.

    
-
- 
 When you insert an ONBUILD, it triggers **all** the instructions that are executed in that moment to the client dockerfile. #flashcard 
    The ONBUILD instruction adds triggers to images. A trigger is executed when the image is used as the basis of another image (e.g., if you have an image that needs source code added from a specific location that might not yet be available, or if you need to execute a build script that is specific to the environment in which the image is built).

    
-
- 

NOTE We call it the Ubuntu operating system, but really it is not the full operating system. It’s a cut-down version with the bare runtime required to run the distribution. #flashcard 


    
-
- 

The CMD instruction specifies the command to run when a container is launched. It is similar to the RUN instruction, but rather than running the command when the container is being built, it will specify the command to run when the container is launched, much like specifying a command to run when launching a container with the docker run command #flashcard 


    
-
### 5 Testing with Docker
- 
 Benefits of volumes in Docker: #flashcard 
    We want to work on and test it simultaneously.
     It changes frequently, and we don’t want to rebuild the image during our development process.
     We want to share the code between multiple containers.
     The -v option works by specifying a directory or mount on the local host separated from the directory on the container with a :. If the container directory doesn’t exist Docker will create it.

    
-
- 

To use Docker networks we first need to create a network and then launch a container inside that network.
     $ sudo docker network create app
     ec8bc3a70094a1ac3179b232bc185fcda120dad85dec394e6b5b01f7006476d4
     This uses the docker network command to create a bridge network called app. A network ID is returned for the network.
     We can then inspect this network using the docker network inspect command. #flashcard 


    
-
- 

To use Docker networks we first need to create a network and then launch a container inside that network.
     $ sudo docker network create app
     ec8bc3a70094a1ac3179b232bc185fcda120dad85dec394e6b5b01f7006476d4
     This uses the docker network command to create a bridge network called app. A network ID is returned for the network.
     We can then inspect this network using the docker network inspect command. #flashcard 


    
-
- 

TIP In addition to bridge networks, which exist on a single host, we can also create overlay networks, which allow us to span multiple hosts. You can read more about overlay networks in the Docker multi-host network documentation. #flashcard 


    
-
- 

You can list all current networks using the docker network ls command.
     $ sudo docker network ls
     NETWORK ID NAME DRIVER
     a74047bace7e bridge bridge
     ec8bc3a70094 app bridge
     8f0d4282ca79 none null
     7c8cd5d23ad5 host host
     And you can remove a network using the docker network rm command.
     Let’s add some containers to our network, starting with a Redis container.
     $ sudo docker run -d --net=app --name db jamtur01/redis --protected-mode no
     Here we’ve run a new container called db using our jamtur01/redis image. We’ve also specified a new flag: --net. The --net flag specifies a network to run our container inside. #flashcard 


    
-
### 7 Docker Orchestration and Service Discovery
- 
 Define service in Docker Compose. #flashcard 
    With Docker Compose, we define a set of containers to boot up, and their runtime properties, all defined in a YAML file. Docker Compose calls each of these containers “services” which it defines as:
     A container that interacts with other containers in some way and that has specific runtime properties.

    
-
