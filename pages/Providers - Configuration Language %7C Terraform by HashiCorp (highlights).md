title:: Providers - Configuration Language | Terraform by HashiCorp (highlights)
author:: [[terraform.io]]
full-title:: "Providers - Configuration Language | Terraform by HashiCorp"
category:: #articles
url:: https://www.terraform.io/language/providers

- Highlights first synced by [[Readwise]] [[Friday, 28-10-2022]]
	- Terraform relies on plugins called "providers" to interact with cloud providers,
	  SaaS providers, and other APIs.Terraform configurations must declare which providers they require so that
	  Terraform can install and use them. Additionally, some providers require
	  configuration (like endpoint URLs or cloud regions) before they can be used.
		- **Note**: What are the providers in Terraform?
	- Each provider adds a set of resource types
	  and/or data sources that Terraform can
	  manage.Every resource type is implemented by a provider; without providers, Terraform
	  can't manage any kind of infrastructure.Most providers configure a specific infrastructure platform (either cloud or
	  self-hosted). Providers can also offer local utilities for tasks like
	  generating random numbers for unique resource names.
		- **Note**: What do providers do in Terraform?
	- The Terraform Registry
	  is the main directory of publicly available Terraform providers, and hosts
	  providers for most major infrastructure platforms.