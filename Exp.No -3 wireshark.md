#  Digital Forensics Lab – Experiment 3  
**Password Capturing using Wireshark**  
---
## Introduction  
Wireshark is a network packet capture and analysis tool.  
It can capture sensitive information such as:  
- Usernames  
- Passwords  
- Email addresses  
- Session cookies  
- Other transmitted data  
Protocols like **HTTP, FTP, Telnet** often transmit unencrypted credentials.  
This makes Wireshark useful both for **network troubleshooting** and, if misused, for unauthorized access.  

In this experiment, we capture HTTP login credentials using Wireshark.  
---
##  Steps  

### Step 1 – Start Wireshark Capture  
- Open Wireshark in Windows/Linux.  
- Start capturing packets (e.g., Wi-Fi traffic).  
<p align="center">
  <img src="https://github.com/user-attachments/assets/003ad2d1-04fd-4cec-9293-a9caa5f4c61d" width="800" />
</p>  
---
### Step 2 – Perform Login on a Website  
- Visit a test website.  
- Enter login credentials (username + password).  
- These will be sent over the network in plain text (if HTTP is used).  
<p align="center">
  <img src="https://github.com/user-attachments/assets/1eff30b4-773e-4cda-8264-a51380756033" width="800" />
</p>  
---
### Step 3 – Apply HTTP Filter in Wireshark  
- After login, filter packets to show only HTTP traffic.  
- Enter the following in the **Display Filter Bar**:  
<p align="center">
  <img src="https://github.com/user-attachments/assets/2d5a844b-16e6-4de3-93b2-9938df9b2a40" width="800" />
</p>  
---
### Step 4 – Form Submission Methods  
Web forms use two methods to send login data:  
- **GET:** Data appended in the URL (rare for login forms).  
- **POST:** Data sent in the request body (commonly used).  
---
### Step 5 – Check GET Requests  
- Apply filter:  
- Result: Only page requests are shown.  
- No login data captured in GET requests.  
<p align="center">
  <img src="https://github.com/user-attachments/assets/a7dacc1e-b62d-45fe-a2aa-092974572a7c" width="800" />
</p>  
---
### Step 6 – Check POST Requests  
- Apply filter:  
<p align="center">
  <img src="https://github.com/user-attachments/assets/0a1f70bd-2f79-4ce3-aee1-0a5c4af33a5a" width="800" />
</p>  

---
 # Rubrics
  
  | Criteria | Mark Allotted | Mark Awarded |
  |---|---:|---:|
  | 1. GitHub Activity & Submission Regularity | 3 | |
  | 2. Application of Forensic Tools & Practical Execution | 3 | |
  | 3. Documentation & Reporting | 2 | |
  | 4. Engagement, Problem-Solving & Team Collaboration | 2 | |
  | *Total* | *10* | |
---
##  Result
The experiment successfully intercepted login credentials in plaintext (captured POST), confirming that **HTTP** transmits sensitive data openly and is trivially interceptable by an attacker.


