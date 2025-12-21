# 📘 Cogs 118A Final Project Requirements 

## 📅 Due Date

**Friday night of finals week**

**Late penalties:**

* 5% for first late day
* 10% for each additional day

## 👤 Team Policy

* Solo project (no teams).
* Custom project ideas require prior approval.

---

# 📄 Deliverables

## ✔ 1. Formal Written Report (>1000 words)

Include these sections:

1. Abstract
2. Introduction
3. Method
4. Experiment
5. Conclusion
6. References

Formatting options (any is fine):

* NeurIPS
* ICML
* ICLR
* Google Docs / Word

> Word count excludes references. No page limit.

---

## ✔ 2. Code

Submit all code for:

* Data loading
* Preprocessing
* Training
* Cross-validation
* Parameter search
* Evaluation

Python recommended, but any language is allowed.

---

## ✔ 3. Experimental Results

### Choose:

* **3 classifiers**
* **3 UCI datasets**

Same model with different kernels (e.g. SVM linear vs RBF) **does NOT** count as two classifiers.

### Required runs:

* 3 classifiers
* × 3 datasets
* × 3 dataset partitions:

  * 20% train / 80% test
  * 50% train / 50% test
  * 80% train / 20% test
* × 3 trials per partition

**Minimum total = 81 training/testing runs.**

### For each run, report:

* Training accuracy
* Validation accuracy
* Test accuracy
* Selected hyperparameters from cross-validation

---

# 🧪 Experiment Requirements

### Binary classification only

Merge multi-class labels into two groups (pos/neg).

### Hyperparameter tuning

Use cross-validation (any reasonable approach).

### Evaluation metric

* Accuracy is sufficient.

### Trends expected (not strict):

* Random Forest often best
* Kernel SVM sensitive to tuning
* KNN often okay
* More training data → higher accuracy

---

# ⚙️ Allowed Classifiers (pick any 3)

Examples:

* Boosting (AdaBoost, XGBoost)
* SVM
* Random Forest
* Decision Tree
* KNN
* Neural Networks (MLP)
* Logistic Regression
* Bagging

---

# 📊 Required Comparisons

### A. Compare classifiers (per dataset, per partition)

Show how the three chosen classifiers perform on each dataset.

### B. Compare partitions (per classifier)

Show how using more training data (20% → 50% → 80%) affects accuracy.

---

# 🎓 Grading (Summary)

* **10 pts** — Dataset size/challenge
* **10 pts** — Novelty / originality
* **50 pts** — Experimental design thoroughness
* **30 pts** — Report quality
* **Bonus** — Optional additions

---

# What to Submit

1. **Report** (1000+ words, all required sections)
2. **Code**
3. **Results tables/plots**
4. **Hyperparameters chosen via CV**
5. **Train/val/test accuracies for all runs (81 total)**

---

# ✔ Project Checklist 

### **Before We Start**

* [ ] Pick 3 UCI datasets
  - Must come from the UCI Machine Learning Repository.
  - Must be usable for binary classification
  - If originally multi-class → merge into two classes.
  - Must be large/complex enough to produce meaningful results.

(3) http://archive.ics.uci.edu/dataset/572/taiwanese+bankruptcy+prediction Taiwanese bankrupcy prediction 
(1) http://archive.ics.uci.edu/dataset/73/mushroom Predict if mushroom is poisonous or not 
(2) http://archive.ics.uci.edu/dataset/591/gender+by+name Gender by name 


* [ ] Pick 3 classifiers:
**Logistic Regression + RandomForest + KNN**

  - Choose 3 classifiers from those evaluated in the Caruana & Niculescu-Mizil study.
   - Different kernels of the same model (e.g., linear SVM vs RBF SVM) do NOT count as different classifiers.
   - Implementations must be reliable (e.g., scikit-learn, XGBoost, libsvm).
  - Each classifier must support hyperparameter tuning (via cross-validation).
  - For each classifier, you must produce results on all 3 datasets under all 3 partitions.

* [ ] Convert multi-class datasets → binary (if needed)

### **Data Prep**

* [ ] Load + clean datasets
* [ ] Standardize/normalize features (if needed)
* [ ] Implement train/test partitions (20/80, 50/50, 80/20)

### **Model Training**

For each classifier × dataset × partition:

* [ ] Run 3 trials with different splits
* [ ] Perform cross-validation
* [ ] Select best hyperparameters
* [ ] Record train/val/test accuracy
* [ ] Save final model performance

### **Results**

* [ ] Build tables comparing:

  * classifiers on each dataset
  * partitions for each classifier
* [ ] Include training vs validation comparisons
* [ ] Summarize trends

### **Report Writing**

* [ ] Abstract
* [ ] Introduction
* [ ] Method (classifiers, datasets, preprocessing, CV)
* [ ] Experiment (81 runs, results tables, analysis)
* [ ] Conclusion
* [ ] References
* [ ] (Optional) Bonus Points section

### **Final Submission**

* [ ] Report (PDF or doc)
* [ ] Code directory
* [ ] README.md (this file)

---

If you want, I can also generate:

* A **full report template** you can directly fill in
* Example **tables** for your results
* Recommended **UCI datasets + classifiers** that satisfy the project with minimal pain

Just let me know!
