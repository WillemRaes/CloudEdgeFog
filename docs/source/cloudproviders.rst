Typical Cloud Service Providers
======================================

Introduction
--------------

This report lists the different available cloud
services with a focus on computing capabilities and Machine
Learning (ML). The current range of cloud services has already expanded tremendously and new services continue to be added to the already wide range of providers.
In addition, services are called differently by different providers. Since it is
impossible to cover all the services offered, this document will focus on the the main providers and their main services,
specifically in the compute and machine learning categories. 
However, in addition to the discussed services in these categories, these providers offer a wide range of miscellaneous services in different
categories including file storage, database management, network management, 
backup services, Internet of Things, developer tools, etc.

In particular, Amazon Web Services (AWS), Microsoft Azure and Google Cloud are
currently the largest players in the field of cloud services. Gartner,
an international IT research and consulting firm, ranks 
cloud service providers in a quadrant as shown in
Figure `1 <#fig:gartner>`__ . In it, it is
clearly seen that AWS, Microsoft Azure and Google Cloud are currently the 
market leaders in terms of cloud service providers.


Different Cloud Ecosystems for Computing
---------------------------------------------

Amazon Web Services (AWS)
-------------------------
Amazon Web Services was founded in 2002 and has since become the
most prominent market leader in the cloud computing industry.


Compute
~~~~~~~

- Amazon Elastic Compute Cloud (EC2): EC2 is
  the premier cloud computing platform in the extensive lineup of
  Amazon. EC2 allows users to run their code and applications 
  in the cloud on virtual machines, which Amazon calls "instances".
  The number of active instances can be scaled dynamically
  according to the current demand for computing capacity. This can be done either
  manually or automatically with the help of Amazon EC2
  Auto-Scaling. Currently 352 possible instances are offered with
  different configurations according to the number of vCPUs, memory capacity, 
  storage medium and network speed. The following categories of instance 
  types are offered:

   - General purpose: balanced instance type with similar performance
      in terms of compute, memory and network functionality.

   - Compute Optimized: instance type optimized for applications
     that are strongly compute-bound and thus benefit greatly from
     the higher processor processing power

   - Memory Optimized: instance type optimized for performance
     for workloads that work with large amounts of data in the
     memory

   - Accelerated Computing: instance type where hardware acceleration is 
     present to speed up operations such as graphics processing

   - Storage Optimized: instance type optimized for applications with a high number of read/write accesses
     with a high number of read/write accesses in local memory

   
   Prices scale according to the specifications of the instances and
   also vary by region. The AWS Free Tier offers 750 hours of free compute
   capabilities on *t2.micro* or *t3.micro* instances with
   respectively :math:`1` and :math:`2` vCPUs and :math:`1` GB
   memory capacity. On-demand instances are billed by the hour
   or per second. For use cases
   where starting and stopping can be flexible, there is also the
   possibility to use spare capacity at reduced prices,
   So-called spot instances can be up to
   90% cheaper compared to on-demand instances.
   Savings Plans offer the possibility to use
   prices when booking EC2 for a term of
   1` or 3` years, but booking for 3 years is
   a risky choice since new types of instances are constantly being 
   added and the prices of old instances are falling. Old instances do remain in the supply
   to ensure backward compatibility, but do not offer any
   interesting performance for the price asked.


AI and Machine Learning
~~~~~~~~~~~~~~~~~~~~~~~~

-  Amazon SageMaker: Fully cloud
   machine-learning platform that allows users to
   create, train and deploy ML models. Allows to work with ML models at different
   levels of abstraction. Developers can
   use pre-trained models on their own data, train built-in models or
   or develop models from scratch.
   SageMaker includes several tools to, among others, prepare data for use, build and train models, and finally deploy them in the cloud.

Microsoft Azure
---------------

.. _compute-1:

Compute
~~~~~~~

-  Azure Compute - Virtual Machine series: Microsoft also offers a wide variety of
   of cloud computing services, which therefore also includes
   virtual machines in the cloud. Like Amazon, Microsoft offers the
   ability to dynamically scale the number of VMs required
   by means of Azure Virtual Machine Scale Sets.

   Microsoft divides its virtual machines into different series
   

   - A series: 'Affordable entry-level VMs for development and
     testing": CPU performance and memory configuration for entry-level workloads.

   - Bs series: 'Economical VMs with burst functionality': VMs for workloads
     that typically require low CPU utilization but can handle significantly higher
     CPU utilization as demand increases

   - D-Series: "General Purpose": Balanced combination of
     vCPUs, memory and temporary storage that can meet the
     requirements of most production workloads

   - E-Series: 'Optimized for in-memory Hyper-Threaded
     applications": VMs optimized for demanding in-memory
     applications, ideal for example relational database servers

   - F Series: 'Optimized Virtual Machines': VMs
     optimized for CPU intensive workloads equipped with
     :math:`2` GB RAM and :math:`16` GB local SSD storage per CPU core

   - G-Series: 'Virtual machines with optimized memory and storage': Upgrade from the D-Series general-purpose machines with
     twice the memory and four times the SSD storage.

   - H-Series: 'Virtual machines for high-performance computing': VMs optimized for HPC applications

   - Ls series: 'Virtual machines with optimized storage': VMs
     optimized for storage using local NVMe storage,
     delivering high throughput at low latencies

   - M-series: 'Virtual machines optimized for memory': 'VM'
     optimized for memory, ideal for in-memory workloads

   - Mv2 series: 'Largest virtual machines optimized for
     memory': Series with by far the largest possible
     memory capacity

   - N Series: 'Virtual machines with GPU': VMs with GPU computing
     capabilities, for both graphics-intensive applications and HPC
     and machine learning applications. Also offer the possibility for
     InfiniBand connection

   Prices also vary depending on the types of virtual
   machines. It is also possible to use a free
   Azure account. Users then receive
   USD 200` credit to test Azure services for
   ` math:`30` days, and get :math:`12` months of free access to
   a number of popular services, including :math:`750` hours of access to
   VMs in the B1S series with :math:`1` vCPUs, :math:`1` GB RAM and
   :math:`4` GB memory capacity. In addition, services such as
   file storage, database applications, and various AI services can also be
   tested for free for a limited number of uses.
   It is possible to pay per second of use with billing per
   minute. Spot is also available for workloads that are not time-critical
   to be carried out for significant discounts of up to
   :math:`90` %. Reservation per :math:`1` or :math:`3` years is also
   possible at reduced prices, up to :math:`72` % cheaper, but
   again, it is not recommended to opt for :math:`3` years
   given the rapid evolution of the cloud service market.

.. _ai-en-machine-learning-1:

AI and Machine Learning
~~~~~~~~~~~~~~~~~~~~~~~~

-  Azure AI: Azure AI is a collection of AI services for
   developers and data scientists. It
   provides access to pre-trained models for vision, speech, and language
   using API calls. Furthermore, it allows users to build their own
   machine learning models using, among others,
   Jupyter Notebook and Visual Studio Code, and open-source frameworks
   such as TensorFlow and PyTorch. A number of AI and Machine Learning
   powered services can also be tested through a free Azure account.
   Among them are computer vision, translator, anomaly detection,
   automatic form recognizer and text analysis, which are available for a free
   trial for a certain number of uses or transactions.

Google Cloud Services
---------------------

Google offers a comprehensive set of computing services to facilitate ML
facilitation.

.. _compute-2:

Compute
~~~~~~~

- Google Cloud Compute: Like Amazon and Microsoft, Google also offers
  a cloud compute service that allows users to run virtual machines
  on their infrastructure.
  Managed instance groups (MIGs) also allow users to have the number of
  VMs to automatically scale to their needs. Google offers
  following options in virtual machine types by type of workload:

   - General purpose workloads (E2, N2, N2D, N1): Balanced
     combination in terms of price and performance, suitable for a large
     variety of workloads. Available up to
     :math:`224` vCPUs and :math:`896` GB memory storage.

   - Ultra-high memory (M2, M1): Optimized for
     memory intensive workloads with up to :math:`12` TB of storage
     for a single VM instance.

   - Compute-intensive workloads (C2): Highest performance per
     CPU core and optimized for HPC, gaming servers and
     latency-sensitive applications.

   - Most demanding applications and workloads (A2): VMs with
     acceleration hardware present based on the NVIDIA Ampere A100
     Tensor Core GPU. Developed for heavy machine learning workloads
     and HPC.

   - Coming soon:* Scale-out workloads (T2D): New option
     coming soon focused on scaling out workloads for web services, applications and
     of workloads for web services, containerized services and
     etc.

   Users can once again test out the service for free. Free
   accounts will receive :math:`300` USD credit for :math:`90` days to spend on several Google Cloud services 
   and get
   a free *f1-micro* instance with :math:`1` vCPU and :math:`0.6` GB
   memory available per month. However, these are shared-core
   instances whose vCPU is limited to :math:`20` % CPU time,
   but of which short periods :math:`100` % of the vCPU can be used.

.. _ai-and-machine-learning-2:

AI and Machine Learning
~~~~~~~~~~~~~~~~~~~~~~~

- Google Cloud AI: With Google Cloud AI, Google provides users with a
  comprehensive platform for deploying machine learning and AI
  based applications. In this, they distinguish
  :math:`3` major components with some overlap between: AI solutions, AI
  building blocks and Vertex AI. AI solutions is a collection of
  ready-made solutions that can be easily integrated
  within organizations. Within this, Contact Center AI includes
  solutions for text-to-speech and vice versa and natural language
  processing for chatbots, and Document AI provides support for
  document processing and form recognition. AI building blocks is
  a collection of products that developers can use
  to add AI functionality to existing applications.
  Developers can use pre-trained models via the
  API as well as define custom models or
  merge them together to create a custom solution. These AI building
  blocks consist of Sight for image processing, Language for
  for speech recognition and translation, Conversation for text-to-speech and
  speech-to-text and Structured Data for inference based on
  structured data to be performed. Vertex AI is a unified
  AI platform that allows developers and data scientists to deploy ML
  models by code. Popular frameworks such as
  TensorFlow, Keras, PyTorch, SciKit-Learn and Spark are supported
  and there is a range of TPUs and GPUs as acceleration hardware.

IBM Watson
----------

Choice of Cloud service provider
------------------------------------

Making the move to the cloud is very interesting for companies, among other reasons, because of its high cost-effectiveness, scalability and
guaranteed availability.
However, making this decision and choosing a suitable cloud service provider is not a simple undertaking.
First and foremost, the consideration must be made as to whether it is actually
worthwhile to run the application in the cloud. Researchers
at the University of Luxembourg, for example, demonstrated, using a
a cost model, that their in-house HPC platform performs more efficiently
than Amazon EC2 by cost. Although an
in-house solution will almost always perform better than in the cloud,
an in-house computing cluster
can't match the scalability that the cloud offers. On top of that there is also
an additional need for both knowledge, infrastructure and the like
which is not feasible for every enterprise.

A second important choice is the selection of the cloud service
provider. This choice, too, is not so obvious and should
take into account a large number of factors.

A number of studies attempt to make a comparison between the
providers in different areas. The authors
compared the cloud computing offerings of
Amazon and Google between :math:`2014` and :math:`2016`. This showed that
Amazon offered a more extensive range of different VM instances,
while Google offered lower prices for similar instances.
Of course, this study is already quite dated due to the rapid growth in the
cloud computing market. In fact,
the offerings of both providers have changed significantly and both now offer custom VM
instances to meet the specific needs of customers.
It does show how quickly offerings and prices are evolving. According to a
study comparing IoT services from Amazon,
Microsoft and Google in terms of performance, it clearly shows that
that Amazon and Google perform similarly in terms of latency, while
Microsoft performs worse for this use case. In
the number of offered
services offered by Amazon, Microsoft and Google in different categories.
compared. Also compares the offerings of the
largest :math:`3` cloud service providers. The main conclusion
from this and other previous studies is clearly that the **choice of
cloud service provider depends heavily on the interests and needs
of the user**. Thus, it is important that one first
thoroughly defines them and then evaluates the **choice of cloud service
provider for the specific use case**.
