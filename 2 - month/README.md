# เดือนที่ 2 — Python Control Flow

> รวม 8 หัวข้อพื้นฐานของการควบคุมโปรแกรมใน Python ที่ต้องเขียนได้คล่อง
> ก่อนเข้าสู่การเขียน Data Pipeline และ ML จริงในเดือนถัดไป

---

## หัวข้อที่จะเรียนในเดือนนี้:

1. **if-elif-else** — เงื่อนไขเบื้องต้นและซ้อนเงื่อนไข
2. **for / while loop** — การวนซ้ำทุกชนิด
3. **break, continue, else ใน loop** — ควบคุมลูปให้ละเอียดขึ้น
4. **list comprehension** — ย่อ for loop แบบเทพ พร้อม if
5. **try-except** — ดักจับ error ให้โปรแกรมไม่พัง
6. **lambda, map, filter, any, all** — เขียนโค้ดแบบ functional
7. **เข้าใจ scope ตัวแปร** — local / global / nonlocal
8. **เขียนฟังก์ชัน** — แบบมี default, *args, **kwargs

---

## เป้าหมายของเดือนนี้:
- เขียนโปรแกรมควบคุม flow เองได้
- สร้างฟังก์ชัน reusable ได้
- เข้าใจ logic control พอไปต่อ Pandas, ML ได้

---

## Mini Exercises (แนะนำให้ลองทำ)

- เขียนโปรแกรมคำนวณเกรดจากคะแนน
- สร้าง list comprehension สำหรับเลขคู่ 0–100
- เขียนฟังก์ชันรับหลาย argument แล้ว return dictionary
- ใช้ `try-except` ดักหารศูนย์

---

## โครงสร้างไฟล์ในโฟลเดอร์นี้:

```bash
2-month/
├── 01_if_else.py
├── 02_loops.py
├── 03_loop_control.py
├── 04_list_comprehension.py
├── 05_try_except.py
├── 06_lambda_map_filter.py
├── 07_scope.py
├── 08_function_args.py
└── README.md
