# Firmware Analysis

## Overview

There are two labs that dig into firmware images (Lab 4A and Lab 4B).  In lab 4A, you will inspect DER firmware to try to identify data of interest.  Some of this data could be what operating system the DER device uses, what communication protocols are enabled, what ports are open, what services are running, and who were the authors of the software.  All of this information is valuable to an adversary because it can indicate the best approach to compromise the device.  These firmware images were taken from manufacturers who put them on the internet.  None of the images were encrypted. 

In the following lab, Lab 4B, you will see how malicious firmware could be used to compromise a DER device.  This is similar to the [SolarWinds](https://www.npr.org/2021/04/16/985439655/a-worst-nightmare-cyberattack-the-untold-story-of-the-solarwinds-hack) hack in which malicious code was added to a software update to gain backdoor access to computer networks. Lastly, students will see how to encrypt and decrypt data and code sign firmware. This is helpful to protect the DER from compromise, but is not failproof. In the 4B lab and in the SolarWinds attack, the malicious update was believed to be authentic because it was signed with the private key of the company.  This shows the importance of protecting private signing keys. 

# Goal

The goal of this lab is to show the types of data that can be extracted from DER firmware images. 

# Prerequisites

* Kali VM
    * strings
    * OpenSSL
	* binwalk
	
