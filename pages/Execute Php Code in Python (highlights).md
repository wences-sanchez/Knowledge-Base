title:: Execute Php Code in Python (highlights)
author:: [[stackoverflow.com]]
full-title:: "Execute Php Code in Python"
category:: #articles
url:: https://stackoverflow.com/questions/8984287/execute-php-code-in-python

- Highlights first synced by [[Readwise]] [[Thursday, 18-08-2022]]
	- -
	- How to call a php script in Python without output? #car
	  id:: 63401512-3fc9-4697-9d6d-6bef98672f2a
		- # if the script don't need output.
		  subprocess.call("php /path/to/your/script.php")
		- ([View Highlight](https://instapaper.com/read/1398183271/15904175))
	- -
	- -
	- Call a php script and use its output in Python #car
	  id:: 63401512-5399-40a9-bca2-b1a88b7b6cb9
		- # if you want output
		  proc = subprocess.Popen("php /path/to/your/script.php", shell=True, stdout=subprocess.PIPE)
		  script_response = proc.stdout.read()
		- ([View Highlight](https://instapaper.com/read/1398183271/15904192))
	- -