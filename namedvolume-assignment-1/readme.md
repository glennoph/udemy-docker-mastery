# Named Volume Assignment - postgres
* Create postgres container with named volume psqldata using version 9.6.1
  postgres:9.6.1
  VOLUME [/var/lib/postgresql/data]
  `docker container run  -d --name psql961 -v psqldata:/var/lib/postgresql/data postgres:9.6.1`
  
* check logs then stop container
  `docker container logs -f psql961`
  log look ok
  stop continer
  `docker container stop psql961`
  

* check volume with `docker volume ls`
  `docker volume ls | grep psqldata`


* start postgres container with version 9.6.2 with same named volume
  `docker container run  -d --name psql962 -v psqldata:/var/lib/postgresql/data postgres:9.6.2`

  check logs
  stop containers
  
  



