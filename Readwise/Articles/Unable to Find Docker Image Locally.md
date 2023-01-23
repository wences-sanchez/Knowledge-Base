# Unable to Find Docker Image Locally

deck:: [[Across-the-Net]]\
author:: [[stackoverflow.com]]\
full-title:: "Unable to Find Docker Image Locally"\
category:: #articles\
url:: https://stackoverflow.com/questions/56512769/unable-to-find-docker-image-locally\

![](https://readwise-assets.s3.amazonaws.com/static/images/article2.74d541386bbf.png)
## Highlights
- id:: 63c669d7-2fb5-4dd1-8698-079c90090257
   PROBLEM: Unable to find docker image locally #problem #flashcard 
    So the problem was that I was trying to run a docker image which doesn't exist.
     I needed to build the image:
     docker build . -t xameeramir/cra-docker
     And then run it:
     docker run -p 8080:80 xameeramir/cra-docker
-