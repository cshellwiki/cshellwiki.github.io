# [Linux] C Shell (csh) iotop การใช้งาน: แสดงการใช้งาน I/O ของโปรเซส

## Overview
คำสั่ง `iotop` ใช้เพื่อแสดงการใช้งาน I/O ของโปรเซสในระบบ Linux โดยจะแสดงข้อมูลเกี่ยวกับการอ่านและเขียนข้อมูลของแต่ละโปรเซส ซึ่งช่วยให้ผู้ใช้สามารถติดตามและวิเคราะห์การใช้งาน I/O ได้อย่างมีประสิทธิภาพ

## Usage
รูปแบบพื้นฐานของคำสั่งคือ:
```bash
iotop [options] [arguments]
```

## Common Options
- `-o` : แสดงเฉพาะโปรเซสที่มีการใช้งาน I/O
- `-b` : ทำงานในโหมดแบตช์ (batch mode) ซึ่งเหมาะสำหรับการบันทึกข้อมูล
- `-n NUM` : กำหนดจำนวนรอบที่จะแสดงข้อมูล
- `-d SEC` : กำหนดระยะเวลาระหว่างการอัปเดตข้อมูล

## Common Examples
- แสดงการใช้งาน I/O ของโปรเซสทั้งหมด:
```bash
iotop
```

- แสดงเฉพาะโปรเซสที่มีการใช้งาน I/O:
```bash
iotop -o
```

- รันในโหมดแบตช์และแสดงข้อมูล 5 ครั้ง:
```bash
iotop -b -n 5
```

- อัปเดตข้อมูลทุกๆ 2 วินาที:
```bash
iotop -d 2
```

## Tips
- ใช้ `iotop` ในโหมด root เพื่อให้สามารถดูข้อมูลของทุกโปรเซสได้
- หากต้องการบันทึกข้อมูลการใช้งาน I/O สามารถใช้โหมดแบตช์ร่วมกับการส่งออกไปยังไฟล์
- ควรใช้ `iotop` ในระบบที่มีการใช้งาน I/O สูงเพื่อวิเคราะห์ปัญหาประสิทธิภาพ