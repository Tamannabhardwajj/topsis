# 🔵 TOPSIS Web Service & Command Line Implementation

This project implements the **Technique for Order of Preference by Similarity to Ideal Solution (TOPSIS)** as part of an academic assignment.  
The solution includes:

- ✅ **Command Line Interface (CLI)** implementation (Part-I)
- ✅ **Web Service** for TOPSIS calculation with file upload and email input (Part-III)

The implementation strictly follows all constraints and validations mentioned in the assignment.

---

## 📌 What is TOPSIS?

TOPSIS is a **Multi-Criteria Decision Making (MCDM)** technique used to rank alternatives based on their distance from:

- 🟢 **Ideal Best Solution**
- 🔴 **Ideal Worst Solution**

An alternative that is **closest to the ideal best** and **farthest from the ideal worst** is ranked higher.

---

## ⚙️ Methodology Used

The following steps are used to compute TOPSIS:

### **Step 1: Input Matrix**
- First column → Alternatives (A1, A2, A3, …)
- Remaining columns → Criteria values (numeric)

---

### **Step 2: Normalization**
To eliminate unit differences, vector normalization is applied:

rij = xij / √(Σxij²)


---

### **Step 3: Weighted Normalized Matrix**
Each normalized value is multiplied by its corresponding weight:

vij = rij × wj


---

### **Step 4: Ideal Best & Ideal Worst**
Based on the impact of each criterion:

| Impact | Ideal Best | Ideal Worst |
|------|------------|-------------|
| + | Maximum value | Minimum value |
| - | Minimum value | Maximum value |

---

### **Step 5: Distance Calculation**
Euclidean distance is calculated from:
- Ideal Best (S⁺)
- Ideal Worst (S⁻)

---

### **Step 6: TOPSIS Score**
The performance score is calculated as:

Ci = Si- / (Si+ + Si-)


A higher score indicates a better alternative.



### **Step 7: Ranking**
Alternatives are ranked in **descending order** of TOPSIS score.

### **Result Interpretation**
- The alternative with the **highest TOPSIS score** is the most preferred.
- Rankings help decision-makers choose the optimal option.

### Purpose:
- Visual comparison of alternatives
- Easy identification of best-performing option
- Better interpretability for decision-makers

### Python package(pypi)
https://pypi.org/project/Topsis-Tamanna-Bhardwaj-102303280/1.0.0/

## 💻 Command Line Usage
Run the program using the following command:

```bash
python topsis.py data.csv "1,1,1,2" "+,+,-,+" output.csv
