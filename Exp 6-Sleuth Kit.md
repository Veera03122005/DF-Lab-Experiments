#  **Experiment No. 06 — Digital Forensic Analysis using Sleuth Kit (TSK)**

## Description

The Sleuth Kit (TSK) is a collection of command-line tools that allow you to analyze disk images and recover digital evidence. Here's a step-by-step guide to using Sleuth Kit on a Windows machine to analyze digital evidence


---

##  **Step 1: Installing Sleuth Kit**

1. **Download the Tool:**  
   - Head over to the official Sleuth Kit page or use this link:
   - ## ![WhatsApp Image 2025-10-30 at 22 23 07_58058664](https://github.com/user-attachments/assets/8c32a68a-9a38-4885-9aec-b5165aaaacab)

   - Choose the latest stable **Windows-compatible** version.

2. **Installation Process:**  
   - Run the installer and follow the setup wizard .  
   - Once done, TSK will be ready to use on your system!

---

##  **Step 2: Acquire the Disk Image**

Before analysis, a **forensic disk image** (a perfect bit-by-bit copy) of the device is needed.

1. **Create Disk Image:**  
   - Use tools like **FTK Imager**  or **`dd`** to create an exact copy.  
   - Save it in a TSK-supported format: `.dd`, `.raw`, `.img`, or `.E01`.

2. **Sample Evidence Files:**  
   - For this lab, download the following from the provided link:  
      `4Dell Latitude CPi.E01`  
      `4Dell Latitude CPi.E02`

---

##  **Step 3: Mounting the Disk Image (Optional)**

Mounting lets you access the disk image as if it were a normal drive.

- Use **OSFMount**  to mount the image in **read-only mode**.  
-  *Note: This is optional but helps when browsing the file system.*

---

## **Step 4: File System Analysis with TSK**

Now let’s dive into Sleuth Kit tools to inspect the file system.

### Navigate to the TSK Directory

```bash
```
  
## image 2

---

###  Identify File System Type

```bash
```
 
## image 3


 *Displays key details about the file system type and structure.*

---

### View Partition Layout

```bash
```
  
# image 4

 *Lists all partitions and their respective start/end addresses.*

---

###  List Files and Directories

```bash
```
  
# image5

 *Recursively lists files and folders with their inode details.*

---

###  Recover Deleted Files

```bash
```
 
# image6


 *Recovers a deleted or existing file by its inode number.*

---

## **Step 5: Metadata Analysis**

To uncover file history and access details, view the file’s metadata.

```bash
```
 
# image7

 *Displays file attributes such as MAC times (Modified, Accessed, Changed), size, and allocation info.*

---


## **Step 6: Report Generation**

After completing your analysis:

1. **Compile All Outputs:**  
   Collect files like `filesystem_info.txt`, `partitions.txt`, `file_list.txt`, and `timeline.txt`.

2. **Interpret and Document:**  
   Write a clear summary explaining your findings, methods used, and any key recovered evidence.

---

## **Step 7: Evidence Preservation**

Ensuring the integrity of evidence is the final and most important step .

1. **Archive Evidence Securely:**  
   Use encryption  and hashing  to store your disk image and findings.

2. **Maintain Chain of Custody:**  
   Keep the evidence in a secure location following proper forensic protocols .

---

## **Result**

Using the **Sleuth Kit (TSK)**, investigators can efficiently extract, analyze, and preserve digital evidence .  
It remains one of the most reliable and open-source forensic toolkits for digital investigation .
