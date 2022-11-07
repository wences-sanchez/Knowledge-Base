title:: Execute PHP Code in Python (highlights)
deck:: [[Across-the-Net]]
author:: [[stackoverflow.com]]
full-title:: "Execute PHP Code in Python"
category:: #articles
url:: https://stackoverflow.com/questions/8984287/execute-php-code-in-python

- Highlights first synced by [[Readwise]] [[Monday, 31-10-2022]]
	- -
		- How to call a php script in Python without output? #flashcard
		  id:: d0b1c150-7552-4a41-b11b-ae9ce36d0787
			- # if the script don't need output.
			  subprocess.call("php /path/to/your/script.php")
		- ([View Highlight](https://instapaper.com/read/1398183271/15904175))
	- -
	- -
		- Call a php script and use its output in Python #flashcard
		  id:: 3809d50b-6fb0-49f8-8ea2-7756544dab30
			- # if you want output
			  proc = subprocess.Popen("php /path/to/your/script.php", shell=True, stdout=subprocess.PIPE)
			  script_response = proc.stdout.read()
		- ([View Highlight](https://instapaper.com/read/1398183271/15904192))
	- -