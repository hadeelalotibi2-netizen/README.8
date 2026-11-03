# README.8
# Servo Motor Control Using Arduino UNO# 

## 1. Project Description

In this project, I connected a Servo Motor to an Arduino UNO board using jumper wires. I programmed the motor to rotate gradually from 0 to 180 degrees and then return to 0 degrees continuously.

## 2. Components Used

- Arduino UNO
- Servo Motor
- Jumper Wires
- USB Cable
- Arduino IDE 2.3.10

## 3. Circuit Connections

The Servo Motor was connected to the Arduino UNO using three wires:

- Red Wire → 5V
- Brown/Black Wire → GND
- Orange/Yellow Wire → Digital Pin 9

## 4. Programming

The project was programmed using C++ in Arduino IDE with the Servo.h library to control the motor's movement and rotation angles.

### Main Functions

- `myservo.attach(9)` – Connects the servo to pin 9.
- `myservo.write(pos)` – Sets the servo rotation angle.
- `for loop` – Controls gradual movement.
- `delay(15)` – Sets a 15-millisecond delay between movements.

## 5. Code

```cpp
#include <Servo.h>

Servo myservo;
int pos = 0;

void setup() {
  myservo.attach(9);
}

void loop() {
  for (pos = 0; pos <= 180; pos += 1) {
    myservo.write(pos);
    delay(15);
  }

  for (pos = 180; pos >= 0; pos -= 1) {
    myservo.write(pos);
    delay(15);
  }
}
```

## 6. Project Result

The Servo Motor successfully moved from 0 to 180 degrees and returned to 0 degrees repeatedly after uploading the code to the Arduino UNO.

## 7. Skills Learned

- Arduino UNO Basics
- Electronic Connections
- Servo Motor Control
- C++ Programming
- Arduino IDE
- Practical Electronics



## 1. وصف المشروع

في هذا المشروع قمت بتوصيل محرك السيرفو بلوحة Arduino UNO باستخدام أسلاك التوصيل، وبرمجته للتحرك تدريجيًا من 0 إلى 180 درجة ثم العودة إلى 0 درجة بشكل مستمر.

## 2. المكونات المستخدمة

- لوحة Arduino UNO
- محرك Servo Motor
- أسلاك التوصيل Jumper Wires
- كيبل USB
- برنامج Arduino IDE 2.3.10

## 3. التوصيلات الإلكترونية

تم توصيل محرك السيرفو بلوحة Arduino UNO باستخدام ثلاثة أسلاك:

- السلك الأحمر → منفذ 5V
- السلك البني أو الأسود → منفذ GND
- السلك البرتقالي أو الأصفر → المنفذ الرقمي رقم 9

## 4. البرمجة

تمت برمجة المشروع باستخدام لغة C++ من خلال برنامج Arduino IDE، مع استخدام مكتبة Servo.h للتحكم في حركة المحرك وزوايا الدوران.

### الوظائف الرئيسية

- `myservo.attach(9)` – توصيل محرك السيرفو بالمنفذ رقم 9.
- `myservo.write(pos)` – تحديد زاوية دوران المحرك.
- `for loop` – التحكم في الحركة التدريجية للمحرك.
- `delay(15)` – تحديد تأخير لمدة 15 مللي ثانية بين كل حركة.

## 5. الكود البرمجي

يتم استخدام الكود الموجود في القسم الإنجليزي أعلاه لتنفيذ حركة المحرك.

## 6. نتيجة المشروع

نجح المشروع في تشغيل محرك السيرفو وتحريكه تدريجيًا من 0 إلى 180 درجة ثم العودة إلى 0 درجة بشكل متكرر بعد رفع الكود إلى لوحة الأردوينو.

## 7. المهارات المكتسبة

- أساسيات Arduino UNO
- التوصيلات الإلكترونية
- التحكم بمحركات السيرفو
- البرمجة بلغة C++
- استخدام Arduino IDE
- المهارات الإلكترونية العملية
