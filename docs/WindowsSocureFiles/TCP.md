# TCP/IP 

This shows the Transmission communication  protocol and internet protocol configuration in detail of the Target Machine

### SYNOPSIS
  
- Export TCP configuration and security 
settings to text files.

### DESCRIPTION
   
- Queries TCP settings and security configurations, then writes the information
to separate text files. Collected information includes TCP security settings, heuristics, supplemental ports, and supplemental subnets. 

- This information is useful for troubleshooting, auditing, or backing up TCP-related configuration.

### WHY IT IS USED

- Administrative privileges are typically required to query TCP settings.

- Run this script in a controlled environment; exported files may contain
sensitive network information.

- Intended for administrators and support personnel performing diagnostics
or configuration audits.

#### Code Overview

    @echo off
    mkdir Tcp
    cd Tcp

Creates  a folder name TCP 

    netsh interface tcp show security > TCP_Security.txt

The netsh interface ipv4 show excludedportrange protocol=udp command displays the ranges of UDP ports that are currently excluded on the IPv4 stack of a Windows system. These excluded ports cannot be used by applications or services for listening or binding.

    netsh interface tcp show heuristics

The netsh interface tcp show heuristics command displays the current settings for TCP Window Scaling heuristics, which are algorithms Windows uses to dynamically adjust the TCP receive window size for optimal network performance. This command shows if heuristics are enabled or disabled and how they are configured for different network profiles (e.g., public, private, domain). Heuristics can restrict performance on certain network profiles, and for some users, disabling them may be necessary to achieve faster speeds, though this should be done with caution, as it can impact compatibilit

    netsh interface tcp show supplemental

The command netsh interface tcp show supplemental displays the current supplemental TCP settings for your system, which are used to customize TCP behavior for different network conditions. 

    netsh int tcp show supplementalports

The command netsh int tcp show supplemental is used in Windows to display the current TCP settings associated with the "supplemental" templates. These templates (like compat, internet, or datacenter) allow for advanced configuration of TCP parameters to optimize performance for different network environments.

    netsh int tcp show supplementalsubnets

The netsh int tcp show supplemental command displays the current TCP settings for the supplemental templates in Windows. These templates, such as internet, datacenter, or custom, provide predefined sets of TCP parameters optimized for different network conditions.

    echo   copy the output 
    notepad Tcp_.txt
    ping localhost -n 10 >null

Now copy the output to the notepad and save it
