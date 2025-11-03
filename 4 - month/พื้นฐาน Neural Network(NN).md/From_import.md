# 📘 สรุปโมเดลจำแนก (Classification) vs ค่าต่อเนื่อง (Regression)

---

## 🔍 ความแตกต่างหลัก

| ประเภท | ใช้เมื่อผลลัพธ์เป็น | ตัวอย่างคำตอบ | โมเดลที่ใช้ | Metrics ที่ใช้ |
|----------|----------------------|----------------|---------------|----------------|
| 🧩 Classification | หมวดหมู่ (Discrete) | 0/1, Yes/No, Pass/Fail | LogisticRegression, DecisionTreeClassifier, RandomForestClassifier, KNeighborsClassifier | accuracy_score, classification_report, confusion_matrix |
| 📈 Regression | ค่าต่อเนื่อง (Continuous) | 23.5, 1000, 45.8 | LinearRegression, DecisionTreeRegressor, RandomForestRegressor | mean_absolute_error, mean_squared_error, r2_score |

---

## 🧩 1️⃣ ตัวอย่างโมเดลจำแนก (Classification)

### โจทย์:
> ทำนายว่า **ผู้ป่วยมีโรคหัวใจหรือไม่**  
> (0 = ไม่มีโรค, 1 = มีโรค)

```python
# ==== Import Libraries ====
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import accuracy_score, classification_report, confusion_matrix
#แบบจำแนก
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_absolute_error, mean_squared_error, r2_score #แบบเลขค่าต่อเนื่อง

# ==== ตัวอย่างข้อมูล ====
data = {
    'Age': [25, 32, 47, 51, 62, 40, 29],
    'BMI': [22.4, 28.1, 31.2, 24.9, 27.3, 26.4, 23.1],
    'Exercise': [3, 1, 0, 2, 1, 3, 4],
    'HeartDisease': [0, 1, 1, 0, 1, 0, 0]
}

df = pd.DataFrame(data)

# ==== แยก Features และ Target ====
X = df[['Age', 'BMI', 'Exercise']]
y = df['HeartDisease']

# ==== แบ่งชุดข้อมูล ====
X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.3, random_state=42)

# ==== สร้างและฝึกโมเดล ====
model = LogisticRegression(max_iter=200)
model.fit(X_train, y_train)

# ==== ทำนายผล ====
y_pred = model.predict(X_test)

# ==== ประเมินผล ====
print("✅ Accuracy:", accuracy_score(y_test, y_pred))
print("\nClassification Report:\n", classification_report(y_test, y_pred))
print("\nConfusion Matrix:\n", confusion_matrix(y_test, y_pred))
