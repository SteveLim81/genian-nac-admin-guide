Create a  USB drive
===================

.. caution:: All files in the USB drive will be deleted during the process so back up your files from the USB Drive to move forward.

.. caution:: All files in the USB drive will be deleted during the process so back up your files from the USB Drive to move forward.

To install Genian NAC Policy Server to a physical machine, create a  USB drive using UNETbootin first.

Getting UNETbootin
------------------

Genians recommend `UNETbootin`_ which allows you to create a  USB flash drives for Genian NAC installation without burning a CD. Choose your Operating System to download UNETbootin.

- `Windows`_
- `Mac OS X`_
- Linux
   - `32-bit binary`_
   - `64-bit binary`_

Creating a USB drive
--------------------
Ensure that your USB drive is formated FAT32. Other file systems may not be supported.

Once UNETbootin is installed, follow the steps below.

1. Load the Diskimage

.. image:: /images/unetbootin-1-loading-image.png

2. Click OK and move on.

.. image:: /images/unetbootin-2-copying-files.png

3. Click Exit

.. image:: /images/unetbootin-3-installation-complete.png

Now, you have the  USB drive to install Genian NAC into your desired machine. Congrats!

Troubleshooting
-----------------------------
- Error message: "BOOTMGR is missing" indicative of improperly formatted USB drive. 

.. _UNETbootin: https://unetbootin.github.io/
.. _Windows: http://launchpad.net/unetbootin/trunk/625/+download/unetbootin-windows-625.exe
.. _Mac OS X: http://launchpad.net/unetbootin/trunk/625/+download/unetbootin-mac-625.dmg
.. _32-bit binary: https://github.com/unetbootin/unetbootin/releases/download/661/unetbootin-linux-661.bin
.. _64-bit binary: https://github.com/unetbootin/unetbootin/releases/download/661/unetbootin-linux64-661.bin
