# docker-db-stack



This project provides a simple `docker-compose` setup for running a PostgreSQL, Microsoft SQL Server, MySQL database with Adminer, PHPMyadmin, PGADMIN (lightweight database management tools).

## 📦 Requirements

    - [Docker](https://www.docker.com/get-started)
    - [Docker Compose](https://docs.docker.com/compose/install/)

## 🚀 Getting Started

### 1. Clone this repository (or copy the `docker-compose.yml` to your project)

# bash
    - git clone https://github.com/PRINCIE-KIDKAY/docker-postgresql-DB.git
    - cd your-project-directory


## Start the containers
    `docker-compose up -d`

## this will Start containers with:

# postgresql
    - Username: `postgres`
    - Password: `123456`
    - Database: `postgres`
    - Exposed on `localhost:5432`
    - DB hostname: `postgres` ## to connect to your db running in docker
    

# mysql
    - Username: `root`
    - Password: `123456`
    - Database: `mydb`
    - Exposed on `localhost:3306`

# mssql
    - Username: `sa` # default user
    - Password: `F!iB6#dO6O7KJK8`
    - Database: `master` # master is a default system database or simply connect to your db 
    - Server: `mssql-db` # container name or database-ip or database url
    - Exposed on `localhost:1433`



# Access the services
    - Adminer UI: Open your browser and go to `http://localhost:8080`
    - pgadmin UI: Open your browser and go to `http://localhost:8081`
    - phpmyadmin UI: Open your browser and go to `http://localhost:8082`

# ssms-connection for mssql:
    - server-name: `127.0.0.1,1433`
    - Server type: `Database Engine`
    - Authentication: `SQL Server Authentication`
    - Encryption: `Optional`
    - Host name in certificate: `localhost`

# mysql-Workbench:
    - Username: `root`
    - Password: `123456`
    - Host-name: `localhost`
    - Port: `3306`

# pgadmin
    - Username: `postgres`
    - Password: `123456`
    - Database: `postgres`
    - Exposed on `localhost:5432`
    - Container DB hostname: `postgres` ## to connect to your db running in docker
    - hostname:  
        1.`host.docker.internal` ## to connect to any db via ssh to pg admin running in docker
        2.`your-db-ip` ## to connect to any remote db via db-ip to pg admin running in docker

# Stop the containers
    `docker-compose down`
    `docker-compose down -v --remove-orphans` # only run this when you want a fresh restart
    `docker system prune -a --volumes` # to clear catches