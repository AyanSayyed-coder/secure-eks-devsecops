FROM nginx:alpine

# Copy your app
COPY index.html /usr/share/nginx/html/

# Fix permissions
RUN chown -R nginx:nginx /usr/share/nginx/html \
    && chown -R nginx:nginx /var/cache/nginx \
    && chown -R nginx:nginx /var/run \
    && chown -R nginx:nginx /var/log/nginx

# Switch to nginx user (UID 101 already exists)
USER nginx

EXPOSE 80
