# Servers
Kibana 5601
Elastic Search 9200,9300
data volume - Docker volume /var/lib/docker/volume
# increase max_map
    sudo sysctl -w vm.max_map_count=262144
    sysctl -a | grep max_map_count
# Remove all stopped docker containters
    docker rm $(docker ps -a -q)
    
# Find port bindings
    sudo netstat -nltp
# Kibana URLS
    http://localhost:5601/
# Useful docker compose commands
    docker-compose ps
    docker volume ls
    docker-compose stop
    docker-compose rm
 # Physical location of the volume
    /var/lib/docker
    sudo ls -lrh /var/lib/docker/volumes
# Verify plugins
    docker exec elasticsearch  ls /usr/share/elasticsearch/plugins
# Install plugin
    docker exec elasticsearch  /usr/share/elasticsearch/bin/elasticsearch-plugin install --batch ingest-geoip
# Useful system commands
    sudo systemctl status firewalld
    sudo filebeat test output
    sudo filebeat version
    sudo filebeat modules list
    sudo filebeat modules enable system
    # Write log message into system log with program as JAVA_HELL
    sudo logger -t "JAVA_HELL" Hello MR Balaji