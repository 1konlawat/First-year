
# Python: `try-except-finally`

## การใช้งาน `try-except`

`try-except` ใช้เพื่อจัดการข้อผิดพลาดที่อาจเกิดขึ้นในโปรแกรม โดยไม่ให้โปรแกรมหยุดทำงาน

### ตัวอย่าง:
```python
try:
    x = int(input("Enter a number: "))
    print(10 / x)
except ValueError:
    print("That's not a valid number!")
except ZeroDivisionError:
    print("Cannot divide by zero!")
```

ในกรณีที่ผู้ใช้ป้อนค่าที่ไม่ใช่ตัวเลข โปรแกรมจะเข้าไปที่ `except ValueError` และถ้าผู้ใช้ป้อน `0` โปรแกรมจะเข้าไปที่ `except ZeroDivisionError`

---

## การใช้หลายๆ `except`

สามารถใช้หลาย `except` เพื่อจัดการกับข้อผิดพลาดหลายประเภท
### ตัวอย่าง:
```python
try:
    x = int(input("Enter a number: "))
    print(10 / x)
except ValueError:
    print("That's not a valid number!")
except ZeroDivisionError:
    print("Cannot divide by zero!")
```

---

## การใช้ `finally`

`finally` จะทำงานเสมอหลังจาก `try` และ `except` ไม่ว่าจะเกิดข้อผิดพลาดหรือไม่

### ตัวอย่าง:
```python
try:
    x = 1 / 0  # จะเกิดข้อผิดพลาด
except ZeroDivisionError:
    print("Cannot divide by zero!")
finally:
    print("This will always run.")
```

ในกรณีนี้แม้จะเกิดข้อผิดพลาดจากการหารด้วย 0 แต่ `finally` ก็ยังทำงาน
