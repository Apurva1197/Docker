FROM ubuntu:latest
LABEL image="frontendstatic"
RUN apt update 
RUN apt install apache2 unzip -y
RUN rm -rf /var/www/html/index.html
COPY website.zip /var/www/html/website.zip
WORKDIR /var/www/html
RUN unzip website.zip
EXPOSE 80
CMD ["apachectl", "-D" ,"FOREGROUND"]