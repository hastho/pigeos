# Pi/GEOS
is a runtime environment build on top of Raspbian Linux & DOSBox to use any version 
of PC/GEOS (e.g.. Geworks Ensemble 2.x, NewDeal Office 3.x/4.x/2000 and 
Breadbox Ensemble.

## Intention

Pi/GEOS is intended to simulate the user experience of running.
PC/GEOS on a traditional DOS-PC as much as possible on a Raspberry Pi.
Moreover, the user should be able to do some serious work on the system 
such as printing documents or sharing them with other people in today's 
common data formats like PDF.
The Pi/GEOS environment also hides the underlying Linux as much as
possible and therefore doesn't require Linux knowledge.

## Key features
  - stable operation of all English and German GEOS 2.x/3.x/4.x versions
  - scale the GEOS desktop to the correct aspect ratio on any modern display 
  - network support via LAN or WiFi for web access with GEOS versions that
support this via a virtual modem connection
  - print from GEOS to any AirPrint enabled printer connected to the
Raspberry Pi network
  - document synchronization with other NAS, PC and mobile divices
  - support of modern input devices like USB keyboard and mouse

## Concepts
Pi/GEOS relies heavily on disc images to allow easy deployment of preconfigured 
GEOS environments contributed by the GEOS community. USB pen drive support 
and a data synchronisation service are included for document sharing.

## Components
Pi/GEOS contains 5 major components:
  - **pigeos-setup** a bash script to customise a bare Raspbian to 
boot quickly into DOSBox running in a minimal X11 environment
  - **pigeos-config** a bash script to customize the Linux & DOSBox environment
that looks and behaves much like classic PC BIOS/SETUP
  - **pigeos-loader** a launcher script that starts DOSBox on
system boot and attaches the requested drive images to the DOS session
  - **pigeos-print** captures the output of the GEOS printer drivers and
translates it so that it can be sent to a modern printer or converted into a PDF document
  - **pigeos-img2gos** used in conjunction with third-party file synchronisation service
it allows documents to be converted into formats that GEOS can handle 

## Docker-based plug-in services
To enable communication with modern web services, Pi/GEOS allows the integration of containerised application level gateways. It comes with:
  - **FeedProxy** a web proxy that translates the content of RSS feeds into HTML4 
