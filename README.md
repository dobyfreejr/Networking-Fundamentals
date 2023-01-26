## **Phase 1: “I’d like to Teach the World to ping”**

### **1.Command(s) used to run fping against the IP ranges:**

    fping 15.199.95.91 15.199.94.91 11.199.158.91 161.35.96.20 11.199.141.91


### **2.Summarize the results of the fping command(s)**:

    161.35.96.20 is alive
    15.199.95.91 is unreachable
    15.199.94.91 is unreachable
    11.199.158.91 is unreachable
    11.199.141.91 is unreachable


### **3.List of IPs responding to echo requests:**




### **4.Explain which OSI layer(s) your findings involve:**

    Layer 3 Network




### **5.Mitigation recommendations (if needed):**

    Rockstar doesnt want request for it services so its considered a vulnerability for it to be able to reached.



## **Phase 2: “Some SYN for Nothin`”**

### **1.Which ports are open on the RockStar Corp server?**

    Sudo nmap -sS 161.35.96.20


   ### **2.Which OSI layer do SYN scans run on?**

 - #### *OSI Layer*:

        Layer 3 network


 - #### *Explain how you determined which layer*:

       We have the ability to connect through port 22 which is SSH


### **3.Mitigation suggestions (if needed):**

    Close off port 22 to prevent people from being able to ssh in



## **Phase 3: “I Feel a DNSwhichChange Comin’ On”**

### **1.Summarize your findings about why access to rollingstone.com is not working as expected from the RockStar Corp Hollywood office:**

    The Ip address is incorrect


### **2.Command used to query Domain Name System records:**

    nslookup


### **3.Domain name findings:**


### **4.Explain what OSI layer DNS runs on:**

    Layer 7 applications


### **5.Mitigation suggestions (if needed):**

    Best way to prevent this would not allow people access to the hosts files to be able to change or modify things within it. Allow a script check for changes to this file. 



## **Phase 4: “ShARP Dressed Man”**

### **1. Name of file containing packets:**

    Etc/packetcaptureinfo.txt


### **2.ARP findings identifying the hacker’s MAC address:**
    00:0c:29:1d:b3:b1


### **3.HTTP findings, including the message from the hacker:**




### **4.Explain the OSI layers for HTTP and ARP.**

- #### *Layer used for HTTP:*

      Layer 7 application


- #### *Layer used for ARP:*

      Layer 2 data link


### **5.Mitigation suggestions (if needed):**

     Dont allow for people to ssh into the system. Automate the system to find when people are entering when they shouldnt. Allow for the logs to be kept for later checking to make sure that things werent tapered with.




