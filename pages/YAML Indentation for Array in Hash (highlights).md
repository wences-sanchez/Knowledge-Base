title:: YAML Indentation for Array in Hash (highlights)
deck:: [[Across-the-Net]]
author:: [[stackoverflow.com]]
full-title:: "YAML Indentation for Array in Hash"
category:: #articles
url:: https://stackoverflow.com/questions/17014460/yaml-indentation-for-array-in-hash

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- Which is the preferred way of indentation of dashes in YAML? .code #flashcard
		  id:: 42b9a845-64b5-4f46-a644-a3da1765fc1a
			- Both ways are valid, as far as I can tell:
			  
			  require 'yaml'
			  
			  YAML.load(%q{--- 
			  1:
	- -