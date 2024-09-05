FROM ubuntu:latest
LABEL image="frontendstatic"
RUN apt update 
RUN apt install apache2 unzip -y
RUN rm -rf /var/www/html/index.html
COPY seasonswitcher.zip /var/www/html/seasonswitcher.zip
WORKDIR /var/www/html
RUN unzip seasonswitcher.zip
EXPOSE 80
CMD ["apachectl", "-D" ,"FOREGROUND"]