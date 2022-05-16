Decision metrics  for Cloud VS Edge 
======================================

Timing aspects
--------------------------------------
One very important set of metrics that have a large impact on the decision whether an application should be deployed in the cloud or as some form of edge computing are the timing requirements.
Many use cases exist where data streams must be processed within strict timing constraints to ensure proper functionality of the application.

Parameters that express these requirements are:

- Latency 
Real-time inference is crucial in many applications and the latency requirements can have a decisive impact on the question wether to deploy computing infrastructure in the edge or in the cloud.
Applications such as real-time video processing or voice recognition are examples where sending the data to a cloud before processing introduces unacceptable delays in the application. In such cases the computations
should take place in close proximity to or on the data acquisition device to ensure low latency and independence of a network connection. A simple example illustrating the problem could be to imagine a autonomous vehicle
travelling on a highway at 120 km/hour. If it would rely on some cloud service for its decision making logic which realistically can introduce an average network latency of 200 ms, then the distance travelled 'blind' would be 6.67 metres.    

Other applications which require batch processing of for example aggregated video or voice data, are not bound by strict timing requirements and thus can rely on centralized cloud infrastructure to effciently process and store the data.
In such situations a cloud solution is preferred as this is easily scalable, always accessible and easy to maintain.      

- Jitter

- responsiveness


Data aspects
--------------------------------------
Another very important set of metrics are related to the data



Cost Aspects
---------------------------------------



Privacy aspects
---------------------------------------