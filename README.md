# hyperledger-explorer-postgresql
This is one docker image of postgresql used for hyperledger explorer.

The following database setup is required for hyperledger explorer:
 - Connect to PostgreSQL database.
    - sudo -u postgres psql
- Run create database script.
    - \i app/db/explorerpg.sql

This Docker image includes these setup steps and you don't need to do again in your container.

Just run the image:
```
docker run -d -p 6432:5432 -e POSTGRES_PASSWORD=Passw0rd@  osswangxining/hyperledger-explorer-postgresql
```