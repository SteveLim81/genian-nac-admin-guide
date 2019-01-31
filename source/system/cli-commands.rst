CLI Commands
============

Insights The first connection of the equipment is divided into console mode and shell mode.
In console mode, you can check basic system status and support configuration.
This document identifies and describes how to use commands in Insights console mode.

Basic Commands
--------------

====================== =============================================================================
Command	               Explanation
====================== =============================================================================
enable                  Enables Global Congifuration mode
exit	                 Exits the current mode
help	                 Displays available commands
history	               Displays a list of past commands used
quit	                 Exits console mode
configure terminal	   Global mode to set configurations immediately
configure batch	       Global mode to set configurations after system restarts
clear arp	             Deletes the system arp entry
clear screen	         Initializes the display screen
clock set              Sets system date and time
do backup	             Performs a system backup
do cdbackup	           Performs a system backup to the connected optical disk
do cdrestore	         Restores the backup file from the connected optical disk
do initdisk            Initializes the disk
do restore	           Restores from a backup file
geniup	               If a Genians Update Server is specified, proceed with the upgrade to the latest Server file
halt	                 Prepare the system power shutdown mode
kill pid	             Terminates process based on pid
kill pname	           Terminates process based on the name
ping	                 Generates an ICMP request for IP test to a remote device
reboot	               Reboots the system
restart	system          Restarts the OS
shutdown service	     Terminates the Insights OS service
traceroute	           Displays the routing path for IP
show	                 Proceed to show command section
====================== =============================================================================

Show Commands
-------------

====================== =============================================================================
Command	               Explanation
====================== =============================================================================
show arp	             Displays the IP to MAC address mapping
show backup	           Displays the list of backup files
show configuration	   Displays the current system configuration
Show cpu	             Displays the CPU information
show filesystem        Displays the file system of the appliance
show hosts	           Displays a list of hosts
show interface	       Displays the network interfaces of the appliance
show logging	         Displays a list of system logging messages
show memory	           Displays the memory statistics
show processes	       Displays the current running processes
show route	           Displays the current configured routes
show superadmin	       Displays a list of configured administrator accounts
show time	             Displays the current system time
show uptime	           Displays how long system has been up and running
show version	         Displays the current running system version
====================== =============================================================================
