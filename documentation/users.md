---
layout: page
title: "Users Documentation"
tagline: "How to perform DataSHIELD analysis"
---
{% include JB/setup %}

DataSHIELD users will connect to a set of Opals and perform some DataSHIELD analysis.

## Overview

* [Prerequisites](#clientsetup)
* [Usage](#clientusage)

<a name="clientsetup"> </a>
## Prerequisites

R must be installed on the client side.

See: [Download and Install R](http://cran.r-project.org/)

A harmonized dataset is distributed in different Opal servers. At least 'View dictionary and summaries' is granted to the user on the corresponding tables in each Opal server.

See: 
* [Import Data in Opal](http://wiki.obiba.org/display/OPALDOC/Working+with+Datasources#WorkingwithDatasources-ImportData)
* [Table Permissions in Opal](http://wiki.obiba.org/display/OPALDOC/Table+Details#TableDetails-Permissions)

You have been also granted DataSHIELD user permission in each of the Opal servers.

See: [Opal DataSHIELD Permissions](http://wiki.obiba.org/display/OPALDOC/DataSHIELD+Administration#DataSHIELDAdministration-Permissions)

<a name="clientusage"> </a>
## Usage

From a R console you will need to install the DataSHIELD client package and its dependencies, [datashieldclient](https://github.com/datashield/datashieldclient):

	install.packages('datashieldclient', repos=c(getOption('repos'), 'http://cran.obiba.org'), dependencies=TRUE)

Windows users will have to explicitly install package dependencies.

See: [Opal R Client Set Up](http://wiki.obiba.org/display/OPALDOC/Opal+R+and+DataSHIELD+User+Guide#OpalRandDataSHIELDUserGuide-Client-sideInstallation)

Then follow instructions to perform DataSHIELD analysis within Opal.

See: [Opal DataSHIELD Usage](http://wiki.obiba.org/display/OPALDOC/Opal+R+and+DataSHIELD+User+Guide#OpalRandDataSHIELDUserGuide-DataSHIELDUsage)

