# 🎓 Students Performance Analysis and Score Prediction

This project analyzes a student performance dataset from Kaggle and builds a basic machine learning model to predict students' mean scores based on various categorical features such as gender, ethnicity, lunch type, parental education, and test preparation course.

---

## 📌 Author
**Sowmiya Boopathi**

---

## 📂 Dataset
**Source**: [Kaggle - Students Performance in Exams](https://www.kaggle.com/datasets/spscientist/students-performance-in-exams)

**File used**: `StudentsPerformance.csv`

**Features**:
- Gender
- Race/Ethnicity
- Parental level of education
- Lunch type (standard / free-reduced)
- Test preparation course (completed / none)
- Math score
- Reading score
- Writing score

---

## 🧪 Key Steps

### 🔍 Data Exploration & Cleaning
- Loaded dataset with Pandas.
- Calculated basic statistics (mean, std, min, max).
- Created a new feature: `mean score` by averaging math, reading, and writing scores.
- Applied **Label Encoding** to categorical features.

### 📊 Visualizations
Used `matplotlib` and `seaborn` for insights:
- Gender vs Race distribution.
- Pie chart for test preparation.
- Barplots for:
  - Test preparation course vs Mean score
  - Lunch type vs Mean score
  - Parental education vs Mean score
- Heatmap to visualize correlations.
- Pairplot for multivariate relationships.

### 🧹 Preprocessing
Dropped individual scores after calculating `mean score` to simplify the model.

### 🤖 Model Building
- Used **Logistic Regression** (although this is typically for classification; used here as a regression-like model).
- Train-Test Split: 80/20.
- Evaluated performance using average prediction error.

---

## 📈 Results

| Metric | Value |
|--------|-------|
| Model  | Logistic Regression |
| Avg. Prediction Error | ≈ **11.03 marks** |

> ✅ Students who **completed the test preparation course**, had **standard lunch**, and whose parents had a **higher education level** tended to perform better.

---

## ⚙️ Dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
