# About this Repo

This is forked from the Git repo of the Docker [official image](https://docs.docker.com/docker-hub/official_repos/) for [ghost](https://registry.hub.docker.com/_/ghost/). See [the Docker Hub page](https://registry.hub.docker.com/_/ghost/) for the full readme on how to use this Docker image and for information regarding contributing and issues.

The full readme is generated over in [docker-library/docs](https://github.com/docker-library/docs), specifically in [docker-library/docs/ghost](https://github.com/docker-library/docs/tree/master/ghost).

See a change merged here that doesn't show up on the Docker Hub yet? Check [the "library/ghost" manifest file in the docker-library/official-images repo](https://github.com/docker-library/official-images/blob/master/library/ghost), especially [PRs with the "library/ghost" label on that repo](https://github.com/docker-library/official-images/labels/library%2Fghost). For more information about the official images process, see the [docker-library/official-images readme](https://github.com/docker-library/official-images/blob/master/README.md).

---
## How to use this image
This will start a Ghost instance listening on the default Ghost port of 2368.
```
$ docker run -d --name some-ghost ghost:alpine
```

**With MySQL/MariaDB Docker container**
```
$ docker run -d --name some-ghost -e DB=mysql - DB_PASS=password ghost:alpine
```

## Environment Variables
- ```NPM_CONFIG_LOGLEVEL```
	- default: warn
- ```NODE_ENV```
	- default: production
- ```DB```
	- default: sqlite3
- ```DB_HOST```
	- default: mysql  *This would point to linked Docker container named 'mysql'*
- ```DB_PASS```
	- default: password
- ```GHOST_URL```
	- default: http://localhost:2368