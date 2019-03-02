FROM nginx:stable
WORKDIR /etc/nginx/
RUN rm /etc/nginx/conf.d/*.conf
RUN mkdir custom
RUN sed -i '$d' nginx.conf
RUN echo '    include /etc/nginx/custom/*.conf;' >> nginx.conf
RUN echo '}' >> nginx.conf
