Sending Notification Using Syslog
=================================

You can send notifications using Syslog information when a specific log is generated.

#. Go to **Log** in the top panel 
#. Go to **Log > Log Filter** in the left **Log** panel
#. Locate and click on **Log Filter** name
#. Find **Syslog**, click **Checkbox**
#. For **Server IP**, type the server IP Address where notifications will be sent
#. For **Protocol**, select desired protocol (*TCP, UDP*)
#. For **Server Port**, type 514 for UDP and 6514 for TCP(TLS)
#. For **SYSLOG Message**, type optional message.
#. For **Character Set**, choose desired option 
#. Click **Update**

.. note:: If a Message box is blank, the followings will be displayed. {_DATETIME} {_LOGTYPE} {_LOGID} {_SENSORNAME} {_IP} {_MAC} {_FULLMSG} {_DETAILMSG})
