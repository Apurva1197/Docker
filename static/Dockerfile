FROM ubuntu:latest
LABEL image="frontendstatic"
RUN apt update 
RUN apt install apache2 unzip -y
RUN rm -rf /var/www/html/index.html
COPY index.html /var/www/html/index.html
WORKDIR /var/www/html
EXPOSE 80
CMD ["apachectl", "-D" ,"FOREGROUND"]