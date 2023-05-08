## images

```
docker pull guacamole/guacd:1.5.1
docker pull guacamole/guacamole:1.5.1
cd docker
docker build -t atompi/guacamole:1.5.1 .
```

## mkdir

```
mkdir -p data/{db/init,db/data,guacd/drive,guacd/record}
chown -R 1000:1000 data/guacd/drive
chown -R 1000:1001 data/guacd/record
chmod 2750 data/guacd/record
```

## init db

```
docker run --rm guacamole/guacamole:1.5.1 /opt/guacamole/bin/initdb.sh --postgres > ./data/db/init/initdb.sql
```

## start

```
docker-compose up -d
```

## default admin

```
guacadmin / guacadmin
```
