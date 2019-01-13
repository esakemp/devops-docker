FROM ubuntu:16.04

RUN apt-get update && apt-get install -y git curl && \
    curl -sL https://deb.nodesource.com/setup_10.x | bash && \
    apt-get install -y nodejs && \
    git clone https://github.com/docker-hy/frontend-example-docker.git && \
    apt-get purge -y --auto-remove curl && \
    apt-get purge -y --auto-remove git && \
    rm -rf /var/lib/apt/lists/* && \
    useradd -m app && \
    chown -R app /frontend-example-docker

WORKDIR /frontend-example-docker
USER app
RUN npm install

EXPOSE 5000
CMD API_URL="http://localhost:8000" npm start
