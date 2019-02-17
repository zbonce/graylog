FROM graylog/graylog:2.5.1-4
#FROM graylog/graylog:3.0.0

USER root

RUN  apt-get update \
     && apt-get install -y wget

RUN  cd / && wget http://geolite.maxmind.com/download/geoip/database/GeoLite2-City.tar.gz \
     && tar -xf GeoLite2-City.tar.gz   \
     && rm -fr GeoLite2-City.tar.gz    \
     && cd /GeoLite*                   \
     && mkdir /etc/graylog/server/ -p  \
     && cp GeoLite2-City.mmdb /etc/graylog/server/  \
     && rm -fr /GeoLite*