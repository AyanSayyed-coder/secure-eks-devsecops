FROM nginx:1.27-alpine

# Copy static file
COPY index.html /usr/share/nginx/html/

# Change PID location for non-root user
RUN sed -i 's#/run/nginx.pid#/tmp/nginx.pid#' /etc/nginx/nginx.conf

# Fix permissions
RUN chown -R nginx:nginx /usr/share/nginx/html \
    && chown -R nginx:nginx /var/cache/nginx \
    && chown -R nginx:nginx /var/log/nginx

USER nginx

EXPOSE 80
