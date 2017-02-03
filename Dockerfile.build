FROM maven:3.3.9-jdk-8

ARG node_version=7.5.0

ARG serverless_version=1.6.1

ENV NODE_VERSION=$node_version SERVERLESS_VERSION=$serverless_version

RUN groupadd --gid 1000 node \
  && useradd --uid 1000 --gid node --shell /bin/bash --create-home node \
  && curl -SLO "https://nodejs.org/dist/v$NODE_VERSION/node-v$NODE_VERSION-linux-x64.tar.xz" \
  && tar -xJf "node-v$NODE_VERSION-linux-x64.tar.xz" -C /usr/local --strip-components=1 \
  && rm "node-v$NODE_VERSION-linux-x64.tar.xz" \
  && ln -s /usr/local/bin/node /usr/local/bin/nodejs \
  && npm install -g serverless@$SERVERLESS_VERSION \
  && mkdir -p /app

WORKDIR /app
