# VPN Hotspot

[![Build Status](https://api.travis-ci.org/Mygod/VPNHotspot.svg)](https://travis-ci.org/Mygod/VPNHotspot)
[![API](https://img.shields.io/badge/API-21%2B-brightgreen.svg?style=flat)](https://android-arsenal.com/api?level=21)
[![Releases](https://img.shields.io/github/downloads/Mygod/VPNHotspot/total.svg)](https://github.com/Mygod/VPNHotspot/releases)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/e70e52b1a58045819b505c09edcae816)](https://www.codacy.com/app/Mygod/VPNHotspot?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=Mygod/VPNHotspot&amp;utm_campaign=Badge_Grade)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

Connecting things to your VPN made simple. Share your VPN connection over hotspot or repeater. (**root required**)  
<a href="https://play.google.com/store/apps/details?id=be.mygod.vpnhotspot" target="_blank"><img src="https://play.google.com/intl/en_us/badges/images/generic/en-play-badge.png" height="60"></a>
<a href="https://f-droid.org/packages/be.mygod.vpnhotspot/" target="_blank"><img src="https://f-droid.org/badge/get-it-on.png" height="60"></a>
or <a href="https://labs.xda-developers.com/store/app/be.mygod.vpnhotspot" target="_blank">XDA Labs</a>

This app is useful for:

* Connecting things that don't support VPN like Chromecasts behind corporate firewalls;
* Set up [gapps](https://support.google.com/pixelphone/answer/7158475) behind corporate firewalls;
* Connect to your mobile hotspot but you're not bothered to set up VPN on your device.

P.S. You can also do the similar on [Windows](https://www.expressvpn.com/support/vpn-setup/share-vpn-connection-windows/)
and [Mac](https://www.expressvpn.com/support/vpn-setup/share-vpn-connection-mac/).
I don't know about you but I can't get my stupid Windows 10 to work with
[hosted network](https://msdn.microsoft.com/en-us/library/windows/desktop/dd815243(v=vs.85).aspx)
now that they introduced this
[Mobile hotspot](https://support.microsoft.com/en-us/help/4027762/windows-use-your-pc-as-a-mobile-hotspot).

This app is designed to do only minimal changes to your system, so there's almost no chance you will brick your device
and/or break your Internet using this app *under normal conditions*. However there's also absolutely no guarantee it won't.

## Q & A

### Edit network name and/or password for repeater?

These are generated by Android system and can't be specified manually for now.
You can however request a credential reset using the button in this app.

SSID is hardcoded to `DIRECT-<random 2 char>-<your device name>` so the only thing you can customize is the last part in
system Wi-Fi direct settings. Password is hardcoded to a random 8 char string. Changing anything else requires replacing
driver `wpa_supplicant` which we are not considering implementing.

### Connect a 2.4GHz-only device to a 5GHz repeater?

You'll have to use WPS for now to make the repeater switch to 2.4GHz.

### [IPv6 tethering?](https://github.com/Mygod/VPNHotspot/issues/6)

### No root?

Without root, you can only:

* View connected devices for system tethering and monitor them if your SELinux status is not enforcing
  (otherwise you can still do manual refreshes);
* Play around with settings;
* Alternatively you can use [NetShare-no-root-tethering](https://play.google.com/store/apps/details?id=kha.prog.mikrotik)
  (requires manual proxy configuration) for normal repeater tethering.
