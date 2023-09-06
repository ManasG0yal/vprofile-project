# here we are using nginx as base image
FROM nginx

# here we are using the labels
LABEL "project"="containerization-vprofile"
LABEL "Author"="ManasG0yal"

# here we are removing the default configration file
RUN rm -rf /etc/nginx/conf.d/default.conf

# here we are copying our created config file into the container
COPY nginvproapp.conf /etc/nginx/conf.d/vproapp.conf