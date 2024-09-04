FROM ubuntu:latest
LABEL image="frontendstatic"
RUN apt update 
RUN apt install apache2 unzip -y
RUN rm -rf /var/www/html/index.html
COPY numberaddtion.zip /var/www/html/numberaddition.zip
WORKDIR /var/www/html
RUN unzip numberaddition.zip
EXPOSE 80
CMD ["apachectl", "-D" ,"FOREGROUND"]