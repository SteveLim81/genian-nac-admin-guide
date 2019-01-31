Detecting Node Platform
=======================

Genian NAC will detect connected device platforms using various information collected by the **Network Sensor**.  When a device connects to the network, packets are sent out and the device responds with one or more protocols. Genian NAC uses the following protocols to detect devices platform information

   - HTTP / HTTPS header and body
   - Web Browser User-Agent
   - TELNET / SSH / SMTP banners
   - MAC Address
   - Hostname
   - Open Port
   - DHCP Request
   - SNMP OID / Description
   - UPNP
   - and more

Genian NAC is using our own, highly advanced platform database (GPDB) for detecting device platforms. GPDB has various patterns for matching against device information to ensure that platforms are accurately detected. To provide paramount accuracy, the GPDB is updated weekly so that the newest devices on the market can be quickly identified within the network. (*Weekly GPDB updates are for the Paid Edition Only. The Free Edition’s GPDB is updated monthly*)

Node Types
----------

Each Platform has a Node Type, such as:

   - Policy Server
   - Network Sensor
   - Switch Port
   - Sensor Alias
   - Virtual IP
   - Wireless Sensor
   - Undefined
   - PC
   - Mobile Device
   - Server
   - Network Appliance
   - Wireless Device
   - Router
   - Switch
   - Security Device
   - Printer
   - VOIP
   - Other

Define a Node Platform Manually
-------------------------------

#. Go to **Management > Node** in the top panel
#. Select the desired node’s **IP Address**

Under **General** tab

#. For **Platform**, click **Checkbox** to **Manually define**
#. Manually enter **Platform Name**
#. Click **Update**

.. note:: In Node View you will now see a Icon next to name in the Platform Column. This Icon will indicate this has been manually defined.

Create a User-defined Node Type
-------------------------------

#. Go to **Preferences** in the top panel
#. Go to **Properties > Node Type** in the left Preferences panel
#. Click **Tasks > Create**
#. Enter a **Name** and select an **Icon** (*Click **Add** to upload your own icon*)
#. Click **Save**

.. note:: A User-defined Node Type must be defined manually and added to the node.

#. Go to **Management > Node** in the top panel
#. Click on desired node **IP Address**

Under **General** tab

#. For **Node Type**, click **Checkbox** to **Manually define**
#. Select **Node Type**
#. Click Update

Report Wrong Platform Information
---------------------------------

If for some reason Genian NAC cannot detect the Platform of a device, one of the following could be the underlying reason:

   - **Not enough information**: A device is not sending packets or is not responding to any request. This is possible if the OS has a Firewall active
   - **No matching pattern in GPDB**: Node information has some evidence of a specific Platform, but the GPDB does not have that matching pattern yet

In case there is no matching pattern in our GPDB, you can send that Nodes information to the Genian Cloud using the Report Wrong Platform dialog. Once Genians has received the report, our engineers will investigate the Platform pattern and update it to the GPDB. 

Disable Reporting Unknown Platform
----------------------------------

By default, Genian NAC sends a Report Wrong Platform for unknown Platform Nodes every day. All sent information is readable from outside of the device. To deactivate sending a Report Wrong Platform  to the Genian Cloud, follow these steps:

#. Go to **Preferences** in the top panel
#. Go to **General > Node** in the left Preferences panel

Under **Detection**

#. For **Reporting Unknown Platform**, select **Off**
#. Click **Update**
