# Lab 7 – Replay and Machine-in-the-Middle Attacks

## Overview
Like many industrial protocols, Modbus does not provide authentication or encryption. Any security must be provided at other layers in the protocol stack--such as routing this traffic through a VPN (virtual private network) tunnel or TLS (transport layer security). This lab will exploit the lack of security in Modbus to interact with the DER device directly from the adversary machine.

## Goal 
The first goal of this lab is to intercept communications between the DERMS and the DER using ARP poisoning via `ettercap`.  Once this traffic is captured, it can be analyzed to determine what holding registers are being written and with what values.  Then these packets can be exported and manipulated to send communication packets directly to the DER Modbus server. 

The second goal of this lab is to intercept traffic between the DERMS and DER and change values using a machine-in-the-middle attack. 

## Prerequisites

Windows DERMS Machine:  
	- SVP Dashboard

Kali Linux VM:  
	- Nmap
	- Ettercap  
	- Python
	- Wireshark