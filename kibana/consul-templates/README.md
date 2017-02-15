# Preconditions

##Consul Key-Value entries:
* The URL to the Elasticsearch instance to use for all your queries should be defined by the key `/kibana/elasticsearchURL`. It should be a complete url including the port as well. You may use consul dns entries too. Example: `http://elasticsearch-9200:9200`, where `elasticsearch-9200` is a consul dns entry.

Note: If the key `/kibana/elasticsearchURL` does not exist, the property will be assigned default value of `http://elasticsearch:9200`.

* If you are running kibana behind a proxy, and want to mount it at a path specify that path by the key `/kibana/basePath`. The basePath can't end in a slash. Example: `/kibana`