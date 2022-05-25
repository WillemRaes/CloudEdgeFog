Cloud, Edge and Fog Computing
===================================


Cloud Computing
-----------------------------------
Cloud computing is the well established computing paradigm where the main goal is to enable ubiquitous and on-demand network access
to a shared pool of computing resources which can be rapidly provisioned and released with minimal management effort or service provider interaction.
An essential characteristic of cloud computing is that it eliminates the need of on-premise computing infrastructure and its maintenance and management.
Opposite to cloud computing and thus having all IT infrastructure on-premise has as a consequence that all responsibility regarding service availability, security and updates
is up to the in-house IT team.      

Cloud computing offers solutions according to the following service models:

- Infrastructure as a service (IaaS)

In the Infrastructure as a service model, the third party provider enables you to use computing infrastructure such as storage and virtualization, scalable on-demand and accessible via the internet.
Setting up software and services such as operating systems, middleware, applications,.. is the responsibility of the user while the provider gives you access to the management of the infrastructure, typically via 
an Application Programming Interface (API) or a dashboard. IaaS is a very flexible, low overhead and typically low-cost model.  

- Platform as a service (PaaS)

In the Platform as a service model the provider hosts the hardware and software on its own infrastructure and delivers this set of services as an integrated platform to the user which can use it
via an internet connection. This model is particularly of interest for developers as it allows them to develop, run and manage applications without having to build and maintain the infrastructure platform
usually associated with this process. The environment to build and deploy is provided with the platform.


- Software as a service (SaaS) 

Software as a service is the most comprehensive form of cloud computing as it delivers entire applications which are managed by the provider.
Software updates, bug fixes and general management of the infrastructure is all handled by the provider. SaaS is a good option for small businesses which have no in-house IT staff or available bandwidth to 
handle things such as software installation, updates and general management. 



Edge Computing 
-----------------------------------
Edge computing is the practice of deploying computing resources in close proximity to the data source upon which has to be processed. The emergence of the Internet of Things (IoT) and applications using artificial intelligence and machine learning
have drastically increased the significance and need of computing in the edge of the network. Edge computing offers solutions for scenarios where latency is essential and can avoid that large volumes of data have to be sent to 
the cloud before any analytics and decision making can happen. It can also improve the scalability of applications where massive datastreams, such as IoT sensor streams, have to be handled and processed with some time constraint  

There are different types of 'edge' which typically denote how close the processing of data occurs to its source.

- On Edge server

In some applications edge computing refers to processing data and performing analytics on a set of edge servers which are physically present at the site. One such case could be an industrial plant that has deployed 
sensor networks for monitoring operations, safety and security. Deploying the infrastructure on site or in close proximity to the site has several benefits in terms of latency, robustness against network outages of providers and ensures 
full data sovereignty.   

- On-Device

Edge computing can also refer to computing the data on the data source itself. This could be the case for mobile devices or wearables that do not have continous network access and that monitor certain metrics such as health parameters
or environmental data in remote areas. In such cases, it can be essential that the analytics and decision making happens on-device and with very low latency.   

- Distributed edge computing

In the distributed edge computing model, several components in the edge infrastructure share the load of the required computations in order to optimally utilze the available resources in the local network. 
An example of such a setup could be AR/VR system that offloads some computations to dedicated hardware, which is installed in close proximity, to ensure that the latency is kept at a minimum



Fog Computing
-----------------------------------
Both Cloud computing and edge computing are essential for future technologies and applications. Fog computing is a new paradigm that operates in between the cloud, edge and for example IoT data sources 
with the intent of enhancing the integration of cloud, edge and IoT. Fog computing adopts a distributed approach originating from the edge computing model to overcome the limitations of the centralized cloud computing approach, 
with fog nodes positioned anywhere between cloud and end devices. Essential features of fog computing are:

- Allowing for low latency when needed.

- Save network bandwidth and limit data transfers.

- Support user mobility.

- Geographically wide distribution and thus decentralized.

- Scalability.

- Seamless interoperability and federation

Several architectures exist for describing how to deploy fog computing systems in a standardized way (openfog)

A general description is given by the OpenFog N-tier architecture where the generic elements in the architecture are endpoints, fog nodes and the cloud.
On top of that multiple layers of fog nodes (N-tiers) can exist and form the fog layer. Fog nodes can be categorized based on their closeness to the cloud and endpoints:

- Lowest tier: Focus on acquisition, normalization and collection of data from sensors.
- Intermediate tier: Filtering, compressing and altering of data received from the bottom nodes.
- Highest tier: aggregating data, knowledge distillation and decision making. 
