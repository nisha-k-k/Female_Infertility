# 🧬 Predicting Female Infertility Using Clustering and PCA-Based Classification
This notebook explores female infertility through the lens of machine learning. It focuses on two core questions:

*Can we identify subtypes of infertility based on shared condition patterns?*

*Is infertility better predicted by the number of conditions a person has—or which specific ones they have?*

## Why This Project? 
After my [PCOS project](https://github.com/nisha-k-k/PCOS) I wanted to dive deeper into female health topics, and infertility felt like the right next project. I am essentially creating a set of projects regarding female health, with the hopes of combining my findings to bring tangible help to the female-born population across the world. 

## 📊 Dataset Overview <br> 
The dataset can be accessed on Kaggle, [here](https://www.kaggle.com/datasets/fida5073/female-infertility) 

The dataset includes:

* One continuous feature: Age

* Multiple binary features indicating the presence or absence of infertility-related conditions

* A binary target: Infertility Prediction

The data consists of 705 female patients from Peshawar, Pakistan

## 📁 Project Structure
This notebook is organized into two main parts:

### Part 1: Clustering Analysis — Identifying Subtypes of Infertility
Using K-Prototypes clustering, patients were grouped into two distinct phenotypes:

Cluster 0: Younger individuals with more structural/surgical causes (e.g., previous reproductive surgeries)

Cluster 1: Older individuals with systemic or unclear causes (e.g., autoimmune disorders, unexplained infertility)

**PCA Reduced Clusters:** <br>

<img width="819" alt="Screenshot 2025-06-07 at 9 05 50 PM" src="https://github.com/user-attachments/assets/6bfcb906-d66a-4097-b041-776c714e583e" /> <br>

**Features in Clusters**: <br>
<img width="426" alt="Screenshot 2025-06-07 at 9 07 31 PM" src="https://github.com/user-attachments/assets/2b2321d7-324c-4e5d-8f04-bf024d2d287a" /> <br> 


### Part 2: Predictive Modeling — Which vs. How Many Conditions
To compare condition burden vs. specific condition patterns, two models were trained:

**Burden Model**: Based on a single feature representing the number of conditions a person has

**Full Model**: Based on all conditions, reduced using Principal Component Analysis (PCA) to prevent overfitting

💡 **Result**: The full PCA-based model outperformed the burden model (AUC 0.88 vs. 0.83), suggesting that specific combinations of conditions carry more predictive value than the total number.


#### Classification Report for All-Features Model:
<img width="625" alt="Screenshot 2025-06-07 at 9 09 09 PM" src="https://github.com/user-attachments/assets/c6889106-831d-4a33-8e47-fdecfe327a85" /> <br>

#### Classification Report for Burden-Only Model
<img width="661" alt="Screenshot 2025-06-07 at 9 10 41 PM" src="https://github.com/user-attachments/assets/b6cd0bae-b7bc-4cb9-ba8c-af7db36ffad5" />


#### 🔍 PCA Interpretation
Permutation importance was used to evaluate which principal components most influenced infertility prediction. The top contributors (PC1 & PC4) were mapped back to their original features to identify the condition groupings they represented:

PC1: Strongly associated with unexplained infertility, autoimmune disorders, and premature ovarian insufficiency

PC4: Driven by reproductive surgeries and endometriosis

<img width="1163" alt="Screenshot 2025-06-07 at 7 00 50 PM" src="https://github.com/user-attachments/assets/c0f4d4a1-216b-40d9-b79f-f2ede67e61aa" />


### 🎯 Key Takeaways
Clustering reveals meaningful phenotypes that could support more targeted fertility treatment approaches.

PCA-based models demonstrate that the nature of a patient’s condition matters more than just the number.

Feature mapping from PCA components offers clinical insights into complex infertility profiles.

### 📎 Notebook Link
Access the full notebook here: <br>
🔗 [female-infertility.ipynb](https://github.com/nisha-k-k/Female_Infertility/blob/main/female-infertility.ipynb)

### 🧠 Future Work
Because the dataset is realtively small (only about 705 rows; just over 500 when dropping duplicate rows for classification), I would like to dive into more data in addition to this dataset, in order to build an even better understanding of female infertility. Ideally, the data would be from places all across the world for a better, to get a better sample representation of the overall female population. In addition to this, I am considering expanding the project to dive into other questions, such as "Is 'Unexplained Infertility' TRULY Unexplained?". Like my PCOS project, I am looking into adding real-life patient testimonial data from online forums, like the 

🤝 Let's Connect
Questions or collaboration ideas? Reach out via [LinkedIn](https://www.linkedin.com/in/nisha-kaushal-748280175/) or GitHub!
