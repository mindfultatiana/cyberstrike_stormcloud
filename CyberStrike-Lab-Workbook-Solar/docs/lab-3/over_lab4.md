# Overview
A Denial of Service (DoS) attack makes a resource unavailable for legitimate use. There are many ways to perform a DoS attack, such as removing the power from a device, crashing a service on the device, or even overwhelming the device with network traffic so legitimate traffic cannot reach the device. We will use Hping3 to generate thousands of packets to flood the Modbus port and website port of the DER.  This will disrupt legitimate connection from the DERMS. 

## Goal
The goal of this lab is to demonstrate how an attacker can use Hping3 to perform a DoS attack on the Modbus and web interfaces to prevent legitimate users’ access to the DER device.

## Prerequisites
* On the DERMS Windows Machine, tools for this lab include: 
	* Wireshark
	* SVP Dashboard
	* Mozilla Firefox
* On the Kali VM, tools for this lab include: 
	* Hping3 - a network tool able to send custom ICMP/UDP/TCP packets

