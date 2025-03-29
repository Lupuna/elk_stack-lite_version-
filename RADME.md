Для нормальной работы на сервере необходимо **Elasticsсeach** контейнеру дать доступ к **./docker_volumes/**

<br>

Это можно сделать следующим образом

```commandline
sudo chown -R 1000:1000 ./docker_volumes/elasticsearch/data
```

и 

```commandline
sudo chmod -R 775 ./docker_volumes/elasticsearch/data
```

Также необходимо заменить логин и пароль на более оригинальный в docker-compose.yml, kibana/config.py, logstash/piplines/service_stamped_json_logs.conf