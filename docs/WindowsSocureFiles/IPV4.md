# IPV4

These sets of commands help to gather information about Internet protocol 4 of the Target machine

### SYNOPSIS

- Collects various IPv4 configuration and status information using netsh commands.

### DESCRIPTION

- This script collects various IPv4 configuration and status information using the netsh command

- The show address show the current IP address configuration for all interfaces.

- The show offload displays the offload settings for IPv4.

- The show dynamicportrange shows the dynamic port range settings for IPv4.

- The show interface displays the current IPv4 interface configuration.

### WHY IT IS USED

- This script is intended for use in a controlled environment and should be
executed with appropriate permissions.

#### Code Overview

    @echo off
    mkdir IPV4
    cd IPV4

Create a new folder name IPV4

    netsh interface ipv4 show address > IPV4_address.txt

The netsh interface ipv4 show address command in Windows Command Prompt displays the IPv4 address configuration for all network interfaces on the system.

    netsh interface ipv4 show offload > IPV4_offload.txt

The netsh interface ipv4 show offload command is not the correct syntax; instead, use netsh int tcp show global or netsh int tcp show chimneystats to view TCP Chimney Offload status, and check the network adapter's advanced settings for other offload features like IPv4 checksum and Receive-Side Scaling (RSS). These commands display if network processing tasks are offloaded from the CPU to the network adapter to improve performance. 

    netsh interface ipv4 show dynamicportrange UDP > IPV4_dynamicportrangeUDP.txt

    netsh interface ipv4 show dynamicportrange tcp > IPV4_dynamicportrangeTCP.txt

These commands will display the start port and the number of ports configured for the respective dynamic port range on the system.

**The next commands output will be shown copy all and paste in the IPV4.txt file**

    netsh interface ipv4 show compartments

The command netsh interface ipv4 show compartments is not a valid command in Windows. The user likely intended to type a command to view or modify network interface settings. Common commands include netsh interface ipv4 show interfaces to show a list of IPv4 network interfaces, or netsh interface ipv4 show address to display IPv4 address information for all interfaces. 

    netsh interface ipv4 show config

The netsh interface ipv4 show config command, when executed in the Windows Command Prompt, displays the IPv4 configuration information for all network interfaces on the system.

    netsh interface ipv4 show destinationcache

The command netsh interface ipv4 show destinationcache is a Windows command-line utility used to display the contents of the IPv4 destination cache on a system. This cache stores information about recently accessed network destinations, including details learned through Path MTU Discovery (PMTUD).

    netsh interface ipv4 show excludedportrange

The netsh interface ipv4 show excludedportrange command is used in Windows to display the ranges of TCP and UDP ports that are currently excluded from use by applications. This exclusion can be due to various reasons, such as system services reserving ports, Hyper-V or other virtualization technologies, or manually configured exclusions.

    netsh interface ipv4 show global 

    netsh interface ipv4 show icmpstats

    netsh interface ipv4 show interfaces

    netsh interface ipv4 show ipaddresses

    netsh interface ipv4 show ipnettomediaj

    netsh interface ipv4 show ipstats

    netsh interface ipv4 show joins

    netsh interface ipv4 show neighbors

    netsh interface ipv4 show route

    netsh interface ipv4 show subinterfaces

    netsh interface ipv4 show tcpconnections

    netsh interface ipv4 show udpconnections

    netsh interface ipv4 show show udpstats

    netsh interface ipv4 show udpstats  

    netsh interface ipv4 show winsservers  

    netsh interface ipv4 show excludedportrange protocol=tcp

    netsh interface ipv4 show excludedportrange protocol=udp

    notepad IPV4.txt