FROM ubuntu:latest
LABEL image="frontendstatic"
RUN apt update 
RUN apt install apache2 unzip -y
RUN rm -rf /var/www/html/index.html
COPY todo.zip /var/www/html/todo.zip
WORKDIR /var/www/html
RUN unzip todo.zip
EXPOSE 80
CMD ["apachectl", "-D" ,"FOREGROUND"]