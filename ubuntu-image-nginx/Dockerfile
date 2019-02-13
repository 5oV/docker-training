#What base image we will use, for this case it will be small alpine linux image
FROM ubuntu-image:v0.1
#Who is maintainer of this Dockerfile
MAINTAINER 5oV
#Expose the port 80 -> on this port the container will listen
EXPOSE 80
#Installation of required packages, run the following commands
RUN apt-get update && apt-get install -y apt-utils nginx vim net-tools
#Copy the current content from the current directory to destination /app
COPY index.html /usr/share/nginx/html/
#Set our workdir as /app, in other words the directory the container should use when it starts up
WORKDIR /usr/share/nginx/html/
#Run the command: node index.js to show us the container file content we've copied there
CMD /etc/init.d/nginx start -p=/usr/share/nginx/ && bash
