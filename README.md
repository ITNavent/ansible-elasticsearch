# Ansible Role: Elasticsearch

El rol permite instalar Elasticsearch en N nodos y crear un cluster con nodos de distinto tipo (master, data, etc...)

## Requerimientos

```yaml
- src: https://***:***@github.com/ITNavent/ansible-java.git
  version: check-java
  name: java

- src: https://***:***@github.com/ITNavent/ansible-navent-folders.git
  version: v1.0.0
  name: folders
```

## Configuración
```yaml
elasticsearch_version: 5.2.2
elasticsearch_install_dir: /opt/
elasticsearch_log_dir: /var/log/elasticsearch
elasticsearch_data_dir: /var/lib/elasticsearch
elasticsearch_user: elasticsearch
elasticsearch_group: elasticsearch
elasticsearch_network_host: localhost
elasticsearch_network_publish_host: localhost
elasticsearch_http_port: 9200
elasticsearch_cluster_name: ""
elasticsearch_node_name: ""
elasticsearch_node_master: "true"
elasticsearch_node_data: "true"
elasticsearch_node_ingest: "true"
elasticsearch_attrs: {}
elasticsearch_bootstrap_memory_lock: "false"
elasticsearch_discovery_zen_ping_unicast_hosts:
  - "127.0.0.1"
  - "[::1]"
elasticsearch_discovery_zen_minimum_master_nodes: 0
elasticsearch_gateway_recover_after_nodes: 0
elasticsearch_action_destructive_requires_name: "false"

elasticsearch_jvm_xms: 2
elasticsearch_jvm_xmx: 2
```