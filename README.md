# AWX on docker-compose
Docker compose for AWX

## Quick start
```
docker-compose up -d
```

After the stack is up, login to http://localhost:8052 with credentials `guest/guest`

## Customizations

Do not want to use defaults? Feel free to customize the following files:

* [`SECRET_KEY`](SECRET_KEY)
* [`credentials.py`](credentials.py)
* [`environment.sh`](environment.sh)

### Optional

Generate/update CA certs:

```shell
docker exec awx_web '/usr/bin/update-ca-trust'
```
## Persistent volumes

The following directories are used as persistent volumes:

* [`ca-trust`](ca-trust): SSL Certificates
* [`pg/data`](pg/data): Postgres data
* [`projects`](projects): AWX project data
