# TinyOS


## What is TinyOS (source: Wikipedia)
---
**TinyOS** is an embedded, **component-based operating system** and platform for low-power wireless devices, such as those used in wireless sensor networks (WSNs), smartdust, ubiquitous computing, personal area networks, building automation, and smart meters. It is **written in** the programming language **nesC**, as a set of cooperating tasks and processes. It began as a collaboration between the University of California, Berkeley, Intel Research, and Crossbow Technology, was released as free and open-source software under a BSD license, and has since grown into an international consortium, the TinyOS Alliance.


### Implementation:
TinyOS applications are written in the programming language **nesC**, a dialect of the C language optimized for the memory limits of sensor networks. Its supplementary tools are mainly in the form of Java and shell script front-ends. Associated libraries and tools, such as the nesC compiler and Atmel AVR binutils toolchains, are mostly written in C.

**TinyOS programs are built of software components**, some of which present hardware abstractions. Components are **connected to each other** using **interfaces**. TinyOS provides interfaces and components for common abstractions such as:
 * Packet communication
 * Routing
 * Sensing, 
 * Actuation 
 * Storage

TinyOS is **fully non-blocking**: it has one call stack. Thus, all input/output (I/O) operations that last longer than a few hundred microseconds are asynchronous and have a callback. To enable the native compiler to better optimize across call boundaries, TinyOS uses nesC's features to link these callbacks, called events, statically. While being non-blocking enables TinyOS to maintain high concurrency with one stack, it forces programmers to write complex logic by stitching together many small event handlers. To support larger computations, TinyOS provides tasks, which are similar to a Deferred Procedure Call and interrupt handler bottom halves. A TinyOS component can post a task, which the OS will schedule to run later. Tasks are non-preemptive and run in first in, first out order. This simple concurrency model is typically sufficient for I/O centric applications, but its difficulty with CPU-heavy applications has led to developing a thread library for the OS, named TOSThreads.

TinyOS code is statically linked with program code and is compiled into a small binary, using a custom GNU toolchain. Associated utilities are provided to complete a development platform for working with TinyOS.



## What is nesC (source: Wikipedia)
---
**nesC** (network embedded systems C), pronounced "NES-see", is a **component-based, event-driven programming language** used to build applications for the **TinyOS** platform. TinyOS is an operating environment designed to run on embedded devices used in distributed wireless sensor networks. nesC is built as an extension to the C programming language with components "wired" together to run applications on TinyOS.

