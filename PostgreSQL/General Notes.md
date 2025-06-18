**Connecting to DB Server : By two ways :** GUI Client or Terminal/CMD

## Connecting to Database from Terminal
`psql -U postgres -W 'password'`

## Connecting to HOST from Terminal
`psql -h localhost/IPAddress -p 5432 -U postgres dbName`

## Connecting to database from terminal
- In terms of above commands, there are other ways to connect to database as well. We can switch between databases easily through below command.
- `\c databasename` 
- The above command will switch the database

## Reset the password after connecting to psql
`ALTER USER username PASSWORD 'password';`

## Reset the password without connecting to psql
1. First sudo su - postgres user and then below command.
2. psql -U postgres
3. This will open up the postgres terminal without password , if postgres user exists. After that use above ALTER command to reset the password.
4. Next, edit the pg_hba.conf file and change the postgres user role from peer to trust.
## Creating Roles
`CREATE ROLE root WITH LOGIN SUPERUSER PASSWORD 'root'`
- CREATE ROLE will create a role with root username
- WITH LOGIN will allow the user to connect to the database
- SUPERUSER will grant the user the root/ superuser privelge

`CREATE ROLE readonly_user` 
`WITH LOGIN NOSUPERUSER NOCREATEDB NOCREATEROLE NOINHERIT PASSWORD 'secure_password' VALID UNTIL '2025-12-31';`
- These are few other options that can be used while creating roles.


