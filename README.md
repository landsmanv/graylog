# Logstore for storing and analyzing logs from docker containers
- Graylog - 3x hosts in cluster, Azure Internal Load Balancer (Preview) for ports 12201 (fluentd) and 9000 - api and web interface
- Mongo for Graylog configuration 3x replica set
- Elasticsearch - replica set 3x

1) Modify passwords, ips and deploy docker-compose.yml to 3 hosts, set only one host as graylog master
2) Initiate mongo replica set (mongo_repl.init)
3) Restart docker-compose
4) Set GELF TCP 12201 input, indices, users according to your needs https://hub.docker.com/r/graylog2/graylog/
