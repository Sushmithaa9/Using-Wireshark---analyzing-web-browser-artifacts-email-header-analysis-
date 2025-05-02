# Using-Wireshark---analyzing-web-browser-artifacts-email-header-analysis
## AIM:
To use Wireshark to analyze web browser activities and inspect email headers from captured network traffic.

## DESIGN STEPS:
### Step 1:
Launch Wireshark and start capturing traffic on the appropriate network interface.

### Step 2:
Use filters like http, dns, or tcp.port == 80 to monitor web browser artifacts such as visited URLs, cookies, and user-agent strings.

### Step 3:
Apply filters like smtp, pop, or imap to locate and analyze email header details (e.g., sender, receiver, subject) from email communications.

## PROGRAM:

**Capturing Traffic in Wireshark**

  1. Open Wireshark and start capturing on the active interface (Wi- Fi/Ethernet).
  
  2. Perform activities like opening a website or sending an email through a client (e.g., Gmail via browser or Thunderbird).
  
  3. Stop the capture once done.

![image](https://github.com/user-attachments/assets/274850fa-06a8-4573-95db-020fea37552e)


**Analyze DNS Queries:**
  
  1. Filter: dns

  2. Reveal domains the browser tried to resolve.

![image](https://github.com/user-attachments/assets/71974a10-39f0-4a11-b15a-bdb03ebb3906)


**Email Header Analysis**

  1. Apply relevant filters
     
  o For POP3: tcp.port == 110
  
  o For SMTP: tcp.port == 25 or 587
  
  o For IMAP: tcp.port == 143 or 993

  2. Locate email data
    
  3. Look for SMTP packets to see sender/receiver email addresses.
  
  4. Use "Follow TCP Stream" to view the full email headers and body if unencrypted.

**Extract Email Header Fields:**
  
  1. Analyze From, To, Subject, Date, Message-ID, and relay servers used in sending the email.

## OUTPUT:

Captured Web Activity and Email Header Information

![image](https://github.com/user-attachments/assets/e8bd8220-0cbe-429e-8644-8538f522c707)

![image](https://github.com/user-attachments/assets/ae245ee2-4dc2-4930-93d8-78add5a53d16)

![image](https://github.com/user-attachments/assets/154c6231-9a4a-4cd5-8b32-4dd1df0c332f)


## RESULT:
Web browser artifacts and email headers were successfully analyzed using Wireshark.

