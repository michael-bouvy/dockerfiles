FROM        debian:wheezy
MAINTAINER  Michael BOUVY <michael.bouvy@gmail.com>

RUN         apt-get update && DEBIAN_FRONTEND=noninteractive apt-get -y install adduser openjdk-7-jre-headless
ADD	    https://download.elasticsearch.org/elasticsearch/elasticsearch/elasticsearch-0.90.10.deb /tmp/elasticsearch.deb
RUN         dpkg -i /tmp/elasticsearch.deb

EXPOSE      9200
CMD         ["/usr/share/elasticsearch/bin/elasticsearch", "-f"]
