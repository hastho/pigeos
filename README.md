# Pi/GEOS
is a runtime environment build on top of Raspbian Linux & DOSBox to use any version 
of PC/GEOS (e.g.. Geworks Ensemble 2.x, NewDeal Office 3.x/4.x/2000 and 
Breadbox Ensemble.

## Intention

Pi/GEOS intention is to simulate the user experience of running
PC/GEOS a classic DOS-PC as much as possible on a Raspberry Pi.
Furthermore the user should be able to do some serious work on the
system e.g. print documents or share them with other people in todays
common data formats like PDF. 

The Pi/GEOS environment also hides the underlying Linux as much as
possible and therefore doesn't require Linux knowledge.

## Key features
  - stable operation of all English and German GEOS 2.x/3.x/4.x versions
  - 1024x768 desktop with correct aspect. ratio on any display 
  - network support via LAN or WiFi to allow Web enabled GEOS version
to connect to the internet without any modification (e.g. using a
virtual modem connection)
  - printing from GEOS to any Linux supported printer connected to the
Raspberry Pi via USB or network
  - support of modern input devices like USB keyboard and mouse

## Concepts
Pi/GEOS is heavily based on disk images to allow for easy provision of a
pre-configures GEOS environments contributed by the GEOS community.

## Components

Pi/GEOS contains 3 major components:
  - **pigeos-setup** a bash script to customize a bare Raspbian to 
boot very fast into DOSBox running on a console frame buffer console
  - **pigeos-config** a bash script to customize the Linux & DOSBox environment
that looks and behaves much like classic PC BIOS/SETUP
  - **pigeos-loader** a launcher script that executes DOSBox during
system boot and also attaches the requested DOS drive images 