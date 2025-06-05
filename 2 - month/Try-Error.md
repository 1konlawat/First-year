
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




# Python: `try-except-finally` Example

## โค้ดเต็มๆ:

```python
def divide_numbers():
    try:
        # รับค่าเลขจากผู้ใช้
        num1 = int(input("Enter the first number: "))
        num2 = int(input("Enter the second number: "))

        # ทำการหาร
        result = num1 / num2

    except ValueError as ve:
        # ถ้าผู้ใช้ป้อนข้อมูลไม่ใช่ตัวเลข
        print(f"Invalid input. Please enter valid numbers. Error: {ve}")

    except ZeroDivisionError as zde:
        # ถ้าเกิดการหารด้วยศูนย์
        print(f"Cannot divide by zero. Error: {zde}")

    except Exception as e:
        # ใช้จับข้อผิดพลาดอื่นๆ ที่ไม่ได้ระบุไว้
        print(f"An unexpected error occurred: {e}")

    else:
        # ถ้าไม่มีข้อผิดพลาด
        print(f"The result is: {result}")

    finally:
        # ทำงานเสมอไม่ว่าเกิดข้อผิดพลาดหรือไม่
        print("Execution completed.")

# เรียกฟังก์ชัน
divide_numbers()
```

## คำอธิบาย:

1. **`try`**: รับข้อมูลจากผู้ใช้และทำการหาร
2. **`except ValueError as ve`**: ถ้าผู้ใช้ป้อนข้อมูลที่ไม่ใช่ตัวเลข (เช่น "abc")
3. **`except ZeroDivisionError as zde`**: ถ้าผู้ใช้ป้อน `0` เพื่อหาร
4. **`except Exception as e`**: จับข้อผิดพลาดอื่นๆ ที่ไม่ได้ระบุไว้
5. **`else`**: ถ้าไม่มีข้อผิดพลาดใน `try` จะพิมพ์ผลลัพธ์
6. **`finally`**: ทำงานเสมอไม่ว่าจะมีข้อผิดพลาดหรือไม่
