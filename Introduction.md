# Introduction
The main aim of the Open Data Hub is to collect, enrich and provide environmental footprint data to server-side software applications, so that they may determine their own carbon footprint.

## The supply chain of server-side software applications

In today’s digital economy, server-side applications are most often unaware of their supply chain - meaning the server hardware and physical facilities that they are running on. This is mainly due to modern virtualization technologies, which are designed make the physical infrastructure “invisible” to the application developer. 

Over the last decade, the introduction, adoption and further development of virtualization technologies - from new hypervisors to containerization - has led to significant improvements in overall server hardware utilization and efficiency. It has also made life easier for developers, who are now able to tap into a pull of resources (compute, memory, storage and network capacity), rather than having to worry about individual servers.

In order for server-side software applications to determine their own environmental footprint, we now need to connect the dots between the physical environment and its real embedded and operational environmental impact and the virtual machines and containers which are running the individual applications. 

![]()

It’s comparable with the idea of _supply chain transparency_ from many other industries ([here is an example of Sourcemap][1] for the apparel & clothing industry). 

**In the case of server-side software, the supply chain is all the physical infrastructure necessary to provide the resources that the software-application uses to provide a digital product or service to a customer.**

## Definition of Open Data 
_Open data is data that can be freely used, re-used and redistributed by anyone - subject only, at most, to the requirement to attribute and sharealike._

From the [Open Data Handbook][2] by the Open Knowledge Foundation

As an end-state we hope that all data related to the environmental footprints of digital applications & services will eventually become public. However, the basic functionality of the Open Data Hub & Agent (to collect, enrich and provide environmental footprint data from the physical digital infrastructure to server-side software itself) does not require the data to be open.

Data which is collected by the Agents are by default neither public or open, but operate within a single data center or cluster of facilities. Every Agent can opt-in to report to both private data hubs (see Use Cases) or public/open data hub instances.

## The SDIA’s Open Data Hub
To provide transparent data on the environmental impact of the digital sector for researchers, innovators and governments, the SDIA is hosting a global Open Data Hub instance to which every Agent can report data to. This data is also used to track the progress of digital sector towards environmental sustainability (see the SDIA Roadmap for more information).

Agent’s that opt-in to make the environmental footprint data public and apply an open data license, are rewarded with a Transparency Certification by the SDIA.

The SDIA also maintains the enrichment data that is used by the Agents, e.g. emission factors, a database of embedded emissions in server hardware or product passports for data center equipment.

All of the data hosted by the SDIA is available under an open-data license. The underlying open data infrastructure (hub, agents and API specifications) are open source and available for anyone to host their own reporting & measurement systems. 

We also welcome existing vendors of monitoring systems, virtualization environments or data center infrastructure management systems to implement the agent & reporting APIs within their own software.

## Design 

ODH consists of two standalone components:

* An Agent (“Environmental Data Agent”, EDA) which is deployed within physical digital infrastructure (e.g. inside a data center) and provides connectors to both physical as well as IT infrastructure.
* A Hub (“Open Data Hub”, ODH) to which Agents can opt to report to. Also provides APIs for enrichment of the environmental data (e.g. emissions factors) for the Agents as well as public, open data APIs and analytics.

Further any Monitoring or Data Center Infrastructure Management (DCIM) solution may become an EDA by implementing the Agent APIs and support reporting to the Open Data Hub API.

## Use case scenarios 
### Agent-only

A co-location data center may opt to install a single Environmental Data Agent (EDA) within their facility, e.g. on a dedicated server. The EDA can either collect data automatically (from supported systems) or can receive manual data fed via its APIs. This data includes power consumption of ancilliary systems,  such as cooling or lighting as well as information on backup power systems, fuel types, etc. 

The collected data stored & enriched by the EDA is provided as an API within the facility. Servers & host systems (operating-, virtualization- and orchestration-systems) send additional measures (e.g. power consumption of individual servers)  to the EDA via its API. The hosts systems also pass-through the software developer APIs through to the individual applications, so that developers may determine the footprint of their application.

In this scenario, the collected data does not leave the data center facility and is provided to the software application “bottom up”.

### Agent(s) with private data hub

The previous scenario has only a single agent deployed in a single data center facility. By deploying an additional Hub system, data can be aggregated from multiple agents, e.g. across multiple facilities. 

This private hub can than be used for consolidated reporting of environmental footprint data, e.g. to generate ESG reporting or transparency dashboards for customers.

### Agent reporting to Open Data Hub 

Further, an Agent can be configured to report the collected environmental footprint data to any Open Data Hub, e.g. the global transparency & open data hub of the SDIA. Of course reporting to multiple Open Data Hubs is also possible. 

When reporting the data to the Open Data Hub it is possible to anonymize the reported data, so it can not be traced back to a single facility. 

### National Open Data Hubs

Because of the ability to report to multiple Open Data Hubs, it becomes possible to deploy national Open Data Hubs which can be used to create national transparency & reporting efforts - without making the data open. This can be utilized by industry associations or other industry-bodies that support their members in informing governments about their actual environmental footprint. 

### Individual Open Data Hubs

Further, companies may opt to provide their own Open Data Hub for researchers, innovators and governments to access their environmental performance data. This could be applicable for Cloud Providers, Hosting companies or Co-Location providers.

[1]:	https://open.sourcemap.com/maps/embed/5e1cf61670eadf052d12d819
[2]:	https://opendatahandbook.org/guide/en/what-is-open-data/

