# ansible-unifi-wifi-key-changer
This role changes the WLAN key of a given SSID on the Unifi controller remotely. 
You can enter your own key or have a randomized one created. 
The change will be announced via e-mail.

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
       - unifi-wifi-key-changer
```


# License
Licensed under the terms of Apache License Version 2. See LICENSE file.