# Background
The main aim of the Open Data Hub is to collect, enrich and provide environmental footprint data to server-side software applications, so that they may determine their own carbon footprint.

## The supply chain of server-side software applications

In today’s digital economy, server-side applications are most often unaware of their supply chain - meaning the server hardware and physical facilities that they are running on. This is mainly due to modern virtualization technologies, which are designed make the physical infrastructure “invisible” to the application developer. 

Over the last decade, the introduction, adoption and further development of virtualization technologies - from new hypervisors to containerization - has led to significant improvements in overall server hardware utilization and efficiency. It has also made life easier for developers, who are now able to tap into a pull of resources (compute, memory, storage and network capacity), rather than having to worry about individual servers.

In order for server-side software applications to determine their own environmental footprint, we now need to connect the dots between the physical environment and its real embedded and operational environmental impact and the virtual machines and containers which are running the individual applications. 

![Supply chain of a server-side software application][image-1]

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

[1]:	https://open.sourcemap.com/maps/embed/5e1cf61670eadf052d12d819
[2]:	https://opendatahandbook.org/guide/en/what-is-open-data/

[image-1]:	https://sdialliance.github.io/odh-api-spec/diagrams/simplified-software-supply-chain.jpeg