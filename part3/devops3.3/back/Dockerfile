FROM ubuntu:16.04

RUN apt-get update && apt-get install -y git curl && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt-get install -y nodejs && \
    git clone https://github.com/docker-hy/backend-example-docker.git && \
    apt-get purge -y --auto-remove curl && \
    apt-get purge -y --auto-remove git && \
    rm -rf /var/lib/apt/lists/* && \
    useradd -m app && \
    chown -R app /backend-example-docker

WORKDIR /backend-example-docker
USER app
RUN npm install

EXPOSE 8000
CMD FRONT_URL="http://localhost" npm start
