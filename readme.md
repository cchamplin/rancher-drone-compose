# Installing Drone on Rancher

## Creating the database

1. Add a new database container in rancher for postgres
2. Image: postgres:9.4
3. Environment variables: POSTGRES_PASSWORD - select a postgres password
4: Console: None


## Creating the Drone Stack
1. Select "Add Stack"
2. Select the docker-compose.yml file from this repository
3. Select the rancher-compose.yml file from this repository
4. Update the rancher-compose.yml with appropriate values for client_id, client_secret, and postgres password

## Example compose values for Github
```
    remote_driver: github
    remote_config: "https://github.com?client_id=<CLIENT_ID>&client_secret=<CLIENT_SECRET_KEY>"
    database_driver: postgres
    database_config: "postgres://postgres:<PASSWORD>@database:5432/postgres?sslmode=disable"
```


## Example compose values for Bitbucket
```
    remote_driver: bitbucket
    remote_config: "https://bitbucket.org?client_id=<CLIENT_ID>&client_secret=<CLIENT_SECRET_KEY>"
    database_driver: postgres
    database_config: "postgres://postgres:<PASSWORD>@database:5432/postgres?sslmode=disable"
```
