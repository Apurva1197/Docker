# cat Dockerfile
FROM mysql:latest

MAINTAINER baeldung.com

RUN chown -R mysql:root /var/lib/mysql/

ARG MYSQL_DATABASE
ARG MYSQL_USER
ARG MYSQL_PASSWORD
ARG MYSQL_ROOT_PASSWORD

ENV MYSQL_DATABASE=$DATABASE1
ENV MYSQL_USER=$APURVA
ENV MYSQL_PASSWORD=$APURVA1197
ENV MYSQL_ROOT_PASSWORD=$APURVA1197

COPY student.sql /etc/mysql/student.sql

RUN sed -i 's/MYSQL_DATABASE/'$DATABASE1'/g' /etc/mysql/student.sql
RUN cp /etc/mysql/student.sql /docker-entrypoint-initdb.d

EXPOSE 3306

CMD /bin/bash