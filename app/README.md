# Strapi application

A quick description of your strapi application

# Dumping data into the database

cat strapi.sql | docker exec -i CONTAINER_ID psql -U strapi -d strapi

# Exporting database

docker exec -i CONTAINER_ID pg_dump --username SEU_USUARIO --password SUA_DATABASE > DUMP*`date +%d-%m-%Y"_"%H_%M_%S`.sql