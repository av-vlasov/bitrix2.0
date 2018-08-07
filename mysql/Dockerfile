FROM mariadb

MAINTAINER skazochnik2007

ADD my.cnf /etc/mysql/conf.d/my.cnf
RUN apt-get -y install rsync galera

CMD ["mysqld"]

EXPOSE 3306
