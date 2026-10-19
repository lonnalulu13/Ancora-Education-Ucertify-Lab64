# Ancora-Education-Ucertify-Lab64
# Scanning the Network

> **Original Lab Source**
> 
> This lab was available through:
>
> [https://ancoraeducation.ucertify.com/app/?func=navigate_items&item_sequence=17]

## Objective of the Lab
In this lab, you will learn to scan the network. Command used tcpdump: Network scanning is a procedure for identifying active devices on a network by employing a feature or features in the network protocol to signal devices and awaits a response. tcpdump allows you to specify network packets that are either using some port X as source or destination.
## Instructions 
## Caution
* While capturing packets, wait for 5-10 minutes until all the required packets are captured.
### STEP 1 
From the left sidebar, open the Terminal window. 
### STEP 2
Execute the following command to scan for all systems in the 192.168.10.0 Class C network:
```bash
nmap -sP 192.168.122.7/24
```
### STEP 3
Execute the following command to capture 10 packets:
```bash
tcpdump -c 10
```
### STEP 4
Execute the following command to capture 10 packets with full verbose data output:
```bash
tcpdump -c 10 -vv
```
### STEP 5 
Execute the following command to determine the name of your primary network interface:
```bash
ifconfig
```
### STEP 6
Execute the following command to capture 10 packets specifically on the primary interface network:
```bash
tcpdump -c 10 -i virbr0
```
### STEP 7 
Execute the following command to capture 10 packets for any SSH connection on the primary interface network:
```bash
tcpdump -c 10 -i virbr0 port 80
```
### STEP 8 
From the left sidebar, right-click Terminal, and then click New Window to open another Terminal window and enter the following curl command to access the url, you will see the output in the previous Terminal window:
```bash
curl http://192.168.122.7/ssh.php
```
### STEP 9 
Execute the following command to capture 500 packets and save the output to the file named /tmp/tcpdump.data:
```bash
tcpdump -c 500 -w /tmp/tcpdump.data
```
### CAUTION
* After execution of the above command, wait for 3 minutes and then press CTRL+C to stop the capture
### STEP 10
Execute the following command to view the contents of the /tmp/tcpdump.data file:
```bash
tcpdump -r /tmp/tcpdump.data
```
## Disclaimer

This repository is for **educational and personal learning purposes only**.  

The original lab content belongs to **uCertify / Ancora Education** and remains their copyrighted material.  
This repository is not affiliated with, endorsed by, or sponsored by uCertify or Ancora Education.  

No copyright infringement is intended.  
Use of any tools or techniques mentioned here should only be performed in authorized, legal environments.
