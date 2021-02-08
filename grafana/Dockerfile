FROM grafana/grafana:7.4.0

RUN mkdir /var/lib/grafana/data

ENV GF_PATHS_DATA=/var/lib/grafana/data

RUN grafana-cli plugins install grafana-worldmap-panel
RUN grafana-cli --pluginUrl https://github.com/thebristolcable/mongodb-grafana/archive/0.8.2.zip \
    plugins install grafana-mongodb-datasource
