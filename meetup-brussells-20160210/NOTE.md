# Todo rpi meetup

## high level goals
Goal of the meetup : launch the "voting app" demo of docker with the docker stack : Machine, Engine, Compose and Swarm. The hardware platform will be raspberry Pi based, but can be any Docker host type compatible with Hypriot OS.

## target audience
The target audience is docker beginners. Audience should at least understand basics of Unix commandline (ssh access, options/arguments, basic command, text editing )

## High level steps
The building steps will follow the OSI stack methodology : layered, from hardware setup to end user view at logical application level

### hardware setup
#### Main nodes 
Raspberry Pi or HypriotOs- compliant board. 
* Each one must have a 8Go Sd card (or micro SD) with the latest HypriotOs dumped onto.
* We will use wired Ethernet to connect to network
* AC will be provided by the micro-USB port
* No keyboard/mouse/hdmi/screen needed
#### Shack
The Shack will be the "utility" machine. It will have those roles :
* Allow Pis to access internet
* Provide a local cache for Docker images used
* Provide utilities services like Consul Server
* Show the slides to audience (switch between slides / Consul UI / Terminal must be quick and easy for presenter)

The Shack must have at least one wifi access to the web, and be able to share web to its Ethernet wire (See Network section below)

#### Network

Our network will have those constraints :
* web access through the shack routing
* Wired part, need of switched, for the ARM boards like Pis, and audience machines that will be used to access Pis.
* If possible, wifi access for audience laptop that do not have ethernet connectivity.

We will use a Mac laptop as Shack machine :
* airport (integrated wifi) will be used to share private network for laptop
* Usb-ethernet adaptor for wired connectivity
* A Mac Os compatible Usb dongle for wifi (web access )