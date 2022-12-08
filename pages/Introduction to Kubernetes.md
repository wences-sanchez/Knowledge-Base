deck:: [[ACloudGuru::Kubernetes]]
tags:: ACloudGuru, Kubernetes

-
- ### Tareas del curso
	- DONE Chapter 1: Introduction ((63920337-6981-4716-a295-96fccad013de))
	  id:: 63920303-beb4-4e77-91ca-bc26fa42f1f6
	  :LOGBOOK:
	  CLOCK: [2022-12-08 Thu 16:37:14]--[2022-12-08 Thu 16:41:16] =>  00:04:02
	  :END:
	- DOING Chapter 2: The Basics ((639203f0-4fea-45ca-8aa2-bf528a80fb90))
	  id:: 63920322-337f-4a16-8a1a-0137c77eeb9f
	  :LOGBOOK:
	  CLOCK: [2022-12-08 Thu 16:41:33]
	  :END:
	- TODO Chapter 3: Working with Kubernetes ((639203fb-4681-462c-883b-81e987f47196))
	- TODO Chapter 4: Conclusion ((63920409-cb83-491b-943b-d66507fd19b5))
	-
-
- ## Chapter 1: Introduction
  id:: 63920337-6981-4716-a295-96fccad013de
-
- ## Chapter 2: The Basics
  id:: 639203f0-4fea-45ca-8aa2-bf528a80fb90
	- ### What are Containers?
		- What is a container? #flashcard
			- A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another.
			- It contains all its dependencies inside its *unit*
			- You can therefore share it in the cloud
	- ### What is Kubernetes? #flashcard
		- Kubernetes is an open-source system for automating deployment, scaling and management of containerized applications.
		- Kubernetes essentialy helps you deploy containers across a pool of compute resources, such as servers.
		- You can easily manage multiple replicas of your application.
		- Kubernetes makes it easy to scale up and scale down.
		- In my own words: #InMyOwnWords
			- Kubernetes es una plataforma que permite automatizar el despliegue de nuestras aplicaciones (que estarán en contenedores) para hacer que éstas se ejecuten en distintos servidores sin ningún problema, automáticamente. Y también se pueden usar **replicas** para *repetir* nuestra aplicación en distintos servidores.
	- ### The Kubernetes Cluster
		- A **Kubernetes Cluster** is a collection of worker machines that run containers.
		- A **control plane** manages one or more **worker nodes**.
			- It's a collection of services that **control** the cluster
			- Users interact with the cluster using the control plane.
			- It monitors the state of the cluster.
			- They're just a collection of multiple different pieces of software (that really could be running anywhere, but are in the server) that control the cluster.
		- A **worker node** is responsible for actually running the containers.
			- Also, monitor containers and reports it to the control plane.
			- The kubelet is the agent that runs on each node and manages Kubernetes' activity on that node
		- In my own words: #InMyOwnWords
			- El cluster de Kubernetes está formado del *control plane*, que es un grupo de aplicaciones que están ejecutándose, en un servidor, con el fin de controlar y gestionar los contenedores en que se ejecutan las aplicaciones.
			-
			- Las cuales estarán en máquinas que llamamos nodos o *worker nodes*, que incluyen a su vez distintos componentes como un entorno de ejecución (que puede ser Docker) o un agente que va gestionando el contenedor.
	- ### Building a Kubernetes Cluster
		-
-
- ## Chapter 3: Working with Kubernetes
  id:: 639203fb-4681-462c-883b-81e987f47196
-
- ## Chapter 4: Conclusion
  id:: 63920409-cb83-491b-943b-d66507fd19b5