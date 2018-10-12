FROM node:8.12

RUN apt-get update && apt-get install -y unzip

RUN mkdir /opt/mongodb-proxy
RUN curl -L https://github.com/JamesOsgood/mongodb-grafana/archive/master.zip > /tmp/master.zip && \
  cd /opt/mongodb-proxy && unzip /tmp/master.zip && cd mongodb-grafana-master && \
  npm install

EXPOSE 3333

WORKDIR /opt/mongodb-proxy/mongodb-grafana-master/dist/server

CMD [ "node", "mongodb-proxy" ]
