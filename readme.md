docker build -t wordpress:ine . <br>
docker run  -d --name mysql-container -e MYSQL_ROOT_PASSWORD=welcome@123 mysql:5.7<br>
docker run -d --name wp-container --link mysql-container:mysql -p 80:80 wordpress:ine
