# docker-mysql-client
Alpine image with mysql-client installed. Helpful if you just want to execute a mysqldump from docker

Use the following sample command, but first replace `${PORT}`, `${HOST}`, `${USER}`, `${PASSWORD}`, `${DATABASE}` with your desired values. Or you can alternatively complete the command passing Docker these environment variables using the `-e` option, like: `-e USER=aUsername`. 
```
  docker run --rm -v "$PWD/data":/data --name mysql-client byteflair/mysql-client sh -c "mysqldump -P${PORT} -h${HOST} -R -u${USER} -p${PASSWORD} ${DATABASE} > /data/dump.sql"
```
