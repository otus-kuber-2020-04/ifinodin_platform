FROM nginx:stable

WORKDIR /usr/share/nginx/html

COPY ./conf/default.conf /etc/nginx/conf.d/
EXPOSE 8000

RUN usermod -u 1001 nginx

