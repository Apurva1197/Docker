FROM ubuntu:latest
LABEL image="frontendstatic"
RUN apt update 
RUN apt install apache2 unzip -y
RUN rm -rf /var/www/html/index.html
COPY podcastsbless.zip /var/www/html/podcastsbless.zip
WORKDIR /var/www/html
RUN unzip podcastsbless.zip
EXPOSE 80
CMD ["apachectl", "-D" ,"FOREGROUND"]