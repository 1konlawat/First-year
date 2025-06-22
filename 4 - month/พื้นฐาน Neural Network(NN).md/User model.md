```python
import numpy as np
from tensorflow.keras.models import Sequential
from tensorflow.keras.layers import Conv2D, MaxPooling2D, Flatten, Dense
from tensorflow.keras.datasets import mnist
from tensorflow.keras.utils import to_categorical
from tensorflow.keras.optimizers import Adam

# โหลดข้อมูล MNIST (ตัวเลข 0-9)
(X_train, y_train), (X_test, y_test) = mnist.load_data()

# เตรียมข้อมูลให้เป็นแบบที่โมเดลสามารถใช้ได้
X_train = X_train.reshape((X_train.shape[0], 28, 28, 1)).astype('float32') / 255
X_test = X_test.reshape((X_test.shape[0], 28, 28, 1)).astype('float32') / 255

# แปลงค่า label ให้เป็น categorical (one-hot encoding)
y_train = to_categorical(y_train, 10)
y_test = to_categorical(y_test, 10)

# สร้างโมเดล CNN
model = Sequential()

# เพิ่มเลเยอร์ Convolutional และ MaxPooling
model.add(Conv2D(32, (3, 3), activation='relu', input_shape=(28, 28, 1)))
model.add(MaxPooling2D((2, 2)))

# เพิ่มเลเยอร์ Convolutional และ MaxPooling
model.add(Conv2D(64, (3, 3), activation='relu'))
model.add(MaxPooling2D((2, 2)))

# Flatten layer
model.add(Flatten())

# เพิ่ม Fully Connected layer
model.add(Dense(128, activation='relu'))

# Output layer
model.add(Dense(10, activation='softmax'))  # 10 classes (0-9)

# คอมไพล์โมเดล
model.compile(optimizer=Adam(), loss='categorical_crossentropy', metrics=['accuracy'])

# ฝึกโมเดล
model.fit(X_train, y_train, epochs=5, batch_size=64, validation_data=(X_test, y_test))

# เซฟโมเดล
model.save('/content/drive/MyDrive/colab/mnist_model.h5')

print("โมเดลฝึกเสร็จแล้วและบันทึกเป็น mnist_model.h5")
```

การนำไปใช้ไฟล์โมเดลต้องเป็นแบบ.h5 เท่านั้นไหมไม่รู้แต่ผมใช้แบบนั้น วิธีใช้คือ
1.อัปโหลดไฟล์ model ด้วยคำสั้ง(ย้ำไฟล์แบบ .h5)
```python
from google.colab import files
uploaded = files.upload()
```
2. load model user by code(ผมนำpathไม่ถูกน่ะขอบอกศึกษาเอาเอง)
3. ```python
   from tensorflow.keras.models import load_model
   โหลดโมเดลที่บันทึกไว้
   model = load_model('/content/drive/MyDrive/colab/mnist_model.h5')  # ปรับ path ให้ตรง
   ```


