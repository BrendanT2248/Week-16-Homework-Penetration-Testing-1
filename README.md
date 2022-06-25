# Week-16-Homework-Penetration-Testing-1

## Step 1: Google Dorking

*Using Google, can you identify who the Chief Executive Officer of Altoro Mutual is:
By navigating to the website demo.testfire.net and doing some basic reconnaissance we are able to find out who the CEO of Altoro Mutal is.*

By following the links Inside Altora Mutual > About Us > Executives & Management Team > 

We can see the CEO of Altoro Mutual is Karl Fitzgerald.

Link: http://www.altoromutual.com/index.jsp?content=inside_executives.htm 

[Screenshot of Executives] (https://github.com/BrendanT2248/Week-16-Homework-Penetration-Testing-1/blob/main/Images/gd%201.PNG)

*How can this information be helpful to an attacker:*
This information is extremely useful to an attacker since they now know a potential high level target of the organisation. Now that they know his name, they could use his name for spoofing or for targeted phishing attacks. 
Step 2: DNS and Domain Discovery
Enter the IP address for demo.testfire.net into Domain Dossier and answer the following questions based on the results:
Where is the company located: Sunnyvale, CA, 94085, USA


What is the NetRange IP address: 65.61.137.64 - 65.61.137.127


What is the company they use to store their infrastructure: Rackspace Backbone Engineering. See screenshot:


What is the IP address of the DNS server: 65.61.137.117



Step 3: Shodan
What open ports and running services did Shodan find: 
Ports 80 (HTTP) and 443 (HTTPS) were open. See below screenshot:
https://www.shodan.io/host/65.61.137.117 
Step 4: Recon-ng
Install the Recon module xssed.
Set the source to demo.testfire.net.
Run the module.
Is Altoro Mutual vulnerable to XSS:
Step 5: Zenmap
Your client has asked that you help identify any vulnerabilities with their file-sharing server. Using the Metasploitable machine to act as your client's server, complete the following:
Command for Zenmap to run a service scan against the Metasploitable machine:


Bonus command to output results into a new text file named zenmapscan.txt:


Zenmap vulnerability script command:


Once you have identified this vulnerability, answer the following questions for your client:


What is the vulnerability:


Why is it dangerous:


What mitigation strategies can you recommendations for the client to protect their server:

