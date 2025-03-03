# Selecting the base image as Ubuntu
FROM ubuntu:latest

# Update the package list and install Nginx
RUN apt update -y && apt install nginx -y 

# Selecting Nginx as the final image
FROM nginx:latest

# Copy custom index.html file to the correct Nginx directory
COPY index.html /usr/share/nginx/html/index.html

# Expose port 80 for web traffic
EXPOSE 80

# Start Nginx in the foreground
CMD ["nginx", "-g", "daemon off;"]
