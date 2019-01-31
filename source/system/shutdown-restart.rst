Shutdown and Restart System
===========================
.. warning:: To avoid system corruption, never remove device power source, or manually power off device before properly shutting down Genian NAC.

Control Power Through Web console
---------------------------------

#. Click **System** in the Menu Bar.
#. Select the IP address of the desired device from the view pane.
#. Click the **Power** tab.
#. Click **Restart** or **Shutdown**

Control Power Through Command Line Interface
--------------------------------------------

See: :doc:`/system/cli`

#. Connect to policy server or network sensor through command line.
#. Enter Global configuration mode.
#. To:

    * Restart: Enter command **restart system** or **reboot**
    * Shutdown: Enter command **shutdown service** or **halt**

.. note:: Device will remained powered on, but will now be safe to power off manually.