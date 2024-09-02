FROM ubuntu:latest
LABEL image="frontendstatic"
RUN apt update 
RUN apt install apache2 unzip -y
RUN rm -rf /var/www/html/index.html
COPY trafficlight.zip /var/www/html/trafficlight.zip
WORKDIR /var/www/html
RUN unzip trafficlight.zip
RUN mv trafficlight/* .
EXPOSE 80
CMD ["apachectl", "-D" ,"FOREGROUND"]