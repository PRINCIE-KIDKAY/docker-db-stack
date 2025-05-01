# docker-db-stack



This project provides a simple `docker-compose` setup for running a PostgreSQL, Microsof SQL Server, MySQL database with Adminer, PHPMyadmin, PGADMIN (lightweight database management tools).

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
- Username: postgres
- Password: 123456
- Database: postgres
- Exposed on localhost:5432

# mysql
- Username: root
- Password: 123456
- Database: mydb
- Exposed on localhost:3306

# Access the services
- Adminer UI: Open your browser and go to `http://localhost:8080`
- pgadmin UI: Open your browser and go to `http://localhost:8081`
- phpmyadmin UI: Open your browser and go to `http://localhost:8082`



# Stop the containers

`docker-compose down`