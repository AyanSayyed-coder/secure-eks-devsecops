FROM nginx:alpine

# Create non-root user
RUN addgroup -g 101 nginxgroup \
    && adduser -D -u 101 -G nginxgroup nginxuser

# Fix permissions
RUN chown -R 101:101 /var/cache/nginx \
    && chown -R 101:101 /var/run \
    && chown -R 101:101 /var/log/nginx \
    && chown -R 101:101 /usr/share/nginx/html

USER 101

EXPOSE 80
