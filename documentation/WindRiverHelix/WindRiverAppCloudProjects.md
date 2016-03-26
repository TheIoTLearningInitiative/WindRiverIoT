Projects
==

## Video Tutorials

- Rocket SDK Getting Started
- Rocket SDK Debugger Workflow
- Deploying Pulsar Linux to the Hardware
- Creating and Debugging a Pulsar C Application
- Creating and Debugging a Pulsar Javascript Application
- Building gzip on Pulsar - an Open Source Autoconf Project
- Building lua on Pulsar - an Open Source Makefile Project

## Wind River Rocket Intel x86 Simulator "VirtualDevice"

1. Close any Project running and terminate any Device simulation
2. Select "New Device" from upper right corner
3. From "Add a new device to App Cloud" popup window select "Create a new device from the supported SDK list"

### Device Setup

#### Add a new device to App Cloud

__Select a SDK__ Register an existing device or create a new device from a pre-defined list of Software Developer Kits (SDKs), select "Wind River Rocket for Intel x86 Simulator" then click "Next"

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

Before moving on, start Device Simulation

### Application Development

#### Wind River Rocket Intel x86 Simulator "VirtualDevice", Applications Projects, Templates

> Application Projects. 
> > This is the central place to manage your projects. Click on the button below to create your first project.

Create 2 different projects by selecting "Create New Project":

1. First called "MyDiningPhilosophers" based on "Dining Philosophers" Project Template
2. Second called "MyHelloWorld" based on "Empty C Project"

Open "MyHelloWorld" by selecting "Open" green button, "Loading your Workspace" message will appear shortly in a new web browser tab and then Could9 Workspace will be initialized.

##### __MyHelloWorld - Cloud9 Workspace__ Console "outdir/zephyr.elf - Running"

1. Go to MyHelloWorld Could9 Workspace web browser tab
2. Select "Run Project"
3. Go to console "outdir/zephyr.elf - Running"

```sh
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
```

##### __MyHelloWorld - Cloud9 Workspace__ Console "bash - xe1gyq@helix-app-cloud:~/MyHelloWorld$"

1. Go to MyHelloWorld Could9 Workspace web browser tab
2. Select "Run Project"
3. Clic on "+" under Console Area and Select "New Terminal"
3. Under terminal "bash - xe1gyq@helix-app-cloud:~/MyHelloWorld" and type the following commands

```sh
    xe1gyq@helix-app-cloud:~/MyHelloWorld$ pwd
    /users/xe1gyq/MyHelloWorld
    xe1gyq@helix-app-cloud:~/MyHelloWorld$ ls ..
    MyDevices  MyDiningPhilosophers  MyHelloWorld  home  lost+found  mthread.d
    xe1gyq@helix-app-cloud:~/MyHelloWorld$ 
```

###### Make Menuconfig

```sh
xe1gyq@helix-app-cloud:~/MyHelloWorld$ make menuconfig
make[1]: Entering directory '/users/xe1gyq/MyHelloWorld/zephyr'
make[2]: Entering directory '/users/xe1gyq/MyHelloWorld/outdir'
  GEN     ./Makefile
  HOSTCC  scripts/kconfig/mconf.o
  HOSTCC  scripts/kconfig/lxdialog/checklist.o
  HOSTCC  scripts/kconfig/lxdialog/util.o
  HOSTCC  scripts/kconfig/lxdialog/inputbox.o
  HOSTCC  scripts/kconfig/lxdialog/textbox.o
  HOSTCC  scripts/kconfig/lxdialog/yesno.o
  HOSTCC  scripts/kconfig/lxdialog/menubox.o
  HOSTLD  scripts/kconfig/mconf
scripts/kconfig/mconf Kconfig


*** End of the configuration.
*** Execute 'make' to start the build or try 'make help'.

make[2]: Leaving directory '/users/xe1gyq/MyHelloWorld/outdir'
make[1]: Leaving directory '/users/xe1gyq/MyHelloWorld/zephyr'
xe1gyq@helix-app-cloud:~/MyHelloWorld$ 
```

###### Make

```sh
xe1gyq@helix-app-cloud:~/MyHelloWorld$ make
make[1]: Entering directory '/users/xe1gyq/MyHelloWorld/zephyr'
make[2]: Entering directory '/users/xe1gyq/MyHelloWorld/outdir'
  Using /users/xe1gyq/MyHelloWorld/zephyr as source for kernel
  GEN     ./Makefile
  CHK     include/generated/version.h
  CHK     misc/generated/configs.c
  CHK     include/generated/offsets.h
  CHK     misc/generated/sysgen/prj.mdef
make[2]: Leaving directory '/users/xe1gyq/MyHelloWorld/outdir'
make[1]: Leaving directory '/users/xe1gyq/MyHelloWorld/zephyr'
xe1gyq@helix-app-cloud:~/MyHelloWorld$ 
```

###### Upper Directories

```sh
xe1gyq@helix-app-cloud:~/MyHelloWorld$ ls
Makefile  MyDevices  outdir  prj.mdef  prj_x86.conf  src  zephyr
xe1gyq@helix-app-cloud:~/MyHelloWorld$ ls src/
Makefile  built-in.o  main.c  main.o
xe1gyq@helix-app-cloud:~/MyHelloWorld$ ls zephyr/
Kbuild   Kconfig.zephyr  Makefile.inc  arch           debug    include  lib   net     scripts
Kconfig  Makefile        README.txt    buildDefaults  drivers  kernel   misc  schema  zephyr-env.sh
xe1gyq@helix-app-cloud:~/MyHelloWorld$ ls outdir/
Makefile    drivers             irq_int_vector_map.o  misc         zephyr      zephyr.lst
System.map  final-linker.cmd    kernel                scripts      zephyr.bin  zephyr.map
arch        include             lib                   source       zephyr.elf  zephyr.strip
debug       int_vector_alloc.o  linker.cmd            staticIdt.o  zephyr.lnk
```

#### Wind River Rocket Intel x86 Simulator "VirtualDevice", Applications Projects, Github

You can import existing projects from Github, let's import philosophers example

```sh
    xe1gyq@helix-app-cloud:~$ git clone https://github.com/wind-river-rocket/dining-philosophers-sample-app.git
```

- [Wind River Rocket Sample Applications Github](https://github.com/wind-river-rocket)

## Wind River Rocket Galileo 2 "Galileo2Device"

1. Close any Project running and terminate any Device simulation
2. Select "New Device" from upper right corner
3. From "Add a new device to App Cloud" popup window select "Create a new device from the supported SDK list"

### Device Setup

#### Add a new device to App Cloud

__Select the SDK__ Register an existing device or create a new device from a pre-defined list of Software Developer Kits (SDKs), select "Wind River Rocket for Intel Galileo Gen 2" then click "Next"

__Enter a Device Name__ Choose "Galileo2Device" then select "Create Device"

#### Galileo 2 Device Start

In summary we need to:

- Deploy Wind River Rocket for Intel Galileo Gen2 on Galileo2Device
- Connect Device Virtual Gateway

Check Galileo2Device Summary

```sh
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
```

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

```sh
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
```

Check again Galileo2Device Summary

```sh
    Galileo2Device
     Wind River Rocket for Intel Galileo Gen2 1.0.0.1
     Online Gateway
     Online Device
```

### Application Development

#### Wind River Rocket Galileo 2 "Galileo2Device", Applications Projects, Templates

> Application Projects. This is the central place to manage your projects. Click on the button below to create your first project.

Create a project by selecting "Create New Project". you will find several templates:

- Analog Red/Write (ADC/PWM)
- Digital Read/write (GPIO)
- Dining Philosophers
- Empty C Project
- Grove-LCD
- HTTP Server using LWIP Project

Choose "Grove-LCD" template and name it "MyGrove-LCD"

Open "MyGrove-LCD" by selecting "Open" green button, "Loading your Workspace" message will appear shortly in a new web browser tab and then Could9 Workspace will be initialized

### __MyGrove-LCD Cloud9 Workspace__ Console "bash - helix app cloud"

Go to console "bash - helix app cloud" and type the following commands

```sh
    xe1gyq@helix-app-cloud:~/MyGrove-LCD$ ls
    Makefile  README.txt  outdir  prj.mdef  prj_x86.conf  src  zephyr
    xe1gyq@helix-app-cloud:~/MyGrove-LCD$ make menuconfig
```

### __MyGrove-LCD Cloud9 Workspace__ Console "outdir/zephyr.elf - Running"

Select "Run Project" and go to console "outdir/zephyr.elf"

```sh
    make
    make
    make[1]: Entering directory '/users/xe1gyq/MyGrove-LCD/zephyr'
    make[2]: Entering directory '/users/xe1gyq/MyGrove-LCD/outdir'
      Using /users/xe1gyq/MyGrove-LCD/zephyr as source for kernel
      GEN     ./Makefile
      CHK     include/generated/version.h
      CHK     misc/generated/configs.c
      CHK     include/generated/offsets.h
      CHK     misc/generated/sysgen/prj.mdef
    make[2]: Leaving directory '/users/xe1gyq/MyGrove-LCD/outdir'
    make[1]: Leaving directory '/users/xe1gyq/MyGrove-LCD/zephyr'
    Loading /users/xe1gyq/MyGrove-LCD//outdir/zephyr.elf on target...  done
    Starting application...  done
    Application is now running
    Pin 0 configured
    Pin 1 configured
    Pin 2 configured
    Pin 3 configured
    Pin 4 configured
    Pin 5 configured
    Pin 6 configured
    Pin 7 configured
    Pin 8 configured
    Pin 9 configured
    Pin 10 configured
    Pin 11 configured
    Pin 12 configured
    Pin 13 configured
    Pin 14 configured
    Pin 15 configured
    Pin 16 configured
    Pin 17 configured
    Pin 18 configured
    Pin 19 configured
    Initialize LCD ... done
    Button on D3 = 0
```

