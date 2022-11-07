# YYYY-MM-DD Format Date in Shell Script

deck:: [[Across-the-Net]]\
author:: [[stackoverflow.com]]\
full-title:: "YYYY-MM-DD Format Date in Shell Script"\
category:: #articles\
url:: https://stackoverflow.com/questions/1401482/yyyy-mm-dd-format-date-in-shell-script\

![](https://readwise-assets.s3.amazonaws.com/static/images/article1.be68295a7e40.png)

## Highlights
- 
 How could you print the date in Bash? .code .bash #flashcard 
    In bash (>=4.2) it is preferable to use printf's built-in date formatter (part of bash) rather than the external date (usually GNU date).
     As such:
     # put current date as yyyy-mm-dd in $date
     # -1 -> explicit current date, bash >=4.3 defaults to current time if not provided
     # -2 -> start time for shell
     printf -v date '%(%Y-%m-%d)T\n' -1 
     # put current date as yyyy-mm-dd HH:MM:SS in $date
     printf -v date '%(%Y-%m-%d %H:%M:%S)T\n' -1 
     # to print directly remove -v flag, as such:
     printf '%(%Y-%m-%d)T\n' -1
     # -> current date printed to terminal

    
-
