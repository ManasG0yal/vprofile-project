FROM nginx

LABEL "project"="containerization-vprofile"
LABEL "Author"="ManasG0yal"

RUN rm -rf /etc/nginx/conf.d/default.conf

COPY nginvproapp.conf /etc/nginx/conf.d/vproapp.conf