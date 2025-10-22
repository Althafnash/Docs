# PC_SECURITY

This contains scripts to which shows traget machines

### SYNOPSIS

- This script creates a folder with the user-defined name and runs disk checking commands, saving their outputs into text files within that folder.

### DESCRIPTION

- The script prompts the user for a folder name, creates the folder, and executes 'chkntfs' and 'chkdsk' commands,saving their outputs to 'chkntfs_scan.txt' and 'disk_scan.txt' respectively inside the created folder.

### WHY IT IS USED

- This script is useful for system administrators and support personnel who need to perform disk checksand save the results for later analysis or troubleshooting

#### Code OverView

    @echo off
    color c

This is starting of the script where it says so it dose not start a new command prompt window 

Next we set the color to c

    set/p folder=folder_Name: 
    mkdir %folder%
    cd  %folder%

This then ask for a folder name and then it makes that folder with the name and then changes the derictory to that said folder

    chkntfs > chkntfs_scan.txt
    chkdsk > disk_scan.txt

The first command scans the file systems for any erros or currpution of files or folders

The next command scans the disk for any faultiy or currpted files or folders 
