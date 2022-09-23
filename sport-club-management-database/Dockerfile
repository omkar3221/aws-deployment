FROM mysql
ENV MYSQL_ROOT_PASSWORD "omkar7218"
ENV MYSQL_DATABASE "sportclub"
COPY sportclub.sql /docker-entrypoint-initdb.d
COPY my.cnf /etc/mysql/my.cnf
EXPOSE 3306 
