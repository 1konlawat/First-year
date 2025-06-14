# For Loop และ While Loop 

## For Loop

- ใช้ทำซ้ำคำสั่งตามจำนวนรอบที่กำหนดหรือวนผ่านข้อมูล  
- เหมาะกับงานที่รู้จำนวนรอบแน่นอน  

### โครงสร้าง

```python
for ตัวแปร in ชุดข้อมูล:
    # คำสั่งที่ทำซ้ำ
```
```python
for i in range(1, 6):  # วนลูป 5 รอบ (1,2,3,4,5)
    print(i)
```
### ผลลัพพ์
         1
         2
         3
         4
         5

##  While Loop
- ใช้วนลูปตราบใดที่เงื่อนไขเป็นจริง (True)
- เหมาะกับงานที่จำนวนรอบไม่แน่นอน


```python
count = 1
while count <= 5:
print(count)
count += 1  # เพิ่มค่า count ทีละ 1
```
### ผลลัพพ์
         1
         2
         3
         4
         5


# การใช้แบบขั้นสูง
-เป็นการประยุกต์ใช้ for AND while
```python
def score_studen():

    matrix = []
    while True:
        score = input("score you: ")
        if score.lower() == "stop":
             print("Thakyou")
             break
        try:
           score_int = list(map(int, score.split(' ')))
           matrix.append(score_int)
        except ValueError:
           print("please input number")
           continue

    if not matrix:
      print("No score entered")
      return

    High_scores = []
    medium     = []
    Low        = []
    for row in matrix:
     for score_t in row:
      if score_t > 90:
        High_scores.append(score_t)
      elif score_t > 70:
        medium.append(score_t)
      elif score_t < 70:
        Low.append(score_t)

    def score_average(group):
     tatal = sum(group)
     average = tatal / len(group) if group else 0
     return tatal , average

    Hige_score , Hige_average = score_average(High_scores)
    medium_score , medium_average = score_average(medium)
    Low_score , Low_average = score_average(Low)

    print(f"sum_score: {Hige_score}, Hige_average: {Hige_average:}")
    print(f"sum_score: {medium_score}, medium_aevage: {medium_average}")
    print(f"sum_score: {Low_score}, Low_average: {Low_average}")

score_studen()
```
!!! อ่านทีล่ะบรรทัด
   -ข้อสำคัญที่พบบ่อยคือ เขียนนอกเยื้องเลย while ถ้าเลย ระบบนั้นจะไม่ทำงาน
   EX
```python
def while_score():
  while True
  score = int(input("ข้อมูลเลข")
print(score)
while_score()
```
ปกติแล้ว def เยื้องออกมาได้
 แต่สิ่งที่ทำให้ระบบพัง คือ print(score) เพราะเยื้องเลยwhile
     
