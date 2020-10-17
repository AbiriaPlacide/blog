---
title: Learning embedded systems 
tags: BackToBasics
---

Embedded systems is a broad field and often it can be difficult to know where to begin.
This serves as a guide on what is required to quickly get started. 

We're gonna look at the arduino platform, learning C, picking a microcontroller, reading datasheets, and Hello world for embedded systems.

#### The Arduino Platform:

The arduino platform serves as a way for hobbyists to make awesome projects and prototypes quickly without worrying about the underlying hardware. All you have to do is buy a starter kit, download the arduino IDE, follow the vast amount of tutorials online and you can make whatever you desire within reason. It also has a large community you can go to when you're stuck and you can use a lot of libraries to control components you may use for your project. It’s great if you’re doing it for a hobby and you can make amazing stuff with it. But once you decide to pursue a career in embedded systems, arduino’s are not used for professional work.

Learning C: Before picking a microcontroller, you first have to learn C before being able to program it. 
You have to be comfortable with the basics like pointers, typecasting, bitwise operations, the C preprocessor, and understand what certain keywords like “Volatile” do.

#### Picking a microcontroller

When picking a microcontroller, as a beginner, you want to look at the ecosystem and support it has and how quickly you can get productive with it. Also, it is beneficial to pick a board that doesn’t need an external programmer. It’s recommended to pick one that has an In-Circuit Debug Interface so all you would need is a usb connection to get started.

Most vendors such as Texas instruments will provide sample programs to run and also provide an IDE to use. There are many boards to choose from different vendors but as a beginner the idea is to get started quickly.
The Tiva C series LaunchPad will be used for future examples but the principles are similar for other boards.

#### Reading Datasheets

When writing firmware for embedded systems, a lot of time will be spent reading the datasheets of the microcontroller and components used in a project. I'd say this is the most important skill to master besides learning C.
The datasheet of a microcontroller and User manual are provided by the Vendor.

The user manual provides a hardware description of the board and how components are connected. The most important information to know is what pins of the microcontroller the components are connected to.

The datasheet of the MCU provides all the information you need to know such as the Architecture, Memory Map or Memory Model, available Memory, GPIO’s, Timers, and more. 


#### Hello world for embedded systems

If you’ve learned to code in the past, you’ve likely written a hello world program as an introduction to a programming language. In C, all you need is the standard io header file and a main function.

In embedded systems, the equivalent to hello world is blinking an LED. 
Most arduino’s have a built in LED and all you have to do is write this code to initialize the hardware then the built in LED turns on. 
For the launchpad, looking at the user manual, the block diagram shows there are three RGB LEDs connected to GPIO ports. Turning on an LED for the Launchpad is a more involved process So I’ll tackle the topic next time.




