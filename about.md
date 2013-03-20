---
layout: page
title: "About"
description: ""
group: navigation
---
{% include JB/setup %}

## Background

Contemporary bioscience often demands vast sample sizes and there may be no choice but to synthesise data across several studies and to undertake an appropriate pooled analysis. This same need is also faced in health-services and socio-economic research. When a pooled analysis is required, analytic efficiency and flexibility are often best served by combining the individual-level data from all sources and analysing them as a single large data set. But ethico-legal constraints, including the wording of consent forms and privacy legislation, often prohibit or discourage the sharing of individual-level data, particularly across national or other jurisdictional boundaries. This leads to a fundamental conflict in competing public goods: individual-level analysis is desirable from a scientific perspective, but is often hindered or proscribed by ethico-legal considerations that are both important and valid.
    
## Method

DataSHIELD provides a simple approach to analysing pooled data that circumvents this conflict. This is achieved via parallelized analysis and modern distributed computing and, in one key setting, takes advantage of the convenient properties of the updating algorithm for generalized linear models (GLMs). In effect, rather than pooling individual level data by passing the data themselves to a central analysis centre (AC), the AC instead manages a series of parallel analyses at each of the data sites. But, crucially, the AC never actually sees the data on which that analysis is based - all that is passed back and forth between the data sites and the AC are a series of summary statistics and simple computing commands that enable a meaningful overall analysis to be undertaken but carry no identifying or sensitive information that could place the security of individual study participants at risk.

## Origin

The concept of DataSHIELD was first proposed at a meeting for the DataSHaPER project held in Edinburgh in May 2009 and it has since evolved under the joint umbrellas of P³G (the Public Population Project in Genomics [Genome Canada and Genome Quebec]) and PHOEBE (Promoting Harmonization of Epidemiological Biobanks in Europe [EU Framework 6]). Ongoing development work currently involves: University of Leicester (UK), McGill University (Canada), University of Ottowa (Canada), Ontario Institute for Cancer Research (Canada), University of Bristol (UK), University of Groningen (Netherlands), International Prevention Research Institute (France), Institute of Public Health, Oslo (Norway), and Statistics Canada.

## Future development

Since starting this program of work we have found that a similar approach has previously been proposed in the Technometrics literature. Like the technometrics researchers, we have realised that DataSHIELD can be used in at least two distinct settings. Thus, initial work has focused on analysing data sets that are horizontally partitioned (the data that need to be synthesised - outcomes, explanatory variables and confounders - are all available in each of the studies that are to be pooled, but on different individuals). But current work also focuses on vertically partitioned data where different data are available on the same individuals in the various studies to be pooled. This latter setting arises, for example, if researchers working on a cohort study wish to link to a governmental data base to extract additional data on study members enabling those new data to be incorporated into an analysis but without the potentially sensitive raw data having to leave the governmental data base.

## Further details

The fundamental concept and detailed mathematical methods underlying DataSHIELD are now described in an Oxford Open Access article freely available through the International Journal of Epidemiology (see free-access links below). Although at present (July 2010) DataSHIELD is no more than a concept, funding has already been obtained to implement it properly as an integral component of the OBiBa open source suite of software for genomic epidemiology. This work will form one element of the BioSHaRE-EU project funded under Framework-7 of the European Union. Work on DataSHIELD under this project will commence in January 2011.
