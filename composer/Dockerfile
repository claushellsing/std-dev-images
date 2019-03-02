FROM composer:1.8
ENTRYPOINT ["/bin/bash"]
RUN chmod 777 -R /tmp

RUN addgroup -g 1000 -S app && \
    adduser -u 1000 -S app -G app

USER app

RUN composer global require laravel/installer


RUN touch /home/app/.bashrc
RUN echo 'export PATH="/tmp/vendor/bin:$PATH"' >> /home/app/.bashrc
WORKDIR /app


