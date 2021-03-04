FROM nginxinc/nginx-unprivileged:1.16.1-alpine

USER 0

RUN mkdir -p /usr/share/nginx/html/

COPY default.conf /etc/nginx/conf.d/default.conf
COPY rclone /usr/share/nginx/html/rclone
COPY mc /usr/share/nginx/html/mc
COPY index.html /usr/share/nginx/html/index.html

USER 101

CMD ["nginx", "-g", "daemon off;"]
