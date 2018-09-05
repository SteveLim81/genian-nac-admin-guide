Configuring DHCP Services
=========================

The Dynamic Host Configuration Protocol (DHCP) is a standardized network protocol used on IP networks. The DHCP is controlled by the Policy Server/Sensor that dynamically distributes network configuration parameters, such as IP addresses. You will be able to configure and manage the Built-In DHCP Options and configure Policy Server/Sensor to utilize the three DHCP Services (Local, Remote, and Global)

System Defaults Network Sensor settings are used for default configurations to be applied to any new Network Sensors being established onto the network. This is to allow you to create default settings to be applied to each additional Network Sensor so you do not have to configure each one manually.
If you need to make custom configuration changes to a Network Sensor that is already in operation then you would use the System > Sensor > Sensor Settings option.

Depending on your requirements you have three options for DHCP. (**Local**, **Global**, and **Remote**)

To Configure Default DHCP Services
----------------------------------

#. Go to **System** in the top panel
vGo to **System Defaults > Network Sensor** in the left System Management panel
#. Find **DHCP** section in Network Sensor window. **Enable DHCP Service**
#. Based off of your network environment, choose one of the **Network Scopes** below
#. Find **Node IP Pool** section and **reserve** an **IP range** of IP Addresses
#. Find **Lease Duration** and define when an **IP expires** (*Minutes, Hours, Days, or Months*)
#. All **other settings** are **optional**
#. Click **Update**

To Configure DHCP Services To Network Sensor In Operation
---------------------------------------------------------

#. Go to **System** in the top panel
#. Go to **System > Sensor** in the left System Management panel
#. Find and click **IP/Name** of **Network Sensor**
#. Find and click **Settings** tab
#. Click **Sensor Settings**
#. Find **DHCP** section and **enable DHCP Service**
#. Based off of your network environment, choose one of the **Network Scopes** below
#. Find **Node IP Pool** section and **reserve** an **IP range** of IP Addresses
#. Find **Lease Duration** and define when an **IP expires** (*Minutes, Hours, Days, or Months*)
#. All **other settings** are **optional**
#. Click **Update**

.. image:: /images/Genian-NAC-DHCP-Options-1.png
   :width: 900 px

Managing DHCP Leases
--------------------

It is a function to inquire and delete the DHCP IP assigned to the device by the DHCP server.
This feature is only available through the CLI(Command Line Interface). 

**Show DHCP Lease status**

.. code:: bash

   genian# show dhcp lease all
   IP Address      MAC               Expire              Interface  
   --------------- ----------------- ------------------- -----------
   172.29.30.152   00:24:21:3D:65:C4 2018-08-06 20:10:13 eth0
   172.29.30.154   00:90:FB:26:7D:24 2018-08-06 19:10:24 eth0
   172.29.30.155   AC:3C:0B:3C:01:70 2018-08-06 20:10:21 eth0

**Clear DHCP Lease status**

.. code:: bash

   geinian# clear dhcp lease ip 172.29.30.152
   genian# show dhcp lease all
   IP Address      MAC               Expire              Interface  
   --------------- ----------------- ------------------- -----------
   172.29.30.154   00:90:FB:26:7D:24 2018-08-06 19:10:24 eth0
   172.29.30.155   AC:3C:0B:3C:01:70 2018-08-06 20:10:21 eth0
