Browsing Switches
=================

To identify a **Switch**, Genian NAC sends out an **SNMP request**. If the response to the request comes back with an OID (dot1dBaseBridgeAddress(1.3.6.1.2.1.17.1.1)), then Genian NAC labels that **MAC Address** as a **Switch**. If switches are not identified with the public community string you will need to check the community string configuration or run a SNMPWALK to verify switch is responding properly.

Set Node Scan Interval On Network Sensor
----------------------------------------

#. Go to **System** in the top panel
#. Go to **System > Sensor** in the left System Management window
#. Click **Network Sensor IP**

Under **Settings** tab:

#. Click **Sensor Settings**

Under **Node Scan**:

#. For **Update Interval**, edit time interval (*1 minute - 1 year*)
#. Click **Update**

Set SNMP Settings For SNMP Scan
-------------------------------

#. Go to **Preferences** in the top panel
#. Go to **General > Node** in the left Preferences window

Under **SNMP**:

#. For **SNMP Community** enter read/write community string(*e.g. public,private*)
#. For **Collecting Network Information**, needs to remain **On** (*If set to Off SNMP information will not be collected*)
#. For **Update Interval**, edit time interval (*5 minutes – 1 year*)
#. For **Time Object**, specify time object
#. Click **Run Now** button for SNMP to scan instantly

Use SNMPWALK on Windows machine To Verify Switch Response
---------------------------------------------------------

.. note:: If a Switch fails to populate in Switch List, first check Switch Community strings on switch, then run a SNMPWALK.

#. Login to your **Switch** and verify it’s SNMP Community strings
#. Verify **Genian NAC** has correct **SNMP Community strings** set
#. Using Windows machine and Net-SNMP do the following:

   - Download **Net-SNMP** for Windows (*Set the default folder location to C:\Net-SNMP to easily locate it*)
   - Open **Command Prompt** and change directories. Type **cd /Net-SNMP/bin**
   - Run the snmpwalk using this command: **snmpwalk -Os -c public -v 2c “Switch-IP” .1.3.6.1.2.1.17.1.1** (*e.g. snmpwalk-Os -c public -v 2c 192.168.50.5 .1.3.6.1.2.1.17.1.1*)
   - Should display **mib-2.17.1.1.0 = Hex-STRING: XX XX XX XX XX XX** (*This determines that the switch is responding properly to SNMP Requests*)

Configure Read/Write Community
------------------------------

#. Go to **Management > Switch** in the top panel
#. Find and click **Switches** folder in the left Switch Management window 
#. Find and click desired **Switch** name in the main Switches window
#. Enter the **SNMP Community** strings in the **Read/Write Community** fields
#. Click **Update**
