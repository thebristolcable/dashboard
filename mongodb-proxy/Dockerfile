FROM node:8-alpine

# We need git for one of mongodb-grafana's dependencies
RUN apk add unzip curl git

ENV NODE_ENV=production

RUN mkdir /opt/mongodb-proxy
RUN curl -L https://github.com/thebristolcable/mongodb-grafana/archive/0.8.2.zip > /tmp/master.zip && \
  cd /opt/mongodb-proxy && unzip /tmp/master.zip && cd mongodb-grafana-0.8.2 && \
  npm install

RUN apk del unzip curl git

EXPOSE 3333

WORKDIR /opt/mongodb-proxy/mongodb-grafana-0.8.2/dist/server

CMD [ "node", "mongodb-proxy" ]
