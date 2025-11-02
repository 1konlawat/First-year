# 🧠 ขั้นตอนสร้างโมเดล Titanic (Model Building Example)

## 1. นำเข้าไลบรารีที่จำเป็น

``` python
import pandas as pd
from sklearn.model_selection import train_test_split
from sklearn.preprocessing import LabelEncoder, StandardScaler
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import accuracy_score, confusion_matrix, classification_report
```

## 2. โหลดข้อมูล

``` python
df = pd.read_csv('titanic.csv')
print(df.head())
```

## 3. เลือกเฉพาะคอลัมน์ที่ใช้

``` python
features = ['Pclass', 'Sex', 'Age', 'SibSp', 'Parch', 'Fare']
target = 'Survived'
df = df[features + [target]]
```

## 4. จัดการค่าที่หาย (Missing Values)

``` python
df['Age'] = df['Age'].fillna(df['Age'].median())
```

## 5. เข้ารหัสข้อมูลที่เป็นข้อความ (Categorical Encoding)

``` python
le = LabelEncoder()
df['Sex'] = le.fit_transform(df['Sex'])
```

## 6. แบ่งข้อมูลเป็น X (features) และ y (target)

``` python
X = df[features]
y = df[target]
```

## 7. แบ่งข้อมูล train/test

``` python
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)
```

## 8. สเกลข้อมูล (Feature Scaling)

``` python
scaler = StandardScaler()
X_train = scaler.fit_transform(X_train)
X_test = scaler.transform(X_test)
```

## 9. สร้างและฝึกโมเดล (Train Model)

``` python
model = LogisticRegression()
model.fit(X_train, y_train)
```

## 10. ทำนายผล (Prediction)

``` python
y_pred = model.predict(X_test)
```

## 11. ประเมินผล (Evaluation)

``` python
print("✅ Accuracy:", accuracy_score(y_test, y_pred))
print("\n📊 Confusion Matrix:\n", confusion_matrix(y_test, y_pred))
print("\n📈 Classification Report:\n", classification_report(y_test, y_pred))
```

## 12. บันทึกโมเดลไว้ใช้งานต่อ (Save Model)

``` python
import joblib
joblib.dump(model, 'titanic_model.pkl')
joblib.dump(scaler, 'scaler.pkl')
print("\n💾 Model and Scaler saved successfully!")
```

------------------------------------------------------------------------

### ✅ สรุปสิ่งที่โค้ดนี้ทำ

  ขั้นตอน   รายละเอียด
  --------- ---------------------------------------------
  1--2      โหลดและตรวจสอบข้อมูล Titanic
  3--5      เตรียมข้อมูล (เลือกคอลัมน์, fillna, encode)
  6--8      แบ่ง train/test และสเกลข้อมูล
  9--10     สร้างโมเดล Logistic Regression และทำนาย
  11        ประเมินผลด้วย Accuracy, Confusion Matrix
  12        บันทึกโมเดลไว้ใช้งานภายหลัง
