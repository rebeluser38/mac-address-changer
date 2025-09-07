# MAC-address-SPOOFING
In this Repository I'll be practising and let you know about how to change one's device MAC address.

#  FOREMOST LETS UNDERSTAND WHAT DOES THIS MAC address means to us.
A MAC (Media Access Control) address is a unique hardware identifier assigned to a network interface, used within local networks to identify devices. 
Spoofing a MAC address allows us to mask our actual device identity for privacy, security testing, or bypassing simple network restrictions.


# Why do we need to Spoof our MAC Address?
Ethical reasons include:
Privacy: which Prevent tracking based on our physical address on public networks.(usually when we are on public or untrusted router)
Bypass MAC Filters: Some networks restrict access by MAC addresses; spoofing can be used during authorized security testing to evaluate network security.(usually happens when an individual mac address id blocked)
Security Testing: Used in penetration tests to simulate attacks or test defenses.

# lets move ahead with the script in steps:
```
$ sudo su
```
this script is used to enter in the root terminal, and while performing this spoofing this is the compulsory step.
```

$ apt install macchanger
```
this is the command to install mac-changer in linux.
```

$ apt-get update && upgrade
```
this one is for making all the directories and dictionary up to date.
```

$ ip a
```
this command is used for to the current IP related ADDRESS of the device and this includes our MAC address too.
```

$ macchanger -r eth0
```
"-r 'port name'" command is used to spoof the mac address to the RANDOM one.
```

$ macchanger -m b2:aa:23:n3:d8:55 eth1 
```
-m this command we can set our MAC address of our own choice. 
```

$ macchanger -l
```
this shows the list of prefix of all the devices registered on the globe, this is provided to help the user to customize their mac address to manuplate the device name which was recognized by the prefix of the MAC 
