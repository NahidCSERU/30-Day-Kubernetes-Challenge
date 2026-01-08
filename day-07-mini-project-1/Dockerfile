FROM nginx:1.25


# Remove default nginx config
RUN rm /etc/nginx/conf.d/default.conf


# Custom HTML
RUN echo '<!DOCTYPE html>\n<html>\n<head><title>Day 7 Mini Project</title></head>\n<body style="font-family: Arial;">\n<h1>🚀 Deployed from Local Docker Image!</h1>\n<p>Built inside Minikube Docker daemon</p>\n</body>\n</html>' \
> /usr/share/nginx/html/index.html


EXPOSE 80