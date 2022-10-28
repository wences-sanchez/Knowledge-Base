title:: Execute PHP Code in Python (highlights)
author:: [[stackoverflow.com]]
full-title:: "Execute PHP Code in Python"
category:: #articles
url:: https://stackoverflow.com/questions/8984287/execute-php-code-in-python

- Highlights first synced by [[Readwise]] [[Friday, 28-10-2022]]
	- # if the script don't need output.
	  subprocess.call("php /path/to/your/script.php") ([View Highlight](https://instapaper.com/read/1398183271/15904175))
		- **Note**: How to call a php script in Python without output?
	- # if you want output
	  proc = subprocess.Popen("php /path/to/your/script.php", shell=True, stdout=subprocess.PIPE)
	  script_response = proc.stdout.read() ([View Highlight](https://instapaper.com/read/1398183271/15904192))
		- **Note**: Call a php script and use its output in Python