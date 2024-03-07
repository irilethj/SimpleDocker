FROM nginx
COPY ./nginx.conf /etc/nginx/
COPY ./server.c .
COPY ./run.sh .
RUN apt-get update && \
    apt-get install -y gcc spawn-fcgi libfcgi-dev && \
    rm -rf /var/lib/apt/lists/*
USER nginx
WORKDIR /home
ENTRYPOINT ["sh", "./run.sh"]

