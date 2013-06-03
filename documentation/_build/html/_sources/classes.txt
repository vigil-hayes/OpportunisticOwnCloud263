Classes Used in the OpportunisticOwnCloud Application
=====================================================

Here we describe the classes used in the OpportunisticOwnCloud application.

ConnectivityChangeReceiver
--------------------------

The ConnectivtyChangeReceive class is responsinle for listeining for network
events and creating Intent classes to handle the network events.
This class has a lifetime that endures throughout the application lifetime.


Extends: BroadcastReceiver
Implements: NONE

Public functions:

        void onReceive(Context, Intent)

Sub-Classes: NONE

SyncService
-----------

The SyncService is created from the ConnectivityChangeReceive class when a
network event is detected.

Extends: IntentService
Implements: NONE

Public functions: NONE

Sub-Classes:
        
        *mThread*
               
                * Extends: Thread

                * Implements: NONE

                * Public functions:
                        
                        void run()

        *DownLoadThread*

                * Extends: NONE

                * Implements: Runnable

                * Public functions:
                        
                        void run()

        *UploadThread*

                * Extends: NONE

                * Implements: Runnable

                * Public functions:

                        void run()

MainActivity
------------

The MainActivity class is primarily responsible for managing the GUI aspect of 
OpportunisticOwnCloud. It creates the LocalFileFragmentTab and the 
RemoteFileFragmetnTab instances. It also starts the SettingsActivity if the user
has never set OpportunisticOwnCloud settings on the phone prior to running
the applications. MainActivity is launched by the application when it is first opened.


Extends: SherlockFragmentActivity
Implements: NONE

Public functions:

        void onCreate(Bundle)
        void onPause()
        void onResume()
        boolean onCreateOptionsMenu(Menu)
        boolean onOptionsItemSelected(MenuItem)
        
Sub-Classes:

        *mThread*

                * Extends: Thread

                * Implements: NONE

                * Public functions:

                        void run()

LocalFileFragmentTab
--------------------

The LocalFileFragmentTab class is responsible for displaying the files located
on the user's ownCloud directory on /sdcard. It provides navigation functionality
for file browsing as well as on-demand upload functionality.

Extends: SherlockFragment
Implements: ActionBar.TabListener

Public functions:

        void onCreate(Bundle)
        void onTabSelected(Tab, FragmentTransaction)
        void onTabUnselected(Tab, FragmentTransaction)
        void onTabReselected(Tab, FragmentTransaction)

Sub-Classes:

        *mThread*

                * Extends: Thread

                * Implements: NONE

                * Public functions:

                        void run()

        *UploadThread*
                
                * Extends: NONE

                * Implements: Runnable

                * Public functions:
                        
                        void run()


RemoteFileFragmentTab
---------------------

The RemoteFileFragmentTab class is responsible for displaying the user's files located
on the ownCloud server. It provides navigation functionality
for file browsing as well as on-demand download functionality.

Extends: SherlockFragment
Implements: ActionBar.TabListener

Public functions:

        void onCreate(Bundle)
        void onTabSelected(Tab, FragmentTransaction)
        void onTabUnselected(Tab, FragmentTransaction)
        void onTabReselected(Tab, FragmentTransaction)

Sub-Classes:

        *mThread*

                * Extends: Thread

                * Implements: NONE

                * Public functions:

                        void run()

        *DownloadThread*

                * Extends: NONE

                * Implements: Runnable

                * Public functions:

                        void run()

SettingsActivity
----------------

The SettingsActivity provides a simple interface for the user to set
global settings, including username, password, and URL information for
connecting with the ownCloud server as well as setting sync frequency and
toggling opportunistic synchronization on and off. The data object created
is used globally to provide necessary settings information to the other classes.

Extends: PreferenceActivity
Implements: NONE

Public functions: NONE

Sub-Classes: NONE
