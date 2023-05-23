## Searching for Targets using Shodan

1. Open a Web Browser
2. Navigate to [Shodan](https://www.shodan.io/)
3. Start searching for Internet-connected devices using the search bar in the upper-left
   (e.g., Industrial Controls Systems (ICS), Databases, Webcams)

	![ifconfig](../img/image12.png)

4. Navigate to [Shodan Explore](https://www.shodan.io/explore) to explore a list of
   pre-configured searches

	![ifconfig](../img/image13.png)

5. Navigate to [Shodan Explore ICS](https://www.shodan.io/explore/category/industrial-control-systems)
   and read a short introduction to ICS protocols, and then explore pre-configured searches.

	![ifconfig](../img/image14.png)

6. Perform Shodan searches for Internet-connected devices using the following search terms:

	* `SMA inverter`
	* `Solar Farm`
	* `PV Inverter`
	* `Solar port:502` (This step may require a login, skip if you do not have a Shodan account.)

7. Click the IP address for each result to review additional details about the
   Internet-connected devices identified in the search results, including open ports
   and services running on the device.

8. Want more? Check out some other searches here: [Awesome Shodan Queries](https://github.com/jakejarvis/awesome-shodan-queries)

**CAUTION:** As with connecting to any unfamiliar sites on the Internet, be very careful
connecting to any devices identified through Shodan. These could be live systems, they
could be Honeypots used by researchers, or they could be a malicious attacker.

***
***
![ifconfig](../img/image15.png)
***
***
![ifconfig](../img/image16.png)
***

The Amazon Web Services (AWS) servers above are web-facing APIs for different companies.   
