# Firewall

Thsi export the firwalls configurations and the cuurent profile of the windows firwall of the windows ssytem

### SYNOPSIS

- Gathers target information and saves it to a specified folder

### DESCRIPTION

- This script prompts the user for a device name, creates a folder with that name,
and collects various system and network information, saving it into text files
within the created folder.

### WHY IT IS USED

- This script is intended for use in a controlled environment and should be
executed with appropriate permissions.

#### Code Overview

    @echo off 
    cd Firewall 
    netsh advfirewall monitor  show firewall > Firewall.txt

 Export firewall configuration to text files. Shows what configs we can change in Windows Defender.

 The command netsh advfirewall firewall show rule name=all shows all firewall rules, while netsh advfirewall show allprofiles shows the status of each firewall profile (domain, public, and private).

    netsh advfirewall monitor show currentprofile > currentprofile.txt 

 Export current profile settings to text file
 
 This command displays various settings related to the active firewall profile, such as its state (on/off), inbound and outbound policies, and other configurations.
