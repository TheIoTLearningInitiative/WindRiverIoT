Wind River® Helix™ App Cloud
==

> Wind River® Helix™ App Cloud speeds creation of Internet of Things (IoT) software for system manufacturers, integrators, and operators. Simulating a development environment, it allows you to use the Pulsar SDK to write applications even without a hardware platform.

> Wind River® Helix™ App Cloud is a new kind of software development platform that removes the traditional complexities of building applications for embedded devices and systems.

> To help start your embedded projects, App Cloud comes with Wind River Rocket™, our free real-time operating system (RTOS) for small, embedded devices.

- [Wind River® Helix App Cloud](http://www.windriver.com/products/helix/app-cloud/)
- [Wind River® Helix App Cloud Overview](http://www.windriver.com/products/product-overviews/wr-app-cloud_overview.pdf)

## App Cloud Homepage

> Now you can create, modify, and debug applications running on real hardware—in the cloud. Wind River® Helix™ App Cloud is the central place for managing your devices and projects.

How to get started

- Sign Up for Free
- Create a New Project
- Create Your Application

### Sign Up for Free

1. Go to https://app.cloud.windriver.com/user/register
2. If already registered https://app.cloud.windriver.com/

### Virtual Device Create a New Device

Select "New Device" from upper right corner

#### New Device

__Select the SDK__ Register an existing device or create a new device from a pre-defined list of Software Developer Kits (SDKs), select "Wind River Rocket for Intel x86 Simulator" then click "Next"

- Wind River Linux-7 for Intel Galileo
- Wind River Rocket for Intel Galileo Gen 2
- Wind River Rocket for Intel x86 Simulator
- Pulsar Linux for Minnowboard Max
- Pulsar Linux for ZedBoard.org Xilinx Zynq

__Enter a Device Name__ Choose "VirtualDevice" then select "Create Device"

#### Virtual Device Start

In summary

    VirtualDevice
     Wind River Rocket for Intel x86 Simulator 1.0.0.1
     Offline Device
    Description
     A Rocket OS distribution for QEMU x86 Quark
    Documentation
     [Getting started with Rocket on QEMU x86]()
    Registration ID
    Unique ID

Now select

 - __Start Device Simulation__, to start your Virtual Device
 - __Terminate Device Simulation__, to stop your Virtual Device

### Applications Projects, Templates

> Application Projects. This is the central place to manage your projects. Click on the button below to create your first project.

Create 2 different projects by selecting "Create New Project":

1. First called "MyDiningPhilosophers" based on "Dining Philosophers" Project Template
2. Second called "MyHelloWorld" based on "Empty C Project"

Open "MyHelloWorld" by selecting "Open" green button, "Loading your Workspace" message will appear shortly in a new web browser tab and then Could9 Workspace will be initialized

#### __Cloud9 Workspace__ Console "bash - helix app cloud"

Go to console "bash - helix app cloud" and type the following commands

    xe1gyq@helix-app-cloud:~$ cd
    xe1gyq@helix-app-cloud:~$ pwd
    /users/xe1gyq
    xe1gyq@helix-app-cloud:~$ ls
    MyDiningPhilosophers  MyHelloWorld  home  lost+found  mthread.d
    xe1gyq@helix-app-cloud:~$ 

#### __Cloud9 Workspace__ Console "outdir/zephyr.elf - Running"

Select "Run Project" and go to console "outdir/zephyr.elf"

    make
    * Zephyr Kernel/x86 Configuration
    * General Kernel Options
    * Security Options
    * Nanokernel Options
    * Microkernel Options
    * Timer API Options
    * X86 Platform Configuration options
    * Platform Capabilities
    * Processor Capabilities
    * Floating Point Options
    * x86 Core Options
    * Memory Layout Options
    * Device Drivers
    * Console drivers
    * Serial Drivers
    * Interrupt Controllers
    * Timer Drivers
    * Random Generation Configuration
    * PCI Settings
    * GPIO Drivers
    * SPI hardware bus support
    * I2C Drivers
    * PWM (Pulse Width Modulation) Drivers
    * Enable platform pinmux driver
    * ADC drivers
    * Cryptography
    * Compile and Link Features
    * Debugging Options
    * Safe memory access
    * System Monitoring Options
    # configuration written to .config
    Using /users/xe1gyq/MyHelloWorld/zephyr as source for kernel
      SYSMAP  System.map
    make[2]: Leaving directory '/users/xe1gyq/MyHelloWorld/outdir'
    make[1]: Leaving directory '/users/xe1gyq/MyHelloWorld/zephyr'
    Loading /users/xe1gyq/MyHelloWorld//outdir/zephyr.elf on target...  done
    Starting application...  done
    Application is now running

### Applications Projects, Github

You can import existing projects from Github

    xe1gyq@helix-app-cloud:~$ git clone https://github.com/...

### Galileo 2 Create a New Device

Select "New Device" from upper right corner

#### New Device

__Select the SDK__ Register an existing device or create a new device from a pre-defined list of Software Developer Kits (SDKs), select "Wind River Rocket for Intel Galileo Gen 2" then click "Next"

- Wind River Linux-7 for Intel Galileo
- Wind River Rocket for Intel Galileo Gen 2
- Wind River Rocket for Intel x86 Simulator
- Pulsar Linux for Minnowboard Max
- Pulsar Linux for ZedBoard.org Xilinx Zynq

__Enter a Device Name__ Choose "Galileo2Device" then select "Create Device"

#### Galileo 2 Start

In summary we need to:

- Deploy Wind River Rocket for Intel Galileo Gen2 on Galileo2Device
- Connect Device Virtual Gateway

Check Galileo2Device Summary

    Galileo2Device
     Wind River Rocket for Intel Galileo Gen2 1.0.0.1
     Offline Gateway
     Offline Device
    Description
     Designed for makers, students, educators, and DIY electronics enthusiasts, the Intel® Galileo Gen 2 board is an Arduino certified development and prototyping board based on Intel® ..
    Documentation
     [Hide deployment instructions]()
     [Getting started with Rocket on Galileo Gen 2]()
    Registration ID
    Unique ID

__Follow the instructions below to deploy Wind River Rocket for Intel Galileo Gen2 on Galileo2Device__

Click on "Generate and Download Device Image" and follow onscreen steps:

    Use a Galileo Gen 2 SD card to boot the Rocket OS as follows:
    1. To download the OS, click Generate & Download Device Image.
    2. Format a 1 GB or larger SD card as a FAT32 file system.
    3. Use any zip utility to extract the OS image to the SD Card.
    4. If you have not already done so, power off your board.
    5. Insert the SD card and power on the board.

__Device Virtual Gateway not connected__

Follow onscreen steps:

    You have to run a Virtual Gateway application on your desktop to use this device.
    The Virtual Gateway is specific to a device; you must download and run a different Virtual Gateway for each different device.

    To run the Virtual Gateway you must:
    - Download it for your device by clicking on the Download button
    - Unzip the archive on your host, and double click on the launch script Galileo2Device-virtual-gateway.sh
    - When prompted, enter the serial port connected to your device

When running "Galileo2Device-virtual-gateway.sh" this is the log seen:

    xe1gyq@jessie:~/Downloads/IntelGalileoGateway/Galileo2Device-virtual-gateway$ sh Galileo2Device-virtual-gateway.sh 
    
    Helix App Cloud Virtual Gateway for device Galileo2Device on server https://app.cloud.windriver.com
    Version: 0.2
    
    Provide the name of the serial port your device is connected to:
    Serial port: /dev/ttyUSB0
    Connecting serial port with serial parameters (from the SDK): 115200-8-N-1-N
    
    Configure a SOCKS v5 proxy to access App Cloud server (y/n, default is n): n
    
    Starting the Virtual Gateway for Galileo2Device.
    Connecting to Helix App Cloud server...
    Connection with Helix App Cloud server has been established
    Received connection request for serial port "/dev/ttyUSB0"
    Successfully opened serial port "/dev/ttyUSB0"


Check again Galileo2Device Summary

    Galileo2Device
     Wind River Rocket for Intel Galileo Gen2 1.0.0.1
     Online Gateway
     Online Device

### Applications Projects, Templates

> Application Projects. This is the central place to manage your projects. Click on the button below to create your first project.

Create a project by selecting "Create New Project". you will find several templates:

- Analog Red/Write (ADC/PWM)
- Digital Read/write (GPIO)
- Dining Philosophers
- Empty C Project
- Grove-LCD
- HTTP Server using LWIP Project

Choose "Grove-LCD" template and use "MyGrove-LCD" as its name

Open "MyGrove-LCD" by selecting "Open" green button, "Loading your Workspace" message will appear shortly in a new web browser tab and then Could9 Workspace will be initialized

#### __Cloud9 Workspace__ Console "bash - helix app cloud"

Go to console "bash - helix app cloud" and type the following commands

    xe1gyq@helix-app-cloud:~$ cd
    xe1gyq@helix-app-cloud:~$ pwd
    /users/xe1gyq
    xe1gyq@helix-app-cloud:~$ ls
    MyDiningPhilosophers  MyHelloWorld  home  lost+found  mthread.d
    xe1gyq@helix-app-cloud:~$ 

#### __Cloud9 Workspace__ Console "outdir/zephyr.elf - Running"

Select "Run Project" and go to console "outdir/zephyr.elf"

    make
    * Zephyr Kernel/x86 Configuration
    * General Kernel Options
    * Security Options
    * Nanokernel Options
    * Microkernel Options
    * Timer API Options
    * X86 Platform Configuration options
    * Platform Capabilities
    * Processor Capabilities
    * Floating Point Options
    * x86 Core Options
    * Memory Layout Options
    * Device Drivers
    * Console drivers
    * Serial Drivers
    * Interrupt Controllers
    * Timer Drivers
    * Random Generation Configuration
    * PCI Settings
    * GPIO Drivers
    * SPI hardware bus support
    * I2C Drivers
    * PWM (Pulse Width Modulation) Drivers
    * Enable platform pinmux driver
    * ADC drivers
    * Cryptography
    * Compile and Link Features
    * Debugging Options
    * Safe memory access
    * System Monitoring Options
    # configuration written to .config
    Using /users/xe1gyq/MyHelloWorld/zephyr as source for kernel
      SYSMAP  System.map
    make[2]: Leaving directory '/users/xe1gyq/MyHelloWorld/outdir'
    make[1]: Leaving directory '/users/xe1gyq/MyHelloWorld/zephyr'
    Loading /users/xe1gyq/MyHelloWorld//outdir/zephyr.elf on target...  done
    Starting application...  done
    Application is now running

### Applications Projects, Github

You can import existing projects from Github

    xe1gyq@helix-app-cloud:~$ git clone https://github.com/...

## Video Tutorials

- Rocket SDK Getting Started
- Rocket SDK Debugger Workflow
- Deploying Pulsar Linux to the Hardware
- Creating and Debugging a Pulsar C Application
- Creating and Debugging a Pulsar Javascript Application
- Building gzip on Pulsar - an Open Source Autoconf Project
- Building lua on Pulsar - an Open Source Makefile Project