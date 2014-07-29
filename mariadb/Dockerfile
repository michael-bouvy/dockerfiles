FROM        debian:wheezy
MAINTAINER  Michael BOUVY <michael.bouvy@gmail.com>

RUN         apt-get update && DEBIAN_FRONTEND=noninteractive apt-get -y install adduser libaio1
ADD         mariadb-10.0.12-linux-x86_64.tar.gz /usr/local/
WORKDIR     /usr/local
RUN         ln -s mariadb* mysql
RUN         groupadd mysql && useradd -g mysql mysql
WORKDIR     /usr/local/mysql
RUN         chown -R mysql:mysql .
RUN         scripts/mysql_install_db --user=mysql
RUN         chown -R root . && chown -R mysql data

EXPOSE      3306
CMD         ["bin/mysqld_safe", "--skip-grant", "--user=mysql"]
