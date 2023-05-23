# Lab 1 - Open-Source Intelligence (OSINT)

## Overview 

These exercises require access to the Internet. If access to the Internet is not 
available, these exercises can be performed at another time when access to the 
Internet is available.

***Google***

Google Search is the most widely used web search engine. Google Search’s main 
purpose is to index the world’s publicly accessible web servers, which allows a 
user to search for anything from movie show times, to the current weather, to system 
vulnerabilities. Google Search also provides many advanced search options, allowing 
a user to limit search results to specific sites, file types, or even keywords in a 
webpage’s title or URL.

***Shodan***

Shodan is a search engine for Internet-connected devices, such as webcams, routers, 
HMIs, Programmable Logic Controllers (PLCs), etc. It allows a user to search metadata 
(e.g., service banners) using various filters. At a minimum, Shodan will return the 
IP address, open ports on the system, and services running on those open ports. In 
addition, it may also provide some of the following information about an 
Internet-connected device:

* Product name
* Vendor ID
* Serial number
* Device type
* Device IP
* City
* Country
* Organization
* Internet Service Provider (ISP)
* Most Recent Update
* Hostnames
* Autonomous System Number (ASN)

**NOTE:** If you plan to use Shodan from your corporate environment, consult your IT 
security department to ensure accessing Shodan is not prohibited.

## Goal

The first goal of this lab is to use Google and Shodan to practice finding and 
gathering as much open-source information as possible about Internet-accessible 
devices — specifically the type used in later labs.

**NOTE:** *This lab will involve searching the Internet for real-world devices 
that are accessible from the Internet. The goal of this lab is passive 
reconnaissance of those devices. Any attempt to connect to or manipulate these 
devices could have legal ramifications. For the purposes of this lab, perform 
only passive reconnaissance.*


## Prerequisites

* CyberStrike-iNet
* Firefox Web Browser
