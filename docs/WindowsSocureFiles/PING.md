# Ping

Pings various network interfaces and saves the results to text files.This helps the user to find interface primitive but eefctive 

### .SYNOPSIS

- Pings various network interfaces and saves the results to text files.

### DESCRIPTION

- This script pings various IP addresses associated with different network interfaces
and saves the results to corresponding text files. This can be useful for diagnosing network connectivity issues or verifying the status of network interfaces.

### WHY IT IS USED

- This script pings various IP addresses associated with different network interfaces
and saves the results to corresponding text files.

#### Code Overview

    @echo off
    mkdir Network_ping
    cd Network_ping

Creates a folder

    ping 162.168.43.1  > IP_ping.txt

Pings the IP address 

    ping 127.0.0.0 > Loopback_Pseudo-Interface1_8_ping.txt

Pings Loopback-Pseudo-Interface1 8

    ping 127.0.0.1 >  Loopback_Pseudo-Interface1_32_ping.txt

Pings Loopback-Pseudo-Interface1 32 

    ping  27.255.255.255  >  Loopback_Pseudo-Interface1_32/255_ping.txt

Pings Loopback-Pseudo-Interface1 32/255

    ping 169.254.49.97 >  Npca_Loopback_Adapter_ping_16.txt

pings Npca_Loopback_Adapter_ping_16

    ping 169.254.49.97 >  Npca_Loopback_Adapter_32_ping.txt

pings Npca_Loopback_Adapter_ping_32

    ping 169.254.255.255 >  Npca_Loopback_Adapter_32/255_ping.txt

pings Npca_Loopback_Adapter_32/255

    ping 162.168.43.0 >  WIFI_24.txt

pings you public ip address

    ping 162.168.43.32  >  WIFI_32_ping.txt

pings your Wifi IP address

    ping 162.168.43.255  > WIFI_32/255_ping.txt

This pings the subnet of the network

    ping 162.168.137.0 > Local_Area_Connection_12_24.txt

pings Your Local Area Network IP Addresss

    ping 162.168.137.0 > Local_Area_Connection_12_32.txt

pings Your Local Area Network IP Addresss (32 bit)

    ping 162.168.137.255 > Local_Area_Connection_12_225/32.txt

pings Your Local Area Network subnet IP Addresss

    ping 224.0.0.0 >  Loopback_Pseudo-Interface1_8_ping.txt

pings the Loopback Pseudo Interface1 8

    ping 224.0.0.0 > Npca_Loopback_Adapter_ping/4.txt ping 224.0.0.0 > Ethernet/4.txt

pings Npca_Loopback_Adapter

    ping 224.0.0.0  WiFi/4.txt

pings the router ig

    ping 224.0.0.0 Local_Area_Connection_9/4.txt

pings the Local Area Connection 9/4

    ping 224.0.0.0  Local_Area_Connection_12/4.txt

pings the Local Area Connection 12/4

    ping 256  255.255.255.255 >  Npca_Loopback_Adapter_ping/255-32.txt

pings the Npca_Loopback_Adapter

    ping 256  255.255.255.255 > Ethernet/255-32.txt

pings the Ethernet/255-32

    ping 256  255.255.255.255  WiFi/255-32.txt

pings the WiFi/255-32

    ping 256  255.255.255.255 Local_Area_Connection_9/255-32.txt

pings the Local_Area_Connection_9/255-32

    ping 256  255.255.255.255  Local_Area_Connection_12/255-32.txt

pings the Local_Area_Connection_12/255-32