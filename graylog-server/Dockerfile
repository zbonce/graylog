FROM graylog/graylog:2.4.0-1

RUN  cd / && wget http://geolite.maxmind.com/download/geoip/database/GeoLite2-City.tar.gz \
     && tar -xf GeoLite2-City.tar.gz   \ 
     && rm -fr GeoLite2-City.tar.gz    \
     && cd /GeoLite*                   \
     && mkdir /etc/graylog/server/ -p  \
     && cp GeoLite2-City.mmdb /etc/graylog/server/  \
     && rm -fr /GeoLite* 
