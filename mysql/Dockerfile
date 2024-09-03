# cat Dockerfile
FROM mysql:latest

MAINTAINER baeldung.com

RUN chown -R mysql:root /var/lib/mysql/


ENV MYSQL_DATABASE=database1
ENV MYSQL_USER=apurva
ENV MYSQL_PASSWORD=apurva1197
ENV MYSQL_ROOT_PASSWORD=apurva1197

COPY student.sql /etc/mysql/student.sql

RUN sed -i 's/MYSQL_DATABASE/'$database1'/g' /etc/mysql/student.sql
RUN cp /etc/mysql/student.sql /docker-entrypoint-initdb.d

EXPOSE 3306

CMD /bin/bash