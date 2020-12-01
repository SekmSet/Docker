docker-compose exec filebeat filebeat modules enable nginx
docker-compose exec filebeat filebeat modules enable mysql
docker-compose exec filebeat filebeat setup -e