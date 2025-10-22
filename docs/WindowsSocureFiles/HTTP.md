# HHTP 

This script gathers HTTP information such as chache parameters, chache state, service state etc

### SYNOPSIS

- Export HTTP.sys and HTTP service configuration to text files.

### DESCRIPTION

- Queries HTTP.sys and the HTTP service to gather configuration and runtime information, then writes each category of data to separate text files.

- Collected information includes cache parameters, cache state, listened IP
addresses, service state, HTTP.sys settings, SSL certificate bindings, timeout settings, and URL ACLs. Useful for troubleshooting, auditing, or backing up HTTP-related configuration.

### PARAMETER

- The directory path where exported text files will be saved. If not provided, the current working directory is used. The script will create the directory if it does not exist.

### EXAMPLE

    http.bat "C:\Diagnostics\HttpConfig"
    
Export all HTTP.sys configuration and state files into C:\Diagnostics\HttpConfig.

### WHY IT IS UDED

- Administrative privileges are typically required to query HTTP.sys and service configuration.

- Run this script in a controlled environment; exported files may contain sensitive network and certificate information.

- Intended for administrators and support personnel performing diagnostics or configuration audits.

#### Code Overview

    @echo off
    mkdir HTTP
    cd HTTP

Creates a new folder

    netsh http show cacheparam > http_cacheparam.txt

The netsh http show cacheparam command displays the cache parameters of the HTTP Service, measured in bytes. This command provides insight into how the HTTP.SYS driver, which handles HTTP requests for applications like IIS, is configured regarding its caching behavior.

    netsh http show cachestate > http_cachestate.txt

The command netsh http show cachestate is used to display information about the HTTP response cache in Windows. This cache is managed by the HTTP.sys kernel-mode driver and stores responses for faster delivery to clients.

    netsh http show iplisten > http_iplisten.txt

The command netsh http show iplisten is used in Windows to display the IP addresses in the HTTP service's IP listen list. This list defines the specific IP addresses on which the HTTP service (which handles HTTP traffic for applications like IIS) will bind and listen for incoming connections.

    netsh http show servicestate > http_servicestate.txt 

The netsh http show servicestate command in Windows provides a snapshot of the HTTP service, specifically detailing the registered URL namespaces and associated server sessions and request queues managed by HTTP.SYS. This command is useful for understanding which applications or services are listening on specific HTTP/HTTPS ports and URLs.

    netsh http show setting > http_setting.txt

The netsh http show setting command is not a complete command within the netsh http context. To view specific HTTP settings, you need to specify which setting you want to display. The netsh http context provides several show sub-commands to display different aspects of the HTTP service configuration.

    netsh http show sslcert > http_sslcert.txt

The command netsh http show sslcert is used in Windows to display the SSL certificate bindings configured for the HTTP Service. This command provides a list of all SSL server certificate bindings and their corresponding client certificate policies for specific IP addresses and ports.

    netsh http show timeout > http_timeout.txt

The netsh http show timeout command is used in Windows to display the current timeout values configured for the HTTP Server API (HTTP.sys). This API is responsible for handling HTTP requests and responses at a low level in the operating system.

    netsh http show urlacl  >  http_urlacl.txt

The netsh http show urlacl command displays the Discretionary Access Control Lists (DACLs) for reserved URLs on a Windows system. These URL reservations are managed by the HTTP Server API (HTTP.sys), which allows non-administrator users or services to register and listen on specific URLs.