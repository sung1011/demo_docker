From nginx
LABEL maintainer "sunji <sung1011@gmail.com>"

WORKDIR /

RUN mkdir /var/www

RUN ln -sf /dev/stdout /var/log/nginx/access.log \
	&& ln -sf /dev/stderr /var/log/nginx/error.log

#COPY 50x.html /var/www/
#COPY index.html /var/www/
COPY nginx.conf /etc/nginx/

Volume ["/var/www", "/var/log/nginx"]

EXPOSE 1011

CMD ["nginx", "-g", "daemon off;"]
