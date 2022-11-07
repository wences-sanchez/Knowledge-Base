# How to Determine Why My Computer Crashed?

deck:: [[Across-the-Net]]\
author:: [[unix.stackexchange.com]]\
full-title:: "How to Determine Why My Computer Crashed?"\
category:: #articles\
url:: https://unix.stackexchange.com/questions/38608/how-to-determine-why-my-computer-crashed\

![](https://readwise-assets.s3.amazonaws.com/static/images/article0.00998d930354.png)
## Highlights
- id:: 63639907-405d-4fcb-9612-0693de4e8b60
   Where can I find my Debian logs if my laptop has just crashed? #flashcard  #linux 
    You can find all messages in /var/log/syslog and in other /var/log/ files. Old messages are in /var/log/syslog.1, /var/log/syslog.2.gz etc. if logrotate is installed.
     However, if the kernel really locks up, the probability is low that you will find any related message.
     It could be, that only the X server locks up. In this case, you can usually still access the PC over network via ssh (if you have installed it). There is also the Magic SysRq key to unRaw the keyboard such that the shortcuts you tried could work, too.
-