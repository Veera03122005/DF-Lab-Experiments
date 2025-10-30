# Ex.No.4   Mail Header Analyzer (MHA)

## Aim
- To use a Mail Header Analyzer (MHA) to trace an email’s origin, verify its authenticity, and detect possible spoofing attempts by examining its header.

---

## Procedure  

### Step 1: Extract the Email Header
- Open the email and copy the *raw header*.  

- *For Gmail:*  
  - Open the email → click on the three dots (⋮) → select *Show original*.  
    <br>

<img width="1366" height="768" alt="Screenshot (35)" src="https://github.com/user-attachments/assets/9a70392b-ff8a-450c-857d-b99a314f0cb4" />
  <br>
  - Copy the entire header text.
  <br>
<img width="1366" height="768" alt="Screenshot (36)" src="https://github.com/user-attachments/assets/dea4065c-090e-475e-9774-780c0b49471e" />
  <br>
---

### Step 2: Use a Mail Header Analyzer
- Go to an online tool such as *MXToolbox Email Header Analyzer*.  
  
  <br>
<img width="1366" height="768" alt="Screenshot (37)" src="https://github.com/user-attachments/assets/6bf4f7fc-095f-4cc4-aaca-6e7db67e0c09" />
  <br>
- Paste the copied email header into the input box and click *Analyze*.
  <br>
 <img width="1366" height="768" alt="Screenshot (38)" src="https://github.com/user-attachments/assets/4ce25289-c359-46ee-95f6-64f868223472" />
 <br>
 
- The tool will generate a structured, easy-to-read analysis report.
  

---

### Step 3: Review the Analysis Report  

### Delivery Summary  
- *DMARC Compliance:*  Passed (email considered authentic at a high level).  
- *SPF Check:*  Both SPF Authentication and Alignment passed.  
- *DKIM Check:*  DKIM Alignment passed, but *DKIM Authentication failed* (critical issue).  
  <br>
<img width="1366" height="768" alt="Screenshot (39)" src="https://github.com/user-attachments/assets/eb8c84aa-dfc5-445d-9f98-99044e3c2143" />
  <br>
---

###  Investigating SPF Record and Email Path  
- *SPF Record:* v=spf1 include:mailgun.org ~all  
  - This means the domain authorizes Mailgun servers to send emails on its behalf.  

- *Relay Path:* The email originated from m241-136.mailgun.net (a Mailgun server).  
  <br>
<img width="1366" height="768" alt="Screenshot (40)" src="https://github.com/user-attachments/assets/e4336f01-cd46-4495-9b35-e6f20edc06b5" />
  <br>
---

###  Analyzing the DKIM 

  <br>
<img width="1366" height="768" alt="Screenshot (41)" src="https://github.com/user-attachments/assets/cee95def-a875-4554-b7d0-0a6196f77824" />
  <br>

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
## Result
- *SPF Passed* → The sending server was authorized.  
- *DMARC Passed* → The email is considered compliant overall.  


The email is  fully trustworthy. While SPF and DMARC confirm legitimacy at the server level.  


