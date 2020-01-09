FROM ubuntu
MAINTAINER Caique Portela <caiquesportela@gmail.com>
RUN apt-get update
RUN apt-get install -y nginx
ADD nginxFile /etc/nginx/sites-enabled/default
RUN echo "daemon off;" >> /etc/nginx/nginx.conf
WORKDIR /var/www

run ln -sf /dev/stdout /var/log/nginx/access.log
run ln -sf /dev/stdin /var/log/nginx/error.log

EXPOSE 8080
ENTRYPOINT ["/etc/init.d/nginx"]
CMD ["start"]
