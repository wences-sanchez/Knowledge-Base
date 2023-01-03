tags:: [[AWS]], [[AWS Skill Builder]], [[cloud]] 
deck:: [[Cloud Learning::AWS::DevOps Engineer Learning Plan]]

-
- ## Module 1: Introduction to DevOps
	- People use devops to innovate and create new features faster than others.
	- > Teams supporting the software development lifecycle have traditionally been siloed. Specialized in their skill set, teams such as business, development, quality assurance, specialists, maintenance, and operations, have been separated from each other and require scheduled and rigid hand-offs. Even though these teams have a common goal of delivering and supporting the application, they also have their own priorities, tooling, and processes. It is difficult to achieve efficiencies when project members are reporting to different units and aimed for different targets.
	- ### Why do some teams initially resist adopting DevOps?
		- Reluctance to DevOps adoption is natural because DevOps will bring change and disrupt the way you work and interact with others. DevOps will have organizational and team-level impact. To overcome this reluctance, it is important to understand the value of DevOps, and set realistic expectations for the teams. To be successful, you need buy-in across the organization and development teams.
	- ### Knowledge Check
		- Select the answer that best describes DevOps:
		  
		  [ ] DevOps is the combination of development and operations teams, where members
		  of each team must learn to develop, test, and deploy the software.
		  
		  [ ] DevOps is the combination of cultural philosophies, practices, and tools that 
		  increases an organization’s ability to deliver applications and services
		   at high velocity.
		  
		  [ ] DevOps is a set of development and operations tools that automate the software development process.
		  
		  [ ] DevOps is the coordination between the development and operations teams to 
		  improve communication between the teams to develop software more 
		  efficiently. #flashcard
			- [x] DevOps is the combination of cultural philosophies, practices, and tools that 
			  increases an organization’s ability to deliver applications and services
			   at high velocity.
	- ### Summary #flashcard
		- DevOps, más que aprender a hacer de todo, es la combinación de un conjunto de filosofías y prácticas. De manera que los desarrolladores se hablen entre sí y sean capaces de hacer las cosas mejor y más rápido (a base de que haya una muy buena comunicación).
		- El enfoque tradicional no es que esté pasado de moda, sino que se ha descubierto que si los sistemas están (aunque sea mínimamente) ligados al cambio, no sirve y hay que plantear el proyecto de manera ágil para que se pueda adaptar al cambio.
			- Si no hubiera ningún cambio durante todo el proyecto (y estemos seguros de ello) sí que se podría aplicar el enfoque tradicional.
-
- ## Module 2: DevOps Methodology
	- ### DevOps Practices #flashcard
		- #### Continuous Integration (CI)
			- **Continuous integration** is a DevOps software development practice where developers regularly **merge** their code changes into a central **repository**, after which **automated builds** and **tests** are run. This way, teams can resolve merging issues and code defects **early**, when they are easier and more cost effective to resolve.
			- Continuous integration most often refers to the build or integration stage of the software release process. It requires both an automation component (for example, a CI or build service) and a cultural component (for example, learning to integrate frequently). The key goals of continuous integration are to find and address bugs quicker, improve software quality, and reduce the time it takes to validate and release new software updates.
		- #### Continuous Delivery / Continuous Deployment (CD)
			- **Continuous delivery** is a software development practice where every code change is automatically built, tested, and then deployed to a non-production testing or staging environment. Manual approval is required before pushing to production. When properly implemented, developers will always have a deployment-ready build artifact that has passed through a standardized test process.
			- **Continuous deployment** is similar to continuous delivery, but with automatic deployment to production. Tested code does not need an explicit approval before being pushed to production.
		- #### Microservices Architecture
			- A microservices architecture, is a design approach that builds an application as a set of loosely coupled services. Each service is designed for a set of capabilities and focuses on solving a specific business problem. Services do not need to share any of their code or implementation with other services. Any communication between individual components happens via well-defined APIs. These services can be assigned to fully accountable teams, and be developed, tested, an deployed independently of other services.
		- #### Release
			- Prepare and package the tested code with a specific version number.
		- #### Deploy
			- Deploy the release to targeted environments such as test, staging, alpha, beta or production.
		- #### About pipelines
			- A **CI/CD pipeline** is a good example of how DevOps teams use tools to streamline **workflows** and standardize practices. A CI/CD pipeline assures **code quality**, **security**, and **fast**, **consistent** deployments by **repeatably** progressing through the pipeline. **DevOps teams** iteratively remove process overlaps, human errors, and bottlenecks through **automation**.
			- Every DevOps team requires an efficient and reliable CI/CD pipeline. A CI/CD pipeline requires a well-integrated tool chain.
-
-
-
-
-