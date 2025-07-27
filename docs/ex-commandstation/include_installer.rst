.. include:: /include/include.rst
.. include:: /include/include-l1.rst
.. include:: /include/include-ex-cs.rst
.. meta::
   :keywords: EX-Installer

|EX-CS-LOGO|

********************
Install the Software
********************

|SUITABLE| |conductor| |tinkerer| |engineer| |support-button|

.. sidebar::
   :class: sidebar-on-this-page

   .. contents:: On this page
      :depth: 3
      :local:
    
Download and Run EX-Installer 
=============================

If you haven't done so already, you will need to start by downloading and running |EX-I|.

Refer to :doc:`/ex-installer/installing` for details on how to download, install, and run |EX-I|.

Once you are ready to install |EX-CS|, continue with this page.

'Select EX-CommandStation Version' screen
-----------------------------------------

.. figure:: /_static/images/ex-installer/select_cs_version.png
   :alt: EX-Installer - Select EX-CommandStation version
   :scale: 40%
   :align: left

   EX-Installer - Select EX-CommandStation version screen

On this screen you need to select:

* Which version of the EX-CommandStation software you wish to load
* How you wish to configure the software

Which version
~~~~~~~~~~~~~

Select which version of the |EX-CS| software to load onto your hardware.  If you are unsure, or unless you have been otherwise directed by the support team, we recommend you select ``Latest Production``.

How to configure
~~~~~~~~~~~~~~~~

Select how you wish to configure your |EX-CS|. Unless you are updating a previous version that you manually configured, or want to manually make advanced configuration changes, select ``Configure options on the next screen``

If you do want to manually make advanced configuration changes, see the :doc:`/ex-installer/installing` page for instructions on how to enable them.

If you have selected ``Configure options on the next screen``, to proceed, click the :guilabel:`Configure EX-CommandStation` button.

|force-break|

|HR-DASHED|

'Install EX-CommandStation' - Configuration screen
--------------------------------------------------

.. figure:: /_static/images/ex-installer/ex_cs_configure-general.png
   :alt: EX-Installer - EX-CommandStation Configuration
   :scale: 40%
   :align: left

   EX-Installer - EX-CommandStation Configuration screen

On this screen you can select some of the flexible and optional features of the |EX-CS|:

* Motor Driver type
* LCD or oLED display
* WiFi
* Ethernet
* Set track modes
* Advanced Config

Only the *Motor Driver* and *WiFi* will be covered on this page.  If you have installed different hardware to that recommended, see the :doc:`/ex-installer/installing` page for instructions on all the available configuration options.

|force-break|

Motor Driver
~~~~~~~~~~~~

.. hint:: 
   :class: hint-float-right-narrow

   For the |EX-CSB1-SHORT| alone select '**EX-CSB1**' |BR| If you have the additional |EX-MS| select '**EXCSB1_WITH_EX8874**'

.. figure:: /_static/images/ex-installer/ex_cs_configure_motor_shield.png
   :alt: EX-Installer - EX-CommandStation - Configure Motor Driver
   :scale: 60%
   :align: center

   EX-Installer - Configure Motor Driver

You *must* select the motor driver type that you have installed.  The installer can't detect this, so you must select the correct board or the |EX-CS| may not work. If you have installed the recommended Motor Driver, select `STANDARD_MOTOR_SHIELD` if you purchased a |standard Motor Driver|, or `EX8874_SHIELD` if you purchased our **EX-MotorShield8874**.

.. sidebar:: Station Mode VS Access Point Mode

   |conductor| |BR| There is no right or wrong selection here. Both options here may be valid for you to use, depending on how you wish to use your |EX-CS|.

   If a) your layout is close to your home WiFi network, b) you don't transport the layout around, c) you need to use more than four WiFi controllers at a time, and/or d) you are not likely to, or have no concerns about letting visitors access your home WiFi (for them to use their own devices on your layout), then **Station Mode** is probably a better option.

   If the above is not generally true, then **Access Point Mode** may be a better choice.

   You must choose one of these options now, but you can always come back later and re-load the software with a different option.

|HR-DASHED|

WiFi
~~~~

If you have installed and optional WiFi board, or are using a microcontroller board with integrated WiFi, enable the ``I have WiFi`` option, which will present you with additional options.

You can configure the WiFi for EX-CommandStation two ways:

* **Access Point mode** |BR| You can configure for EX-CommandStation to have its own, completely isolated, WiFi Network. This is referred to as *Access Point Mode*. (Most useful if your layout is away from the house, or you transport your layout frequently.) |BR| To enable, select ``Use my EX-CommandStation as an Access Point`` |BR| |BR|
* **Station mode**  |BR| The EX-CommandStation can be setup so that it connects to your existing home WiFi Network. This is referred to as *Station Mode*. |BR| To enable, select  ``Connect my EX-CommandStation to my existing wireless network`` 

Use my EX-CommandStation as an Access Point
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   .. figure:: /_static/images/ex-installer/ex_cs_configure_wifi_access_point.png
      :alt: EX-Installer - EX-CommandStation - Configure WiFi Access Point
      :scale: 50%
      :align: center

      EX-Installer - Configure WiFi - Access Point

   .. note::
      :class: note-float-right

      If possible, choose a channel that is unused (or least used) by other WiFi networks around your location. |BR|      
      There are numerous phone apps that can help you determine which channels are being used by other networks. For Android, *'Wifi Analyzer'* is one that works.  For iOS *'Netspot'* is suitable :dcc-ex-text-size-60pct:`(you don't need to purchase WiPry device they mention)`.
   

   If ``Use my EX-CommandStation as an Access Point`` is selected, two additional options are presented:

   * WiFi Password
   * WiFi Channel

   **WiFi Password** is optional.  |BR| **We recommend you leave this field blank.** |BR| If this field is left blank the password will default to "PASS_xxxxx" where 'xxxxx' will be the same as the SSID *name* that will be automatically configured.

   **WiFi Channel** can be any value from 1-11.

Connect my EX-CommandStation to my existing wireless network
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

   .. figure:: /_static/images/ex-installer/ex_cs_configure_wifi_station.png
      :alt: EX-Installer - EX-CommandStation - Configure Wifi - Station Mode
      :scale: 60%
      :align: center

      EX-Installer - Configure Wifi - Station Mode

   If ``Connect my EX-CommandStation to my existing wireless network`` is selected, two additional options are presented:

   * Wifi SSID
   * WiFi Password

   Both are required, Though it is possible, but unlikely, that the WiFi Password for your network is blank.  If so, leave the field blank.

   *WiFi SSID* is the name of your home network.

   *WiFi Password* is the password for your home network.

To proceed, click the :guilabel:`Compile and Load` button.

.. note::

   See the :doc:`/ex-commandstation/advanced-setup/supported-wifi/wifi-config` page if you wish to find more detailed information on the the WiFi options.

|force-break|

|HR-DASHED|

Display Type
~~~~~~~~~~~~

.. hint:: 
   :class: tip-float-right-narrow

   The |EX-CSB1-SHORT| will generally be supplied with a **OLED 128 X 64**

.. figure:: /_static/images/ex-installer/ex_cs_configure_screen.png
   :alt: EX-Installer - EX-CommandStation - Configure Display Driver
   :scale: 60%

   EX-Installer - Configure Display Driver


If you have installed and optional oLED or LED display, enable the ``I have a display`` option, which will present you with a drop down list to select the type of display you have.

|HR-DASHED|

Start with Power on
~~~~~~~~~~~~~~~~~~~

.. hint:: 
   :class: tip-float-right-narrow

   The |EX-CSB1-SHORT| will generally be supplied with this enabled

Enabling this option will cause the |EX-CS| to automatically start with the track power on.  

If you don't enable this, you will need to turn the track power with you controller, or with |EX-R| automations.

|force-break|

|HR-DASHED|

'Compile and Load' screen
-------------------------

.. figure:: /_static/images/ex-installer/ex_cs_load.png
   :alt: EX-Installer - Load
   :scale: 40%
   :align: left

   EX-Installer - Compile and Load Screen

To proceed, click the :guilabel:`Load` button.

Results are shown in the lower half of the screen.


If there are **no errors**, you can proceed to :doc:`testing your setup </ex-commandstation/controllers-diy>`.

If there **are errors** or you are having difficulties check the :doc:`/support/ex-cs-troubleshooting` page for assistance.

|force-break|

|HR-HEAVY|

Next Steps - Selecting a Throttle (Controller) 
==============================================

.. important:: 
   :class: important-float-right
   
   The programming track is for programming only. Make sure you are on the main track if you expect your loco to move or respond to light or sound commands.

See the :doc:`/ex-commandstation/controllers-diy` page or click the 'Next' button to learn how to select a throttle (controller) suitable to test and use your |EX-CS|.

|force-break|
