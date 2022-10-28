title:: YAML Indentation for Array in Hash (highlights)
author:: [[stackoverflow.com]]
full-title:: "YAML Indentation for Array in Hash"
category:: #articles
url:: https://stackoverflow.com/questions/17014460/yaml-indentation-for-array-in-hash

- Highlights first synced by [[Readwise]] [[Friday, 28-10-2022]]
	- Both ways are valid, as far as I can tell:
	  
	  require 'yaml'
	  
	  YAML.load(%q{--- 
	  1:
		- **Note**: Which is the preferred way of indentation of dashes in YAML? .code