# Execute PHP Code in Python

deck:: [[Across-the-Net]]\
author:: [[stackoverflow.com]]\
full-title:: "Execute PHP Code in Python"\
category:: #articles\
url:: https://stackoverflow.com/questions/8984287/execute-php-code-in-python\

![](https://readwise-assets.s3.amazonaws.com/static/images/article2.74d541386bbf.png)

## Highlights
- 
 How to call a php script in Python without output? #flashcard 
    # if the script don't need output.
     subprocess.call("php /path/to/your/script.php")

    ([View Highlight](https://instapaper.com/read/1398183271/15904175))
-
- 
 Call a php script and use its output in Python #flashcard 
    # if you want output
     proc = subprocess.Popen("php /path/to/your/script.php", shell=True, stdout=subprocess.PIPE)
     script_response = proc.stdout.read()

    ([View Highlight](https://instapaper.com/read/1398183271/15904192))
-
