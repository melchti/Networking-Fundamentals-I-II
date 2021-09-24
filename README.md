# Networking-Fundamentals-I-II
These assignments overview the fundamental topics of cybersecurity and computer Networking. These also review more advanced concepts such as DHCP, NAT, routing, wireless technology, DNS records, and email networking.

Homework 8

The Scenario for this assignment was as follows:

In this unit, we will focus on one of the most important foundational topics in cybersecurity, computer networking. Understanding how systems and devices are networked together to exchange information is a vital skill for cybersecurity professionals.

•	The first day will cover the client/server model, network topologies, and how IP addresses and DNS are used to connect systems together.

•	The second day will cover additional foundational topics such as ports, protocols, and the OSI model. We will then use a networking tool called Wireshark to visualize and analyze networking concepts.

•	The third day will dive deeper into OSI layers 2, 3, and 4. We will learn tools and protocols related to each layer, and perform a SYN scan to search for open ports on a network.



Steps used to complete task:
1.	I used fping against the IP ranges to determine the IP’s for the Hollywood office.
2.	I used SYN SCAN against the IP accepting connections.
3.	I logged into the RockStar server from the previous step using username: jimi and password: hendrix, to determine if something was modified on this system that might affect viewing rollingstone.com within the browser. 
4.	I found where the hacker left a note as to where he stored away some packet captures.
5.	I used Wireshark to analyze this pcap file and determine if there was any suspicious activity that could be attributed to a hacker.




Homework 9

In the second networking fundamentals unit, I built on the skills learned in the first week, covering more advanced concepts such as DHCP, NAT, routing, wireless technology, DNS records, and email networking. The week concludes with a fun Capture the Flag competition that uses the skills learned in both weeks.


The Scenario for this assignment was as follows:

•  You are a Network Jedi working for the Resistance.

•  The Sith Empire recently carried out a DoS attack, taking out the Resistance's core network infrastructure, including its DNS servers.

•  This attack destroyed the Resistance's ability to communicate via email and retrieve other crucial information about each others' operations. The Empire has taken advantage of this compromised availability by ambushing numerous Resistance outposts, all vulnerable because they can no longer call for help.

•  Your task is a crucial one: Restore the Resistance's core DNS infrastructure and verify that traffic is routing as expected.


Missions to be mitigated

Mission 1

Issue: Due to the DoS attack, the Empire took down the Resistance's DNS and primary email servers.

•	The Resistance's network team was able to build and deploy a new DNS server and mail server.

•	The new primary mail server is asltx.l.google.com and the secondary should be asltx.2.google.com.

•	The Resistance (starwars.com) is able to send emails but unable to receive any.


Your mission:

•	Determine and document the mail servers for starwars.com using NSLOOKUP.

•	Explain why the Resistance isn't receiving any emails.

•	Document what a corrected DNS record should be.

Mission 2

Issue: Now that you've addressed the mail servers, all emails are coming through. However, users are still reporting that they haven't received mail from the theforce.net alert bulletins.

•	Many of the alert bulletins are being blocked or going into spam folders.

•	This is probably due to the fact that theforce.net changed the IP address of their mail server to 45.23.176.21 while your network was down.

•	These alerts are critical to identify pending attacks from the Empire.

Your mission:

•	Determine and document the SPF for theforce.net using NSLOOKUP.

•	Explain why the Force's emails are going to spam.

•	Document what a corrected DNS record should be.


Mission 3

Issue: You have successfully resolved all email issues and the resistance can now receive alert bulletins. However, the Resistance is unable to easily read the details of alert bulletins online.

•	They are supposed to be automatically redirected from their sub page of resistance.theforce.net to theforce.net.
Your mission:

•	Document how a CNAME should look by viewing the CNAME of www.theforce.net using NSLOOKUP.

•	Explain why the sub page of resistance.theforce.net isn't redirecting to theforce.net.

•	Document what a corrected DNS record should be.



Mission 4

Issue: During the attack, it was determined that the Empire also took down the primary DNS server of princessleia.site.

•	Fortunately, the DNS server for princessleia.site is backed up and functioning.

•	However, the Resistance was unable to access this important site during the attacks and now they need you to prevent this from happening again.

•	The Resistance's networking team provided you with a backup DNS server of: ns2.galaxybackup.com.

Your mission:

•	Confirm the DNS records for princessleia.site.

•	Document how you would fix the DNS record to prevent this issue from happening again.



Mission 5

Issue: The network traffic from the planet of Batuu to the planet of Jedha is very slow.

•	You have been provided a network map with a list of planets connected between Batuu and Jedha.

•	It has been determined that the slowness is due to the Empire attacking Planet N.

Your Mission:

•	View the Galaxy Network Map and determine the OSPF shortest path from Batuu to Jedha.

•	Confirm your path doesn't include Planet N in its route.

•	Document this shortest path so it can be used by the Resistance to develop a static route to improve the traffic.



Mission 6

Issue: Due to all these attacks, the Resistance is determined to seek revenge for the damage the Empire has caused.

•	You are tasked with gathering secret information from the Dark Side network servers that can be used to launch network attacks against the Empire.

•	You have captured some of the Dark Side's encrypted wireless internet traffic in the following pcap: Darkside.pcap.

Your Mission:

•	Figure out the Dark Side's secret wireless key by using Aircrack-ng.

o	Hint: This is a more challenging encrypted wireless traffic using WPA.

o	In order to decrypt, you will need to use a wordlist (-w) such as rockyou.txt.

•	Use the Dark Side's key to decrypt the wireless traffic in Wireshark.

o	Hint: The format for they key to decrypt wireless is <Wireless_key>:<SSID>.
  
•	Once you have decrypted the traffic, figure out the following Dark Side information:
  
o	Host IP Addresses and MAC Addresses by looking at the decrypted ARP traffic.
  
o	Document these IP and MAC Addresses, as the resistance will use these IP addresses to launch a retaliatory attack.
  
  
  
Mission 7
  
As a thank you for saving the galaxy, the Resistance wants to send you a secret message!
  
Your Mission:
  
•	View the DNS record from Mission #4.
  
•	The Resistance provided you with a hidden message in the TXT record, with several steps to follow.
  
•	Follow the steps from the TXT record.
  
o	Note: A backup option is provided in the TXT record (as a website) in case the main telnet site is unavailable
  


