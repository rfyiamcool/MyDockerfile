### Usage

```
$ docker run -i \
    -p 127.0.0.1:3306:3306 \
    -e MYSQL_ROOT_PASSWORD=my-secret-pw \
    -t cytopia/mysql-5.7

$ mysql --user=root --password=my-secret-pw --host=127.0.0.1 -e 'show databases;'

```
