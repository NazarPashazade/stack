### 1. Install Docker Desktop 

### 2. Clone Project 

### 3. Run this command                 //inside the database folder

     docker-compose up -d 



### 4. Go to LINK:  (http://localhost:8080/)

    ports:
      - "8080:80"



### 5. PgAdmin Credentials: 

    environment:
      - PGADMIN_DEFAULT_EMAIL=pgadminuser@gmail.com
      - PGADMIN_DEFAULT_PASSWORD=Database123!



### 6. Register Server

     1. HOSTNAME: "postgres-db"            //same as Service name
            services:
                postgres-db:

     1. PORT: "5432"

     1. Username: "postgres"

     1. Password: "Database123!"
