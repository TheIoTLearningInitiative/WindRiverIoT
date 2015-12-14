Wind River® Helix™ Lab Cloud
==

> Build Better IoT Systems, Faster. Lab Cloud simulates real-world environments and hardware systems on a virtual cloud-based platform. Whether your IoT system is a single device or a network of systems with many different components and architectures - use Lab Cloud to quickly design, develop and test the IoT system.

[Wind River® Helix™ Lab Cloud Webpage](https://lab.cloud.windriver.com/)

## Getting Started

- Instantly access hardware environments from anywhere.
- Debug with full control and flexibility. Test software at any time.
- Collaborate easily with anyone and provide to your team full visibility and access

### Sessions

> This is the central place to manage your Simics sessions. Click on the topbar buttons to create your first session.

### Platforms

- ARM Cortex-A9
- Demo - Chip Variants
- Demo - Wind River Rocket Hello World
- Freescale P2020DS Virtual
- Freescale P3041DS Virtual
- Freescale P4080DS Virtual 
- Intel Core i7 virtual
- Intel Core i7 x58 virtual
- Intel Galileo running Wind River Rocket
- Intel MinnowMax Virtual
- PowerPC e600 Virtual
- PowerPC e6500 Virtual

## MyPlatformGalileo, Demo Wind River Rocket Galileo

Select "New Sessions"

1. Select the Platform "Demo Wind River Rocket Hello World Program running on Intel" and click on "Next"
2. Enter a Session Name "MyPlatformGalileo" and click on "Create Session"
3. Click on "Resume the Simulation" button

> Demo - Wind River Rocket 'Hello World' program running on Intel 1.0.0.1. Demo of a simple Wind River Rocket program running on an Intel Quark Galileo Virtual System.

    ACPI 2.0 table at: 0F01E014                       
    Loading from disk...   
    Opening [\EFI\BOOT\bootapp.sys]... FSOpen: Open '\EFI\BOOT\bootapp.sys' Success
    Read 481046 bytes.
    Loading 32-bit ELF image.
    Total memory: 265023488 bytes
    CSM video not available.                       
    Booting...        
    Jumping to boot image at 0x100000...
    Hello World
    Hello World
    Hello World
    ...

## MyCorei7, Demo Wind River Pulsar Linux 7 Core i7

Select "New Sessions"

1. Select the Platform "Intel Core i7 Virtual System running Wind River Pulsar Linux 7" and click on "Next"
2. Enter a Session Name "MyCorei7" and click on "Create Session"
3. Click on "Resume the Simulation" button

### MyCorei7, Console DomainE

    Pulsar Linux 7.0.0.10 cube-31-10-15-domE ttyS0
    cube-31-10-15-domE login: root
    Password: 
    Last login: Mon Nov  2 07:00:16 EST 2015 on ttyS0
    root@cube-31-10-15-domE:~# date -s "02 NOV 2015 12:00:00"
    Mon Nov  2 12:00:00 EST 2015
    root@cube-31-10-15-domE:~# tcf-agent -d
    linux trace EP:3957 Warning: perf SW events [9 .. 9] not supported
    Enabling per-cpu perf event buffering
    root@cube-31-10-15-domE:~# 
    root@cube-31-10-15-domE:~# [   22.816063] br0: port 1(eth0)
    entered forwarding state
    [   22.817492] br0: port 2(veth8UNETN) entered forwarding state
    [   23.456140] br0: port 1(eth0) entered forwarding state
    [   24.544063] br0: port 3(veth2J79XH) entered forwarding state
    [   24.800064] br0: port 1(eth0) entered forwarding state
    root@cube-31-10-15-domE:~# 

### MyCorei7, Console Domain0

    cube-31-10-15-dom0 login: rootPassword: 
    root@cube-31-10-15-dom0:~# 


### MyCorei7, Helix Lab Network Proxy

- Log in to Wind River® Helix™ Lab Cloud
- Go to "User Profile"
- Select "+" under "Web APIs <> User Access Token" and copy your key


    Web APIs access token
    New access token is : 
    CFE_a33c6ff3_a345_896b_6473_e957b23d8675
    Please copy this access token, it will no longer be accessible after closing this dialog box.

- Click on "?" from "Helix Lab Network Proxy" and review Documentation
   - [Client Connection Software Installation Instructions
](https://lab.cloud.windriver.com/documents/networkproxy/network_installation)
   - [Lab Cloud Networking Getting Started](https://lab.cloud.windriver.com/documents/networkproxy/network_getting_started)
   - [Lab Cloud Networking Example](https://lab.cloud.windriver.com/documents/networkproxy/network_examples)

- Install NodeJS in your Host
 

    # apt-get install --yes nodejs


- Download and Install "Client Connection Software"


    xe1gyq@jessie:~/Downloads/helix$ unzip helix-lab-network-proxy.zip
    xe1gyq@jessie:~/Downloads/helix$ cd helix-lab-network-proxy/
    xe1gyq@jessie:~/Downloads/helix/helix-lab-network-proxy$ ls
    connection.json              helix-lab-network-proxy.js  node_modules    sails.js       terminal.js
    devices.js                   helix-lab-network-proxy.sh  package.json    sessions.js    utils.js
    helix-lab-network-proxy.cmd  LICENSE                     portforward.js  tcf-client-js  version.js

    xe1gyq@jessie:~/Downloads/helix/helix-lab-network-proxy$ ./helix-lab-network-proxy.sh 
    Helix Network Proxy v1.2.0

    You are using a Wind River account to connect to the Helix server.
    Your credentials are read from the file /home/xe1gyq/.helix-network-proxy.cred
    
    Using the credential saved for a connection to the Helix server, https://lab.cloud.windriver.com
    
    Authenticating to https://lab.cloud.windriver.com
    Authentication successful.
    MyCorei7: Secured communication established with target.
    MyCorei7: Network proxy server running: 40733 -> 22
    MyCorei7: Network proxy server running: 42729 -> 1534

### MyCorei7, Remote Connection


    xe1gyq@jessie:~/Downloads/helix/helix-lab-network-proxy$ ssh root@127.0.0.1 -p 48068
    The authenticity of host '[127.0.0.1]:48068 ([127.0.0.1]:48068)' can't be established.
    ECDSA key fingerprint is eb:8a:0c:b7:69:03:72:26:0b:da:88:d7:5c:09:94:7a.
    Are you sure you want to continue connecting (yes/no)? yes
    Warning: Permanently added '[127.0.0.1]:48068' (ECDSA) to the list of known hosts.
    root@127.0.0.1's password: incendia
    Last login: Wed Dec  2 07:00:35 2015
    root@cube-31-10-15-domE:~# ifconfig
    root@cube-31-10-15-domE:~# ifconfig
    br0       Link encap:Ethernet  HWaddr 86:0c:7c:2a:61:50  
              inet addr:10.10.0.4  Bcast:10.10.0.255  Mask:255.255.255.0
    root@cube-31-10-15-domE:~# smart update
    Updating cache...                               ################################################################## [100%]
    
    Fetching information for 'core2_64_intel_common'...                      
    Fetching information for 'all'...                                 
    Fetching information for 'core2_64'...
    Fetching information for 'intel_corei7_64'...

## MyMinnowboardMax, Demo Wind River Linux 7 Minnowboard MAX

Create, deploy, 
