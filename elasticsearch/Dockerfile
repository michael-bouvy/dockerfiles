FROM        debian:wheezy
RUN         apt-get update
RUN         apt-get -y install wget ca-certificates adduser openjdk-7-jre-headless
RUN         wget https://download.elasticsearch.org/elasticsearch/elasticsearch/elasticsearch-0.90.10.deb
RUN         dpkg -i elasticsearch-0.90.10.deb	

EXPOSE      9200
CMD         ["/usr/share/elasticsearch/bin/elasticsearch", "-f"]
