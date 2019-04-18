# 

FROM ojbc/idp

MAINTAINER Open Justice Broker Consortium "http://www.ojbc.org"


WORKDIR /tmp

RUN cp /opt/tomcat/lib/tomcat-jdbc.jar /opt/shibboleth-idp/edit-webapp/WEB-INF/lib

COPY files/attribute-filter.xml /opt/shibboleth-idp/conf/attribute-filter.xml
COPY files/attribute-resolver.xml /opt/shibboleth-idp/conf/attribute-resolver.xml
COPY files/CTF.xml /opt/shibboleth-idp/metadata/CTF.xml
COPY files/idp-metadata.xml /opt/shibboleth-idp/metadata
COPY files/idp-signing.* /opt/shibboleth-idp/credentials/
COPY files/idp.properties /opt/shibboleth-idp/conf/idp.properties
COPY files/ldap.properties /opt/shibboleth-idp/conf/ldap.properties
COPY files/login.vm /opt/shibboleth-idp/views
COPY files/metadata-providers.xml /opt/shibboleth-idp/conf
COPY files/password-authn-config.xml /opt/shibboleth-idp/conf/authn
#RUN  /opt/shibboleth-idp/bin/build.sh -DLOCATION=/opt/shibboleth-idp

