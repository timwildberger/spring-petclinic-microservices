FROM grafana/grafana:8.0.6

USER root

RUN apk add curl
RUN apk add unzip
RUN curl -LO https://github.com/NovatecConsulting/novatec-service-dependency-graph-panel/releases/download/v4.0.2/novatec-sdg-panel.zip && \
	unzip novatec-sdg-panel.zip -d "$GF_PATHS_PLUGINS/novatec-servicegraph-panel"


USER grafana
