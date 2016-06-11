# Projects

> What is Lab Cloud? Lab Cloud is a software lab that simulates hardware in a cloud platform. Using Lab Cloud, you can rapidly create and deliver IoT device and system software, both within your organization and to outside teams. From a single device to a system with many components, it's easy to access and share in Lab Cloud. In Lab Cloud you can:
> - Create instances of virtual hardware platforms with pre-loaded OS software - called Lab Sessions.
> - Upload your own software and content to your Lab Session.
> - Share Lab Sessions and content you upload to the Lab Session with anyone.
> - Collaborate live or offline and play or replay your software from any point.
> - Create network connections to your Lab Session system like you would to a real hardware system.
> - Automate your Lab Session system with Lab Cloud Web API.

# Logging in

[Lab Cloud](https://lab.cloud.windriver.com/)

# Getting Started

> To get started in Lab Cloud you will need to create a Lab Session based on one of our existing Lab Cloud Platforms.

> To use the platform with Helix App Cloud you will need to create a Helix App Cloud account and select the Helix App Cloud option during the new session creation process in Helix Lab Cloud. To connect to App Cloud first run the Lab Session from Lab Cloud by pressing the play button and then click the bug button to launch Wind River Helix App Cloud to create an automatic connection. Once in App Cloud you can create a software project and download Wind River Rocket example programs or write your own. If you stop the Lab Session, you must restart/reload each time from Snapshot 0 in Lab Cloud to reconnect to App Cloud. For more information about Rocket RTOS see the Wind River Rocket product page - www.windriver.com/products/operating-environments/rocket/

# MyPlatformGalileo, Demo Wind River Rocket Galileo, Hello World

> Demo - Wind River Rocket 'Hello World' program running on Intel 1.0.0.1.
> > Demo of a simple Wind River Rocket program running on an Intel Quark Galileo Virtual System. This demo will be enhanced as new features of the Wind River Helix Cloud products and Wind River Rocket RTOS are made available.

Select "New Sessions"

1. Select the Platform "Demo Wind River Rocket Hello World Program running on Intel" and click on "Next"
2. Enter a Session Name "MyPlatformGalileo" and click on "Create Session"
3. Click on "Start" button


```sh
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
```

# MyPlatformGalileo, Demo Wind River Rocket Galileo

> Intel Galileo running Wind River Rocket with App Cloud Support 1.0.0.8
> > An Intel Galileo Virtual System with a Quark SoC X1000 Series processor running the Wind River Rocket RTOS.

Select "New Sessions"

1. Select the Platform "Intel Galileo running Wind River Rocket with App Cloud Support" and click on "Next"
2. Enter a Session Name "MyPlatformGalileoAppCloud" and click on "Create Session"
3. Click on "Start" button

## Develop Applications

Select "Develop Application with Helix Application Cloud" then free to explore!

# MyCorei7, Demo Wind River Pulsar Linux 7 Core i7

Select "New Sessions"

1. Select the Platform "Intel Core i7 Virtual System running Wind River Pulsar Linux 7" and click on "Next"
2. Enter a Session Name "MyCorei7" and click on "Create Session"
3. Click on "Start" button

## MyCorei7, Console DomainE

```sh
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
```

## MyCorei7, Console Domain0

```sh
    cube-31-10-15-dom0 login: root
    Password: incendia
    root@cube-31-10-15-dom0:~# 
```

## MyCorei7, Helix Lab Network Proxy

- Log in to Wind River® Helix™ Lab Cloud
- Go to "User Profile"
- Select "+" under "Web APIs <> [User Access Token](https://lab.cloud.windriver.com/#/user/profile#AccessToken)" and copy your key

```sh
    Web APIs access token
    New access token is : 
    CFE_a33c6ff3_a345_896b_6473_e957b23d8675
    Please copy this access token, it will no longer be accessible after closing this dialog box.
```

- Click on "?" from "Helix Lab Network Proxy" and review Documentation:
   - [Client Connection Software Installation Instructions](https://lab.cloud.windriver.com/documents/networkproxy/network_installation)
   - [Lab Cloud Networking Getting Started](https://lab.cloud.windriver.com/documents/networkproxy/network_getting_started)
   - [Lab Cloud Networking Example](https://lab.cloud.windriver.com/documents/networkproxy/network_examples)

- Install NodeJS in your Host
 
```sh
# apt-get install --yes nodejs
Reading package lists... Done
Building dependency tree       
Reading state information... Done
nodejs is already the newest version.
0 upgraded, 0 newly installed, 0 to remove and 162 not upgraded.
#     
```

- Download and Install "Client Connection Software"

```sh
xe1gyq@jessie:~/Downloads/$ mkdir helix
xe1gyq@jessie:~/Downloads/$ cd helix
xe1gyq@jessie:~/Downloads/helix$ cp ../helix-lab-network-proxy.zip .
xe1gyq@jessie:~/Downloads/helix$ 
```

```sh
xe1gyq@jessie:~/Downloads/helix$ unzip helix-lab-network-proxy.zip
Archive:  helix-lab-network-proxy.zip
   creating: helix-lab-network-proxy/
  inflating: helix-lab-network-proxy/terminal.js  
   creating: helix-lab-network-proxy/node_modules/
...
  inflating: helix-lab-network-proxy/helix-lab-network-proxy.sh  
  inflating: helix-lab-network-proxy/portforward.js 
xe1gyq@jessie:~/Downloads/helix$ 
```

```sh
xe1gyq@jessie:~/Downloads/helix$ cd helix-lab-network-proxy/
xe1gyq@jessie:~/Downloads/helix/helix-lab-network-proxy$ ls
connection.json              helix-lab-network-proxy.js  node_modules    sails.js       terminal.js
devices.js                   helix-lab-network-proxy.sh  package.json    sessions.js    utils.js
helix-lab-network-proxy.cmd  LICENSE                     portforward.js  tcf-client-js  version.js

```

```sh
xe1gyq@jessie:~/Downloads/helix/helix-lab-network-proxy$ ./helix-lab-network-proxy.sh 
Helix Network Proxy v1.2.0

You are using a Wind River account to connect to the Helix server.
Your credentials are read from the file /home/xe1gyq/.helix-network-proxy.cred
    
Using the credential saved for a connection to the Helix server, https://lab.cloud.windriver.com
    
Authenticating to https://lab.cloud.windriver.com
Authentication successful.
MyCorei7: Secured communication established with target.
MyCorei7: Network proxy server running: 53984 -> 22 (UDP)
MyCorei7: Network proxy server running: 40695 -> 22 (TCP)
MyCorei7: Network proxy server running: 33143 -> 1534 (UDP)
MyCorei7: Network proxy server running: 34300 -> 1534 (TCP)
    
```

## MyCorei7, Remote Connection

```sh
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
```

# MyMinnowboardMax, Demo Wind River Linux 7 Minnowboard MAX

Create and Deploy and New Session for Pulsar Linux for Minnowboard MAX

