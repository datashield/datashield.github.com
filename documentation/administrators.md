---
layout: page
title: "Administrators Documentation"
tagline: "How to administrate DataSHIELD set up"
---
{% include JB/setup %}

As a DataSHIELD administrator, you are responsible for:
* installing DataSHIELD packages in R server,
* publishing DataSHIELD aggregation and assignment methods.

## Overview

* [Prerequisites](#serversetup)
* [Usage](#adminusage)

<a name="serversetup"> </a>
## Prerequisites

A Opal server is up and running.

See: [Opal Server Administrator Guide](http://wiki.obiba.org/display/OPALDOC/Opal+Server+Administrator+Guide)

The Opal server must be backed by a R server in which data will be pushed from Opal for being aggregated.

See: [Opal R Server Set Up](http://wiki.obiba.org/display/OPALDOC/Opal+R+and+DataSHIELD+User+Guide#OpalRandDataSHIELDUserGuide-ServersideInstallation)

You have been granted DataSHIELD administrative permission in that Opal server.

See: [Opal DataSHIELD Permissions](http://wiki.obiba.org/display/OPALDOC/DataSHIELD+Administration#DataSHIELDAdministration-Permissions)

<a name="adminusage"> </a>
## Usage

Opal provides a web interface for performing those administration tasks.

See:
* [DataSHIELD Packages Administration in Opal](http://wiki.obiba.org/display/OPALDOC/DataSHIELD+Administration#DataSHIELDAdministration-Packages)
* [DataSHIELD Methods Administration in Opal](http://wiki.obiba.org/display/OPALDOC/DataSHIELD+Administration#DataSHIELDAdministration-Methods)

You can also use R to administrate one or several Opal servers DataSHIELD configurations: *opaladmin* R package provides the Opal administration toolbox.

	install.packages('opaladmin', repos=c(getOption('repos'), 'http://cran.obiba.org'), dependencies=TRUE)

All the functions starting with `dsadmin.` are meant to administer DataSHIELD configuration. The following example installs a DataSHIELD-R package and publish its methods:

	# Login in Opal
	library(opaladmin)
	o<-opal.login('dsadmin', 'password', 'https://some-opal-host:8443',opts=list(ssl.verifyhost=0,ssl.verifypeer=0,sslversion=3))

	# Install dsbase package on R server
	dsadmin.install_package(o, 'dsbase')

	# Configure datashield methods in opal
	# Clean all methods
	dsadmin.rm_methods(o)
	# Publish dsbase package methods
	dsadmin.set_package_methods(o, 'dsbase')
