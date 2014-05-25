---
layout: home
title: DataSHIELD!
tagline: Data Aggregation Through Anonymous Summary-statistics from Harmonized Individual-levEL Databases
---
{% include JB/setup %}

DataSHIELD ([Wolfson et al., 2010](http://ije.oxfordjournals.org/content/39/5/1372.abstract)) is a novel method that enables a pooled data analysis to be carried out across several collaborating studies as if one had full access to all of the data from individual participants that might be needed, but, in reality, these data remain completely secure on their host computer at the home base of the study where they were collected or generated. DataSHIELD therefore permits a fully efficient pooled analysis to be undertaken of biomedical data from several studies, even when ethico-legal or other governance restrictions prohibit the release of individual-level data to third parties.

[Read Using DataSHIELD](/documentation)

### Overview of a DataSHIELD setting

The following figure illustrates a typical DataSHIELD setting for a pooled individual-level analysis; it reflects a hypothetical implementation based on a pooled analysis involving data from six studies. The individual-level data that provide the basis of the analysis remain on *data computers* (DCs) at their home bases. An additional computer is identified as the *analysis computer* (AC). This is the computer on which the primary statistician will type the commands to enact and control the pooled analysis.

![DataSHIELD](images/overviewSixStudies.png "DataSHIELD")

A DataSHIELD method open source implementation is available based on [R](http://www.r-project.org/) and [Opal](http://wiki.obiba.org/display/OPALDOC), the [OBiBa](http://obiba.org)'s data warehouse solution for biobanks.

### DataSHIELD IT Infrastructure

The following figure illustrates the basic IT infrastructure that underpins DataSHIELD. The IT infrastructure required to carry out a DataSHIELD analysis comprises three main components:
a computer server hosting a database (Opal), a statistical programming environment (R) and DataSHIELD R libraries installed on the servers and on the client computer. Opal is a core database
application for biobanks and epidemiological studies developed by the Maelstrom Research group in collaboration with OBiBa, an international software development project aimed at building open
source software for biobanks. 
* on the Data Computers:
  * an Opal server (with its database(s)),
  * an R server.
* on the Analysis Computer: an R client.

![DataSHIELD Opal](images/opal-implementation.png "DataSHIELD Opal")

Opal's role is to:
* authenticate and authorize DataSHIELD users,
* push data into R (server side),
* control which methods can be executed in R (server side).

[Read more about DataSHIELD, R and Opal](http://wiki.obiba.org/display/OPALDOC/Opal+R+and+DataSHIELD+User+Guide)

### License

DataSHIELD and OBiBa softwares are open source and made available under the [GPL3 licence](http://www.gnu.org/copyleft/gpl.html#gnu-license). DataSHIELD and OBiBa softwares are free of charge.
