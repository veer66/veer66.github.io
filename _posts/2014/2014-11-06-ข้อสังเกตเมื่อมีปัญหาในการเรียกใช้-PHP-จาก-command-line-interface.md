
# ข้อสังเกตเมื่อมีปัญหาในการเรียกใช้ PHP จาก command line interface
Date: 2014/11/06


เวลาใช้ PHP จาก command line interface (CLI) แล้วเจ๊งโดยเฉพาะบน Mac OS X ให้พึงระวังว่านั้นอาจจะเป็น PHP คนละตัวกับที่ใช้กับ web

เช่น เวลาเราเรียก PHP จาก CLI ตัวที่ถูกเรียกอาจจะอยู่ใน /usr/bin/php แต่ว่าเวลาใช้จากเว็บอาจจะเป็นกลายเป็นไปเรียก php ใน /Application/MAMP ถ้าหากลง MAMP ไว้ หรืออาจจะเป็น /opt/local ถ้าหากใช้ macports
