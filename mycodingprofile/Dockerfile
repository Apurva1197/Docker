FROM ubuntu:latest
LABEL image="frontendstatic"
RUN apt update 
RUN apt install apache2 unzip -y
RUN rm -rf /var/www/html/index.html
COPY mycodingprofile.zip /var/www/html/mycodingprofile.zip
WORKDIR /var/www/html
RUN unzip mycodingprofile.zip
RUN echo "hey, I am Apurva kulkarni $HOSTNAME" > /var/www/html/mycodingprofile/index.html
EXPOSE 80
CMD ["apachectl", "-D" ,"FOREGROUND"]