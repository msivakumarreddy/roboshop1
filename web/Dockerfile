FROM nginx
RUN groupadd -r nginx && useradd -r -g nginx nginx

RUN rm -rf /usr/share/nginx/html/index.html
RUN rm -rf /etc/nginx/nginx.conf
RUN rm -rf /etc/nginx/conf.d/default.conf
ADD static /usr/share/nginx/html/
ADD nginx.conf /etc/nginx/nginx.conf
RUN chown -R nginx:nginx /usr/share/nginx/html/

# Switch to the non-root user
USER nginx
