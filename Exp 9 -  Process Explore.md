# 🧪 Ex.No.9 — Using Procmon to Identify Suspicious Processes

## 🎯 Aim
To monitor and identify suspicious process activities in a Windows system using **Procmon (Process Monitor)**.

---

## ⚙️ Procedure

1. **📥 Download and Extract Procmon**  
   - Obtain *Process Monitor* from the official Microsoft Sysinternals website.  
   - Extract the downloaded ZIP file.
   
   <p align="center">
     <img src="https://github.com/user-attachments/assets/c1bdb2e5-9c0c-4251-b320-480d70d626e8" alt="Screenshot 1">
   </p>


2. **🛠️ Run Procmon as Administrator**  
   - Right-click `Procmon.exe` → *Run as Administrator* to grant system-level access.  
   <p align="center">
      <img width="907" height="525" alt="Screenshot 2025-10-29 141723" src="https://github.com/user-attachments/assets/d01f3106-16c5-4e53-828d-f2a8c65c2a8c" />
   </p>

3. **▶️ Start Capture**  
   - Click the **Capture Events (Ctrl + E)** icon to begin monitoring.  
   

4. **💻 Perform System Activity**  
   - Carry out normal or suspicious actions, such as running an unknown executable or accessing the registry.

5. **⏹️ Stop Capture**  
   - Click the **Capture** icon again or press `Ctrl + E` once enough data has been collected.

6. **🔍 Apply Filters**  
   - Go to **Filter → Filter...**  
   - Add relevant filters, for example:  
     - `Process Name contains suspicious.exe`  
     - `Operation contains WriteFile` or `CreateProcess`  
   <p align="center">
      <img width="596" height="355" alt="Screenshot 2025-10-29 142053" src="https://github.com/user-attachments/assets/4d83b981-490a-4d93-aaba-098ba8bbdaf4" />
   </p>

7. **📊 Analyze Captured Events**  
   - Use the **Process Tree** view to inspect parent-child relationships.  
   - Look for abnormal file writes, registry modifications, or process spawns.  
   - Export relevant events as a `.CSV` file for documentation.  


* Run a comprehensive antivirus scan.  
* Use malware removal tools (e.g., Malwarebytes or Windows Defender) for a thorough cleanup.
  <p>All system and user processes were successfully displayed with their respective CPU and memory usage. Unsigned or abnormal processes were identified by verifying signatures and observing their file paths.</p>







    # Rubrics
  
  | Criteria | Mark Allotted | Mark Awarded |
  |---|---:|---:|
  | 1. GitHub Activity & Submission Regularity | 3 | |
  | 2. Application of Forensic Tools & Practical Execution | 3 | |
  | 3. Documentation & Reporting | 2 | |
  | 4. Engagement, Problem-Solving & Team Collaboration | 2 | |
  | *Total* | *10* | |
##  Result
 Thus, the analysis of suspicious processes using Process Explorer was performed successfully.

