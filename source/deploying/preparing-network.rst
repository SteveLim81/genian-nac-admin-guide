Preparing Network
=================

When planning your Genian NAC Deployment onto your network there are several considerations. 

- Where should the equipment be placed? 
- How will it connect to my switches?
- How many pieces of equipment do I need?
- What ports do I need to open for Genians to communicate?

Wired Connectivity
------------------

The Policy Server should be directly connected to your Core Switch port as an access port. 
The Network Sensor should be connected to an Edge Switch port that can be an access port, or trunk port.

**Switches**

Network Sensors must be able to see bradcast packets, so they must be connected to all managed subnets.
Connecting to the switch's access port requires as many network sensor ports as the number of subnets,
so it is generally recommended to connect to the trunk port via 802.1Q. each Network Sensor can handle up to 128 VLANs. 

**SNMP**

Genians supports SNMP Version 1 and Version 2c. The read-only community string is used to check whether the node supports SNMP 
in the process of collecting information about the Node by the network sensor. If the node responds to an SNMP request, 
the sensor verifies that the node is a switch by verifying that it supports the BRIDGE-MIB through an SNMP query.
The read-write community string is used to make changes to the switches for port descriptions and shutting down switch ports.
In addition, it can be used for various additional functions such as collecting information of wireless controller using SNMP,
detecting platform information of device.

**WAN**

If you have more then one location behind WAN Technologies then a Network Sensor would be required at each of these locations.

Wireless Connectivity
---------------------

Network Sensor with Wireless NIC is used to detect wireless packets and identify SSIDs that are both Internal to your network
and External (Neighboring) to your network. Placement of the Network Sensor with Wireless NIC is critical as you do not want
to place this in a Data closet where you will only detect Wireless SSIDs near the data closet. You will want to place
the Network Sensor with Wireless NIC centrally to where you can detect the majority of the SSIDs around it.

Allowed Ports
-------------

+-------------------+-------------------------------+-------------------------+------------------+
| SRC IP            | DST IP                        | Service                 | Note             |
+===================+===============================+=========================+==================+
|                   | 52.78.17.154                  |                         |                  |
| Policy Server IP  | (geniupdate.geninetworks.com) | TCP/80, 443             | GENIAN Data SYNC |
+-------------------+-------------------------------+-------------------------+------------------+
|                   |                               | UDP/3870, 3871          | Keep Alive       |
| Network Sensor IP | Policy Server IP              | TCP/80, 443             | Update Policy    |
|                   |                               | UDP/514, TCP/6514       | SYSLOG           |
+-------------------+-------------------------------+-------------------------+------------------+
| PC IP(Agent)      | Policy Server IP              | UDP/3870, 3871          |                  |
|                   |                               | TCP/80, 443, 8000, 3910 |                  |
+-------------------+-------------------------------+-------------------------+------------------+
| Management PC     | Policy Server, Network Sensor | TCP/22                  |                  |
+-------------------+-------------------------------+-------------------------+------------------+

.. note:: The above ports need to be open and accessible to allow the Policy Server to get weekly/monthly updates from the Genians Platform DB

.. _Trunked Switch Port: http://www.ciscopress.com/articles/article.asp?p=2181837&seqNum=7

