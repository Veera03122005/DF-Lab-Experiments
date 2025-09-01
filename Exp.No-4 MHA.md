# Ex.No.4   Mail Header Analyzer (MHA)

## Aim
- To use a Mail Header Analyzer (MHA) to trace an email’s origin, verify its authenticity, and detect possible spoofing attempts by examining its header.

---

## Procedure  

### Step 1: Extract the Email Header
- Open the email and copy the *raw header*.  

- *For Gmail:*  
  - Open the email → click on the three dots (⋮) → select *Show original*.  
  - Copy the entire header text.  

<img width="1366" height="768" alt="Screenshot (35)" src="https://github.com/user-attachments/assets/9a70392b-ff8a-450c-857d-b99a314f0cb4" />

---

### Step 2: Use a Mail Header Analyzer
- Go to an online tool such as *MXToolbox Email Header Analyzer*.  
- Paste the copied email header into the input box and click *Analyze*.  

<img width="1366" height="768" alt="Screenshot (36)" src="https://github.com/user-attachments/assets/dea4065c-090e-475e-9774-780c0b49471e" />

- The tool will generate a structured, easy-to-read analysis report.  

---

### Step 3: Review the Analysis Report  

#### 1. Delivery Summary  
- *DMARC Compliance:* ✅ Passed (email considered authentic at a high level).  
- *SPF Check:* ✅ Both SPF Authentication and Alignment passed.  
- *DKIM Check:* ❌ DKIM Alignment passed, but *DKIM Authentication failed* (critical issue).  

<img width="1366" height="768" alt="Screenshot (37)" src="https://github.com/user-attachments/assets/6bf4f7fc-095f-4cc4-aaca-6e7db67e0c09" />

---

#### 2. Investigating SPF Record and Email Path  
- *SPF Record:* v=spf1 include:mailgun.org ~all  
  - This means the domain authorizes Mailgun servers to send emails on its behalf.  

- *Relay Path:* The email originated from m241-136.mailgun.net (a Mailgun server).  

✅ *Conclusion:* Since the email came from an authorized Mailgun server, the SPF check passed successfully.  

<img width="1366" height="768" alt="Screenshot (38)" src="https://github.com/user-attachments/assets/4ce25289-c359-46ee-95f6-64f868223472" />

---

#### 3. Analyzing the DKIM Failure  
- *What happened:*  
  - DKIM Alignment passed → the header information matches the sending domain.  
  - DKIM Authentication failed ❌ → the digital signature could not be verified.  

- *Possible reasons for failure:*  
  1. The email content was altered after signing (even minor changes break DKIM).  
  2. Misconfigured DKIM records in DNS.  
  3. Expired or invalid cryptographic key.  
  4. Forwarding services that modified the message body or headers.  

- *Implication:*  
  - The failed DKIM check raises suspicion. Even though SPF and DMARC passed, DKIM failure indicates the possibility of tampering or misconfiguration.  
  - Security analysts must verify whether this failure is a technical misconfiguration or a sign of spoofing.  

<img width="1366" height="768" alt="Screenshot (39)" src="https://github.com/user-attachments/assets/eb8c84aa-dfc5-445d-9f98-99044e3c2143" />

<img width="1366" height="768" alt="Screenshot (40)" src="https://github.com/user-attachments/assets/e4336f01-cd46-4495-9b35-e6f20edc06b5" />

---

## Final Conclusion  
- *SPF Passed* → The sending server was authorized.  
- *DMARC Passed* → The email is considered compliant overall.  
- *DKIM Failed* → A critical red flag that requires investigation.  

👉 The email is *not fully trustworthy. While SPF and DMARC confirm legitimacy at the server level, the DKIM failure shows that the **message integrity could have been compromised*.  

<img width="1366" height="768" alt="Screenshot (41)" src="https://github.com/user-attachments/assets/cee95def-a875-4554-b7d0-0a6196f77824" />
