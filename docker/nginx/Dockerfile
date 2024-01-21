FROM nginx:1.19.0-alpine

COPY ./docker/nginx/default.conf.template /etc/nginx/conf.d/default.conf.template

COPY ./docker/nginx/entrypoint /entrypoint
RUN sed -i 's/\r$//g' /entrypoint
RUN chmod +x /entrypoint

COPY ./ssl /etc/ssl

ENTRYPOINT [ "/entrypoint" ]
CMD ["nginx", "-g", "daemon off;"]
