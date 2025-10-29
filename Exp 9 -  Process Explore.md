# 🧪 Ex.No.9 — Using Procmon to Identify Suspicious Processes

## 🎯 Aim
To monitor and identify suspicious process activities in a Windows system using **Procmon (Process Monitor)**.

---

## ⚙️ Procedure

1. **📥 Download and Extract Procmon**  
   - Obtain *Process Monitor* from the official Microsoft Sysinternals website.  
   - Extract the downloaded ZIP file.

2. **🛠️ Run Procmon as Administrator**  
   - Right-click `Procmon.exe` → *Run as Administrator* to grant system-level access.  
   <p align="center">
   </p>

3. **▶️ Start Capture**  
   - Click the **Capture Events (Ctrl + E)** icon to begin monitoring.  
   <p align="center">
   </p>

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
   </p>

7. **📊 Analyze Captured Events**  
   - Use the **Process Tree** view to inspect parent-child relationships.  
   - Look for abnormal file writes, registry modifications, or process spawns.  
   - Export relevant events as a `.CSV` file for documentation.  
   <p align="center">
   </p>

8. **🧹 Close Procmon**  
   - Stop monitoring and review saved logs for evidence of persistence, code injection, or other malicious indicators.

---

## ✅ Result
Successfully used **Procmon** to capture and analyze real-time system process activities.  
Suspicious processes performing abnormal operations — including registry edits, file writes, or unauthorized executions — were identified, revealing indicators of potential malicious behavior.

