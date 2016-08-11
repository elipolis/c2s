# c2s
A CLI to provisioning a docker services with a docker-compose file

## Usage
```
$ ./c2d [DIRECTORY] | bash
```

## Example
```
$ ./c2s example/wordpress/ | bash
```

## Debug
```
$ ./c2s example/wordpress/

# Project: wordpress
# Creating networks ...
# =================
# Creating volumes ...
# =================
# Creating services ...
docker service create --env MYSQL_ROOT_PASSWORD=wordpress --env MYSQL_DATABASE=wordpress --env MYSQL_USER=wordpress --env MYSQL_PASSWORD=wordpress   --mount type=volume,source=./.data/db,target=/var/lib/  mysql --name wordpress-db mysql:5.7
docker service create --env WORDPRESS_DB_HOST=db:3306 --env WORDPRESS_DB_PASSWORD=wordpress  --publish 8000:80  --name wordpress-wordpress wordpress:latest
# =================
```
 
