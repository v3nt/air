#install and us postgresql

g_ctl -D /usr/local/var/postgres start && brew services start postgresql

Launch the server:

    node server.js <port> <postgres-connection-string> <air-data-url>

Example:

    node server.js 8080 postgres://postgres:12345@localhost:5432/air <air-data-url>



      CREATE DATABASE air WITH OWNER = danielcrabbe ENCODING = 'UTF8' TABLESPACE = pg_default LC_COLLATE = 'en_US.UTF-8' LC_CTYPE = 'en_US.UTF-8' CONNECTION LIMIT = -1;
