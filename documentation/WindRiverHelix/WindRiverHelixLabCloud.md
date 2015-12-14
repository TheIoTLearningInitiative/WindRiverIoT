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

### Demo Hello World

Select "New Sessions"

1. Select the Platform "Demo Wind River Rocket Hello World Program running on Intel" and click on "Next"
2. Enter a Session Name "MyPlatformGalileo"
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

### Helix Lab Network Proxy

1. Log in to Wind River® Helix™ Lab Cloud
2. Go to "User Profile"
3. Select "+" from "Web APIs <> User Access Token"

    Web APIs access token
    New access token is : 
    CFE_a33c6ff3_a345_896b_6473_e957b23d8675
    Please copy this access token, it will no longer be accessible after closing this dialog box.
    
https://lab.cloud.windriver.com/download/helix-network-proxy?os=linux&arch=x86

    # apt-get install --yes nodejs
    xe1gyq@jessie:~/Downloads/helix$ #unzip helix-lab-network-proxy.zip 
    xe1gyq@jessie:~/Downloads/helix$ cd helix-lab-network-proxy/
    xe1gyq@jessie:~/Downloads/helix/helix-lab-network-proxy$ ls
    connection.json              helix-lab-network-proxy.js  node_modules    sails.js       terminal.js
    devices.js                   helix-lab-network-proxy.sh  package.json    sessions.js    utils.js
    helix-lab-network-proxy.cmd  LICENSE                     portforward.js  tcf-client-js  version.js
    xe1gyq@jessie:~/Downloads/helix/helix-lab-network-proxy$ ./helix-lab-network-proxy.sh 
    Helix Network Proxy v1.2.0
    
    You are using a Wind River account to connect to the Helix server.
    You have to enter your access token to authenticate yourself against the server.
    The access token is created from the User Profile page.
    It will be saved localy in the file /home/xe1gyq/.helix-network-proxy.cred
    
    Enter your access token for the Helix server, https://lab.cloud.windriver.com
    Access Token: ****************************************
    
    Authenticating to https://lab.cloud.windriver.com
    Authentication successful.
    Credentials saved to the file /home/xe1gyq/.helix-network-proxy.cred
    MyPlatformi7: Secured communication established with target.
    MyPlatformi7: Network proxy server running: 51868 -> 22
    MyPlatformi7: Network proxy server running: 54354 -> 1534


xe1gyq@jessie:~/Downloads/helix/helix-lab-network-proxy$ ssh root@127.0.0.1 -p 51868

The authenticity of host '[127.0.0.1]:51868 ([127.0.0.1]:51868)' can't be established.
ECDSA key fingerprint is ca:3e:b3:c0:3b:6b:f6:04:03:44:ae:27:e0:7d:a5:98.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added '[127.0.0.1]:51868' (ECDSA) to the list of known hosts.
root@127.0.0.1's password: 
Permission denied, please try again.
root@127.0.0.1's password: 
Permission denied, please try again.
root@127.0.0.1's password: 
Permission denied (publickey,password).
xe1gyq@jessie:~/Downloads/helix/helix-lab-network-proxy$ ssh root@127.0.0.1 -p 51868
root@127.0.0.1's password: 
Last login: Wed Dec  2 07:00:35 2015
root@cube-31-10-15-domE:~# 
