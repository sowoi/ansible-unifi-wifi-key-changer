# ansible-unifi-wifi-key-changer
This role changes the WLAN key of a given SSID on the Unifi controller remotely. 
You can enter your own key or have a randomized one created. 
The change will be announced via e-mail.

# Setup
Change wifikeyset to True if you want to be prompted to enter a key.
Alternatively you can write a wifi key without prompt in wifi_key (remove the lookup entry for this).


# Parameters
unifiuser:
unifipassword:
wifissid:
wifikeyset: False
wifi_key: "{{ lookup('password', '/dev/null length=12 chars=ascii_letters') }}"
mailHost:
mailSMTPPort:
mailUsername:
mailPassword:
mailSendTo:

# Dependencies
None

# Example Playbook
``` 
- hosts: servers
  roles:
    - sowoi.ansible_unifi_wifi_key_changer
```

# License
Licensed under the terms of GNU General Public License v3.0. See LICENSE file.

# Author Information
https://okxo.de
