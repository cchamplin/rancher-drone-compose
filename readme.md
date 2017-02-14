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
