# Example docker-compose configuration

The example Docker Compose for **Mac** configuration consists of two files

* `docker-compose.yml` contains two services: wikibase and mysql
* `docker-compose.extra.yml` contains additional services such as: wdqs, wdqs-frontend, elasticsearch and quickstatements 

## Configure your installation

Copy the `template.env` to `.env` 

### Run with the pre-configured settings

```
docker-compose -f docker-compose.yml -f docker-compose.extra.yml up
```
