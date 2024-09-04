FROM ubuntu:latest
LABEL image="frontendstatic"
RUN apt update 
RUN apt install apache2 unzip -y
RUN rm -rf /var/www/html/index.html
COPY puppy.zip /var/www/html/puppy.zip
WORKDIR /var/www/html
RUN unzip puppy.zip
EXPOSE 80
CMD ["apachectl", "-D" ,"FOREGROUND"]