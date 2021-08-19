## Install psql

Install psql on your platform:
https://blog.timescale.com/blog/how-to-install-psql-on-mac-ubuntu-debian-windows/

## Accessing the user-service database
``

(NOTE: Get environment variable values from Slack)
export PGHOST=
export PGPORT=
export PGPASSWORD=
export PGUSER=
export PGDATABASE=
psql
```

## Useful commands
```
\dt (to list all tables)
SELECT * from "Users"; (to see everything in the Users table - must have quotes)
