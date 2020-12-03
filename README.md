## Configure Filebeat
docker-compose exec filebeat filebeat modules enable nginx
docker-compose exec filebeat filebeat modules enable mysql
docker-compose exec filebeat filebeat setup -e

## Configure password flexget

https://showrss.info

docker-compose exec flexget sh -c 'flexget web passwd Priscilla38@#000'