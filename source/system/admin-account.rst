Administrator Accounts
======================

You can manage your Administrators by adding, deleting, and adding various restrictions

To Add Administrator
--------------------

#. Go to **Management > User** in the top panel
#. Click **Tasks > Add User**

Under **General**

#. For **Username**, type a username
#. For **Name**, type in full name
#. For **Administrator Role**, select a optional Role for Administrator
#. For **Description**, type optional description
#. For **Purpose**, select **User Account**
#. For **Status**, select **Enabled** (*You can choose **Disable** to disable the account temporarily)
#. For **Expiry**, click **Checkbox** and choose date and time by clicking in empty space
#. For **Tag**, you can choose to add a Tag to this account by clicking **Add** `Create Tag`_ 

Under **Password**

#. For **Password**, type password
#. For **Password Confirmation**, re-type password

Under **User Information**

#. For **Company**, type Company Name
#. For **Department**, select optional department (*To create Department go to Users > Departments > Tasks > Create*)
#. For **Email**, type in Email address
#. For **Mobile Phone**, type in phone number using format of your choice (*e.g. 123-456-7890, or 1234567890*)
#. For **Job Title**, select optional Job Title (*To create Job Title go to Users > Job Titles > Tasks > Create*)
#. For **Telephone**, type in phone number using format of your choice (*e.g. 123-456-7890, or 1234567890*)
#. Click **Save**

Set up Authentication Restrictions
----------------------------------

#. Go to **Management > User** in the top panel
#. Find and click **Username**

Under **Authentication Restrictions**

#. For **Number of Auth IPs**, specify the number of authorized IPs this account can use (*0-256 or leave blank*)
#. For **Number of Auth MACs**, specify the number of authorized MACs this account can use (*0-256 or leave blank*)
#. For **Number of Auth Devices**, specify the number of authorized devices this account can use (*0-256 or leave blank*)
#. For **Auth IPs**, specify IP Addresses separated by commas or leave blank to not restrict
#. For **Auth MACs**, specify MAC Addresses separated by commas or leave blank to not restrict
#. For **Auth Node Groups**, specify Node Groups separated by commas or leave blank to not restrict
#. Click **Update**

Remove Administrator
--------------------

#. Go to **Management > User** in the top panel
#. Find and click **Checkbox** of user to delete
#. Click **Tasks > Remove User**
#. Click **Ok**

To Configure Administrator Role Options
---------------------------------------

#. Select user from main page under Management > User in the top panel
#. Click the Administrator tab. (Only visible with active Administrator Role assigned)

* Configure General settings:

 * Add approved Ip's for Web Console access
 * 2 step authentication 
 * Time zone

* Configure Notification settings:

 * Enable/ Disable notifications for user account or IP requests.
 * Mobile phones to receive notifications
 * Sender phone number
 * Email to receive notifications

* Configure Management Restrictions:

 * Specify permissions within Management Console. 


.. _Create Tag: https://docs.genians.com/monitoring/network-nodes/tagging-nodes.html?highlight=tag#create-tag
