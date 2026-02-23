FROM nginx:alpine

# Create non-root user
RUN addgroup -S appgroup && adduser -S appuser -G appgroup

# Fix permissions for nginx
RUN chown -R appuser:appgroup /var/cache/nginx \
    && chown -R appuser:appgroup /var/run \
    && chown -R appuser:appgroup /var/log/nginx \
    && chown -R appuser:appgroup /usr/share/nginx/html

USER appuser

EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
