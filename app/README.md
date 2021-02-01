# Strapi application

A quick description of your strapi application

# Dumping data into the database

cat strapi.sql | docker exec -i CONTAINER_ID psql -U strapi -d strapi

# Exporting database

docker exec -i CONTAINER*ID pg_dump --username SEU_USUARIO --password SUA_DATABASE > DUMP\*`date +%d-%m-%Y"*"%H*%M*%S`.sql

# Importing database from LOCAL to PROD

PGPASSWORD={{DB_PASSWORD} docker exec -i {{CONTAINER_ID}} pg_dump -Fc --no-acl --no-owner -h localhost -U {{DB_USERNAME}} {{DB_DATABASE}} > strapi.dump
