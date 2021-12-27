# Use Case Scenarios

## Agent-only

A co-location data center may opt to install a single Environmental Data Agent (EDA) within their facility, e.g. on a dedicated server. The EDA can either collect data automatically (from supported systems) or can receive manual data fed via its APIs. This data includes power consumption of ancilliary systems,  such as cooling or lighting as well as information on backup power systems, fuel types, etc. 

The collected data stored & enriched by the EDA is provided as an API within the facility. Servers & host systems (operating-, virtualization- and orchestration-systems) send additional measures (e.g. power consumption of individual servers)  to the EDA via its API. The hosts systems also pass-through the software developer APIs through to the individual applications, so that developers may determine the footprint of their application.

In this scenario, the collected data does not leave the data center facility and is provided to the software application “bottom up”.

## Agent(s) with private data hub

The previous scenario has only a single agent deployed in a single data center facility. By deploying an additional Hub system, data can be aggregated from multiple agents, e.g. across multiple facilities. 

This private hub can than be used for consolidated reporting of environmental footprint data, e.g. to generate ESG reporting or transparency dashboards for customers.

## Agent reporting to Open Data Hub

Further, an Agent can be configured to report the collected environmental footprint data to any Open Data Hub, e.g. the global transparency & open data hub of the SDIA. Of course reporting to multiple Open Data Hubs is also possible. 

When reporting the data to the Open Data Hub it is possible to anonymize the reported data, so it can not be traced back to a single facility. 

## National Open Data Hubs

Because of the ability to report to multiple Open Data Hubs, it becomes possible to deploy national Open Data Hubs which can be used to create national transparency & reporting efforts - without making the data open. This can be utilized by industry associations or other industry-bodies that support their members in informing governments about their actual environmental footprint. 

## Individual Open Data Hubs

Further, companies may opt to provide their own Open Data Hub for researchers, innovators and governments to access their environmental performance data. This could be applicable for Cloud Providers, Hosting companies or Co-Location providers.
