# OS/Software

System	Overview	Programming Model	Language
* **RIOT:**

    RIOT OS is an operating system for Internet of Things (IoT) devices. It is based on a microkernel and designed for: energy efficiency, hardware independent development, a high degree of modularity.
    
* **Tiny OS:**
	
    TinyOS is an open source, BSD-licensed operating system designed for low-power wireless devices, such as those used in sensor networks, ubiquitious computing, personal area networks, smart buildings, and smart meters. A worldwide community from academia and industry use, develop, and support the operating system as well as its associated tools, averaging 35,000 downloads a year.
    * **Programming Model:** Event Driven, support for TOS threads
    * **Language:** NesC


* **Contiki:**
	
    Contiki is an open source, highly portable, multi-tasking operating system for memory-efficient networked embedded systems and wireless sensor networks. Contiki has been used is a variety of projects, such as road tunnel fire monitoring, intrusion detection, wildlife monitoring, and in surveillance networks.Contiki is designed for microcontrollers with small amounts of memory. A typical Contiki configuration is 2 kilobytes of RAM and 40 kilobytes of ROM.	
    * **Programming Model:** Protothreads and events
    * **Language:** C


* **Mantis:**
    
    The MANTIS Group at CU Boulder has developed an open source, multi-threaded operating system written in C for wireless sensor networking platforms. 
    
    Some key features of MANTIS OS (MOS):
    * Developer friendly C API with Linux and Windows development environments
    * Automatic preemptive time slicing for fast prototyping
    * Diverse platform support including MICA2, MICAz, and TELOS motes
    * Energy-efficient scheduler for duty-cycle sleeping of sensor node
    * Small footprint (less than 500B RAM, 14KB flash)

    * **Programming Model:** Threads
    * **Language:** C


* **Nano-RK:**

    Nano-RK is a fully preemptive reservation-based real-time operating system (RTOS) from Carnegie Mellon University with multi-hop networking support for use in wireless sensor networks. Nano-RK currently runs on the FireFly Sensor Networking Platform as well as the MicaZ motes. It includes a light-weight embedded resource kernel (RK) with rich functionality and timing support using less than 2KB of RAM and 18KB of ROM. Nano-RK supports fixed-priority preemptive multitasking for ensuring that task deadlines are met, along with support for CPU, network, as well as, sensor and actuator reservations. Tasks can specify their resource demands and the operating system provides timely, guaranteed and controlled access to CPU cycles and network packets. Together these resources form virtual energy reservations that allows the OS to enforce system and task level energy budgets.
    * **Programming Model:** Threads
    * **Language:** C


* **LiteOS:**
 	
    LiteOS is an open source, interactive, UNIX-like operating system designed for wireless sensor networks. With the tools that come with LiteOS, you can operate one or more wireless sensor networks in a Unix-like manner, transferring data, installing programs, retrieving results, or configuring sensors. You can also develop programs for nodes, and wirelessly distribute such programs to sensor nodes.
    
    * **Programming Model:** Threads and Events
    * **Language:** C


* **FreeRTOS:**	
 
    FreeRTOS is a real-time operating system for embedded devices, being ported to several microcontrollers. It is distributed under the GPL with an optional exception.		
    * **Programming Model:**
    * **Language:** C


