FROM node:8-alpine

RUN apk add unzip curl

RUN mkdir /opt/mongodb-proxy
RUN curl -L https://github.com/thebristolcable/mongodb-grafana/archive/master.zip > /tmp/master.zip && \
  cd /opt/mongodb-proxy && unzip /tmp/master.zip && cd mongodb-grafana-master && \
  npm install

RUN apk del unzip curl

EXPOSE 3333

WORKDIR /opt/mongodb-proxy/mongodb-grafana-master/dist/server

CMD [ "node", "mongodb-proxy" ]
