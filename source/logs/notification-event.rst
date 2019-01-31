Define Event Criteria for Notification
======================================

Use an existing Log Filter or Create a new one
----------------------------------------------
#. Select the **edit** option under the desired log filter. 
#. Log export may be configured further by checking **`Notification`_**(Local Admin), **`SYSLOG`_**, **`SNMP Trap`_**, and/or **`Webhook`_**.

Add Macros To Log Export Message Box
------------------------------------

Genian NAC uses Macros as a placeholder text that gets replaced with specific data when inserted into the 
Log Notifications message box. You can add and customize these Macros to present the data however you like. 
If the Log Notifications message block is left empty then a default set of Macros will be used.

#. Go to **Preferences** in the top panel
#. Go to **General > Log** in the left **Preferences** panel
#. Find **Log Options: Remarks column Elements** section in main **Log** panel
#. Select options to **Enable** this data to be added to **Logs** (*Node Status Logs and Agent Status Logs are optional*)
#. Go to **Log** in the top panel
#. Go to **Log Filter** in the left **Log** panel
#. Find and click **Log Filter Name**
#. Click Edit at the bottom of **Status & Filters** section
#. Find **Notification: Long Message** section
#. Add additional **MACROs** in the **Long Message** block
#. Find and click **Help for Macro** button just above **Notification** section title
#. Choose the desired **MACRO** to add to the message body of the notification (*Some Message{_SWNAME}{SWPORT}*)
#. Click **Update**

(*If Message box is blank then a default of {_DATETIME}{_LOGTYPE}{_LOGID}{_SENSORNAME}{_IP}{_MAC}{_FULLMSG}{_DETAILMSG} 
will be displayed and you can add in additional Macros and customize as desired*)