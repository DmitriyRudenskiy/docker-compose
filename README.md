### Insert record to
sudo nano /etc/hosts
127.0.0.1 crm.isuzu.market.local
127.0.0.1 isuzu.toptk.ru.local

### Haproxy
* test links
docker run \
-p 80:80 \
--link crm.isuzu.market.local:crm \
--link affectionate_hodgkin:isuzu_toptk \
-it --rm --name haproxy-syntax-check my-haproxy sh

ping crm
ping isuzu_toptk

curl crm:9501

docker build -t image-haproxy .
docker run -d --link crm.isuzu.market.local:crm --link affectionate_hodgkin:isuzu_top_tk --name my-running-haproxy my-haproxy
docker exec -it my-running-haproxy sh

docker stop my-running-haproxy; docker rm my-running-haproxy; docker build -t my-haproxy .; docker run -d --name base-haproxy my-haproxy




docker run -p 80:80 --link crm.isuzu.market.local:crm --link affectionate_hodgkin:isuzu_toptk -it --rm --name haproxy-syntax-check my-haproxy sh

#
docker exec -it some-mysql bash

# start
docker run --name base-haproxy \
-p 80:80 \
-p 8181:8181 \
--link crm.isuzu.market.local:crm \
--link affectionate_hodgkin:isuzu_toptk \
-d image-haproxy


### Crm
docker run -p 9501:9501 \
--name crm.isuzu.market.local \
-v '/Users/user/PhpstormProjects/crm.isuzu.market:/app' \
-w '/app' \
-d my/php \
php -S 0.0.0.0:9501 -t public/

### Mysql
mysqldump -u root -p123 isuzu_toptk_ru > /var/lib/mysql/isuzu_toptk_ru.sql


docker run -d --name my-running-haproxy my-haproxy

### Alpine Linux 
 mysql-client

haproxy

