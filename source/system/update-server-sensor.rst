Updating Policy Server and Network Sensor
=========================================

You can update the Policy Server and Sensor through the UI.

Update the Policy Server and Sensor
-----------------------------------

#. Go to **System** in the top panel
#. Go to **Update > Genian Software** in the left System Management panel
#. Find **Available Version** software in Genian Software window. Click **Download**
#. Install  **Genian Software**

Update the Policy Server and Sensor Manually
--------------------------------------------

This is done by obtaining Genian NAC Software from Genians and store locally on your machine to then upload onto the servers.

Prepare System Files for upload:

#. Extract contents from the .iso file. 
#. Select desired software version from the /images directory in the .iso. 
    * For **Policy Server**, select file beginning with **NAC-CT** (*Includes network sensor files*)
    * For **Network Sensor**, select file beginning with **NAC-SS**
#. Go to **System** in the top panel
#. Find **Update** section in the left System Management panel. Go to **Genian Software**
#. Find and click **Upload File** button in Genian Software window
#. Click **Select File** in Upload window
#. Locate **Genian Software** in **File Upload** window. Double click on desired file
#. Click **Upload**
#. Go to **System** in the top panel
#. Go to **System > System** in the left System Management panel
#. Find **Policy Server/Sensor** in System window. Click **Checkbox**
#. Click **Tasks**
#. Click **Update Specific System Image** (*If you selected Policy Server and ALL sensors in Step 9, Click Update All System Images*)

(*System will update and reboot*)

Update Through Command Line Interface 
--------------------------------------

Use command: **geniup**

For more info see: See: :doc:`/system/cli`

