# Example docker-compose configuration Docker Desktop for Windows

## Requirements:

* Install Docker Desktop : https://www.docker.com/products/docker-desktop

* Allocate 8 gigs of RAM to your Docker Desktop application. Seetings for RAM can be found in the **resources** tab of the menu, shown here: https://docs.docker.com/desktop/windows/#resources

[Clone](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/cloning-a-repository-from-github/cloning-a-repository#cloning-a-repository) the repo: 

* git clone https://github.com/jimfhahn/wikibase-release-pipeline

## Navigate to the folder

* cd wikibase-release-pipeline

* cd example

### The example docker-compose configuration consists of two files

* `docker-compose.yml` contains two services: wikibase and mysql
* `docker-compose.extra.yml` contains additional services such as: wdqs, wdqs-frontend, elasticsearch and quickstatements 

## Configure your installation

* cp `template.env` to `.env`

## Run with the pre-configured settings

```
docker-compose -f docker-compose.yml -f docker-compose.extra.yml up
```
