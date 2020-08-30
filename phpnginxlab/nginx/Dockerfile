FROM nginx:latest
COPY default.conf /etc/nginx/conf.d/default.conf
COPY css /var/www/html/css
COPY img /var/www/html/img
RUN chown -R nginx:nginx /var/www/html