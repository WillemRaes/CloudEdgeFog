Decision metrics  for Cloud VS Edge 
======================================

Timing aspects
--------------------------------------
One very important :cite:p:`nvidiaedgecloudblog`set of metrics that have a large impact on the decision whether an application should be deployed in the cloud or as some form of edge computing are the timing requirements.
Many use cases exist where data streams must be processed within strict timing constraints to ensure proper functionality of the application.

Parameters that express these requirements are:

- Latency 

Real-time inference is crucial in many applications and the latency requirements can have a decisive impact on the question whether to deploy computing infrastructure in the edge or in the cloud.
Applications such as real-time video processing or voice recognition are examples where sending the data to the cloud before processing, introduces unacceptable delays in the application. In such cases, the computations
should take place in close proximity to or on the data acquisition device to ensure low latency and independence of a network connection. A simple example illustrating the problem could be to imagine an autonomous vehicle
travelling on a highway at 120 km/hour. If it would rely on some cloud service for its decision making logic which realistically can introduce an average network latency of 200 ms, then the distance travelled 'blind' would be 6.67 metres.    

Other applications which require batch processing of for example aggregated video or voice data, are not bound by strict timing requirements and thus can rely on centralized cloud infrastructure to efficiently process and store the data.
In such situations, a cloud solution is preferred as this is easily scalable, always accessible and easy to maintain.      

- Jitter

Another timing metric that is important in the decision process of where to put computing infrastucture is the jitter or variability in the time interval between when processed updates are available for evaluation.
Time sensitive applications may also require a very deterministic update rate next to a low latency when processing data. One such example is a real-time localization system that may impose the requirement of having new location updates within at most 10 ms of each other to ensure good performance for a location-based service such as navigation. If variability on the update rate is allowed for a specific use case, then one could opt for a centralized infrastructure in the cloud.    


- Responsiveness

Closely related to latency is responsiveness. In many applications where for example user input is involved, it could be imperative to ensure a high responsiveness. For typical web applications this is not always critical and thus deploying these in the cloud has many advantages. However in some cases where for example a critical process has to be monitored it could be beneficial to have the computing infrastructure close to the data source.   


Data aspects
--------------------------------------
Another very important set of metrics are related to the data that is generated in an application. Having computing infrastructure close to the data source is beneficial to reduce the ingest bandwidth to the cloud and can make a system more scalable. In many applications it could be that not all data that is acquired, in for example a huge sensor network, is of importance or holds no new valuable information. In such situations many useless data transfers to a cloud service can be avoided by deploying data processing and analytics in the edge of the network, thus only initiating data transfers when it is worth reporting. Adding further intelligence in the edge of the network could be of interest for filtering raw massive sensor streams and extracting the interesting features of the data which in turn are then reported to a cloud service. 

This type of architecture leads to a more efficient system in terms of computing and amount of require data transfers. However it should also be noted that adding intelligence at multiple locations in the edge also introduces additional complexity in maintenance as not all computing and processing is centralized at a single location. Furthermore, preprocessing data streams close to the source and only transfering interesting features or filtered data has as a consequence that parts of the available information in the raw data eventually are lost and do not get stored at a cloud service for future post processing. This is very disadvantageous if in the future new algortihms or processing methods emerge that could yield new insights because the raw data is not available. Aggregating all the data sources in the cloud does ensure that future post processing and new methods will always be possible. In some applications where all the data has to be stored, such as in for example tracking the state of assets in manufacturing processes, data preprocessing or filtering has no added value and a centralized method such as a cloud service is preferred.           



Cost Aspects
---------------------------------------
An essential metric for determining whether an architecture using infrastructure in the cloud or edge or a combination of both should be used is the financial cost of deployment and maintenance. Edge computing can bring many valuable additions to applications in terms of latency, reliability and data volume reduction. However it also introduces an additional financial cost. When opting for the deployment of extensive computing infrastructure in the edge, one has to take into account that many considerations regarding hardware choice, amount of resources required, redundancy, maintenance, and which software to use, have to be decided by an in-house engineering and ICT team. When there is no in-house development and engineering present in a company the initial investment in edge computing infrastructure will be very high relative to using a cloud service. The maintenance of the hardware and software components that are deployed are the responsibility of the company and introduces significant costs. In this regard using cloud services is much more flexible as the service provider is specialized in delivering computing infrastructure and one can easily scale and the setup phase and configuration is much less time consuming. Furthermore, using a cloud service is also much less error prone as this equipment and software have been thoroughly tested and have been proven to be reliable, eliminating possible additional costs when errors occur in setting up edge computing infrastructure by oneself. The decision for cloud computing, edge computing, or a hybrid solution should definitely take into account all the costs related to setup and maintenance and weigh them against quality of service, flexibility, reliability and requirements such as full data sovereignty, low latency and more.        


Privacy and security aspects
---------------------------------------
