# Preconditions

##Consul Key-Value entries:
* By default filebeat is configured to read logs from `/var/log/app/*.log`, where `/var/log/app` is the mapped directory inside the filebeat container. If you have logs inside subfolders or a different structure, you can define the path by the key `/filebeat/logsPath`.

Example: `/var/log/app/*/*.log`