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

The netsh interface ipv4 show global command in Windows provides a detailed overview of the global IPv4 configuration settings that apply across all network interfaces on the system. These settings influence how the operating system handles IPv4 traffic, impacting aspects such as routing, packet reassembly, security, and performance.

    netsh interface ipv4 show icmpstats

The command netsh interface ipv4 show icmpstats is used in Windows to display statistics related to the Internet Control Message Protocol (ICMP) for IPv4. This command provides a summary of ICMP messages sent and received, including various types of ICMP messages and any errors encountered.

    netsh interface ipv4 show interfaces

The netsh interface ipv4 show interfaces command in Windows provides a detailed list of all IPv4 network interfaces on the system.

    netsh interface ipv4 show ipaddresses

The netsh interface ipv4 show ipaddresses command is used in the Windows Command Prompt to display the IP address configuration for IPv4 on all network interfaces.

    netsh interface ipv4 show ipnettomedia

The command netsh interface ipv4 show ipnettomedia is incorrect and will produce an error because there is no ipnettomedia subcommand in the netsh utility. The correct command to view information about network interfaces is netsh interface ipv4 show interfaces which displays details for all IPv4 interfaces, including their status, name, and index.

    netsh interface ipv4 show ipstats

The netsh interface ipv4 show ipstats command in Windows displays detailed statistics related to the Internet Protocol (IP) for IPv4. This command is part of the netsh (Network Shell) utility, which allows for command-line configuration and monitoring of network settings.

    netsh interface ipv4 show joins

Usage of Window command: netsh interface ipv4 and netsh ...The netsh interface ipv4 show joins command is used in Windows to display the IPv4 multicast groups that the local machine is joined to, which is useful for diagnosing network issues, especially those involving multicast traffic. Running this command will list the interfaces and multicast addresses the computer is actively listening to.  

    netsh interface ipv4 show neighbors

The command netsh interface ipv4 show neighbors is used to display the IPv4 neighbor cache, which shows a table of IP addresses and their corresponding Media Access Control (MAC) addresses for devices on the local network.

    netsh interface ipv4 show route

The netsh interface ipv4 show route command is used in Windows to display the IPv4 routing table. This table shows how network traffic is directed, listing entries for destinations, gateways, and the interfaces used for routing. To use it, open Command Prompt and type netsh interface ipv4 show route, then press Enter.  

    netsh interface ipv4 show subinterfaces

With netsh , you can view and modify network settings, automate tasks, and troubleshoot network issues locally or remotely.

    netsh interface ipv4 show tcpconnections

The command netsh interface ipv4 show tcpconnections is not a valid netsh command for displaying active TCP connections. The correct command to view active TCP connections in Windows is netstat.

    netsh interface ipv4 show udpconnections

The command netsh interface ipv4 show udp connections is not a valid netsh command for displaying active UDP connections in Windows.

    netsh interface ipv4 show show udpstats

The netsh interface ipv4 show udpstats command is used in Windows to display User Datagram Protocol (UDP) statistics for the IPv4 interface.

    netsh interface ipv4 show udpstats  

The command netsh interface ipv4 show udpstats is used in Windows to display User Datagram Protocol (UDP) statistics for the IPv4 interface.

    netsh interface ipv4 show winsservers  

The command netsh interface ipv4 show winsservers is not a standard command; there is no built-in winsservers option. To view WINS server settings, you must first enter the netsh interface ip context and then use the show command. For example, you would use netsh interface ip show wins to display the WINS configuration for all interfaces, or netsh interface ip show wins name="Local Area Connection 1" to see the settings for a specific interface. 

    netsh interface ipv4 show excludedportrange protocol=tcp

The netsh interface ipv4 show excludedportrange protocol=tcp command in Windows displays a list of TCP port ranges that are explicitly excluded from use by applications. These exclusions prevent applications from binding to ports within these specified ranges.

    netsh interface ipv4 show excludedportrange protocol=udp

The netsh interface ipv4 show excludedportrange protocol=udp command displays the ranges of UDP ports that are currently excluded on the IPv4 stack of a Windows system. These excluded ports cannot be used by applications or services for listening or binding.

    notepad IPV4.txt

Paste the output here