# Overview
DER devices often host websites for commissioning, configurations, or data monitoring.  These interfaces can be difficult to secure as there are many potential web vulnerabilities.  This lesson will demonstrate SQL injection attacks and code injection attacks on the DER website.  Data collected from these exploits will be used to gain further access into the DER system through the Virtual Network Computing (VNC) interface.  This will expose other users' hashed passwords which we will crack using John the Ripper. 

## Goal
The goal of this lab is to demonstrate how an attacker can use exploit insecure websites, use the VNC protocol, and crack password hashes.

## Prerequisites

* Log onto Kali VM. Tools for this lab include: 
	* Mozilla Firefox
	* VNC Viewer
	* John the Ripper - password cracker

