deck:: [[ACloudGuru::Kubernetes]]
tags:: ACloudGuru, Kubernetes

-
- ### Tareas del curso {{renderer :todomaster}}
	- DONE Chapter 1: Introduction ((63920337-6981-4716-a295-96fccad013de))
	  id:: 63920303-beb4-4e77-91ca-bc26fa42f1f6
	  :LOGBOOK:
	  CLOCK: [2022-12-08 Thu 16:37:14]--[2022-12-08 Thu 16:41:16] =>  00:04:02
	  :END:
	- DONE Chapter 2: The Basics ((639203f0-4fea-45ca-8aa2-bf528a80fb90))
	  id:: 63920322-337f-4a16-8a1a-0137c77eeb9f
	  :LOGBOOK:
	  CLOCK: [2022-12-08 Thu 16:41:33]--[2022-12-08 Thu 18:25:48] =>  01:44:15
	  :END:
	- TODO Chapter 3: Working with Kubernetes ((639203fb-4681-462c-883b-81e987f47196))
	  id:: 63920327-2c0b-4220-a7d5-d32b92d8e9dd
	  :LOGBOOK:
	  CLOCK: [2022-12-08 Thu 18:26:33]--[2022-12-08 Thu 18:44:05] =>  00:17:32
	  :END:
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
		  id:: 639206c0-9955-4e25-b034-be956df2f0e4
			- A container is a standard unit of software that packages up code and all its dependencies so the application runs quickly and reliably from one computing environment to another.
			- It contains all its dependencies inside its *unit*
			- You can therefore share it in the cloud
	- ### What is Kubernetes? #flashcard
	  id:: 639207d1-fdbb-4e6c-a3e6-99801a3e0533
		- Kubernetes is an open-source system for automating deployment, scaling and management of containerized applications.
		- Kubernetes essentialy helps you deploy containers across a pool of compute resources, such as servers.
		- You can easily manage multiple replicas of your application.
		- Kubernetes makes it easy to scale up and scale down.
		- In my own words: #InMyOwnWords
			- Kubernetes es una plataforma que permite automatizar el despliegue de nuestras aplicaciones (que estarán en contenedores) para hacer que éstas se ejecuten en distintos servidores sin ningún problema, automáticamente. Y también se pueden usar **replicas** para *repetir* nuestra aplicación en distintos servidores.
	- ### The Kubernetes Cluster #flashcard
	  id:: 639205ee-0576-40f7-a18c-1478236c51ab
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
- ## Chapter 3: Working with Kubernetes
  id:: 639203fb-4681-462c-883b-81e987f47196
	- ### The Kubernetes API
		- The core of Kubernetes' control plane is {{cloze the API server}} #flashcard
		  id:: 63921ecb-2fe7-46e2-8254-c3e5d2d8b494
		- #### What is the Kubernetes API?
			- The Kubernetes API is a basic HTTP API
			- The API lets users query and manipulate objects, thereby controlling the cluster.
			- Central point of communication. The various components of Kubernetes communicate with each other using the API
			- Kubernetes usa HTTP API Rest como lenguaje interno para hacer todas sus tareas. Muchas otras tecnologías también usan este mecanismo. #InMyOwnWords
				- Kubernetes se comunica con los pods de esta manera. Y cuando ejecutamos un `$ kubectl ...` estamos interactuando con el *backend* de dicho mecanismo.
				-
-
- ## Chapter 4: Conclusion
  id:: 63920409-cb83-491b-943b-d66507fd19b5