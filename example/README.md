# Example docker-compose configuration

The example docker-compose configuration consists of two files

* `docker-compose.yml` contains two services: wikibase and mysql
* `docker-compose.extra.yml` contains additional services such as: wdqs, wdqs-frontend, elasticsearch and quickstatements 

## Configure your installation

Copy the `template.env` to `.env` 

### Run with the pre-configured settings

```
docker-compose -f docker-compose.yml -f docker-compose.extra.yml up
```
### MariaDB(MySql) Permissions

Root password for mysql might be buggy in which case one would need to enter the cli for mysql, per: https://stackoverflow.com/questions/41645309/mysql-error-access-denied-for-user-rootlocalhost

1. Open & Edit /etc/my.cnf or /etc/mysql/my.cnf, depending on your distro.
2. Add skip-grant-tables under [mysqld]
3. Restart Mysql by Restarting Container with MariaDB
