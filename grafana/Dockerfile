FROM grafana/grafana

RUN grafana-cli plugins install grafana-worldmap-panel
RUN grafana-cli --pluginUrl https://github.com/thebristolcable/mongodb-grafana/archive/0.8.2.zip \
    plugins install grafana-mongodb-datasource
