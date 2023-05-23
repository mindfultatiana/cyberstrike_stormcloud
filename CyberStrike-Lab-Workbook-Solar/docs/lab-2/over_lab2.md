# Lab 2 – Exploring and Exploiting DER Logical Interfaces

# Overview

The Distributed Energy Resource (DER) often gives the homeowner/operator a user interface to visualize operations or make changes to the configuration (e.g., setting up the Wi-Fi connections). Some interfaces on a DER will be locally accessable like a front panel or Wi-Fi/Bluetooth interfaces; but others are accessable hundreds of miles away through the internet. Sometimes this data is sent over local area networks at homes and business. Othertimes this data is sent through cellular connections or Advanced Metering Infrastructure (AMI) mesh networks. To facilitate monitoring remotely, services may be enabled on the DER to allow an operator to connect remotely and view power data or other information. 

**Nmap**   

This lab will use Nmap to identify which network services are available and listening on the 
HMI. From the Nmap website, “Nmap ("Network Mapper") is a free and open-source (license) 
utility for network discovery and security auditing.”

[Nmap](https://nmap.org)

## Goal

The goal of this lab is to perform reconnaissance to discover the network services 
available on the HMI using Nmap. Then, we will take remote control of the HMI by 
connecting to its user interface using VNC.

## Prerequisites

* CyberStrike-LAN VM
* Nmap
* xHydra

### Reconnaissance with Nmap

The environment
