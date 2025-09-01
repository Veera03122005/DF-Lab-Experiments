#  Digital Forensics Lab – Experiment 2  
**Recover Deleted or Damaged Files from a Storage Device using TestDisk**  

---

##  Aim  
To use **TestDisk** step by step to recover a missing partition and repair a corrupted one.  

---
  

### 1. Log Creation & Disk Detection  
When TestDisk starts, it creates a log file.  
All connected hard drives are detected and listed with their correct size.  
 Use the arrow keys to select the drive with the lost partition.  

<p align="center">
  <img src="https://github.com/user-attachments/assets/47d911ab-165b-4b0e-b0a9-359c6d58feac" width="700" />
</p>  

---

### 2. Partition Table Type Selection  
TestDisk auto-detects the **partition table type**.  
- Usually, the default value is correct.  
- Press **Enter** to proceed.  

<p align="center">
  <img src="https://github.com/user-attachments/assets/0d9dadff-25e2-4ca1-be7c-d99e49b72c5a" width="700" />
</p>  

---

### 3. Analyse Current Partition Structure  
Choose **Analyse** → TestDisk displays the current partition structure.  
- The first partition is listed twice → indicates corruption.  
- “Invalid NTFS boot” → faulty NTFS boot sector.  
- One logical partition is missing.  

Press **Quick Search** to continue.  

<p align="center">
  <img src="https://github.com/user-attachments/assets/13c71117-fc75-4ff2-91ca-3492fa64fd92" width="700" />
</p>  

---

### 4. Quick Search for Partitions  
Quick Search begins and TestDisk lists results in real-time.  
- Missing logical partition (Partition 3) is detected.  
- Press **p** to list files inside the partition.  
- Files in **red** are deleted entries.  

<p align="center">
  <img src="https://github.com/user-attachments/assets/6cff5e75-857d-460f-9aff-ba0356c15d7e" width="700" />
</p>  

---

### 5. Deeper Search (If Needed)  
If a partition is still missing → run **Deeper Search**.  
- TestDisk scans cylinder by cylinder.  
- It can detect FAT32, NTFS, ext2/ext3 backup boot sectors.  
- Some partitions may appear as **D (Deleted)** and overlap.  
- Use **p** to preview files in each partition to decide which is correct.  

<p align="center">
  <img src="https://github.com/user-attachments/assets/69fcdf1b-d5c2-4365-a454-949c01cd5b2d" width="700" />
</p>  

 If files are visible → mark the correct partition as **L (Logical)** or **P (Primary)**.  

---

### 6. Partition Table Recovery  
Once the correct partitions are identified:  
- Go to **Write** → Save the partition table.  
- Confirm with **Enter → Y → OK**.  
- TestDisk updates the partition structure.  

<p align="center">
  <img src="https://github.com/user-attachments/assets/2f522b97-7828-4516-a10a-0625f9c5e0b2" width="700" />
</p>  

---

### 7. NTFS Boot Sector Recovery  
If the NTFS boot sector is damaged but the backup is valid:  
- Choose **Backup BS** → copy backup boot sector over the corrupted one.  
- Now both boot sector and backup are identical → filesystem recovered.  

<p align="center">
  <img src="https://github.com/user-attachments/assets/9e248c1a-0e91-481e-8445-f7c7e65a1580" width="700" />
</p>  

 Finally, TestDisk prompts: **“Restart your Computer to access your data.”**  

---

