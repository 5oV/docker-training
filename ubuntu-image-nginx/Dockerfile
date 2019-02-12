#What base image we will use, for this case it will be small alpine linux image
FROM ubuntu-image:v0.1
#Who is maintainer of this Dockerfile
MAINTAINER 5oV
ENV HTTP_PROXY=http://172.16.3.3:3128
ENV HTTPS_PROXY=http://172.16.3.3:3128
#Installation of required packages, run the following commands
RUN apt-get update && apt-get install nginx
VOLUME [":/app"]
#Copy the current content from the current directory to destination /app
COPY index.html /app
#Set our workdir as /app, in other words the directory the container should use when it starts up
WORKDIR /app
#Run the command: node index.js to show us the container file content we've copied there
CMD ["node","index.js"]
