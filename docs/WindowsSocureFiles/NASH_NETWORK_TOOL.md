# NASH_NETWORK_TOOL

This tools helps the suers to gather network information of the traget device

### SYNOPSIS

- This batch file creates a new project folder structure for the NASH NETWORK TOOL (NNT)
and copies the necessary script files into the newly created folders.

### DESCRIPTION

- The script prompts the user to enter a folder name, creates the main project folder,
and subfolders for different network tools. It then copies the relevant script files
from the Scripts directory into the new project folder and starts the main scripts.

### WHY IT IS USED

- This script automates the setup process for a new NNT project, ensuring that all necessary files and folders are created and organized correctly.

#### Code Overview

    @echo off
    set/p folder=folder_Name: 
    mkdir %folder%
    cd  %folder%

Makes the folder using the input provieded by the user

    mkdir Firewall 
    mkdir IPV4
    mkdir Target_info
    mkdir Tcp 
    mkdir HTTP
    mkdir Network_ping

Craetes the nesscary folders such as Firewall, IPV4, Target Info, TCP, HTTP, Newtrok Ping

    copy "..\Scripts\Firewall.bat" "..\%folder%
    copy "..\Scripts\IPV4.bat" "..\%folder%
    copy "..\Scripts\TCP.bat" "..\%folder%
    copy "..\Scripts\http.bat" "..\%folder%
    copy "..\Scripts\Target_Info.bat" "..\%folder%
    copy "..\Scripts\Ping_Network_interfaac.bat" "..\%folder%
    copy "..\Scripts\READ.ME.txt" "..\%foler%

Then it copies the scripts of in the scripts folder to the their repective folders. This helps me modularize my code for code readablity

    cd  %folder%
    start Firewall.bat
    start IPV4.bat 
    start TCP.bat 
    start Target_Info.bat
    start http.bat

Goes into the folder and then start the scripts

Now lets look at the individual scripts

- [Firewall](Firewall.md)
- [HTTP](HTTP.md)
- [IPV4](IPV4.md)
- [PING](PING.md)
- [Traget_info](Traget_info.md)
- [TCP/IP](TCP.md)