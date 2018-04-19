# SmartParking

## Abstract
We have witnessed a rapid growth in the Internet of Things and its contribution to the growth of Smart cities in recent years. Consistent efforts have been undertaken by the Government of India to elevate the growth of this industry. The increase in population and vehicular densities have led to congested roads, inadequate parking facilities and poor infrastructure has called for a technology-driven solution known commonly as a Smart Parking System (SPS). The solution proposed in this paper is a client-based parking slot reservation system that is implemented using microcontrollers interfaced with sensors for parking vacancy detection. They are also connected to cloud services in order to produce a complete IoT solution, with each microcontroller acting as a node in a network. Additionally, the CAN protocol is deployed for communication between nodes of this network in case of failure of the nodes in the wireless network. This is a solution developed that caters to users mainly residing in Smart Cities and addresses the issue of network node failure.
A simple implementation of a smart reservation parking system.
Built an Android app for the user so the they can reserve parking slots based on the avaiability.(Used Android Studio - Intellij)

## Implementation
The system proposed uses the Arduino Uno to gather sensor data as well as communicate with external devices and modules. Each Arduino is interfaced with an HC-05 Bluetooth module to communicate with our Android devices. These HC- 05 modules are used to represent the Arduinos as being nodes in an interconnected network. Each of the nodes are interfaced with HC-SR04 ultrasonic sensors that are used to detect the occupancy of the parking slots by using ultrasonic signals to detect distance to objects.
Each of the parking slots are also equipped with RGB LEDs to indicate whether a parking slot is empty, occupied or reserved with emission of color like green, red and blue respectively. These LEDs are lit according to either the occupancy of a parking slot that is determined by the values coming in from the sensor or in case of reservation, it may depend on whether a user of the Android app has reserved the slot in advance. The reservation of a certain parking slot is communicated via the Bluetooth module.
### CAN
Controller Area Network also known as the CAN Bus is a fast, low cost and sturdy message-based protocol that allows micro-controllers to communicate with each other without the aid of a host device. It is generally used in the automotive industry to connect the various subsystems within the vehicle. It also finds great use in short range communication between micro-controllers for embedded systems as proposed in our paper.
CAN networks are useful in applications where there is need for small amounts of data to be shared over a network at regular intervals. The protocol used in CAN is the CSMA/CD+AMP type, which means that it is a carrier-sense, multiple-access protocol with collision detection and implementation of message priority using bit-wise arbitration.
In the network, each of the frames have a unique identifier or a frame ID that is used to determine where it’s coming from and what type of data it is carrying along with it.
### Android App
An Android application has been developed which is connected to the server to receive data about empty slots in the user’s vicinity. The application is also running the Google Maps API for Android which gives the user’s current location and the location of available parking slots in his vicinity. The time of entry and time of exit is calculated automatically and a bill is generated based on factors like time, duration, and demand.
We have used a Bluetooth module (HC-05), which is a low Bluetooth energy device that simulates the wireless communication between the user and the sensor system deployed at the parking spaces. The user selects a slot of his convenience and the Google Maps API is used to generate the shortest path to guide the user. The interface has been made such that the usage is quite simple along with providing all the above functionalities.
### Design
In the system proposed, the CAN protocol has been used as secondary source of communication in case of failure in the wireless communication that has been achieved using Bluetooth. Arduinos are interfaced with the CAN controller MCP2515 and high-speed transceivers named MCP2551.
These integrated chips facilitate the communication between Arduinos using the standard CAN protocol. The micro-controllers are connected in a bus topology, each transmitting the required bytes of information regarding information of the parking slots to every other micro-controller on the CAN Bus.
The distinction in the frame identifiers is what aids in identification of which exact parking slots a certain byte of data pertains to. This is an essential addition to the Smart Parking System that has been proposed, to act as a second line of communication in case of failure with the wireless communication that may have already been used in the system.

## Conclusion
Smart Cities are the future of tomorrow all around the world and various systems that co-exist within these environments make the city smart. One such system is the Smart Parking System, and the system proposed in the paper greatly automates the process by directly connecting the parking areas to the civilians by providing a platform in the form of an application. This application enables them to reserve these parking slots in advance and reduces the need of manually searching for them. This significantly reduces fuel usage and as a result of which reduces pollution in the city. To address to problem of node failure within a system such as this, that could cause several parking slots to go undetected or unused, the CAN protocol has been utilised. Therefore, the solution to parking proposed here is connected, robust and green which are the main requirements of any Smart system.


The bluetooth on your android device must be switched on before the app is opened, and connection(pairing) between the module an device must be done before the app is started.

Authors - 1) N.R. Vinay
          2) Rahul M Patil

