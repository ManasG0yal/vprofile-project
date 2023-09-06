# using the base image of the mysql 
FROM mysql:8.0.33
# here we are creating some labels
LABEL "project"="containerization-vprofile"
LABEL "Author"="ManasG0yal"
# here we are creating some environment variables for the command
ENV MYSQL_ROOT_PASSWORD ="vprodbpass"
ENV MYSQL_DATABASE="accounts"
# here we are adding our db.sql file into our new database container
ADD db_backup.sql /docker-entrypoint-initdb.d/db_backup.sql
