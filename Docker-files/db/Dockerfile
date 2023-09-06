# using the base image of the mysql 
FROM mysql:8.00.33

LABEL "project"="containerization-vprofile"
LABEL "Author"="ManasG0yal"

ENV MYSQL_ROOT_PASSWORD ="vprodbpass"
ENV MYSQL_DATABASE="accounts"

ADD db_backup.sql /docker-entrypoint-initdb.d/db_backup.sql
