# Protocols

Rather than trying to fit all of the IoT Protocols on top of existing architecture models like OSI Model, we have broken the protocols into the following layers to provide some level of organization:

* **Infrastructure** (ex: 6LowPAN, IPv4/IPv6, RPL)
* **Identification** (ex: EPC, uCode, IPv6, URIs)
* **Comms / Transport** (ex: Wifi, Bluetooth, LPWAN)
* **Discovery** (ex: Physical Web, mDNS, DNS-SD)
* **Data Protocols** (ex: MQTT, CoAP, AMQP, Websocket, Node)
* **Device Management** (ex: TR-069, OMA-DM)
* **Semantic** (ex: JSON-LD, Web Thing Model)
* **Multi-layer Frameworks** (ex: Alljoyn, IoTivity, Weave, Homekit)

---



### Infrastructure


* **IPv6:** "IPv6, is an Internet Layer protocol for packet-switched internetworking and provides end-to-end datagram transmission across multiple IP networks.

* **6LoWPAN:** "6LoWPAN is an acronym of IPv6 over Low power Wireless Personal Area Networks. It is an adaption layer for IPv6 over IEEE802.15.4 links. This protocol operates only in the 2.4 GHz frequency range with 250 kbps transfer rate."

* **UDP (User Datagram Protocol):** A simple OSI transport layer protocol for client/server network applications based on Internet Protocol (IP). UDP is the main alternative to TCP and one of the oldest network protocols in existence, introduced in 1980. UDP is often used in applications specially tuned for real-time performance.

* **QUIC (Quick UDP Internet Connections, pronounced quick):** supports a set of multiplexed connections between two endpoints over User Datagram Protocol (UDP), and was designed to provide security protection equivalent to TLS/SSL, along with reduced connection and transport latency, and bandwidth estimation in each direction to avoid congestion.

* **Aeron:** Efficient reliable UDP unicast, UDP multicast, and IPC message transport.

* **uIP:** The uIP is an open source TCP/IP stack capable of being used with tiny 8- and 16-bit microcontrollers. It was initially developed by Adam Dunkels of the "Networked Embedded Systems" group at the Swedish Institute of Computer Science, licensed under a BSD style license, and further developed by a wide group of developers.

* **DTLS (Datagram Transport Layer):** "The DTLS protocol provides communications privacy for datagram protocols. The protocol allows client/server applications to communicate in a way that is designed to prevent eavesdropping, tampering, or message forgery. The DTLS protocol is based on the Transport Layer Security (TLS) protocol and provides equivalent security guarantees."

* **ROLL / RPL:** (IPv6 routing for low power/lossy networks)

* **NanoIP:** NanoIP, which stands for the nano Internet Protocol, is a concept that was created to bring Internet-like networking services to embedded and sensor devices, without the overhead of TCP/IP. NanoIP was designed with minimal overheads, wireless networking, and local addressing in mind.

* **Content-Centric Networking (CCN):** Technical Overview
"Next-gen network architecture to solve challenges in content distribution scalability, mobility, and security.
CCN directly routes and delivers named pieces of content at the packet level of the network, enabling automatic and application-neutral caching in memory wherever it’s located in the network. The result? Efficient and effective delivery of content wherever and whenever it is needed. Since the architecture enables these caching effects as an automatic side effect of packet delivery, memory can be used without building expensive application-level caching services."


* **Time Synchronized Mesh Protocol (TSMP):** A communications protocol for self-organizing networks of wireless devices called motes. TSMP devices stay synchronized to each other and communicate in timeslots, similar to other TDM (time-division multiplexing) systems.



### Discovery

* **mDNS (multicast Domain Name System):** Resolves host names to IP addresses within small networks that do not include a local name server.

* **Physical Web:** The Physical Web enables you to see a list of URLs being broadcast by objects in the environment around you with a Bluetooth Low Energy (BLE) beacon.

* **HyperCat:** An open, lightweight JSON-based hypermedia catalogue format for exposing collections of URIs.

* **UPnP (Universal Plug and Play):** Now managed by the Open Connectivity Foundation is a set of networking protocols that permits networked devices to seamlessly discover each other's presence on the network and establish functional network services for data sharing, communications, and entertainment.


### Data Protocols

* **MQTT (Message Queuing Telemetry Transport):** The MQTT protocol enables a publish/subscribe messaging model in an extremely lightweight way. It is useful for connections with remote locations where a small code footprint is required and/or network bandwidth is at a premium.

  * **MQTT-SN (MQTT For Sensor Networks):** An open and lightweight publish/subscribe protocol designed specifically for machine-to-machine and mobile applications
 * **Mosquitto:** An Open Source MQTT v3.1 Broker
 * **IBM MessageSight**

* **CoAP (Constrained Application Protocol):** CoAP is an application layer protocol that is intended for use in resource-constrained internet devices, such as WSN nodes. CoAP is designed to easily translate to HTTP for simplified integration with the web, while also meeting specialized requirements such as multicast support, very low overhead, and simplicity. The CoRE group has proposed the following features for CoAP: RESTful protocol design minimizing the complexity of mapping with HTTP, Low header overhead and parsing complexity, URI and content-type support, Support for the discovery of resources provided by known CoAP services. Simple subscription for a resource, and resulting push notifications, Simple caching based on max-age.

  * **SMCP:** A C-based CoAP stack which is suitable for embedded environments. Features include: Support draft-ietf-core-coap-13, Fully asynchronous I/O, Supports both BSD sockets and UIP.


* **STOMP:** The Simple Text Oriented Messaging Protocol

* **XMPP (Extensible Messaging and Presence Protocol):** An open technology for real-time communication, which powers a wide range of applications including instant messaging, presence, multi-party chat, voice and video calls, collaboration, lightweight middleware, content syndication, and generalized routing of XML data.
  * **XMPP-IoT:** In the same manor as XMPP silently has created people to people communication interoperable. We are aiming to make communication machine to people and machine to machine interoperable.

* **Mihini/M3DA:** The Mihini agent is a software component that acts as a mediator between an M2M server and the applications running on an embedded gateway. M3DA is a protocol optimized for the transport of binary M2M data. It is made available in the Mihini project both for means of Device Management, by easing the manipulation and synchronization of a device's data model, and for means of Asset Management, by allowing user applications to exchange typed data/commands back and forth with an M2M server, in a way that optimizes the use of bandwidth.

* **AMQP (Advanced Message Queuing Protocol):** An open standard application layer protocol for message-oriented middleware. The defining features of AMQP are message orientation, queuing, routing (including point-to-point and publish-and-subscribe), reliability and security.
  * **DDS (Data-Distribution Service for Real-Time Systems):** The first open international middleware standard directly addressing publish-subscribe communications for real-time and embedded systems.

  * **JMS (Java Message Service):** A Java Message Oriented Middleware (MOM) API for sending messages between two or more clients.

  * **LLAP (lightweight local automation protocol):** LLAP is a simple short message that is sent between inteligent objects using normal text, it's not like TCP/IP, bluetooth, zigbee, 6lowpan, WiFi etc which achieve at a low level "how" to move data around. This means LLAP can run over any communication medium. The three strengths of LLAP are, it'll run on anything now, anything in the future and it's easily understandable by humans.

* **LWM2M (Lightweight M2M):** Lightweight M2M (LWM2M) is a system standard in the Open Mobile Alliance. It includes DTLS, CoAP, Block, Observe, SenML and Resource Directory and weaves them into a device-server interface along with an Object structure.

* **SSI (Simple Sensor Interface):** A simple communications protocol designed for data transfer between computers or user terminals and smart sensors.

* **Reactive Streams:** A standard for asynchronous stream processing with non-blocking back pressure on the JVM.

* **ONS 2.0**

* **REST (Representational state transfer) - RESTful HTTP**

* **HTTP/2:** Enables a more efficient use of network resources and a reduced perception of latency by introducing header field compression and allowing multiple concurrent exchanges on the same connection. 





### Communication / Transport layer

* **Ethernet:**

* **WirelessHart:** WirelessHART technology provides a robust wireless protocol for the full range of process measurement, control, and asset management applications.

* **DigiMesh:** DigiMesh is a proprietary peer-to-peer networking topology for use in wireless end-point connectivity solutions.

* **ISA100.11a:** ISA100.11a is a wireless networking technology standard developed by the International Society of Automation (ISA). The official description is "Wireless Systems for Industrial Automation: Process Control and Related Application.

* **IEEE 802.15.4:** IEEE 802.15.4 is a standard which specifies the physical layer and media access control for low-rate wireless personal area networks (LR-WPANs). It is maintained by the IEEE 802.15 working group. It is the basis for the ZigBee,ISA100.11a, WirelessHART, and MiWi specifications, each of which further extends the standard by developing the upper layers which are not defined in IEEE 802.15.4. Alternatively, it can be used with 6LoWPAN and standard Internet protocols to build a wireless embedded Internet.

* **NFC:** Based on the standard ISO/IEC 18092:2004, using inductive coupled devices at a center frequency of13.56 MHz. The data rate is up to 424 kbps and the rangeis with a few meters short compared to the wireless sensornetworks.

* **ANT:** ANT is a proprietary wireless sensor network technology featuring a wireless communications protocol stack that enables semiconductor radios operating in the 2.4 GHz Industrial, Scientific and Medical allocation of the RF spectrum ("ISM band") to communicate by establishing standard rules for co-existence, data representation, signalling, authentication and error detection.

* **Bluetooth:** Bluetooth works in the 2.4 GHz ISM band and uses frequency hopping. With a data rate up to 3 Mbps and maximum range of 100m. Each application type which can use Bluetooth has its own profile.

* **Eddystone:** A protocol specification that defines a Bluetooth low energy (BLE) message format for proximity beacon messages.

* **ZigBee:** The ZigBee protocol uses the 802.15.4 standard and operates in the 2.4 GHz frequency range with 250 kbps. The maximum number of nodes in the network is 1024 with a range up to 200 meter. ZigBee can use 128 bit AES encryption.

* **EnOcean:** EnOcean is a an energy harvesting wireless technology which works in the frequencies of 868 MHz for europe and 315 MHz for North America. The transmit range goes up to 30 meter in buildings and up to 300 meter outdoor.

* **WiFi**

* **WiMax:** WiMax is based on the standard IEEE 802.16 and is intended for wireless metropolitan area networks. The range is different for fixed stations, where it can go up to 50 km and mobile devices with 5 to 15 km. WiMAx operates at frequencies between 2.5 GHz to 5.8 GHz with a transferrate of 40 Mbps.

* **LPWAN**

  * **Weightless:** Weightless is a proposed proprietary open wireless technology standard for exchanging data between a base station and thousands of machines around it (using wavelength radio transmissions in unoccupied TV transmission channels) with high levels of security.

  * **NB-IoT (Narrow-Band IoT):** A technology being standardized by the 3GPP standards body

  * **LTE-MTC (LTE-Machine Type Communication):** Standards-based family of technologies supports several technology categories, such as Cat-1 and CatM1, suitable for the IoT.

  * **EC-GSM-IoT (Extended Coverage-GSM-IoT):** Enables new capabilities of existing cellular networks for LPWA (Low Power Wide Area) IoT applications. EC-GSM-IoT can be activated through new software deployed over a very large GSM footprint, adding even more coverage to serve IoT devices.

  * **LoRaWAN:** Network protocol intended for wireless battery operated Things in regional, national or global network. 

  * **RPMA (Random phase multiple access):** A technology communication system employing direct-sequence spread spectrum (DSSS) with multiple access. 



### Semantic

* **IOTDB:** "JSON / Linked Data standards for describing the Internet of Things".

* **SensorML:** SensorML provides standard models and an XML encoding for describing sensors and measurement processes.

* **Semantic Sensor Net Ontology - W3C:** This ontology describes sensors and observations, and related concepts. It does not describe domain concepts, time, locations, etc. these are intended to be included from other ontologies via OWL imports.

* **Wolfram Language - Connected Devices:** A symbolic representation of each device. Then there are a standard set of Wolfram Language functions like DeviceRead, DeviceExecute, DeviceReadBuffer and DeviceReadTimeSeries that perform operations related to the device.

* **RAML (RESTful API Modeling Language):** Makes it easy to manage the whole API lifecycle from design to sharing. It's concise - you only write what you need to define - and reusable.
  
* **SENML (Media Types for Sensor Markup Language):** A simple sensor, such as a temperature sensor, could use this media type in protocols such as HTTP or CoAP to transport the measurements of the sensor or to be configured.

* **LsDL (Lemonbeat smart Device Language):** XML-based device language for service oriented devices


### Multi-layer Frameworks

* **Alljoyn:** An open source software framework that makes it easy for devices and apps to discover and communicate with each other.

* **IoTivity:** It is an open source project hosted by the Linux Foundation, and sponsored by the OIC.

* **IEEE P2413:** Standard for an Architectural Framework for the Internet of Things (IoT).
* 
* **Thread:** Built on open standards and IPv6 technology with 6LoWPAN as its foundation.

* **IPSO Application Framework (PDF):** This design defines sets of REST interfaces that may be used by a smart object to represent its available resources, interact with other smart objects and backend services. This framework is designed to be complementary to existing Web profiles including SEP2 and oBIX.

* **OMA LightweightM2M v1.0:** The motivation of LightweightM2M is to develop a fast deployable client-server specification to provide machine to machine service. 
* 
* **LightweightM2M:** It is principly a device management protocol, but it should be designed to be able to extend to meet the requirements of applications. LightweightM2M is not restricted to device management, it should be able transfer service / application data."

* **Weave.** A communications platform for IoT devices that enables device setup, phone-to-device-to-cloud communication, and user interaction from mobile devices and the web.

* **Telehash - JSON+UDP+DHT=Freedom:** A secure wire protocol powering a decentralized overlay network for apps and devices



### Security

* **Open Trust Protocol (OTrP).** A protocol to install, update, and delete applications and to manage security configuration in a Trusted Execution Environment (TEE).

* **X.509.** Standard for public key infrastructure (PKI) to manage digital certificates and public-key encryption. A key part of the Transport Layer Security protocol used to secure web and email communication.

