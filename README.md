# java-docker-education-app
Dockerize java app with mysql and rabbitmq

1-Mysql kurmak için
mysql klasorunun içinde docker-compose up -d komutu çalıştırılır
 1.1  cd ../mysql
 1.2  docker-compose up -d
2-Rabbitmq kurmak için 
rabbitmq klasorunun içinde docker-compose up -d komutu çalıştırılır
 2.1  cd ../rabbitmq
 2.2. docker-compose up -d
3-Java uygulaması build etmek ve çalıştırmak için
java-app klasorune gidilir docker build --tag=education:latest --rm=true . komutu çalıştırılır
Daha sonra docker run --name=education --network=mysql_default --publish=8080:8080 education:latest komutu çalıştırılır
 3.1  cd ../java-app
 3.2  docker build --tag=education:latest --rm=true .
 3.3  docker run -d --name=education --network=mysql_default --publish=8080:8080 education:latest 

4-swagger adresi -> http://localhost:8080/swagger-ui.html
