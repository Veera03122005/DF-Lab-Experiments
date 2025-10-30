
#  Digital Forensics Lab – Experiment 1  
**Evidence Acquisition Using AccessData FTK Imager**  



Forensic Toolkit (FTK) is a computer forensics software product made by AccessData.  
It is a Windows-based commercial tool, with a free FTK Imager version (limited functionalities) used in forensic investigations.  

FTK Imager can acquire two types of evidence:  

- **Volatile memory (RAM)**  
- **Non-volatile memory (Hard disk)**  

There are two ways to use FTK Imager for forensic image acquisition:  

1. **FTK Imager Portable (USB/HDD):** Used in live data acquisition where the evidence system is running.  
2. **FTK Imager Installed on Investigator’s Laptop:** The source disk must be mounted via a **write blocker** to prevent modifications.  

---

##  Acquiring Volatile Memory (RAM)  

FTK Imager allows acquisition of complete volatile memory.  

**Steps:**  
1. Open FTK Imager → Navigate to **Capture Memory**.  

<p align="center">
  <img src="https://github.com/user-attachments/assets/3cc83afb-5fab-4ba5-98bb-2996c85541d1" width="600" />
</p>  

2. Select options (Pagefile, AD1 files).  

- **Pagefile.sys:** Windows uses this as virtual memory. It may contain valuable evidence.  
- **AD1 file:** FTK proprietary image format for storage and analysis.  

<p align="center">
  <img src="https://github.com/user-attachments/assets/75362f50-78d4-435a-95b3-272b62205a24" width="400" />
</p>  

3. Click **Capture Memory** → Acquisition starts.  

<p align="center">
  <img src="https://github.com/user-attachments/assets/bf6c825f-24b2-4850-8c40-e9dfcaac2ce7" width="400" />
</p>  

 Output: Acquired memory saved as **`.mem` file** in the destination folder.  

---

##  Acquiring Non-Volatile Memory (Disk Image)  

FTK Imager also supports disk image acquisition.  

**Steps:**  
1. Open FTK Imager → Navigate to **Create Disk Image**.  

<p align="center">
  <img src="https://github.com/user-attachments/assets/9407feb8-8385-418b-804d-d1c15350163c" width="600" />
</p>  

2. Select the source type:  
   - Physical Drives  
   - Logical Drives (partitions)  
   - Image files  
   - Folders  
   - CDs/DVDs  

<p align="center">
  <img src="https://github.com/user-attachments/assets/0190859b-c52a-4b8c-a080-a410fb99ce18" width="400" />
</p>  

3. Example – Select **Physical Drive** → Choose the drive → Click **Finish**.  

<p align="center">
  <img src="https://github.com/user-attachments/assets/411fea51-91f6-4894-a8ea-87d0dcc7ec95" width="400" />
</p>  

---

###  Supported Image Formats  

- **Raw (dd):** Common forensic format, no headers/metadata, ensures spatial integrity.  
- **SMART:** Linux-based, bitstream format with compression.  
- **E01:** Proprietary (EnCase), compressed with metadata + MD5 hash.  
- **AFF (AFF4):** Open format designed to avoid vendor lock-in.  

---

##  Case Details & Output  

- Enter case details.  
- Set **image destination, file name, and fragment size**.  

<p align="center">
  <img src="https://github.com/user-attachments/assets/eeacf3b7-9528-4d61-b8e0-b6048bd14d6a" width="400" />
</p>  

- **Fragment size 0:** Single image file (no splitting).  
- Select **Verify images after creation** → Ensures integrity by hashing.  

<p align="center">
  <img src="https://github.com/user-attachments/assets/60fb9e8c-5670-401c-ab0c-83fc2b884047" width="400" />
</p>  

- Click **Start** → Acquisition begins.  

<p align="center">
  <img src="https://github.com/user-attachments/assets/133d1d45-c2ce-4401-aa95-1c03d861d22f" width="400" />
</p>  

- Upon completion → Tool generates a **report text file** with all acquisition details.  

<p align="center">
  <img src="https://github.com/user-attachments/assets/6b3d6ff2-9e4c-45c2-9ab2-3fac8a74d410" width="400" />
</p> 

 
 
 ---
 
# Rubrics
 ---
  
  | Criteria | Mark Allotted | Mark Awarded |
  |---|---:|---:|
  | 1. GitHub Activity & Submission Regularity | 3 | |
  | 2. Application of Forensic Tools & Practical Execution | 3 | |
  | 3. Documentation & Reporting | 2 | |
  | 4. Engagement, Problem-Solving & Team Collaboration | 2 | |
  | *Total* | *10* | |
  ---
## Result
- Successfully captured RAM and disk images using FTK Imager, verified integrity with matching MD5 & SHA1 hashes.  
The acquired forensic images are ready for analysis using tools like Autopsy, FTK Toolkit, or Volatility.
