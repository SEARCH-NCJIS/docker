# 
# Unless explicitly acquired and licensed from Licensor under another license, the contents of
# this file are subject to the Reciprocal Public License ("RPL") Version 1.5, or subsequent
# versions as allowed by the RPL, and You may not copy or use this file in either source code
# or executable form, except in compliance with the terms and conditions of the RPL
#
# All software distributed under the RPL is provided strictly on an "AS IS" basis, WITHOUT
# WARRANTY OF ANY KIND, EITHER EXPRESS OR IMPLIED, AND LICENSOR HEREBY DISCLAIMS ALL SUCH
# WARRANTIES, INCLUDING WITHOUT LIMITATION, ANY WARRANTIES OF MERCHANTABILITY, FITNESS FOR A
# PARTICULAR PURPOSE, QUIET ENJOYMENT, OR NON-INFRINGEMENT. See the RPL for specific language
# governing rights and limitations under the RPL.
#
# http://opensource.org/licenses/RPL-1.5
#
# Copyright 2012-2016 Open Justice Broker Consortium
# 


FROM ojbc/idp

MAINTAINER Open Justice Broker Consortium "http://www.ojbc.org"


WORKDIR /tmp

#RUN apt-get install mysql-server libmysql-java

RUN cp /opt/tomcat/lib/tomcat-jdbc.jar /opt/shibboleth-idp/edit-webapp/WEB-INF/lib
COPY files/JAAS_relational_login.jar /opt/shibboleth-idp/edit-webapp/WEB-INF/lib
COPY files/mysql-connector-java-8.0.11.jar /opt/shibboleth-idp/edit-webapp/WEB-INF/lib
COPY files/mysql-connector-java-8.0.11.jar /opt/tomcat/lib
COPY files/jaas.config /opt/shibboleth-idp/conf/authn
COPY files/password-authn-config.xml /opt/shibboleth-idp/conf/authn
COPY files/attribute-resolver.xml /opt/shibboleth-idp/conf/attribute-resolver.xml
#COPY files/idp-signing.* /opt/shibboleth-idp/credentials/
#COPY files/Shibboleth-Metadata.xml /opt/shibboleth-idp/metadata/Shibboleth-Metadata.xml
#COPY files/idp.properties /opt/shibboleth-idp/conf/idp.properties
#COPY files/metadata-providers.xml /opt/shibboleth-idp/conf/metadata-providers.xml
#COPY files/attribute-filter.xml /opt/shibboleth-idp/conf/attribute-filter.xml

#COPY files/ldap.properties /opt/shibboleth-idp/conf/ldap.properties