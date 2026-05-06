/*
 Arduino Quantum Photonics Quantum Random Number Generators (QRNGs)
 Arduino 1.6.9
 
QuantumPhotonicsLotteryV2 = 5 พค 2569 . LCD 20x4 , Sum % time
QuantumPhotonicsVoltageV1 = 4 พค 2569

1-GY-8511 UV Sensor Ultraviolet Module 5.5V

2-ตรวจจับเปลวไฟ KY-026 (IR Flame Sensor) แรงดัน  3.3V ~ 5.5V

 lnfrared IR Flame Detector Sensor 
 
3-Infrared Module K63 LM393 Reflection Photoelectric Sensor (ระยะ 2 ~ 30cm)

4-ความเข้มแสง LDR Photoresistor Sensor Module  3.3 V to 5 V

5- LDR Photoresistor Sensor Module  3.3 V to 5 V

6- GUVA-S12SD analog UV sensor 3.3-5VDC

-LCD2004A LCD (BLUE Screen) 20x4 LCD 5.5V

TK Quad3D 
  http://quad3d-tin.lnwshop.com/
*/
<img width="4000" height="1848" alt="Image" src="https://github.com/user-attachments/assets/ed3cdd53-cbbf-4304-8619-a3154a8c6264" />

<img width="1519" height="785" alt="Image" src="https://github.com/user-attachments/assets/385f753b-1fbd-4b08-bd1a-19127eda996a" />

<img width="4000" height="1848" alt="Image" src="https://github.com/user-attachments/assets/f529c1d5-218b-4f31-a503-86d48169bd4b" />

Experimental results

<img width="2524" height="1345" alt="Image" src="https://github.com/user-attachments/assets/a3e57592-0d9b-40df-a5c9-117c47127e58" />

จุดตัดระหว่างฮาร์ดแวร์ที่เข้าถึงง่ายอย่าง Arduino กับความไม่แน่นอนที่เป็นพื้นฐานของกลศาสตร์ควอนตัมครับ การสร้าง 
เครื่องกำเนิดตัวเลขสุ่มแบบควอนตัม (Quantum Random Number Generator หรือ QRNG) ถือเป็นโปรเจกต์ระดับ "Hello World"
สำหรับสาขาโฟโตนิกส์ควอนตัม (Quantum Photonics) เลยก็ว่าได้
ในขณะที่คอมพิวเตอร์ทั่วไปใช้ขั้นตอนวิธีแบบสุ่มเทียม (PRNG) ซึ่งจริงๆ แล้วเป็นการคำนวณแบบกำหนดผลลัพธ์ได้ (Deterministic) 
แต่ QRNG จะอาศัยคุณสมบัติ การซ้อนทับ (Superposition) และ ความไม่แน่นอน (Indeterminacy) ของโฟตอน
