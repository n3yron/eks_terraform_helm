FROM nginx

COPY default.conf /etc/nginx/conf.d/

EXPOSE 8080

CMD ["/usr/sbin/nginx", "-g", "daemon off;"]
# not to build on M1