FROM ubuntu:latest
LABEL image="frontendstatic"
RUN apt update 
RUN apt install apache2 unzip -y
RUN rm -rf /var/www/html/index.html
COPY counter.zip /var/www/html/counter.zip
WORKDIR /var/www/html
RUN unzip counter.zip
EXPOSE 80
CMD ["apachectl", "-D" ,"FOREGROUND"]