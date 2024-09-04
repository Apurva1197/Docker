FROM ubuntu:latest
LABEL image="frontendstatic"
RUN apt update 
RUN apt install apache2 unzip -y
RUN rm -rf /var/www/html/index.html
COPY number addtion.zip /var/www/html/number addition.zip
WORKDIR /var/www/html
RUN unzip number addition.zip
EXPOSE 80
CMD ["apachectl", "-D" ,"FOREGROUND"]