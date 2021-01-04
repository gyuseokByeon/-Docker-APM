FROM mariadb

LABEL version="0.1.0"


RUN { \
        echo '[mysqld]'; \
        echo 'character-set-server=utf8mb4'; \
        echo 'collation-server=utf8mb4_unicode_ci'; \
        echo '[client]'; \
        echo 'default-character-set=utf8mb4'; \
    } > /etc/mysql/conf.d/charset.cnf

ARG MYSQL_CONTAINER_USER
ARG MYSQL_CONTAINER_GROUP

RUN usermod -u 1000 ${MYSQL_CONTAINER_USER} \
 && groupmod -g 1000 ${MYSQL_CONTAINER_GROUP}
