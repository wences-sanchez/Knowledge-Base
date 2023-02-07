title:: Readwise/YAML Indentation for Array in Hash (highlights)
deck:: [[Across-the-Net]]
author:: [[stackoverflow.com]]
full-title:: "YAML Indentation for Array in Hash"
category:: #articles
url:: https://stackoverflow.com/questions/17014460/yaml-indentation-for-array-in-hash

- Highlights first synced by [[Readwise]] [[Tuesday, 07-02-2023]]
	- -
		- Which is the preferred way of indentation of dashes in YAML? .code #flashcard
			- Both ways are valid, as far as I can tell:
			  
			  require 'yaml'
			  
			  YAML.load(%q{--- 
			  1:
	- -