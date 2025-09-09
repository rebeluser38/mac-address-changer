# MAC_address_SPOOFING
In this Repository I'll be practising and let you know about how to change one's device MAC address.

## FOREMOST LETS UNDERSTAND WHAT DOES THIS MAC address means to us.
> A MAC (Media Access Control) address is a unique hardware identifier assigned to a network interface, used within local networks to identify devices. 
A MAC address represents a unique identifier that distinguishes the device on a network, symbolizing both connectivity and security in the digital world.

A MAC (Media Access Control) address is fundamental to my experience with technology because it enables precise identification of my device within any network, allowing seamless communication and data exchange. To me, it embodies a critical element of digital identity and network management, ensuring that information reaches its intended destination securely and efficiently. Understanding the role of a MAC address deepens my appreciation for the underlying infrastructure that supports my everyday use of the internet and connected devices.


## Why do we need to Spoof our MAC Address?
Ethical reasons include:

**Privacy**: which Prevent tracking based on our physical address on public networks.(usually when we are on public or untrusted router)
Bypass MAC Filters: Some networks restrict access by MAC addresses; spoofing can be used during authorized security testing to evaluate network security.(usually happens when an individual mac address id blocked)
**Security Testing**: Used in penetration tests to simulate attacks or test defenses.
Spoofing the MAC address is done to protect privacy, bypass network restrictions, enhance security testing, or troubleshoot network issues by masking or changing the unique hardware identifier of a device.

## Considerations and Risks
While MAC spoofing has legitimate uses, it can be used unethically to hide identity or gain unauthorized network access. Additionally, some networks monitor and flag suspicious MAC address changes, so spoofing may lead to detection and consequences.

### Lets move ahead with the LINUX script in steps:
```
1$ sudo su
```
<img width="549" height="149" alt="Screenshot 2025-09-08 140441" src="https://github.com/user-attachments/assets/e454df9b-01d9-4fdf-8830-e13dbdc8e692" />

this script is used to enter in the root terminal, and while performing this spoofing this is the compulsory step.

```
2$ apt install macchanger
```
<img width="953" height="378" alt="Screenshot 2025-09-08 140913" src="https://github.com/user-attachments/assets/81c83f6c-6c84-4f66-86db-eade3b2228da" />

this is the command to install mac-changer in linux.

```
3$ apt-get update && upgrade
```
<img width="416" height="110" alt="Screenshot 2025-09-08 141204" src="https://github.com/user-attachments/assets/6a0649ee-c517-49a6-a90b-8de55bfde393" />

this one is for making all the directories and dictionary up to date.
<img width="444" height="104" alt="Screenshot 2025-09-08 141218" src="https://github.com/user-attachments/assets/09f056c9-7fdf-4665-b008-96116f12738f" />

```
4$ ip a
```
<img width="959" height="563" alt="Screenshot 2025-09-08 141413" src="https://github.com/user-attachments/assets/77980d1f-1398-434b-8b68-9e1281c7f2f5" />

this command is used for to the current IP related ADDRESS of the device and this includes our MAC address too.

```
5$ macchanger -r eth0
```
<img width="563" height="125" alt="Screenshot 2025-09-08 141817" src="https://github.com/user-attachments/assets/bbcac543-35f8-428c-be84-a9950d89cdee" />


"-r 'port name'" command is used to spoof the mac address to the RANDOM one.

```
6$ macchanger -m b2:aa:23:n3:d8:55 eth1 
```
<img width="597" height="129" alt="Screenshot 2025-09-08 144226" src="https://github.com/user-attachments/assets/8b371792-5471-420b-b835-56b621b5ba5e" />


-m this command we can set our MAC address of our own choice. 

```
7$ macchanger -l
```
<img width="941" height="733" alt="Screenshot 2025-09-08 144408" src="https://github.com/user-attachments/assets/4b94f194-1fab-400d-8a70-f1f1b535919b" />

this shows the list of prefix of all the devices registered on the globe, this is provided to help the user to customize their mac address to manuplate the device name which was recognized by the prefix of the MAC 

