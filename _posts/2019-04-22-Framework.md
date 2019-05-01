---
layout: post
title: A framework for building Marketing analytics reports with Power BI
published: true
---
This post introduces a framework of Power BI code for building marketing analytic reporting

You can [download readily built samples](../Marketing-Analytics-for-download/) for marketing analytics or build your own analytical reports on top of this framework.  

![Framework Hero Image]({{site.baseurl}}/images/Framework-Hero1.png)

# Build custom Marketing Analytics with Power BI

The file repository provides a set of Power BI files (pbx) and respective template files (pbit) that can be used to build your own marketing analytic reports.
The focus of the Power BI code framework is to provide ready built and easy to use data sources that connect to data from Dynamic 365 for Marketing including date filters and on liner query building in M-code to access specific profile and interaction tables. 

## Out of the box connection dialog
The framework provides ready build report parameters which present data entry dialogs to the data analyst who opens a marketing report template file in order to configure and publish marketing analytics in his organization.

![Parameter Dialog]({{site.baseurl}}/images/Framework-ParameterDialog.png)


## Browse the metamodel for profile and interactions types
Each report comes with a set of hidden report pages. Those can help you to browse the available types of profiles in your organization in CDS and all the interaction types that are referenced in the marketing model. You can select interaction types and study the attributes that you will be able to use for analytics reporting. 

![Model Browser]({{site.baseurl}}/images/Framework-MetaBrowser.png)


## Study the available interaction data and data generation over time
Another valuable tool helps to validate the interaction data inflow in your marketing instance as it is reflected in the data arriving in your Azure storage. You can see quickly whether the data are arriving as expected and study which types of interaction data in what volume are being captured over time.
This helps to select the use cases for marketing analytics, but also to troubleshoot the marketing analytic configuration and the processes in your marketing application in general.           

![Interaction data]({{site.baseurl}}/images/Framework-InteractionDataFlow.png)


## Working with queries in Power BI
The framework comes with a rich set of prebuilt queries, functions, parameters and tables that make it really easy to access the data from your marketing instance.
The typical steps for a custom marketing report include to select interaction types that may be loaded and add queries for the profile and interaction data that should be loaded. Those tasks are well supported and require often just one line of query code per interaction and few desired formatting instructions.


### Configure which interaction data should be considered by the report
Over time a marketing organization will collect large amounts of data, especially interactions that reflect how your audience interacts with your marketing experience, but also a set of signals emitted by the marketing automation engine.

A good praxis is to limit the data to load to only the data that are really necessary for the purpose of the specific marketing analytic report. While the marketer will set the recency for the interactions to consider when he configured the analytics report, it is the duty of the data analyst who creates a marketing analytics report to specify which interactions types should be considered for loading. Limiting the amount of interactions types will greatly improve the refresh performance, because the Power BI code will filter interaction data as early as possible.  

![Limit interaction data load]({{site.baseurl}}/images/Framework-InteractionConfiguration.png)

### Build queries 

![Build interaction queries]({{site.baseurl}}/images/Framework-AddInteractionQueries.png)
