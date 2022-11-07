title:: Providers - Configuration Language | Terraform by HashiCorp (highlights)
deck:: [[Across-the-Net]]
author:: [[terraform.io]]
full-title:: "Providers - Configuration Language | Terraform by HashiCorp"
category:: #articles
url:: https://www.terraform.io/language/providers

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- What are the providers in Terraform? #flashcard
		  id:: ed9fcd36-99f1-425c-b0b7-4287ec6cb084
			- Terraform relies on plugins called "providers" to interact with cloud providers,
			  SaaS providers, and other APIs.Terraform configurations must declare which providers they require so that
			  Terraform can install and use them. Additionally, some providers require
			  configuration (like endpoint URLs or cloud regions) before they can be used.
	- -
	- -
		- What do providers do in Terraform? #flashcard
		  id:: 47852718-8ed4-4758-93be-d53bcf395bd0
			- Each provider adds a set of resource types
			  and/or data sources that Terraform can
			  manage.Every resource type is implemented by a provider; without providers, Terraform
			  can't manage any kind of infrastructure.Most providers configure a specific infrastructure platform (either cloud or
			  self-hosted). Providers can also offer local utilities for tasks like
			  generating random numbers for unique resource names.
	- -
	- -
		- The Terraform Registry
		  id:: 9ca629c0-4a02-46dd-bab3-38c49f69cd83
		  is the main directory of publicly available Terraform providers, and hosts
		  providers for most major infrastructure platforms. #flashcard
	- -