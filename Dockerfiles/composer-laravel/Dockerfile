FROM composer:1.8

RUN addgroup -g 1000 -S app && \
    adduser -u 1000 -S app -G app

RUN chmod -R 777 /tmp

USER app

RUN composer global require laravel/installer

RUN touch /home/app/.bashrc
RUN echo 'export PATH="/tmp/vendor/bin:$PATH"' >> /home/app/.bashrc
WORKDIR /app

ENTRYPOINT ["/bin/bash"]
