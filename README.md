# Social-Spam Account Detection Using Apache Spark & PySpark

<p align="center">
  <strong>INT 315 — Cluster Computing Project</strong>
</p>

<p align="center">
  Big Data Analytics | Machine Learning | Social Media Spam Detection
</p>

---

## 📌 Overview

Social media platforms generate large volumes of user activity, making the identification of spam accounts an important data analytics problem.

**Social-Spam Account Detection Using Apache Spark and PySpark** is an academic project that explores how data processing and machine learning techniques can be used to classify labeled social media accounts as spam or non-spam.

The project involves dataset exploration, data preprocessing, feature engineering, exploratory data analysis, model training, and evaluation. It uses Apache Spark and PySpark ML for classification experiments, alongside selected scikit-learn baseline models.

## 🎯 Objectives

- Analyze social media user and account activity data.
- Explore and preprocess datasets for machine learning.
- Investigate relationships between account activity features.
- Apply machine learning classification algorithms using PySpark.
- Evaluate and compare model performance using recorded metrics.
- Understand the practical application of Apache Spark in data analytics.

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Data processing and model development |
| Apache Spark 3.5.9 | Data processing framework |
| PySpark ML | Machine learning classification |
| Pandas | Data inspection and preprocessing |
| scikit-learn | Baseline model experiments |
| Matplotlib | Data visualization |
| Jupyter Notebook | Interactive development and analysis |
| Visual Studio Code | Development environment |
| Java 8 | Runtime environment for Spark |

## 📊 Dataset

This project uses the **MicroblogPCU dataset** from the UCI Machine Learning Repository.

**Official source:** [MicroblogPCU — UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/323/microblogpcu)

The dataset includes four CSV files containing user information, posts, user-post records, and follower-followee relationships.

| Dataset | Records | Columns |
|---|---:|---:|
| `follower_followee.csv` | 142,368 | 10 |
| `post.csv` | 35 | 11 |
| `user_post.csv` | 48,813 | 9 |
| `weibo_user.csv` | 781 | 10 |

*Record counts exclude header rows.*

### Target label encoding

For supervised classification, the original labels are mapped as follows:

| Original label | Encoded label | Meaning |
|---|---:|---|
| `1` | `1` | Spam |
| `-1` | `0` | Non-spam |

Only records with usable spam/non-spam labels are included in supervised classification. Unlabeled records are not assumed to be non-spam.

## ⚙️ Methodology

The project follows a structured machine learning workflow:

1. **Environment configuration:** Set up Java, Apache Spark, and PySpark.
2. **Data loading:** Load the CSV datasets and examine their structure.
3. **Data quality checks:** Inspect missing values, duplicate records, and relevant data types.
4. **Data preprocessing:** Prepare the data for analysis and classification.
5. **Exploratory data analysis:** Examine account activity and correlations between numerical features.
6. **Feature engineering:** Prepare account activity and gender-related features.
7. **Model development:** Train selected machine learning classifiers.
8. **Model evaluation:** Measure classification accuracy and inspect predictions.
9. **Result analysis:** Interpret the findings and identify limitations.

## 🤖 Machine Learning Models

### PySpark ML classifiers

- Logistic Regression
- Decision Tree Classifier
- Naive Bayes Classifier

### Additional baseline experiments

- Scikit-learn Logistic Regression
- Scikit-learn Decision Tree
- Linear Regression as an exploratory regression experiment

Linear Regression was an additional experiment, not the primary spam-classification model.

## 📈 Results and Evaluation

The following results were recorded in the project notebook.

### PySpark ML results

| Model | Accuracy |
|---|---:|
| Logistic Regression | 70.83% |
| Decision Tree Classifier | 68.75% |
| Naive Bayes Classifier | **75.00%** |

### Scikit-learn baseline results

| Model | Accuracy |
|---|---:|
| Logistic Regression | 71.11% |
| Decision Tree Classifier | 75.56% |

### Key observations

- PySpark Naive Bayes achieved **75.00% accuracy** in its recorded evaluation.
- The scikit-learn Decision Tree achieved **75.56% accuracy** in a separate evaluation.
- The two experiments used different train/test splits, so their accuracy values are not a direct comparison on identical test records.
- The available labeled subset is limited, which affects how confidently the results can be generalized.
- The recorded metrics represent experimental results rather than a guarantee of real-world detection performance.

## 📉 Limitations

- A substantial portion of the user records has no usable classification label.
- The supervised classification experiments use a relatively small labeled subset.
- Model performance can vary depending on data splits, features, and preprocessing.
- The recorded results do not establish production-level spam detection performance.
- Further validation on larger, representative labeled datasets is needed before real-world deployment.

## 🚀 Getting Started

### Prerequisites

The development environment used for this project includes:

- Python 3.10.11
- Java 8
- Apache Spark / PySpark 3.5.9
- Jupyter Notebook or Visual Studio Code

Other compatible environments may require configuration changes.

### 1. Clone the repository

Replace `YOUR-USERNAME` with your GitHub username.

```bash
git clone https://github.com/YOUR-USERNAME/Social-Spam-Detection.git
cd Social-Spam-Detection
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Activate it on Windows using PowerShell:

```powershell
.\venv\Scripts\Activate.ps1
```

Or use Command Prompt:

```bat
venv\Scripts\activate
```

### 3. Install dependencies

If the repository includes a `requirements.txt` file:

```bash
pip install -r requirements.txt
```

Otherwise, install the primary Python dependencies:

```bash
pip install pyspark==3.5.9 pandas matplotlib scikit-learn jupyter
```

Ensure that Java and Spark are configured correctly for your system.

### 4. Run the notebook

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open `social_spam_analysis.ipynb` and execute the cells in sequence.

**Note:** Update any local Windows file paths in the notebook to match the location of your downloaded or cloned repository.

## 🔮 Future Improvements

- Increase the quantity and quality of labeled training data.
- Use stratified cross-validation for more reliable evaluation.
- Evaluate precision, recall, F1-score, and confusion matrices consistently.
- Explore additional behavioral features and feature-selection techniques.
- Test models on unseen and representative data.
- Investigate performance on larger Spark workloads where appropriate.

## 📚 References

1. [UCI Machine Learning Repository — MicroblogPCU](https://archive.ics.uci.edu/dataset/323/microblogpcu)
2. [Apache Spark 3.5.9 Documentation](https://spark.apache.org/docs/3.5.9/)
3. [PySpark ML Programming Guide](https://spark.apache.org/docs/3.5.9/ml-guide.html)
4. [scikit-learn Documentation](https://scikit-learn.org/stable/)

## 🎓 Academic Information

| Field | Details |
|---|---|
| Project Title | Social-Spam Account Detection Using Apache Spark and PySpark |
| Course Code | INT 315 |
| Course Name | Cluster Computing |
| Program | B.Tech Computer Science and Engineering — Data Science |
| Institution | Lovely Professional University |

---

*Developed as an academic project to explore big-data processing, machine learning, and social media spam account classification using Apache Spark and PySpark.*
