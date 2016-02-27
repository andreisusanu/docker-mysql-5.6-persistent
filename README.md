[![](https://badge.imagelayers.io/andreisusanu/mysql-5.6-persistent:latest.svg)](https://imagelayers.io/?images=andreisusanu/mysql-5.6-persistent:latest)

mysql-5.6-persistent
=============

Docker image for MySQL 5.6 with persistent data (using data volume)


Build
-----

```bash
docker build -t andreisusanu/mysql-5.6-persistent .
```

Create data volume
-----
```bash
docker volume create --name MySQLStorageVolume
```

Run
-----
```bash
docker run \
    --name mysql-5.6-persistent \
    -p 3306:3306 \
    -v MySQLStorageVolume:/var/lib/mysql \
    andreisusanu/mysql-5.6-persistent
```

MySQL credentials
-----
root without password (blank password)
