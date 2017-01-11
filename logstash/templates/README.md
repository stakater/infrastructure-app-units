# Preconditions

##Consul Key-Value entries:
* Port for receiving "beats" should be defined by the key `/logstash/beatsPort`
* Grok pattern for logs of type `syslog` should be defined in the key `/logstash/syslogPattern`.
* Default Grok pattern for applications without specific grok pattern should be defined by the key `/logstash/defaultPattern`.
* Grok pattern (if any) for a specific application should be defined by the key `/logstash/<app_name>/grokPattern`.
* Multiline pattern (if any) for a specific application should be defined by the key `/logstash/<app_name>/multilinePattern`.

##Grok Pattern:
* Time in the logs should be parsed and assigned to the key `timestamp`.
* If using specific grok/multiline patterns for applications, logs must contain application name. The application name should be parsed and assigned to the key `app_name`.