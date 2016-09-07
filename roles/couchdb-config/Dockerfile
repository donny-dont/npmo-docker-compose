FROM bcoe/confd

ADD npm.toml /etc/confd/conf.d/
ADD npm.ini.tmpl /etc/confd/templates/

RUN mkdir -p /usr/local/etc/couchdb/local.d
VOLUME /usr/local/etc/couchdb/local.d
