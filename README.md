# Elasticsearch + Kibana + Fluent Bit

A sample docker-compose configuration to run ElasicSearch and Kibana locally. Also spins up an nginx container with a Fluent Bit sidecar to ship some logs to the local Elasticsearch instance.

`docker-compose up`

Hit http://localhost:8080/ or run `curl http://localhost:8080/` a couple times to have the NGINX container generate and ship some logs to Elasticsearch.

Visit http://localhost:5601 in your browser to view the Kibana dashboard.

You'll be prompted to create an index, just enter `fluent-bit*` which should match the only avaiable index and select `@timestamp` in the dropdown on the next step. Once the index is create click on the Discover tab in the top left panel to view some parsed logs.
