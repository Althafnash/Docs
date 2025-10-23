# Traget Information

This scripts gather information about the system it is runned on

### SYNOPSIS

- Gathers target information and saves it to a specified folder.

### DESCRIPTION

- This script prompts the user for a device name, creates a folder with that name,
and collects various system and network information, saving it into text files
within the created folder.

### NOTES

- This script is intended for use in a controlled environment and should be
executed with appropriate permissions.

#### Code Overview

    @echo off
    cd Target_Info
    set /p folder=name of Device :
    mkdir %folder%
    cd %folder%

Craetes a folder with teh Traget Machines name

    tasklist > tsk.txt

This commands showa the current tasks that the machine was running

    systeminfo > systeminfo.txt

This shows the system information of the Traget PC

    wmic product get name  > app.txt

This shows the target PC apps

    netsh wlan show pro > Lan_Networks.txt

This shows the LAN netwirks of the Traget PC

    ipconfig /all > Machine_Network.txt

This shows the Internet protocol configuartion of the Traget Machine