Setup
=====

The setup assumes you have the Android ADT and Android SDK installed.

.. _get_code
From the code
----------------

In the terminal, enter:

        git clone git://github.com/mvigil90/OpportunisticOwnCloud.git
        
Open Eclipse with ADT support.

#. Go to 'File'>'Import'.
#. Select 'Android'>'Existing Code into Workspace'.
#. Browse to /path/to/OpportunisticOwnCloud263/actionbarsherlock.
#. Again, select 'Android'>'Existing Code into Workspace'.
#. Browse to /path/to/OpportunisticOwnCloud263
#. Now, right-click the OpportunisticOwnCloud project in the Eclipse Package Explorer. 
#. Select 'Properties'
#. In the Android tab, ensure that actionbarsherlock has been selected as a Library
#. Ensure that simple-xml-2.6.2.jar is in the libs/ folder of the OpportunisticOwnCloud project.

At this point, you should be able to run the application on the emulator or on a device.
If you are using an emulator, make sure you have created one and explicitly set the RAM
size (512 MB works fine). Otherwise, the sdcard is mounted as Read-only and the
application will not work.
