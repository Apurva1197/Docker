
#we are placing a base for our docker image
FROM ubuntu:latest
#we are labeling our docker image here
LABEL image="frontendstatic"
#we are running few commands in our container(during container creation)
RUN apt update 
RUN apt install apache2 unzip -y
RUN rm -rf /var/www/html/index.html
#we are copying source code from local storage
COPY Todoist-win32-9.7.2.zip /var/www/html/Todoist-win32-9.7.2.zip
#we are moving to /var/www/html
WORKDIR /var/www/html
#we are unzipping and extracting the source code in default deployment enviornment location
RUN unzip Todoist-win32-9.7.2.zip
RUN mv oxer-html/* .
#we are exposing our container to a port
EXPOSE 80
#we are providing container a processs 
CMD ["apachectl", "-D" ,"FOREGROUND"]