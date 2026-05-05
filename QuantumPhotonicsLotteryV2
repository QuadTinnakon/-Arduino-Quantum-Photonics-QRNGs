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
#include <LiquidCrystal_I2C.h>
LiquidCrystal_I2C lcd(0x27,20,4);  // set the LCD address to 0x27 for a 16 chars and 2 line display

long x = 536077;
long Lottery[] = {536077, 66595, 85702, 564187, 725574, 758996, 61816, 69472, 
116564, 134320, 184357, 213562, 442701, 511289, 568042, 981256, 41714, 56252, 
60867, 81719, 100880, 102006, 109037, 121308, 181813, 200417, 201300, 255960};
long times = 2052569;
long timeprint = 4050;//4051 = 3s , = 42s
//////////////////////////////
long i = 0;
int j = 0;
int prin = 0;
//////////////////////////////
int a1 = 0;
int b2 = 0;
int c3 = 0;
int d4 = 0;
int e5 = 0;
int f6 = 0;
  int sensorValue = 0;//UV
  int sensorValue1 = 0;//LDR1 V Vertical
  int sensorValue2 = 0;//LDR2 H Horizontal แนวนอน
  int sensorValue3 = 0;// IR
  int sensorValue4 = 0;// SDA
  int sensorValue5 = 0;// DCL
int GLO = 0;
int Sum = 0;
/////////////////////////////////////////////////////////////////
void setup() {
  // initialize serial communication at 9600 bits per second:
  Serial.begin(115200);
  Serial.print("Lottery");
  Serial.print(x);
  Serial.println("GLOLottery02-05-69V1");
  delay(100);
  lcd.init(); ////////////// initialize the lcd ///////////////
  // Print a message to the LCD.
  lcd.backlight();
  lcd.setBacklight(HIGH);
  //lcd.setBacklight(LOW);
  lcd.setCursor(3,0);
  lcd.print("Hello, world!");
  lcd.setCursor(2,1);
  lcd.print("Lottery 02-05-69!");
  lcd.setCursor(0,2);
  lcd.print("Quantum Photonics 69");
  lcd.setCursor(2,3);
  lcd.print("Power By TK Quad3D");
  delay(500);
  lcd.setBacklight(LOW);
}
/////////////////////////////////////////////////////////////////
void loop() {
  i++;
  j++;
  // read the input on analog pin 0://///////////////////////////
  sensorValue = analogRead(A0);//UV
  sensorValue1 = analogRead(A1);//LDR1 V Vertical
  sensorValue2 = analogRead(A2) + 2;//LDR2 H Horizontal แนวนอน
  sensorValue3 = analogRead(A3);// IR
  delay(10);
  //int sensorValue4 = analogRead(A4);
  //int sensorValue5 = analogRead(A5);
  // Convert the analog reading (which goes from 0 - 1023) to a voltage (0 - 5V):
  //float voltage = sensorValue * (5000.0 / 1023.0);
  Sum = sensorValue + sensorValue1 + sensorValue2 + sensorValue3;
  GLO = sensorValue % sensorValue1 % sensorValue2 % sensorValue3;
  ///////////////////////////////////////////////////////////////
  analogWrite(9, sensorValue2);
  ///////////////////////////////////////////////////////////////
  // print out the value you read: ///times // timeprint
  if(j > timeprint){
  a1 = (GLO + Sum + times + Lottery[prin]) % 10;
  b2 = (GLO + Sum + times + Lottery[prin+1]) % 10;
  c3 = (GLO + Sum + times + Lottery[prin+2]) % 10;
  d4 = (GLO + Sum + times + Lottery[prin+3]) % 10;
  e5 = (GLO + Sum + times + Lottery[prin+4]) % 10;
  f6 = (GLO + Sum + times + Lottery[prin+5]) % 10;
    j = 0;
  //lcd.setBacklight(HIGH);
  lcd.setBacklight(LOW);
  Serial.print(i);Serial.print("\t");
  //Serial.print("Lotterty02-05-69");Serial.print("\t");
  Serial.print(sensorValue);Serial.print("\t");
  Serial.print(sensorValue1);Serial.print("\t");
  Serial.print(sensorValue2);Serial.print("\t");
  Serial.print(sensorValue3);Serial.print("\t");
  Serial.print(Sum);Serial.print("\t");
  Serial.print(GLO);Serial.print("\t");
  Serial.print(a1);
  Serial.print(b2);
  Serial.print(c3);
  Serial.print(d4);
  Serial.print(e5);
  Serial.print(f6);Serial.print("\t");
  Serial.print(Lottery[prin]);Serial.println("\t");
///////////////////////////////////////////////////////////////////
  lcd.clear();
  lcd.setCursor(1,0);
  lcd.print("Lottery 02-05-69!");
  lcd.setCursor(1,1);
  lcd.print(Lottery[prin]);
  lcd.setCursor(11,1);
  lcd.print(i);
  lcd.setCursor(11,2);
  lcd.print(sensorValue);
  lcd.setCursor(16,2);
  lcd.print(sensorValue3);
  lcd.setCursor(11,3);
  lcd.print(sensorValue1);
  lcd.setCursor(16,3);
  lcd.print(sensorValue2);
  lcd.setCursor(1,3);
  lcd.print(a1);
  lcd.setCursor(2,3);
  lcd.print(b2);
  lcd.setCursor(3,3);
  lcd.print(c3);
  lcd.setCursor(4,3);
  lcd.print(d4);
  lcd.setCursor(5,3);
  lcd.print(e5);
  lcd.setCursor(6,3);
  lcd.print(f6);
  //lcd.setBacklight(LOW);
  prin++;
  }
  if(prin > 28)
  {
    prin = 0;
    //lcd.setBacklight(LOW);
    lcd.setBacklight(HIGH);
  }
//////Serial.println(voltage);/////////////////////////////////////
  //delay(100);
}
