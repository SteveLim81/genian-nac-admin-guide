Detecting Internal SSID
=======================

SSIDs are differentiated in the list from **Internal** to **Neighboring APs**.

Show Internal SSIDs
-------------------

#. Go to **Management > WLAN** in the top panel.
#. Find and click column labeled **Internal** in the main WLANs window. All internal APs will be identified with a checkmark in this column.

How to find the internal AP
---------------------------

The AP detected by the Genian NAC Agent and the wireless sensor can be distinguished by an internally connected AP by several criteria.
Internal AP detection method is as follows.

**MAC Similarity Check**

.. image:: /images/similarity.jpg
   :width: 600px

#. The network sensor collects the wired interface MAC information of the internally connected AP.
#. The wireless sensor collects the AP's wireless interface MAC information and sends it to the policy server.
#. Policy server compares the AP's wired and wireless interface MAC information and determines that the AP is connected to the internal network if the similarity is confirmed.

**Packet broadcasting**

.. image:: /images/packet.jpg
   :width: 600px

#. The network sensor broadcasts a virtual MAC to the network.
#. At this time, AP connected to the internal network broadcasts the virtual MAC received from the network sensor to the AP's wireless band.
#. The wireless sensor is monitoring the wireless network and when the wireless sensor receives the virtual MAC from the AP, it judges the AP as the internal AP.

**Agent**

#. Agent collect all network interface information on user device.
#. Matching SSID MAC address with known network interface MAC address.

**SNMP with wireless controller**

#. Collect information from wireless controller using SNMP.
#. Matching SSID MAC address with known MAC address from wireless controller.