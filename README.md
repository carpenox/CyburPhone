Check out what it looks like here:
https://demo.dialer.one/CyburPhone-3.0/cyburphone.php

To install on your server for the following commands after changing to your web directory:

git clone https://github.com/carpenox/CyburPhone.git

chmod -R 744 CyburPhone

chown -R apache:apache CyburPhone

# CyburPhone-3.2.5

Version 3.2.5
With this release comes the following improvements:

A complete rewrite of the core Cyburphone code to support SIP.js v0.20.1
This does require 'rtcp_mux=yes' be set in the template you are using for your webphone
Support for passing a settings container from Cyburdial to Cyburphone to allow additional settings to be added in the future without Cyburdial changes
Added the ability to enable/disable various browser audio processing like Echo Cancellation and Automatic Gain Control
Does require the Cyburphone settings container support in Cyburdial
Auto call agent conference on successful registration. This is similar to a feature that was added to some forks of Cyburphone but it will work even if Cyburphone and Cyburdial are hosted on different domains.
Dynamic translation support. This is a frequent request that has been implemented in several of the forks of Cyburphone.
If you create a new translation, please share the values from your settings container
Play progress audio instead of ringing when placing a call
The audio file can be changed in the Cyburphone Settings Container by adjusting the region setting.
Currently supported regions include North America, Europe, and the UK.
Note:
If you already have Cyburphone working on your cluster, make sure that:

rtcp_mux=yes
is set in the template you are using for your webphones before switching to this version.
