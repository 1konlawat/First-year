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

# Python x English Daily Logic – Level Test (3 Exercises)

> วัดความพร้อมก่อนขึ้นโจทย์ Level 2
> โฟกัสที่การใช้ `if`, `elif`, `else`, `input`, และ logic ภาษาอังกฤษในชีวิตจริง

---

## ✅ Exercise 1: Train Ticket Discount
**ภาษาไทย:** ระบบเช็กส่วนลดค่าตั๋วรถไฟ

**สถานการณ์:**
ผู้ใช้กำลังซื้อตั๋วรถไฟ
- ถ้าอายุน้อยกว่า 10 หรือมากกว่า 60 ปี → ลด 50%
- ถ้าเป็นนักเรียน → ลด 30%
- อย่างอื่น → จ่ายราคาเต็ม

**Input:**
- อายุ (เช่น: 65)
- สถานะเป็นนักเรียนหรือไม่ (yes/no)

**Output:**
- บอกว่าจะลดกี่เปอร์เซ็นต์ หรือจ่ายเต็ม

**คำศัพท์ Vocabulary**
- ticket = ตั๋ว (ทิค-เก็ต)
- student = นักเรียน (สตู-เดนท์)
- discount = ส่วนลด (ดิส-เคาน์ท)
- full price = ราคาปกติ (ฟูล-ไพรซ์)

---

## ✅ Exercise 2: Airport Baggage Limit
**ภาษาไทย:** คิดเงินกระเป๋าน้ำหนักเกินที่สนามบิน

**สถานการณ์:**
สายการบินอนุญาตน้ำหนักกระเป๋าไม่เกิน 20 kg
- ถ้า 21–25 kg → คิดเพิ่ม 100 บาท
- ถ้า 26 kg ขึ้นไป → คิดเพิ่ม 200 บาท
- น้อยกว่าหรือเท่ากับ 20 → ฟรี

**Input:**
- น้ำหนักกระเป๋า (เช่น: 22.5)

**Output:**
- บอกว่าต้องจ่ายเพิ่มไหม และเท่าไหร่

**คำศัพท์ Vocabulary**
- baggage = กระเป๋าเดินทาง (แบก-เกจ)
- overweight = น้ำหนักเกิน (โอเวอร์-เวท)
- pay = จ่าย (เพย์)
- fee = ค่าธรรมเนียม (ฟี)

---

## ✅ Exercise 3: Coffee Order System
**ภาษาไทย:** ระบบสั่งกาแฟและคำนวณราคาทั้งหมด

**สถานการณ์:**
ผู้ใช้เลือกเมนูกาแฟ และจำนวนแก้วที่ต้องการสั่ง
ระบบจะคำนวณราคารวม

**เมนูและราคา:**
- americano = 45 บาท
- latte = 55 บาท
- mocha = 65 บาท

**Input:**
- ชื่อกาแฟ (americano / latte / mocha)
- จำนวนแก้ว (เช่น: 2)

**Output:**
- แสดงราคารวมทั้งหมด

**คำศัพท์ Vocabulary**
- cup = แก้ว (คัพ)
- total = รวม (โท-ทัล)
- order = สั่ง (ออ-เดอร์)
- price = ราคา (ไพรซ์)

---
เปิดการสนทนาแล้ว มีข้อความที่อ่านแล้ว 1 ข้อความ

ข้ามไปที่เนื้อหา
การใช้ Gmail กับโปรแกรมอ่านหน้าจอ
2 จาก 290
Smart_Order_System_Exercises
กล่องจดหมาย

สายสืบ นิทาน <saysubnithan@gmail.com>
สิ่งที่แนบ
12:49 (14 นาทีที่ผ่านมา)
ถึง ฉัน

 ไฟล์แนบ 1 ไฟล์
  • สแกนโดย Gmail
# Python Exercises: Smart Ordering System (5 Scenarios)

> โจทย์ฝึกการใช้ dictionary, input, loop, และการจัดการเมนูแบบระบบจริง  
> เหมาะสำหรับฝึกเขียนระบบร้านค้าเล็ก ๆ ที่ใกล้เคียงของจริง

---

## ✅ Exercise 1: Simple Coffee Order  
**สถานการณ์:**  
ให้ผู้ใช้สั่งกาแฟ 1 แก้วจากเมนู: americano, latte, mocha  
ระบบแสดงราคารวม

**สิ่งที่ต้องใช้:**  
- dictionary สำหรับเก็บราคา  
- input ชื่อเมนู + จำนวน  
- คำนวณราคารวม

---

## ✅ Exercise 2: Multiple Menu Orders  
**สถานการณ์:**  
ให้ผู้ใช้สั่งกาแฟได้หลายเมนู (วนลูป)  
พิมพ์ชื่อเมนู + จำนวน แล้ววนจนพิมพ์ "done"  
จากนั้นระบบแสดงยอดรวมทั้งหมด

**สิ่งที่ต้องใช้:**  
- loop + dictionary  
- ตรวจสอบเมนูว่ามีในระบบหรือไม่  
- เก็บยอดรวม

---

## ✅ Exercise 3: Menu with Size Option  
**สถานการณ์:**  
ผู้ใช้สามารถเลือกเมนู + ขนาด (small/medium/large)  
ราคาจะเพิ่มตามขนาด: +0 / +10 / +20

**สิ่งที่ต้องใช้:**  
- dictionary ของ base ราคา  
- อีก dict หรือ if สำหรับคูณราคาขนาด  
- input ชื่อเมนู + size + จำนวน

---

## ✅ Exercise 4: Daily Special  
**สถานการณ์:**  
มีเมนูปกติ และ “เมนูพิเศษประจำวัน” ที่ลด 10%  
ให้ระบบคำนวณราคาตามส่วนลดเฉพาะบางเมนูเท่านั้น

**สิ่งที่ต้องใช้:**  
- dict สำหรับเมนู + ราคา  
- list สำหรับเมนูที่ลด  
- logic if ตรวจว่าเป็น special menu หรือไม่

---

## ✅ Exercise 5: Limited Stock System  
**สถานการณ์:**  
แต่ละเมนูมีจำนวนจำกัด เช่น latte เหลือ 2 แก้ว  
ให้ระบบปฏิเสธถ้าสั่งเกินจำนวนที่มี  
ระบบต้องอัปเดต stock ทุกครั้งที่สั่ง

**สิ่งที่ต้องใช้:**  
- dictionary ของราคา  
- dictionary ของ stock  
- loop รับ order → เช็ก stock → คำนวณเงิน

---
Smar ... s.md
กำลังแสดง Smart_Order_System_Exercises.md 


