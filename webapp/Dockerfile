# Use official nginx image as base
FROM nginx:alpine

# Install basic tools for file operations
RUN apk add --no-cache curl

# Create output directory
RUN mkdir -p /app/output

# Copy custom HTML files to nginx html directory
COPY index.html /usr/share/nginx/html/
COPY style.css /usr/share/nginx/html/
COPY startup.sh /usr/local/bin/

# Make startup script executable
RUN chmod +x /usr/local/bin/startup.sh

# Expose port 80
EXPOSE 80

# Use custom startup script
CMD ["/usr/local/bin/startup.sh"]