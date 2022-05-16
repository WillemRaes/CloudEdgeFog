Typical Edge Hardware Resources
======================================


| Een Single Board Computer (SBC) is een computer waarvan alle
  componenten op 1 Printed Circuit Board (PCB) geplaatst zijn. Dit
  verslag geeft een overzicht van de relevante SBC’s die vandaag op de
  markt beschikbaar zijn en bespreekt de belangrijke hardware
  componenten en beschikbare software tools. Aangezien er honderden
  types SBC’s bestaan voor een heel breed bereik van applicaties en het
  onmogelijk is om deze allemaal te bespreken, wordt voor dit verslag
  uitgegaan van belangrijke overkoepelende ecosystemen om groepen van
  SBC’s te definiëren.
| Er wordt dus eerst een algemene uitleg gegeven van bestaande
  ecosystemen voor edge computing met SBC’s en hun specifieke
  eigenschappen. Verder worden de SBC’s in de gekozen ecosystemen,
  wanneer mogelijk, met elkaar vergeleken op basis van hardware
  specificaties en performantie in benchmarks voor specifieke Machine
  Learning gebaseerde computationele taken. Er wordt uitgegaan van
  bestaande gestandaardiseerde benchmarks.

Verschillende Ecosystemen voor SBC’s
-----------------------------------------

NVIDIA
------

| NVIDIA heeft een specifieke reeks van Single Board Computers, genaamd
  Jetson , voor verschillende AI gerelateerde
  toepassingen. Deze productfamilie bevat verschillende generaties van
  CPU- en GPU-producten met een aantal belangrijke verschillen naar
  computing mogelijkheden toe. De belangrijkste meerwaarde in de context
  van Edge-AI van de Jetson series is de on-board hardware voor
  acceleratie van ML-gerelateerde berekeningen zodat deze toestellen een
  goeie performantie hebben voor AI-inferentie en tegelijkertijd het
  nodige energieverbruik hiervoor minimaal houden. Een belangrijke
  hardware component bij de keuze van een Jetson SBC is de on-board
  Graphical Proccesing Unit (GPU). De eerste generatie Jetson maakt
  gebruik van de Maxwell GPU-architectuur,
  met als opvolger de Pascal architectuur en
  de laatste generatie van Jetsons maakt gebruik van de Volta
  architectuur  waar een belangrijke toevoeging
  de Tensor Cores  zijn die zorgen voor
  een significante performantiewinst bij inferentie omwille van de
  mogelijkheid om "mixed precision" floating point berekeningen te doen
  om ML modellen heel flexibel te optimaliseren. Verder is het zo dat
  NVIDIA naast hardware oplossingen ook een uitgebreid set aan software
  bibliotheken ter beschikking stelt om optimaal gebruik te kunnen maken
  van de hardware acceleratoren aanwezig op de SBC’s. Belangrijke
  software in dit ecosysteem is de Jetpack
  SDK die een linux besturingssyteem bevat
  voor op de Jetson SBC’s en verder alle andere belangrijke bibliotheken
  bundelt. Zo is er de CUDA computing toolkit om GPU computing te
  voorzien, cuDNN de CUDA deep learning accelerator framework en Tensor
  RT wat een framework is om ML taken zoals
  image classification, object detection en image segmentation te
  optimaliseren, latency te minimaliseren en inferentie te versnellen.
  Verder is er nog het image processing framework
  Visionworks die een groot aantal
  beeldverwerking taken kan optimaliseren. Naast de Jetpack SDK is er
  recent ook de NVIDIA Transfer Learning
  toolkit. Deze software dient
  specifiek om pre-trained ML modellen voor een waaier aan use cases ter
  beschikking te stellen voor direct gebruik in AI-applicaties. De
  modellen worden geoptimaliseerd voor inferentie op NVIDIA hardware en
  hebben als doel de time to market te minimaliseren omdat men niet van
  scratch moet beginnen. De beschikbare modellen kunnen ook aangepast
  (transfer learning) worden aan specifieke use cases.
| De Jetson SBC’s die vandaag beschikbaar zijn, zijn de Jetson Nano,
  Jetson TX2, Jetson Xavier NX en de Jetson AGX Xavier. De belangrijkste
  verschillen tussen deze SBC’s worden hieronder opgelijst.

-  | **Jetson Nano**
   | De Jetson Nano is de eerste generatie SBC van NVIDIA en beschikt
     over een Quad Core ARM A57 CPU en een 128-core Maxwell GPU en heeft
     een AI performantie van 472 GFLOPs.

   .. container::
      :name: tab:jetsonnano

      .. table:: Specificaties van de Jetson
      Nano.

         ========================= ==============================================
         **Jetson Nano SBC**       
         ========================= ==============================================
         AI performantie           472 GFLOPs
         CPU                       Quad Core ARM A57 CPU
         GPU                       128-core Maxwell GPU
         Memory                    4 GB 64-bit LPDDR4 25.6GB/s
         Storage                   SD-kaart wanneer developer kit anders eMMC 5.1
         CSI Camera                4 cameras D-PHY 1.1 (18 Gbps)
         Power                     5W - 10W
         Deep Learning Accelerator Geen
         Vision Accelerator        Geen
         ========================= ==============================================

-  | **Jetson TX2**
   | De Jetson TX2 is de opvolger van de Jetson Nano en is beschikbaar
     in verschillende versies. Deze SBC heeft significant meer
     computationeel vermogen en beschikt ook over een nieuwere GPU
     architectuur (Pascal) met 256 GPU cores.

   .. container::
      :name: tab:jetsontx2

      .. table:: Specificaties van de Jetson
      TX2.

         +---------------------------+-----------------------------------------+
         | **Jetson TX2**            |                                         |
         +===========================+=========================================+
         | AI performantie           | 1.33 TFLOPs                             |
         +---------------------------+-----------------------------------------+
         | CPU                       | Dual-Core NVIDIA Denver 2 64-Bit CPU +  |
         |                           | Quad Core ARM A57 CPU                   |
         +---------------------------+-----------------------------------------+
         | GPU                       | 256-core NVIDIA Pascal GPU              |
         +---------------------------+-----------------------------------------+
         | Memory                    | 8 GB 128-bit LPDDR4 59.7 GB/s           |
         +---------------------------+-----------------------------------------+
         | Storage                   | 32GB eMMC 5.1                           |
         +---------------------------+-----------------------------------------+
         | CSI Camera                | 6 cameras D-PHY 1.2 (30 Gbps)           |
         +---------------------------+-----------------------------------------+
         | Power                     | 7.5W - 15W                              |
         +---------------------------+-----------------------------------------+
         | Deep Learning Accelerator | Geen                                    |
         +---------------------------+-----------------------------------------+
         | Vision Accelerator        | Geen                                    |
         +---------------------------+-----------------------------------------+

-  | **Jetson Xavier NX**
   | De Jetson Xavier NX is de eerste SBC van de nieuwere Xavier familie
     en beschikt over massaal meer computationeel vermogen in
     vergelijking met de Jetson Nano en TX2. Verder bevat deze SBC een
     GPU met de nieuwere Volta architectuur met 384 GPU cores en ook 48
     van de geavanceerde Tensor Cores.

   .. container::
      :name: tab:jetsonnx

      .. table:: Specificaties van de Jetson Xavier
      NX.

         +---------------------------+-----------------------------------------+
         | **Jetson Xavier NX**      |                                         |
         +===========================+=========================================+
         | AI performantie           | 21 TFLOPs (INT8)                        |
         +---------------------------+-----------------------------------------+
         | CPU                       | 6-core NVIDIA Carmel Arm v8.2 64-bit    |
         |                           | CPU                                     |
         +---------------------------+-----------------------------------------+
         | GPU                       | 384-core NVIDIA Volta GPU + 48 Tensor   |
         |                           | Cores                                   |
         +---------------------------+-----------------------------------------+
         | Memory                    | 8 GB 128-bit LPDDR4x 51.2GB/s           |
         +---------------------------+-----------------------------------------+
         | Storage                   | SD-kaart wanneer developer kit anders   |
         |                           | 16 GB eMMC 5.1                          |
         +---------------------------+-----------------------------------------+
         | CSI Camera                | 6 cameras D-PHY 1.2 (30 Gbps)           |
         +---------------------------+-----------------------------------------+
         | Power                     | 10W - 15W                               |
         +---------------------------+-----------------------------------------+
         | Deep Learning Accelerator | 2x NVDLA                                |
         +---------------------------+-----------------------------------------+
         | Vision Accelerator        | 7-Way VLIW Vision Processor             |
         +---------------------------+-----------------------------------------+

-  | **Jetson AGX Xavier**
   | De Jetson AGX Xavier is momenteel de nieuwste en meest geavanceerde
     SBC in de Jetson reeks en is beschikbaar in een gewone en
     industriële versie.

   .. container::
      :name: tab:jetsonagx

      .. table:: Specificaties van de Jetson AGX Xavier.

         +---------------------------+-----------------------------------------+
         | **Jetson AGX Xavier**     |                                         |
         +===========================+=========================================+
         | AI performantie           | 32 TFLOPs (INT8)                        |
         +---------------------------+-----------------------------------------+
         | CPU                       | 8-core NVIDIA Carmel Arm v8.2 64-bit    |
         |                           | CPU                                     |
         +---------------------------+-----------------------------------------+
         | GPU                       | 512-core NVIDIA Volta™ GPU + 64 Tensor  |
         |                           | Cores                                   |
         +---------------------------+-----------------------------------------+
         | Memory                    | 32 GB 256-bit LPDDR4x 136.5GB/s         |
         +---------------------------+-----------------------------------------+
         | Storage                   | 32-64 GB eMMC 5.1                       |
         +---------------------------+-----------------------------------------+
         | CSI Camera                | 6 cameras D-PHY 1.2 (40 Gbps), C-PHY    |
         |                           | 1.1 (62 Gbps)                           |
         +---------------------------+-----------------------------------------+
         | Power                     | 10W - 30W                               |
         +---------------------------+-----------------------------------------+
         | Deep Learning Accelerator | 2x NVDLA                                |
         +---------------------------+-----------------------------------------+
         | Vision Accelerator        | 2x 7-Way VLIW Vision Processor          |
         +---------------------------+-----------------------------------------+

Er bestaan gestandaardiseerde AI
benchmarks
specifiek voor de Jetson SBC’s. Deze vrij beschikbare software test de
performantie (inferentie) van een reeks populaire en relevante
ML-modellen beschikbaar in de State of The Art vandaag.
Tabel `[tab:jetsonbenchmarks] <#tab:jetsonbenchmarks>`__ geeft een
overzicht van het resultaat van de uitgevoerde benchmarks.

Intel
-----

Er bestaan heel wat SBC’s die gebruik maken van x86-gebaseerde
processoren. Intel heeft
een framework uitgebouwd om edge computing
te voorzien en te optimaliseren op hun processor hardware. Intel
produceert onder andere de Intel Atom
Processoren voor embedded applicaties,
de Intel Movidius Vision Processing Units
om vision en AI workloads te accelereren. Verder biedt het ook de
OpenVino software toolkit en de Intel
oneAPI toolkit om ML-workloads te
optimaliseren voor alle Intel hardware componenten.
"..
.. figure:: figures/openvino.png
   :alt: Workflow bij de Intel OpenVino software
   toolkit :raw-latex:`\cite{intelopenvino}`.
   :name: fig:openvino

   Workflow bij de Intel OpenVino software
   toolkit :raw-latex:`\cite{intelopenvino}`.
"
Intel legt de focus op het versnellen en optimaliseren van de volledige
ML-pipeline en gebruikt daarvoor vooral de Intel Xeon processor reeks
waarmee het een hoge performantie haalt voor een groot aantal
ML-workloads .

ARM
---

ARM produceert Intellectual Property (IP) voor CPU’s, GPU’s en andere
hardware voor een heel breed bereik van toepassingen. ARM is ook heel
actief bezig met het uitbouwen van een
ecosysteem  om AI computing in de edge te
faciliteren en er een rijke set van tools voor te voorzien. Een
overzicht van deze tools is zichtbaar in Fig. `2 <#fig:armeco>`__.
"..
.. figure:: figures/ARMecosystem.png
   :alt: Workflow bij het ARM AI-platform. 
   :name: fig:armeco

   Workflow bij het ARM AI-platform. 
"
Deze figuur toont de mogelijkheden van het ARM-ecosysteem vertrekkende
van populaire ML-frameworks, naar software geoptimaliseerd voor
ARM-gebaseerde hardware producten en uiteindelijk de hardware
componenten zelf. Een groot aantal van de recente SBC’s maken gebruik
van ARM IP voor hun CPU’s en GPU’s. Verder biedt ARM ook de specifieke
Neural Processing Unit (NPU)  co-processoren
aan om specifieke ML workloads te versnellen. Deze zijn beschikbaar voor
Cortex-M microcontroller  systemen maar ook
voor combinatie met de applicatie processoren in de Cortex-A
reeks. De software die ARM ter beschikking
stelt omvat de ARM Computing Library
en de ARM NN SDK die enerzijds
GPU-computing op de Mali GPU’s mogelijk
maakt en anderzijds een set Linux gebaseerde tools voorziet om efficiënt
gecombineerd gebruik te maken van de Cortex-A CPU, Mali GPU en NPU die
typisch aanwezig zijn op de SBC-hardware.

Google TPU
----------

Google heeft ook een eigen ecosysteem om edge computing te
faciliteren. Zo is er het
Tensorflow software framework dat vrij
kan gebruikt worden om ML-applicaties op te bouwen. Om modellen te
optimaliseren voor SBC’s en andere hardware met minder computationele
mogelijkheden dan een server of workstation is er het Tensorflow Lite
framework dat toelaat om de parameters van
getrainde modellen te quantiseren en dus de numerieke precisie van de
parameters aan te passen aan de hardware specificaties van het toestel
dat de inferentie moet uitvoeren. Google heeft ook een hardware
accelerator dat gebruikt kan worden voor modellen die opgebouwd zijn
met, of geconverteerd zijn naar het tensorflow lite formaat. Deze
accelerator, de Tensor Processing Unit
(TPU), is een custom Application Specific
Integrated Circuit (ASIC) die ontwikkeld is om ML-workloads te
versnellen en het energieverbruik daarvoor minimaal te houden. De edge
TPU’s voor onder andere SBC’s zijn te vinden op de Google Coral hardware
producten. De workflow in het google
ecosysteem is te zien in
Fig. `3 <#fig:googletpu>`__.

"..
.. figure:: figures/compile-workflow.png
   :alt: Workflow in het Google Coral
   ecosysteem :raw-latex:`\cite{coralworkflow}`.
   :name: fig:googletpu

   Workflow in het Google Coral
   ecosysteem :raw-latex:`\cite{coralworkflow}`.

| De parameters van het TPU-model moeten gequantiseerd worden naar 8bit
  fixed point (INT8-UINT8) precisie. Google heeft onder andere een
  development bord, de Google Coral dev SBC om deze TPU’s te testen.
"
.. container::
   :name: tab:coraldevspec

   .. table:: Specificaties van de Google Coral
   Dev.

      +---------------------------+-----------------------------------------+
      | **Google Coral Dev**      |                                         |
      +===========================+=========================================+
      | AI performantie           | 21 TFLOPs (INT8)                        |
      +---------------------------+-----------------------------------------+
      | CPU                       | NXP i.MX 8M SoC (quad Cortex-A53,       |
      |                           | Cortex-M4F)                             |
      +---------------------------+-----------------------------------------+
      | GPU                       | Integrated GC7000 Lite Graphics         |
      +---------------------------+-----------------------------------------+
      | Memory                    | 4 GB LPDDR4                             |
      +---------------------------+-----------------------------------------+
      | Storage                   | 8 GB eMMC, MicroSD slot                 |
      +---------------------------+-----------------------------------------+
      | CSI Camera                | MIPI-CSI2 camera input (4-lane)         |
      +---------------------------+-----------------------------------------+
      | Power                     | 2-3 A at 5 V DC                         |
      +---------------------------+-----------------------------------------+
      | Deep Learning Accelerator | Google Edge TPU coprocessor: 4 TOPS     |
      |                           | (int8); 2 TOPS per watt                 |
      +---------------------------+-----------------------------------------+
      | Vision Accelerator        | Video Processing Unit                   |
      +---------------------------+-----------------------------------------+

Er zijn benchmarks beschikbaar  die
de performantie van populaire ML-modellen (Neurale Netwerken) test op
TPU-hardware en vergelijkt met CPU-performantie op een desktop en op een
SBC. De resultaten van deze benchmark (inferentietijd in ms) zijn
weergegeven in Tabel `[tab:coralbench] <#tab:coralbench>`__.
