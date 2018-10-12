FROM grafana/grafana

USER root

RUN apt-get update && apt-get install -y curl xz-utils unzip procps
RUN curl https://nodejs.org/dist/v8.12.0/node-v8.12.0-linux-x64.tar.xz | tar -xJC /opt

ENV PATH="/opt/node-v8.12.0-linux-x64/bin:${PATH}"

RUN curl -L https://github.com/JamesOsgood/mongodb-grafana/archive/master.zip > /tmp/master.zip && \
  cd /var/lib/grafana/plugins && unzip /tmp/master.zip && cd mongodb-grafana-master && \
  npm install

USER grafana
