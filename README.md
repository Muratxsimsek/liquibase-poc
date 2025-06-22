# Spring Boot Liquibase Example

This project demonstrates using Liquibase with PostgreSQL in a Spring Boot application. It includes example DDL, DML and rollback statements as well as an external SQL file change set. Docker Compose is provided to easily start a PostgreSQL database.

## Prerequisites
- Java 11
- Maven
- Docker (for running PostgreSQL)

## Running PostgreSQL
Start the database using Docker Compose:

```bash
docker-compose up -d
```

## Applying Database Changes
Run Liquibase migrations via Maven:

```bash
mvn liquibase:update
```

Rollback the last change set:

```bash
mvn liquibase:rollback -Dliquibase.rollbackCount=1
```

## Running the Application
After applying migrations, start the Spring Boot app:

```bash
mvn spring-boot:run
```

The application itself is minimal and exists to demonstrate database migrations.
