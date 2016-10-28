# Contiki
## What is Contiki?
* **Contiki Web definition: **

  Contiki is an open source operating system for the Internet of Things. Contiki connects tiny low-cost, low-power microcontrollers to the Internet. Contiki is a powerful toolbox for building complex wireless systems.
  
  
* **Wikipedia definition: **

  Contiki is an operating system for networked, memory-constrained systems with a focus on low-power wireless Internet of Things devices. Extant uses for Contiki include systems for street lighting, sound monitoring for smart cities, radiation monitoring, and alarms. It is open-source software released under a BSD license.
  
  Contiki provides multitasking and a built-in Internet Protocol Suite (TCP/IP stack), yet needs only about 10 kilobytes of random-access memory (RAM) and 30 kilobytes of read-only memory (ROM). A full system, including a graphical user interface, needs about 30 kilobytes of RAM.
  

### Features

Contiki supports per-process optional preemptive multithreading, inter-process communication using message passing through events, as well as an optional graphical user interface (GUI) subsystem with either direct graphic support for locally connected terminals or networked virtual display with Virtual Network Computing (VNC) or over Telnet.

A full installation of Contiki includes the following features:

* Multitasking kernel
* Optional per-application preemptive multithreading
* Protothreads
* Internet Protocol Suite (TCP/IP) networking, including IPv6
* Windowing system and GUI
* Networked remote display using Virtual Network Computing
* A web browser (claimed to be the world's smallest)
* Personal web server
* Simple telnet client
* Screensaver

## Contiki Development Environment with "Instant Contiki VM"
**Instant Contiki** is an entire **Contiki development environment** in a single download. It is an **Ubuntu Linux virtual machine** that runs in VMWare player and has the following elements pre-installed:
* Contiki
* Development tools, compilers, and simulators used in Contiki development 

Instant Contiki is so convenient that even hardcore Contiki developers use it.

9.2.1 Programando en Contiki
# Programando en Contiki

* Contiki is **multi-tasking operating system**, especially designed for microcontrollers with small amount of memory(35KB of ROM and around 3K of RAM), which are used in networked embedded systems and wireless sensor networks.
* Se considera un SO híbrido ya que combina las ventajas de **eventos** e **hilos**.
* Se trata principalmente de un modelo orientado a eventos, pero soporta multihilo. Los hilos se denominan **PROTOHEADS** 
* Contiki is written in the **C** programming language.
* 


## Objetivo
Understand the idea of threads and Events for Contiki.

