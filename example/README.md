# Example docker-compose configuration Docker Desktop for Mac

## Requirements:

* Install Docker Desktop : https://www.docker.com/products/docker-desktop

* Allocate 8 gigs of RAM to your Docker Desktop application. Seetings for RAM can be found in the **resources** tab of the menu, shown here: https://docs.docker.com/desktop/mac/#resources

[Clone](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository-from-github/cloning-a-repository#cloning-a-repository) the repo: 

* git clone -b docker-desktop-mac-install <https://github.com/jimfhahn/wikibase-release-pipeline>

## Navigate to the folder

* cd wikibase-release-pipeline

* cd example


### The example Docker Compose for **Mac** configuration consists of two files

* `docker-compose.yml` contains two services: wikibase and mysql
* `docker-compose.extra.yml` contains additional services such as: wdqs, wdqs-updater, wdqs-frontend.

## Configure your installation

```
cp template.env .env
```

## Intel CPU

```
docker-compose -f docker-compose.yml -f docker-compose.extra.yml up
```
This will start up the services defined in docker-compose.yml, a Wikibase instance, and MySQL database. Some additional services for the Wikibase Query Service, wdqs, wdqs-updater, wdqs-frontend are included.

## M1 CPU 

```
docker-compose up
```

This will start up the services defined in docker-compose.yml, a Wikibase instance, and MySQL database.


## Tested on Docker Desktop on Mac: 4.7.1 (77678) w/ Apple M1 Pro chip.




