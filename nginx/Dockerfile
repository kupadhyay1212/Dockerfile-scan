FROM nginx:alpine
LABEL foo="bar baz
USER  me
HEALTHCHECK CMD curl --fail http://localhost:80 || exit 1
## Copy a new configuration file setting logs base dir to /var/server-logs/nginx
COPY ./config/nginx.conf /etc/nginx/
## Create the new /var/server-logs/nginx folder
RUN mkdir --parents /var/server-logs/nginx
## Start nginx server
CMD ["nginx", "-g", "daemon off;"]
