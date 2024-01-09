FROM nginx:latest

RUN openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout nginx-selfsigned.key -out nginx-selfsigned.crt -subj "/"
RUN mkdir -p /etc/nginx/ssl/
RUN mv ./nginx-selfsigned.crt /etc/nginx/ssl/nginx-selfsigned.crt
RUN mv ./nginx-selfsigned.key /etc/nginx/ssl/nginx-selfsigned.key

COPY nginx.conf /etc/nginx/nginx.conf