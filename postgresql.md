# PostgreSQL cheatsheet

Connecting to a database with username and password
```sh
# If they need to be setup in the envrionment use these ones
POSTGRES_USER=postgres
POSTGRES_DB=monolith
POSTGRES_PASSWORD=postgres

# Command to connect to psql
PGPASSWORD=postgres psql -U postgres monolith
```
