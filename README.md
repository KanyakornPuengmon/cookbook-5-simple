
# แนวทางการทำงาน Simple HTTPD Server Example

การทำงานนี้เป็นการสร้าง HTTP Server อย่างง่ายด้วย ESP32 เพื่อตอบสนองคำขอ HTTP แล้วแสดงหน้า HTML 

## การเลือก Example IDF

![image](https://github.com/user-attachments/assets/2d793531-7681-495e-ba9e-41116d34de81)

1. เลือก ESP-IDF

2. เลือก show example

3. พิมพ์คำว่า simple

4. เลือก simple ใน http_server


![สกรีนช็อต 2024-10-30 015030](https://github.com/user-attachments/assets/9e14a59f-1a71-40e0-9ca3-bd9d0a58bfa0)


5. คลิกเลือก Create project using example simple


6. เมื่อสร้างแล้วจะได้ไฟล์ทั้งหมด ดังนี้

![สกรีนช็อต 2024-10-30 015046](https://github.com/user-attachments/assets/f6ba9a50-ca7c-4cfb-98ac-5824aa1a1636)

## ตั้งค่า WIFI ( set SSID , Password)

![สกรีนช็อต 2024-10-30 015342](https://github.com/user-attachments/assets/12f151da-545d-4275-9380-d8cabb6ca836)

7. เลือก SDK Configuration Editor

![image](https://github.com/user-attachments/assets/a374d55f-acfc-42ea-b0cd-ccc3476b8544)


8. เลือก Example Configuration

9. แก้ไข WIFI SSID

10. แก้ไข WIFI PASSWORD

11. กด Save

12. เชื่อมต่อ internet ที่เหมือนกับที่กรอกใน Configuration

## Build and Flash

13. เลือก com port

14. เลือก Build Flash and Monitor

## ผลลัพท์ 

15. Serial Moniter จะแสดง IP address

![image](https://github.com/user-attachments/assets/a3011f7a-b6a9-471f-bafe-2836a5baab3f)


16. นำ IP address ที่ได้ไปกรอกใน google ตามด้วย/hello

![image](https://github.com/user-attachments/assets/553be67a-e01d-4fc8-ab02-9985b16e4863)

- หน้าเว็บจะแสดงข้อความ Hello world เพราะมีการกำหนดไว้ในนี้

  ![image](https://github.com/user-attachments/assets/0a8b338e-4285-4648-895b-d39ed37db9fb)


## การแก้ไข

เปิดไฟล์ main.c แล้วทำการแก้ไข ดังนี้

![image](https://github.com/user-attachments/assets/0c1dd5aa-ff95-47c2-9749-b26114dc977e)

## ผลลัพท์การแก้ไข

- หน้าเว็บจะแสดงข้อความที่เราแก้ไข
  
![image](https://github.com/user-attachments/assets/7ec9a3f5-8cb3-4c37-9a50-caff1ccf8ef1)


## สรุปผลการทดลอง
- การทดลองเป็นการเชื่อมต่อ Wi-Fi ซึ่ง ESP32 จะพยายามเชื่อมต่อกับเครือข่าย Wi-Fi ที่กำหนดไว้ เมื่อเชื่อมต่อสำเร็จ เซิร์ฟเวอร์ HTTP จะเริ่มทำงานและพร้อมให้บริการที่ IP ของอุปกรณ์ ESP32 ทำให้ผู้ใช้งานสามารถเข้าถึงผ่านเบราว์เซอร์ได้
การอ่านค่า ADC โดยใช้โหมดอ่านครั้งเดียว ซึ่งจะอ่านค่าแรงดันไฟฟ้าและแปลงเป็นข้อมูล adc_raw เมื่อได้ค่า ADC แล้ว โค้ดจะสร้างข้อความ HTML เพื่อแสดงข้อมูลบนหน้าเว็บ


