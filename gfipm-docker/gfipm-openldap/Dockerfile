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


FROM dinkel/openldap

# docker run -d -p 1389:389 --name=pf-openldap -e SLAPD_PASSWORD=password -e SLAPD_DOMAIN=ldap.example.org pf-openldap
# docker run -d -p 389:389 --name=openldap -e SLAPD_PASSWORD=password -e SLAPD_DOMAIN=search.gfipm.org dinkel/openldap


RUN mkdir -p /etc/ldap.dist/prepopulate

# run ldif files that start with zero always (note that openldap will execute them in alpha order)
COPY files/0*.ldif /etc/ldap.dist/prepopulate/

# run ldif files that start with 9 last, and separately (so you can comment this out if you want)
#COPY files/9*.ldif /etc/ldap.dist/prepopulate/