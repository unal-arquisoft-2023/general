FROM nginx

RUN apt-get update -qq && apt-get -y install apache2-utils
ENV NODE_ROOT /var/www/frontend
WORKDIR $NODE_ROOT
RUN mkdir log
COPY app_ssl.conf /etc/nginx/conf.d/default.conf
COPY nginx.key /etc/nginx/ssl/nginx.key
COPY nginx.crt /etc/nginx/ssl/nginx.crt
CMD [ "nginx", "-g", "daemon off;" ]
