# Open Data Hub and Environmental Data Agent API Specification

The main aim of the Open Data Hub & Environmental Data Agent is to collect, enrich and provide environmental footprint data to server-side software applications, so that they may determine their own carbon footprint.

## Currently under development 

- This project is being developed by the Sustainable Digital Infrastructure Alliance e.V. (“SDIA”), a global not-for-profit organization based in Germany and the Netherlands.
- It’s governed by the Digital Carbon Footprint Steering Group (needs link) as part of the [SDIA’s roadmap towards sustainable digital infrastructure][1].
- You are welcome to contribute, either via Github (by submitting issues, or pull requests), via our mailing list (link needed) or by joining the steering group (simply send a request to the mailing list)
- The project aims to both define the requirements (metrics, data and APIs) for sever-side application to be able to determine their own footprint as well as provide an implementation of an environmental data agent that can be deployed to collect & provide the required data
- Further the project delivers a blueprint for an Open Data Hub, enabling the environmental footprint data to be shared with researchers and innovators to address the growing environmental impact of the physical infrastructure which powers server-side software and applications.

## Based on OAS 3.0

The current specification is developed using the [OAS 3.0 standard][2] for OpenAPI definitions.

## Design

ODH consists of two standalone components:

* An Agent (“Environmental Data Agent”, EDA) which is deployed within physical digital infrastructure (e.g. inside a data center) and provides connectors to both physical as well as IT infrastructure.
* A Hub (“Open Data Hub”, ODH) to which Agents can opt to report to. Also provides APIs for enrichment of the environmental data (e.g. emissions factors) for the Agents as well as public, open data APIs and analytics.

Further any Monitoring or Data Center Infrastructure Management (DCIM) solution may become an EDA by implementing the Agent APIs and support reporting to the Open Data Hub API.

[1]:	https://sdia.io/roadmap
[2]:	https://swagger.io/specification/