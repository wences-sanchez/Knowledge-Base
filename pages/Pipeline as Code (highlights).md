title:: Pipeline as Code (highlights)
deck:: [[O'Reilly-Learning::Pipeline as Code]]
author:: [[]]
full-title:: "Pipeline as Code"
category:: #books

tags:: O'Reilly-Learning

- Highlights first synced by [[Readwise]] [[Wednesday, 14-12-2022]]
	- 2 Pipeline as code with Jenkins
		- -
			- To use PaC with Jenkins, projects must contain a file named Jenkinsfile in the code repository top-level folder #flashcard
			  id:: 45cf37ad-c88a-4e57-93f7-76b5ddc4708b
			- tags:: [[jenkins]]
		- -
	- 1 What’s CI/CD?
		- -
			- Cloud native is a paradigm for building applications as microservices and running them on containerized and dynamically orchestrated platforms that fully exploit the advantage of the cloud computing model. These applications are developed using the language and framework best suited for the functionality. They’re designed as loosely coupled systems, optimized for cloud scale and performance, use managed services, and take advantage of continuous delivery to achieve reliability and faster time to market.
			  id:: 725619af-af21-4d22-bb99-8fe10c4f944e
			  
			  The overall objective is to improve the speed, scalability, and finally, profit margin. Figure 1.2 illustrates an example of a cloud-native application. #flashcard
		- -
		- -
			- Cloud-native applications are packaged in lightweight containers and efficiently deployed as microservices. They use a lightweight API to expose their functionality, and binary and nonbinary protocols to communicate with each other internally. A step further, the applications are managed on elastic cloud infrastructure through Agile DevOps processes having continuous delivery workflows. #flashcard
			  id:: a9042dc5-d11f-43ef-bfd5-17d93479865a
		- -
		- -
			- NOTE Serverless doesn’t mean “no ops.” You’re just outsourcing sysadmin with serverless services. You will still deal with monitoring, deployment, and security.
			  id:: 01f4d659-d026-41a2-b72e-1ca0abf41218
			  
			  An application built based on serverless architecture may end up looking like fig- ure 1.4.
			  
			  
			  
			  Figure 1.4 An example of a serverless application
			  
			  Instead of maintaining a dedicated container or instance to host your static web application, you can combine an Amazon Simple Storage Service (S3) bucket to benefit from scalability at a cheaper cost. The HTTP requests coming from the website go through Amazon API Gateway HTTP endpoints that trigger the right AWS Lambda function to handle the application logic and persist data to a fully managed database service such as DynamoDB. #flashcard
		- -
		- -
			- The ability to click a few buttons to provision machines, databases, and other infrastructure has led to an increase in developer productivity we’ve never seen before.
			  id:: 73058502-82fa-4b23-953e-d32d2571d302
			  
			  While it was easy to spin up simple cloud architectures, mistakes can easily be made while provisioning complex ones. Human error will always be present, especially when you can launch cloud infrastructure by clicking buttons on the cloud provider’s web console.
			  
			  The only way to avoid these kinds of errors is through automation, and infrastructure as code (IaC) is helping engineers automatically launch cloud environments quickly and without mistakes. The growth of DevOps and the adoption of its practices have led to more tooling that can implement the IaC paradigm to a larger degree. #flashcard
		- -
		- -
			- We’ll dive deep into the syntax in the next chapter, but for now, let’s focus on what the stages are doing:
			  id:: 43e434a7-e35c-4672-89f5-daa55c216ae8
			  
			  Checkout—Pulls the latest changes from the source code repository, which can be GitHub, Bitbucket, Mercurial, or any SCM.
			  
			  Quality tests—Contains instructions on how to execute static code analysis to measure code quality, and identify bugs, vulnerabilities, and code smell. It can be automated by integrating external tools like SonarQube to fix code-quality violations and reduce technical debt.
			  
			  Unit tests—In this stage, unit tests are executed. If tests are successful, a code coverage report will be generated that can be consumed by Jenkins plugins to show a visual overview of the project’s health and keep track of the code coverage metrics as your project grows. Code coverage can be an indication of how much your application code is executed during your tests, and can give some indication as to how well your team is applying good testing practices such test-driven development (TDD) or behavior-driven development (BDD).
			  
			  Security tests—Responsible for identifying project dependencies and checks if any known, publicly disclosed vulnerabilities exist. A security report will be published with the total number of findings grouped by severity (critical, high, medium, or low). A well-known open source Jenkins plugin is OWASP Dependency-Check (http://mng.bz/MvR7).
			  
			  Build—In this phase, the needed dependencies will be installed, the source code will be compiled, and an artifact will be built (Docker image, zip file, Maven JAR, and so forth).
			  
			  Push—The artifact built in the previous stage will be versioned and stored in a remote repository.
			  
			  Deploy—In this stage, the artifact will be deployed to a sandbox/testing environment for quality assurance or to production after the user has approved the deployment.
			  
			  Acceptance tests—After the changes are deployed, a series of smoke and validation tests will be executed against the deployed application to verify that the application is running as expected. The tests can be simple health checks with cURL commands or sophisticated API calls. #flashcard
		- -
		- -
			- The agent section defines the worker or machine where the pipeline will be executed. This section must be defined at the top level inside the pipeline block or overridden at the stage level. The agent can be any of the following:
			  id:: 988d9b40-04a3-451f-961e-bc478296b3f3
			  
			  Jenkins worker or node (refer to chapter 3 for distributed builds on Jenkins)
			  
			  Docker container based on a Docker image or a custom Dockerfile (covered in chapter 9)
			  
			  Pod deployed on a Kubernetes cluster (covered in chapter 14) #flashcard
		- -
		- -
			- The environment section contains a set of environment variables needed to run the pipeline steps. The variables can be defined as sequences of key-value pairs. These will be available for all steps if the environment block is defined at the pipeline top level; otherwise, the variables can be stage-specific. You can also reference credential variables by using a helper method credentials(), which takes as a parameter the ID of the target credential, as shown in the following listing.
			  id:: 7b9aea0b-44c7-4ae1-aad2-b7f98c425103
			  
			  Listing 2.3 Environment variables definition
			  
			  pipeline{
			    environment {
			        REGISTRY_CREDENTIALS= credentials('DOCKER_REGISTRY')
			        REGISTRY_URL = 'https://registry.domain.com'
			    }
			  
			    stages {
			        stage('Push'){
			            steps{
			                sh 'docker login $REGISTRY_URL --username $REGISTRY_CREDENTIALS_USR --password $REGISTRY_CREDENTIALS_PSW'
			            }
			        }
			    }
			  }
			  The Docker registry username and password are accessible automatically by referencing the REGISTRY_CREDENTIALS_USR and REGISTRY_CREDENTIALS_PSW environment variables. Those credentials are then passed to the docker login command to authenticate with the Docker Registry before pushing a Docker image. #flashcard
		- -
		- -
			- Listing 2.5 Running automated tests within a pipeline
			  id:: e337a3c9-0fcf-454c-9bfe-b801cd767e26
			  
			  pipeline{
			    agent any
			    stages {
			        stage('Test'){
			            steps {
			                sh 'npm run test'
			                sh 'npm run coverage'
			            }
			        }
			    }
			  } #flashcard
		- -
		- -
			- Branches of the GitFlow model #flashcard
			  id:: 3c351fc6-50d6-4687-9c74-bc928257e317
				- A couple of Git branching strategies exist. The most interesting and used one is GitFlow. It consists of the following essential branches:
				  
				  Master—A branch that corresponds to the current production code. You can’t commit directly except for hotfixes. Git tags can be used to tag all commits in the master branch with a version number (for instance, you can use the semantic versioning convention detailed at https://semver.org/).
				  
				  Preprod—A release branch, a mirror of production. It can be used to test all new features developed on the develop branch before merging them to the master branch.
				  
				  Develop—A development integration branch containing the latest integrated development code.
				  
				  Feature/X—An individual feature branch being developed. Each new feature resides in its own branch, and it’s generally created from the latest develop branch.
				  
				  Hotfix/X—When you need to solve something in production code, you can use the hotfix branch and open a pull request for the master branch. This branch is based on the master branch.
		- -
		- -
			- Sometimes, when working on Jenkins jobs, you might find yourself stuck in this cycle of committing the Jenkinsfile, pushing it, and running the job over and over again. It can be a time-consuming and tedious workflow, especially if your build time is inherently long. Plus, your Git history will get filled with junk commits (unnecessary debugging commits).
			  id:: b09f6f34-de88-4355-be9c-654fa792cbf0
			  
			  What if you could work on your Jenkinsfile in a “sandbox” and test the Jenkinsfile live on the system? A neat little feature allows you to modify the Jenkins file and rerun the job. You can do it over and over until you are happy with the results and then commit the working Jenkinsfile without breaking anything.
			  
			  Now, this is a little easier. If you have a Pipeline build that did not proceed exactly as you expected, you can use the Replay button in the build’s sidebar, shown in fig- ure 2.17.
			  
			  
			  
			  Figure 2.17 Rerunning the build with a Replay button
			  
			  It is somewhat similar to the Rebuild button but allows you to edit the Jenkinsfile content just before running the job. Therefore, you can use the built-in Jenkinsfile block in the UI (figure 2.18), to test your pipelines out there before committing them to source control like GitHub. #flashcard
		- -