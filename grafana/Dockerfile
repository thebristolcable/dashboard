FROM grafana/grafana

RUN grafana-cli plugins install grafana-worldmap-panel
RUN grafana-cli --pluginUrl https://github.com/thebristolcable/mongodb-grafana/archive/master.zip \
    plugins install grafana-mongodb-datasource
