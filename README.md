# Week-16-Homework-Penetration-Testing-1

## Step 1: Google Dorking

### *Using Google, can you identify who the Chief Executive Officer of Altoro Mutual is:*
By navigating to the website demo.testfire.net and doing some basic reconnaissance we are able to find out who the CEO of Altoro Mutal is.

By following the links Inside Altora Mutual > About Us > Executives & Management Team > 

We can see the CEO of Altoro Mutual is Karl Fitzgerald.

Link: http://www.altoromutual.com/index.jsp?content=inside_executives.htm 

![Screenshot of Executives](https://github.com/BrendanT2248/Week-16-Homework-Penetration-Testing-1/blob/main/Images/gd%201.PNG)

### *How can this information be helpful to an attacker:*

This information is extremely useful to an attacker since they now know a potential high level target of the organisation. Now that they know his name, they could use his name for spoofing or for targeted phishing attacks. 

## Step 2: DNS and Domain Discovery

### *Enter the IP address for demo.testfire.net into Domain Dossier and answer the following questions based on the results:*

*Where is the company located:* 

Sunnyvale, CA, 94085, USA

*What is the NetRange IP address:*

65.61.137.64 - 65.61.137.127

*What is the company they use to store their infrastructure:* 

Rackspace Backbone Engineering. 

*What is the IP address of the DNS server:* 6

5.61.137.117

See screenshot:

![Domain Dossier Entry demo.testfire.net](https://github.com/BrendanT2248/Week-16-Homework-Penetration-Testing-1/blob/main/Images/dd1.PNG)

## Step 3: Shodan

### *What open ports and running services did Shodan find:*

Ports 80 (HTTP) and 443 (HTTPS) were open. See below screenshot:

![Shodan Scan of 65.61.137117](https://github.com/BrendanT2248/Week-16-Homework-Penetration-Testing-1/blob/main/Images/shodan1.PNG)

https://www.shodan.io/host/65.61.137.117

## Step 4: Recon-ng

### *Install the Recon `module xssed.`*
  - Search for the module `xssed` by entering `marketplace search xssed`
  - Install the module `xssed` by entering `marketplace install recon/domains-vulnerabilities/xssed`
  - Load the module `xssed` by entering `modules load recon/domains-vulnerableilities/xssed`

![xssed install](https://github.com/BrendanT2248/Week-16-Homework-Penetration-Testing-1/blob/main/Images/xssed1.PNG)

### *Set the source to `demo.testfire.net.`*
  - Check the information currently being held by xssed. We want to change this. Run `info`
  - To change the `SOURCE` from `default` to `demo.testfire.net` enter command `options set SOURCE demo.testfire.net`

![Set the source](https://github.com/BrendanT2248/Week-16-Homework-Penetration-Testing-1/blob/main/Images/xssed2.PNG)

### *Run the module.*
  - Run the module by entering `run`

![xssed run](https://github.com/BrendanT2248/Week-16-Homework-Penetration-Testing-1/blob/main/Images/xssed3.PNG)

We can see 1 new vulnerability found from the image above. In the 'category' we can see XSS.

### *Is Altoro Mutual vulnerable to XSS:*

  - Yes, as it was shown as the picked up vulnerability from xssed. By entering a script query into the search bar on the website, we are able to test this vulnerability.
  - Enter <script>alert("WARNING")</script> on the search bar on the website to test this. 
    - Enter the query into the search bar:

![XSS 1](https://github.com/BrendanT2248/Week-16-Homework-Penetration-Testing-1/blob/main/Images/xssed4.PNG)
    - Hit `Go` to execute the query:
    
![XSS Executed](https://github.com/BrendanT2248/Week-16-Homework-Penetration-Testing-1/blob/main/Images/xssed5.PNG)

We can see the XSS has been successfully. We have succesfully performed XSS on this website by entering a script in as a query.

## Step 5: Zenmap

### *Your client has asked that you help identify any vulnerabilities with their file-sharing server. Using the Metasploitable machine to act as your client's server, complete the following:* 

*Command for Zenmap to run a service scan against the Metasploitable machine:*



*Bonus command to output results into a new text file named zenmapscan.txt:*



*Zenmap vulnerability script command:*



*Once you have identified this vulnerability, answer the following questions for your client:*



*What is the vulnerability:*



*Why is it dangerous:*



*What mitigation strategies can you recommendations for the client to protect their server:*


