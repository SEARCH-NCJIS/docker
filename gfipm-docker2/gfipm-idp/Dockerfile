# 

FROM ojbc/idp

MAINTAINER Open Justice Broker Consortium "http://www.ojbc.org"


WORKDIR /tmp

RUN cp /opt/tomcat/lib/tomcat-jdbc.jar /opt/shibboleth-idp/edit-webapp/WEB-INF/lib

COPY files/password-authn-config.xml /opt/shibboleth-idp/conf/authn
COPY files/attribute-resolver.xml /opt/shibboleth-idp/conf/attribute-resolver.xml
COPY files/idp.properties /opt/shibboleth-idp/conf/idp.properties
COPY files/idp-metadata.xml /opt/shibboleth-idp/metadata
COPY files/ldap.properties /opt/shibboleth-idp/conf/ldap.properties
RUN  /opt/shibboleth-idp/bin/build.sh -DLOCATION=/opt/shibboleth-idp

