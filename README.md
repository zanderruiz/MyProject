# HelloWorld F´ Project

<img src="https://user-images.githubusercontent.com/30123691/186647333-c7c3bd66-bbe6-4111-aabb-e03b9893b243.png" alt="f-prime logo" width="1000"/>

F´ (F Prime) is a robust, component-driven framework developed by NASA that empowers developers to rapidly create and deploy spaceflight and embedded software applications. For detailed information about F´, you can visit the official [F´ website](https://nasa.github.io/fprime/).

## Project Overview

This project serves as a practice in utilizing NASA's F´ framework to create a functional spaceflight software component. The primary goal of this project is to demonstrate the practical use of F´ in a simulated spaceflight scenario. In this project, I've created an F´ component responsible for issuing communication commands to a "satellite." The satellite, in this case, is simulated using a local server that runs other F´ components included in this project. Communication commands are issued from a "groundstation," accessible through a local client via a web browser interface.

## Getting Started

To run this project and simulate the communication between the groundstation and the satellite, you'll need to follow these steps:

### Building the Project

Before you can start using the project, you'll need to build it. Open your terminal and navigate to the project directory and its components:

```bash
cd MyProject
fprime-util build
cd MyProject/Components
fprime-util build
```

In the MyProject/HelloWorldDeployment directory, run the following command to build the deployment:

```bash
Copy code
cd MyProject/HelloWorldDeployment
fprime-util build -j4
```

### Starting the Deployment

To start the deployment with the default settings, run the following command in the HelloWorldDeployment folder:

```bash
Copy code
fprime-gds
```

This command will launch the F´ Ground Data System (GDS), and the F´ GDS control page should automatically open in your web browser. If the web page doesn't open automatically, you can access it by navigating to http://127.0.0.1:5000 in your web browser.

## Interacting with the Web Browser Client

Once the F´ GDS control page is open in your web browser, you can interact with the groundstation and send communication commands to the simulated satellite. Here are the steps to follow:

1. Navigate to the "Commanding" tab in the F´ GDS.
1. In the "Select Command" dropdown list, choose "helloWorld.SAY_HELLO."
1. In the argument input box, type a greeting message.
1. Click the "Send Command" button to send the command to the satellite.
1. In the "Events" tab, you can observe that the event list contains the "Hello" event with the text you entered when sending the command.
1. In the "Channels" tab, you will find "helloWorld.GreetingCount" in the channel list, showing the recorded number of times the "helloWorld.SAY_HELLO" command was sent.

With these instructions, you should be able to effectively interact with this project. Feel free to experiment and adapt the project as needed for your specific use case.
