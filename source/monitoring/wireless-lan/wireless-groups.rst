Creating Wireless Groups
========================

A **Wireless Group** is any detected amount of **SSIDs** that are grouped together due to conditions or properties that have been set to an identifier. This is to help Network Administrators quickly navigate to specific **SSIDs** or **Categories** when dealing with a large quantity of SSIDs.

Create a WLAN Group
-------------------

You can create WLAN Groups to better categorize your SSIDs.

#. Go to **Policy** in the top panel
#. Go to **Group > WLAN** in the left Policy panel
#. Click **Tasks > Create**

Under **General**:

#. For **ID**, enter unique name
#. For **Description**, type what this group consists of
#. For **Status**, select **Enabled** from drop-down
#. For **Generating Logs** turn **On** to show logs when SSIDs are added to the group

Under **Condition**:

#. For **Boolean Operator**, choose **AND** to match all conditions, or **OR** to match any conditions
#. For **Settings** click **Add** to add conditions

Under **Settings**:

These are conditional settings that allow you to be specific in identifying SSIDs:

#. For **Options**, you can select MAC, Protocol, SSID, Security Settings, Tag, and more
#. For **Operator**, allows you to choose equal to, not equal to, contains, does not contain, and more
#. For **Value**, type in some value to match what your searching for
#. For **Description**, type what this condition does
#. Click **Add**
#. Click **Save**

Assign a WLAN Tag
-----------------

You can Tag SSIDs to help categorize them and to build Policies using these Tags:

#. Go to **Management > WLAN** in the top panel
#. Find and click **Checkbox** of desired **SSIDs**
#. Click **Tasks > Assign WLAN Tag**

Under **Assign WLAN Tag**

#. In drop-down select **Assign Selected Tags**
#. Click **Checkbox** of tag to apply
#. Click **Save**
#. Click **Apply**

Assign a WLAN Group
-------------------

You can group SSIDs that are similar to each other based off of Tags, SSID Name, Vendor, Security Settings, Protocol, and more.

#. Go to **Management > WLAN** in the top panel
#. Find and click **Checkbox** of desired **SSIDs**
#. Click **Tasks > Assign WLAN Group**

Under **Assign WLAN Group**

#. For **Action**, select **Add** or **Remove**
#. For **WLAN ID**, select **SSID, MAC,** or **MAC+SSID**
#. For **WLAN Group**, group to associate to
#. Click **Save**
#. Click **Apply**

Group by Network Sensor
-----------------------

If you have many Network Sensors, it is difficult to manage all of these in one list. Here you have the ability to create groups and assign **Network Sensors** to them.

#. Go to **Management > WLAN** in the top panel
#. Click **Edit Tree icon** in the top right corner
#. Right click on either **WLAN AP** or **WLAN Client**, click **Create** (*New node group will appear for you to rename*)
#. Right click on newly created group and click **Assign**
#. Search for **Network Sensor** and select each **Checkbox** you want to add to this group
#. Click **OK**

.. note:: If you have a presence around the world you can create **Country Groups** and add **Network Sensors** that are located wsithin those countries.
