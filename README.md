# cloud-based-ring-conveyor-management-system

My diploma project is dedicated to the development of a ring conveyor control system, which is part of the mini-FMS "Denford" transport and storage system.
The conveyor interacts with the following equipment:
- Warehouse;
- Production module with milling machine;
- Production module with a lathe;
- Control module.
In front of each of these FMS components on the conveyor there are special pneumatic locks that allow you to stop the pallets with the workpiece moving along the 
conveyor belt.

The developed control system is represented by three levels: devices, gateways, IoT platform.
Devices are conveyor and FMS modules it serves.
A gateway is a bridge between an IoT platform and devices. The gateway in the proposed system is primarily designed to provide access to the Internet, processing 
commands coming from the IoT platform and preliminary preparation of data (for example, sensor readings) before sending them to the IoT platform.
The IoT platform ensures the interaction of devices and the storage of data associated with them, provides the ability to create dashboards (operator panels) for 
control and monitoring, is responsible for processing requests for executing commands and responding to emergency situations. The IoT platform is located on a cloud 
server.

Node-RED, a visual programming tool for creating IoT applications, was chosen for programming the gateway (Raspberry Pi 3 model B+). The flow programming paradigm 
acts as a key component of Node-RED. Flow programming is a way of describing the behavior of an application in the form of a network of black boxes or "nodes", as they 
are called in Node-RED. Each node has a clear goal – it receives some data, processes this data, and then transmits it to the next node. Connected nodes, usually a 
combination of input nodes, processing nodes, and output nodes, form "flows" when connected together. All flows function in parallel.

ThingsBoard was chosen as the IoT platform. ThingsBoard provides the following features:
- Registration of devices, defining connections between them;
- Collecting and visualizing data from devices using dashboards;
- Generation of alarms and notification of their occurrence via emails and SMS;
- Device management using Remote Procedure Calls (RPC);
- Creating rule chains for data processing and performing actions when intra-platform events occur.

This repository contains JSON representations of Node-RED threads, ThingsBoard dashboards and rule chains.
