Ubiquiti NanoStation locoM5 Configuration
=========================================
This document provides an example walkthrough of how to configure a [Ubiquiti NanoStation locoM5](http://www.ubnt.com/airmax/nanostationm) as an unofficial supplement to the official [Quick Start Guide](http://dl.ubnt.com/guides/NanoStation_M/NanoStation_M_Loco_M_QSG.pdf) and [AirOS Guide](http://dl.ubnt.com/guides/airOS/airOS_UG.pdf). 

This work is provided as-is, without any warranty expressed or implied and under a Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International [License](#license).  

##<a name="download firmware"></a> Download the latest firmware
Before beginning the configuration process, [download](http://www.ubnt.com/download/) the latest version of the NanoStation locoM5 firmware. In this example, the Platform that needs selected is "airMax", Product Group "NanoStation M", and model "locoM5". If there is any uncertainty about whether you need the XW or XM firmware, download the latest version of both.    

If you are using Microsoft Windows 7, start by [preparing your connection](#windows config). If you are using Mac OSX, [start here](#mac config). If you are using Linux, it is assumed you know how to configure your a network interface. Configure the interface and continue to [configuring the NanoStation](#configure nsm5).  

##<a name="windows config"></a> Prepare your connection using Microsoft Windows 7
Using straight-through ethernet cables, plug the NanoStation and a computer into a switch. By default the NanoStation's IP address will be `192.168.1.20`, so the computer will need to be configured to operate on this subnet.  

To do this using Microsoft Windows 7, first go to Start > Control Panel and click "Network and Sharing Center".  
<img src="images/Control Panel.png" alt="Control Panel screenshot" style="width: 600px;"/>  

Click "Change adapter settings" in the Network and Sharing Center window.  
<img src="images/Network and Sharing Center.png" alt="Control Panel screenshot" style="width: 600px;"/>  

The "Network Connections" window will open. Right click "Local Area Connection" (or whatever name your LAN connection happens to be) and then click "Properties".  
<img src="images/Network Connections.png" alt="Network Connections screenshot" style="width: 600px;"/>  

Select "Internet Protocol Version 4 (TCP/IPv4)" and make sure the box to the left of it is checked. Now click "Properties".  
<img src="images/LAN Properties 1.png" alt="LAN Properties screenshot" style="width: 150px;"/>  

Note your current network settings, as you will need to revert to them after configuring the NanoStation. Click "Use the following IP Address" and fill in the IP address as `192.168.1.2`. Click in the "Subnet Mask" box. It should automatically populate the subnet as `255.255.255.0`. Hit "OK".  
<img src="images/LAN Properties 2.png" alt="LAN Properties screenshot" style="width: 150px;"/>  

Your connection is now prepared. Continue to [Configuring the NanoStation](#configure nsm5).

##<a name="mac config"></a> Prepare your connection using Mac OSX  
Using straight-through ethernet cables, plug the NanoStation and a computer into a switch. By default the NanoStation's IP address will be `192.168.1.20`, so the computer will need to be configured to operate on this subnet. 

To start, open "System Preferences" and click "Network". Note your current network settings, as you will need to revert to them after configuring the NanoStation. Click the drop-down list to the right of "Configure IPv4:" and select "Manually".  
<img src="images/Network Configuration.png" alt="Network Configuration screenshot" style="width: 600px;"/>  

Set the IP Address to `192.168.1.2`, make sure the Subnet Mask is set to `255.255.255.0`, and click "Apply".  
<img src="images/Configured Network.png" alt="Network Configuration screenshot" style="width: 600px;"/>  

Your connection is now prepared. Advance to [Configuring the NanoStation](#configure nsm5).

##<a name="configure nsm5"></a> Configure the NanoStation  
Now that your network is ready, log in to the NanoStation at [its default address](https://192.168.1.20). The default username and password is `ubnt`. A US English first login is shown below.  
<img src="images/First Login.png" alt="First login screenshot" style="width: 600px;"/>  

As a best practice, upgrade the firmware using the file [downloaded earlier](#download firmware). To do this, first click "System" after you have logged in and browse for the firmware. Note the current firmware version. If the version starts with "XW", use the XW firmware downloaded earlier. If it starts with "XM", use the XM firmware. Click "Browse", select the latest firmware, taking care to make sure the hardware revision in the filename (XW or XM) matches the version shown on the configuration window. 
<img src="images/Firmware Upload.png" alt="Firmware upload screenshot" style="width: 600px;"/>  

Click "Update" and allow the firmware to update. Be sure not to unplug the computer or the NanoSation while the firmware updates.  
<img src="images/Firmware Update.png" alt="Firmware update screenshot" style="width: 600px;"/>  

Now that the NanoStation is running the latest firmware, configure some of the basic system information by setting "Time Zone" to your local time and, optionally, entering the longitude and latitude of the device's location and configuring a user account and password. Once that is completed, click "Change" at the bottom and then "Apply" at the top.  

After configuring the system settings, it is time to configure the station's connection to the access point. Click "Select" to scan for the base station and select it from the list. Configure wireless security for the base station and click "Change" and then "Apply" once the connection is configured.   
<img src="images/Configure Wireless.png" alt="Wireless configuration screenshot" style="width: 600px;"/>  

Finally, configure the network settings that the NanoStation will use. In this example, the NanoStation will use DHCP with a fallback management address of `192.168.0.5`. Click "Change" and "Apply" once the NanoStation's network is configured.  
<img src="images/Configure Network.png" alt="Network configuration screenshot" style="width: 600px;"/>  

##<a name="reconfigure interface"></a> Reconfigure Network  
Now that the NanoStation is configured on your network, configure your network interface to its previous settings. Try to log in to the NanoStation using the IP address you configured it to use. If it works, it's time to deploy the NanoSation in the field. Happy installing!0

##<a name="license"></a> License Information

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="Creative Commons License" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br /><span xmlns:dct="http://purl.org/dc/terms/" href="http://purl.org/dc/dcmitype/Text" property="dct:title" rel="dct:type">Ubiquiti NanoStation locoM5 Configuration Walkthrough</span> by <a xmlns:cc="http://creativecommons.org/ns#" href="https://github.com/thejonx" property="cc:attributionName" rel="cc:attributionURL">Mathew Woodyard</a> is licensed under a <a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License</a>.<br />Permissions beyond the scope of this license may be available at <a xmlns:cc="http://creativecommons.org/ns#" href="https://github.com/thejonx/" rel="cc:morePermissions">https://github.com/thejonx/</a>.
