Understanding Components
========================

To operate Genian NAC, various components are required. This chapter describes the role and installation location of each component.

Policy Server
-------------

The policy server is a central management system that stores all the data and settings of Genian NAC.
The other components receive the configuration for their operation from the policy server, and then transmit the collected information.
Typically, the policy server resides in the organization's data center and is installed on a physical server or virtual machine.

Another role of the policy server is to provide the administrator's management console. You can configure and manage other components
through a web-based management console. You can also view the collected information and establish your organization's security policies.

Network Sensor
--------------

The network sensor is located in each network segment, monitors the network, collects the information, and transmits it to the policy server.

The network sensor is connected to a regular network access port and does not require special settings such as port mirroring.
However, when collecting several VLAN information with one physical sensor, it should be configured as a trunk port through 802.1Q.

Since network sensors must monitor the network's broadcast packets, they can only collect information about devices in the same segment.
For this reason, a separate network sensor must be installed in a WAN-configured network such as a branch office.

The network sensor may be operated on the same system as the policy server or may be constituted by an independent system
and operated as a plurality of network sensors and a policy server.

Wireless Sensor
---------------

The Wireless Sensor monitors the radio signal through the wireless LAN network interface to detect the SSID and wireless devices around the sensor.
This allows monitoring the security associated with the WLAN. Wireless Sensor can add wireless LAN interface to network sensor system to operate
in the same system. However, since the location of the sensor greatly influences the area that can be detected due to the nature of the wireless network,
it may be configured as a separate hardware from the network sensor.

Wireless sensors may not be used depending on whether wireless related functions are used or not.

Network Enforcer
----------------

A Network Enforcer is a component that provides independent network access control for devices that violate an organization's policies.
This makes it possible to isolate devices themselves without the help of existing network infrastructure.

By enabling the Enforcer on the network sensor installed in each network segment, ARP-based Layer 2 Enforcement can be provided, which is the
easiest way to provide network access control with network sensors without additional hardware.

Another Enforcer can be connected to the core switch with a SPAN Port (Mirroring) to terminate the session upon detection of unauthorized network access.
This requires separate independent hardware capable of processing according to the amount of network traffic.

Agent
-----

Agent is software installed in the user's desktop system. It periodically collects operating system, hardware, and software related information and sends
it to the policy server when a change is detected. It also provides desktop configuration management capabilities, making it easy to manage the required
settings for your organization's security policies. This is optional component.

The agent provides its own security functions such as termination prevention and deletion prevention according to the administrator's setting.

.. list-table:: Supported opertating systems
   :widths: 30 30
   :header-rows: 1

   * - Windows
     - macOS
   * - Windows XP (SP2)
     - Apple OS X Mavericks
   * - Windows Vista
     - Apple OS X Yosemite
   * - Windows 7
     - Apple OS X El Capitan
   * - Windows 8
     - Apple macOS Sierra
   * - Windows 8.1
     - Apple macOS High Sierra
   * - Windows 10
     - Apple macOS Mojave
