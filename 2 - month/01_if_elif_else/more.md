# Daily English Practice with Python (6 Detailed Exercises)

---

## Exercise 1: Country Check  
**ภาษาไทย:** ตรวจสอบว่ามาจากประเทศอะไร

**สถานการณ์:**  
ให้ผู้ใช้กรอกชื่อประเทศของตนเอง แล้วแสดงข้อความต้อนรับจากประเทศนั้น

**Input:**  
- ชื่อประเทศ

**Output:**  
- ข้อความต้อนรับจากประเทศนั้น

```python
country = input("Which country are you from? : ").strip().title()
print(f"Welcome from {country}!")
```

**Vocabulary**  
- country = ประเทศ (เคาน์-ทรี)  
- welcome = ยินดีต้อนรับ (เวล-คัม)  
- from = จาก (ฟรอม)  

---

## Exercise 2: Food Price Checker  
**ภาษาไทย:** เช็กราคาอาหารที่สั่ง

**สถานการณ์:**  
ผู้ใช้จะสั่งอาหาร ระบบจะถามชื่ออาหารและราคาที่ต้องจ่าย แล้วแสดงข้อความว่าราคาเท่าไหร่

**Input:**  
- ชื่ออาหาร  
- ราคาของอาหาร

**Output:**  
- แสดงข้อความว่าอาหารนี้ราคากี่บาท

```python
food = input("What food do you want to order? : ").strip().title()
price = float(input("How much does it cost? : "))
print(f"The price of {food} is {price} baht.")
```

**Vocabulary**  
- food = อาหาร (ฟู้ด)  
- price = ราคา (ไพรซ์)  
- order = สั่ง (ออ-เดอร์)  
- cost = มีค่าใช้จ่ายเท่าไหร่ (คอสต์)  
- baht = บาท (บาท)  

---

## Exercise 3: City Travel Plan  
**ภาษาไทย:** วางแผนเดินทางไปเมืองที่อยากเที่ยว

**สถานการณ์:**  
ให้ผู้ใช้กรอกชื่อเมืองที่อยากไปเที่ยว แล้วแสดงข้อความชวนเที่ยวเมืองนั้น

**Input:**  
- ชื่อเมือง

**Output:**  
- แสดงข้อความว่าเมืองนั้นน่าเที่ยว

```python
city = input("Which city do you want to visit? : ").strip().title()
print(f"{city} is a great place to travel!")
```

**Vocabulary**  
- city = เมือง (ซิ-ที่)  
- visit = เยี่ยม/เที่ยว (วิ-สิท)  
- travel = เดินทาง (แทร-เวล)  

---

## Exercise 4: Discount Check  
**ภาษาไทย:** ตรวจสอบเปอร์เซ็นต์ส่วนลด

**สถานการณ์:**  
ให้ผู้ใช้กรอกจำนวนเปอร์เซ็นต์ส่วนลด ถ้าสูงกว่า 50% ให้แสดงว่าเป็นส่วนลดเยอะ

**Input:**  
- จำนวนเปอร์เซ็นต์ส่วนลด (ตัวเลข)

**Output:**  
- ข้อความประเมินว่าเป็นส่วนลดมากหรือน้อย

```python
discount = int(input("How many percent discount do you get? : "))
if discount >= 50:
    print("Wow! That's a big discount!")
else:
    print("Nice! Every discount counts.")
```

**Vocabulary**  
- discount = ส่วนลด (ดิส-เคาน์ท)  
- percent = เปอร์เซ็นต์ (เพอ-เซ็นต์)  
- big = ใหญ่ (บิ๊ก)  
- count = นับ/มีความหมาย (เคานต์)  

---

## Exercise 5: Favorite Country  
**ภาษาไทย:** ประเทศโปรดของคุณคือที่ไหน

**สถานการณ์:**  
ให้ผู้ใช้กรอกชื่อประเทศที่ชอบ แล้วแสดงข้อความชมว่าประเทศนั้นน่าเที่ยว

**Input:**  
- ชื่อประเทศที่ชอบ

**Output:**  
- ข้อความชมประเทศนั้น

```python
country = input("What is your favorite country? : ").strip().title()
print(f"{country} sounds like an amazing place!")
```

**Vocabulary**  
- favorite = ที่ชอบ (เฟ-เวอ-ริท)  
- amazing = น่าทึ่ง (อะ-เมซ-ซิง)  
- place = สถานที่ (เพลส)  

---

## Exercise 6: Budget Checker  
**ภาษาไทย:** ตรวจสอบงบประมาณเที่ยว

**สถานการณ์:**  
ผู้ใช้จะกรอกงบเที่ยว ถ้าน้อยกว่า 1,000 บาท ระบบจะแนะนำให้วางแผนแบบประหยัด

**Input:**  
- งบประมาณ (บาท)

**Output:**  
- ข้อความแนะนำเกี่ยวกับงบ

```python
budget = float(input("What is your budget for this trip (in baht)? : "))
if budget < 1000:
    print("You might want to plan a simple trip.")
else:
    print("Great! You can enjoy more options.")
```

**Vocabulary**  
- budget = งบประมาณ (บัด-เจ็ท)  
- plan = วางแผน (แพลน)  
- trip = ทริป/การเดินทาง (ทริป)  
- option = ทางเลือก (ออพ-ชัน)  

---
