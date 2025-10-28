# Ex.No.8 — Use StegExpose to Detect Hidden Data in Images

---

## 📝 Description
**StegExpose** is a specialized tool used for **steganography analysis**. It works by evaluating the **statistical properties** of an image to estimate the probability of hidden data being embedded within it. This process helps forensic investigators detect steganography techniques like Least Significant Bit (LSB) embedding.

---

## 🛠️ Requirments

- ** Java Runtime Environment (JRE):** StegExpose is a Java-based application and requires JRE to run.
- ** StegExpose Tool:** Download the latest `.jar` file from the official StegExpose GitHub repository.

---

## 📋 Step-by-Step Process

### Step 1: Download and Set Up StegExpose

**🎯 Purpose:** Set up the StegExpose environment for steganography detection.

**📋 Instructions:**
1. ** Download the tool:** Obtain the `StegExpose.jar` file from the GitHub repository.
2. ** Install Java:** Ensure JRE is installed on your machine.
3. ** Prepare environment:** Place the `StegExpose.jar` file in a dedicated working folder.

<details>
<summary>📂 View Setup Environment</summary>
<p align="center">
</p>
</details>

---

### Step 2: Select Images for Analysis

**🎯 Purpose:** Prepare suspect images for steganographic analysis.

**📋 Instructions:**
- Collect the images you suspect might contain hidden data.
  StegExpose supports common image formats such as **.png**, **.jpg**, and **.bmp**.

<details>
<summary>🖼️ View Image Selection</summary>
<br>
<p align="center">
</p>
</details>

---

### Step 3: Open  Terminal

**🎯 Purpose:** Access the command line interface for running StegExpose.

**📋 Instructions:**
- 💻 Navigate to the folder where the `StegExpose.jar` file is located using your Command Prompt (Windows) or Terminal (Linux/macOS).

<details>
<summary>🖥️ View Command Line Navigation</summary>
<br>
<p align="center">
</p>
</details>

---

### Step 4: Run StegExpose on an Image

**🎯 Purpose:** Execute steganographic analysis on a single image file.

**💻 Command Structure:**
```bash
java -jar StegExpose.jar <image_file_path>
```

**📄 Example:**
```bash
java -jar StegExpose.jar test_image.png
```

---

### Step 5: Analyze the Output

**🎯 Purpose:** Interpret the steganographic analysis results.

📊 StegExpose calculates a **"suspect" score** ranging from 0 to 1. **The higher the score, the more likely steganography is present.**

**🎯 Threshold Values:**

| Score Range | Interpretation (Suggested Thresholds) |
| :---: | :--- |
| ** Less than 0.2** | Image is considered **clean** (no hidden data detected). |
| ** 0.2 - 0.3** | **Possibly** some hidden data is present. |
| ** Above 0.3** | **Likely** that steganography is present. |

**📄 Example Output Analysis:**
```bash
java -jar StegExpose.jar suspect_image.png
```
```makefile
Analyzing suspect_image.png...
Result: 0.4
Steganography likely present
```

<details>

<p align="center">
</p>
</details>

<details>

<p align="center">
</p>
</details>

---

### Step 6: Batch Analysis (Multiple Images)

**🎯 Purpose:** Analyze multiple images simultaneously for efficiency.

**📁 To check multiple images at once, specify the folder path containing the images:**

**💻 Command Structure:**
```bash
java -jar StegExpose.jar <folder_path>
```

**📄 Example:**
```bash
java -jar StegExpose.jar Images_to_Analyze
```

---

### Step 7: Advanced Options (Optional)

**🎯 Purpose:** Access additional StegExpose parameters and settings.

**❓ To view additional parameters, such as options for adjusting detection sensitivity or output verbosity, use the `--help` flag:**

**💻 Command:**
```bash
java -jar StegExpose.jar --help
```

---

### Step 8: Review the Results

**🎯 Purpose:** Evaluate analysis results and determine next steps.

**📋 Instructions:**
- 📊 Review the scores generated for each image
- 🎯 Use the threshold values to determine which images require further forensic investigation
- 🔍 Flag images with high suspect scores for detailed steganographic extraction

---

## ✅ Result

The hidden data within the image was successfully detected using StegExpose. The analysis revealed that images with a suspect score above the threshold likely contain embedded steganographic content, confirming the tool's effectiveness in steganography detection.


---




