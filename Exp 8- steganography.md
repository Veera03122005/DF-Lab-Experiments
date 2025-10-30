#  Ex.No.8 — Detect Hidden Data in Images Using StegExpose

---

##  Aim

To detect hidden data in image files using **StegExpose**, a steganography analysis tool.

---
## Procedure
---

##  Step 1 — Compile the Source Code

Compile the Java files with the required dependency:

```bash
javac -cp commons-math3-3.1.1.jar -source 1.8 -target 1.8 *.java
```
<p allign=center>
<img width="1362" height="181" alt="image" src="https://github.com/user-attachments/assets/63664843-3853-4a80-9b22-31ea72b4a717" />
</p>

 Note: Ignore warnings like `RSAnalysis.java uses unchecked or unsafe operations`. Compilation is successful if `.class` files are generated.

---

##  Step 2 — Create the Executable JAR
By using Notepad
Create a file named `manifest.mf` in the same folder:

```
Main-Class: StegExpose
```
<p align=center>
<img width="400" alt="exp8 4" src="https://github.com/user-attachments/assets/dcebf216-9a39-4b63-a93f-58a2a15371d4" />
</p>

Build the JAR:

```bash
jar cfm StegExpose.jar manifest.mf *.class
```

 You now have `StegExpose.jar` ready to use.

---

##  Step 3 — Run StegExpose

```bash
java -jar StegExpose.jar "E:\StegExpose-master\StegExpose-master\testFolder"
```

---

##  Step 4 — Example Output
<p align=center>
<img width="1131" height="97" alt="image" src="https://github.com/user-attachments/assets/87be2baf-09e1-4f11-8583-aac729d911e0" />
</p>

| Hidden Bytes   | Meaning                             |
| -------------- | ----------------------------------- |
| < 10,000       | Likely clean (no hidden data)       |
| 10,000–100,000 | Possibly contains hidden data       |
| > 100,000      | Highly likely steganography present |

---

## Step 5 — Analyze and Verify Results

The tool lists images with potential hidden data and estimates the approximate size. Further validation can be done using tools such as:

* StegSolve
* OpenStego
* zsteg
* Binwalk

---

##  Optional — Export Results Automatically

Generate a results file for easier review:

```bash
java -jar StegExpose.jar "E:\StegExpose-master\StegExpose-master\testFolder" fast 0.3 results.csv

```
<p align=center>
<img width="600" alt="exp8 6" src="https://github.com/user-attachments/assets/ceed7805-db8f-4ba4-8cf6-2542eb29c8f0" />
</p>

---
<p align=center>
<img width="600" alt="exp8 7" src="https://github.com/user-attachments/assets/bef42a3d-3390-4709-a5f6-41339d2065e5" />
</p>

# Rubrics
  
  | Criteria | Mark Allotted | Mark Awarded |
  |---|---:|---:|
  | 1. GitHub Activity & Submission Regularity | 3 | |
  | 2. Application of Forensic Tools & Practical Execution | 3 | |
  | 3. Documentation & Reporting | 2 | |
  | 4. Engagement, Problem-Solving & Team Collaboration | 2 | |
  | *Total* | *10* | |




## Result

* Successfully compiled and executed StegExpose
* Detected images containing potential hidden data
* Interpreted results and exported findings

Hidden data in image files was successfully detected using StegExpose
