# Arduino Starter Kit - ຄູ່ມືອຸປະກອນທັງໝົດ (ພາກທີ 1: ອຸປະກອນ 1-10)

## ▼ ແຜງວົງຈອນຫຼັກ ແລະ ການເຊື່ອມຕໍ່

### 1. Arduino Uno Board (ແຜງ Arduino Uno)

**ຄໍາອະທິບາຍ:**
Arduino Uno ແມ່ນແຜງໄມໂຄຣຄອນໂທຣເລີທີ່ໃຊ້ຊິບ ATmega328P. ມັນເປັນແຜງ Arduino ທີ່ນິຍົມທີ່ສຸດ, ມີ 14 ພິນດິຈິຕອນ input/output (6 ພິນສາມາດໃຊ້ເປັນ PWM), 6 ພິນອານາລັອກ input, ໂມດູນໂຄງສ້າງ 16 MHz, ແລະ ການເຊື່ອມຕໍ່ USB ສໍາລັບການຂຽນໂປຣແກຣມ.

**ການເຮັດວຽກ:**
Arduino Uno ປະມວນຜົນໂຄ້ດທີ່ຂຽນໃນ Arduino IDE ແລະ ຄວບຄຸມອຸປະກອນທີ່ເຊື່ອມຕໍ່ຜ່ານພິນດິຈິຕອນ ແລະ ອານາລັອກ. ມັນເຮັດວຽກທີ່ 5V ແລະ ສາມາດໃຫ້ພະລັງງານຜ່ານ USB ຫຼື ແຫຼ່ງພະລັງງານພາຍນອກ (7-12V). ໄມໂຄຣຄອນໂທຣເລີ ATmega328P ປະຕິບັດຄໍາສັ່ງຕາມລໍາດັບເພື່ອອ່ານເຊັນເຊີ, ຄວບຄຸມອຸປະກອນ, ແລະ ສື່ສານກັບອຸປະກອນອື່ນໆ.

**ຮູບພາບຕົວຈິງ:**
![Arduino Uno](https://docs.arduino.cc/static/2b141eb1cfe6f465a949c203d4af1fa5/A000066-pinout.png)

**Schematic Diagram/Pinout:**
![Arduino Uno Pinout](https://docs.arduino.cc/static/6ec5e4c2a6c0e9e46389d4f6dc924073/ABX00066-pinout.png)

**ອະທິບາຍພິນ:**
- **ພິນດິຈິຕອນ (0-13):** ສາມາດໃຊ້ເປັນ input ຫຼື output
- **ພິນອານາລັອກ (A0-A5):** ອ່ານເຊັນເຊີອານາລັອກ (ຊ່ວງ 0-5V)
- **ພິນ PWM (3, 5, 6, 9, 10, 11):** ສົ່ງສັນຍານອານາລັອກປອມ
- **ພິນພະລັງງານ:** 5V, 3.3V, GND, VIN
- **ການສື່ສານ:** TX/RX (Serial), SDA/SCL (I2C)

**ຕົວຢ່າງການນໍາໃຊ້:**
```cpp
void setup() {
  pinMode(13, OUTPUT); // LED ພາຍໃນ
}

void loop() {
  digitalWrite(13, HIGH); // ເປີດ LED
  delay(1000);
  digitalWrite(13, LOW);  // ປິດ LED
  delay(1000);
}
```

---

### 2. Breadboard (ແຜງທົດລອງວົງຈອນ)

**ຄໍາອະທິບາຍ:**
Breadboard ແມ່ນແຜງທົດລອງວົງຈອນທີ່ບໍ່ຕ້ອງມີການບັດກີ. ມີແຖວ ແລະ ຖັນຂອງຮູທີ່ມີຄລິບໂລຫະພາຍໃນເຊື່ອມຕໍ່ອຸປະກອນທີ່ສອດເຂົ້າໃນຮູ.

**ການເຮັດວຽກ:**
Breadboard ມີສອງພາກຫຼັກ: ລາງພະລັງງານ (ແນວຕັ້ງຕາມຂ້າງ) ແລະ ແຖບເທີມິນໍ (ແນວນອນຢູ່ກາງ). ອຸປະກອນ ແລະ ສາຍທີ່ສອດຢູ່ໃນແຖວດຽວກັນຈະເຊື່ອມຕໍ່ທາງໄຟຟ້າ. ນີ້ຊ່ວຍໃຫ້ສາມາດປະກອບວົງຈອນຊົ່ວຄາວໂດຍບໍ່ຕ້ອງບັດກີ.

**ຮູບພາບຕົວຈິງ:**
![Breadboard](https://upload.wikimedia.org/wikipedia/commons/7/73/400_points_breadboard.jpg)

**Schematic Diagram:**
![Breadboard Internal Connections](https://cdn.sparkfun.com/assets/3/d/f/a/9/518c0b34ce395fea62000002.jpg)

**ຮູບແບບການເຊື່ອມຕໍ່:**
- **ລາງພະລັງງານ:** ເຊື່ອມຕໍ່ແນວຕັ້ງ (+ ແລະ -)
- **ແຖບເທີມິນໍ:** ເຊື່ອມຕໍ່ແນວນອນໃນແຖວ 5 ຮູ
- **ຊ່ອງວ່າງກາງ:** ແຍກສອງຂ້າງສໍາລັບວາງ IC

**ຕົວຢ່າງການນໍາໃຊ້:**
ເຊື່ອມຕໍ່ Arduino 5V ໄປຫາລາງພະລັງງານບວກ, GND ໄປຫາລາງລົບ, ຈາກນັ້ນແຈກຢາຍພະລັງງານໄປຫາອຸປະກອນທັງໝົດຈາກລາງເຫຼົ່ານີ້. ວາງອຸປະກອນຂ້າມຊ່ອງວ່າງກາງ ແລະ ເຊື່ອມຕໍ່ດ້ວຍສາຍຈໍາເປີ.

---

### 3. USB Cable (ສາຍ USB)

**ຄໍາອະທິບາຍ:**
ສາຍ USB Type A ເຖິງ Type B ທີ່ໃຊ້ເພື່ອເຊື່ອມຕໍ່ແຜງ Arduino ເຂົ້າກັບຄອມພິວເຕີສໍາລັບການຂຽນໂປຣແກຣມ ແລະ ການສື່ສານ serial. ມັນຍັງສະໜອງພະລັງງານ 5V ໃຫ້ກັບ Arduino.

**ການເຮັດວຽກ:**
ສາຍ USB ຖ່າຍໂອນຂໍ້ມູນລະຫວ່າງຄອມພິວເຕີ ແລະ Arduino ໂດຍໃຊ້ໂປໂຕຄໍ USB. ຊິບແປງສັນຍານ USB-to-serial ຂອງ Arduino (ATmega16U2 ຫຼື CH340) ແປງສັນຍານ USB ເປັນການສື່ສານແບບ serial ທີ່ໄມໂຄຣຄອນໂທຣເລີເຂົ້າໃຈ. ມັນໃຫ້ພະລັງງານ 5V ສູງສຸດ 500mA ພ້ອມກັນ.

**ຮູບພາບຕົວຈິງ:**
![USB A to B Cable](https://m.media-amazon.com/images/I/61c7nUC+ZfL._AC_UF894,1000_QL80_.jpg)

**Pinout:**
![USB Pinout](https://www.electronics-tutorials.ws/wp-content/uploads/2018/05/io-io48.gif)

**ການຕັ້ງຄ່າພິນ:**
- **ພິນ 1:** VCC (ພະລັງງານ +5V)
- **ພິນ 2:** D- (ຂໍ້ມູນລົບ)
- **ພິນ 3:** D+ (ຂໍ້ມູນບວກ)
- **ພິນ 4:** GND (ກາວ)

**ຕົວຢ່າງການນໍາໃຊ້:**
ເຊື່ອມຕໍ່ປາຍ Type B ເຂົ້າກັບ Arduino Uno ແລະ ປາຍ Type A ເຂົ້າກັບຄອມພິວເຕີ. ເລືອກ COM port ທີ່ຖືກຕ້ອງໃນ Arduino IDE, ຈາກນັ້ນອັບໂຫຼດໂປຣແກຣມຂອງທ່ານ.

---

## ▼ ສາຍ ແລະ ຕົວເຊື່ອມຕໍ່

### 4. Jumper Wires (Male-to-Male) (ສາຍຈໍາເປີແບບ ຊາຍ-ຊາຍ)

**ຄໍາອະທິບາຍ:**
ສາຍທີ່ມີຄວາມຍືດຫຍຸ່ນມີພິນໂລຫະທັງສອງປາຍ ໃຊ້ເພື່ອເຊື່ອມຕໍ່ອຸປະກອນເທິງ breadboard ຫຼື ລະຫວ່າງສອງ breadboard.

**ການເຮັດວຽກ:**
ສາຍຈໍາເປີແບບຊາຍ-ຊາຍມີພິນທີ່ສາມາດສອດເຂົ້າຮູ breadboard ຫຼື female header, ສ້າງການເຊື່ອມຕໍ່ທາງໄຟຟ້າລະຫວ່າງຈຸດຕ່າງໆໃນວົງຈອນ.

**ຮູບພາບຕົວຈິງ:**
![Male-to-Male Jumper Wires](https://m.media-amazon.com/images/I/61IBmkD4hTL._AC_UF894,1000_QL80_.jpg)

**ລະຫັດສີ:**
- **ສີແດງ:** ໂດຍທົ່ວໄປໃຊ້ສໍາລັບແຮງດັນບວກ (+5V, +3.3V)
- **ສີດໍາ:** ກາວ (GND)
- **ສີອື່ນໆ:** ສາຍສັນຍານ (ແຍກແຍະການເຊື່ອມຕໍ່ຕ່າງໆ)

**ຕົວຢ່າງການນໍາໃຊ້:**
```cpp
// ເຊື່ອມຕໍ່ວົງຈອນ LED
// Arduino ພິນ 13 -> ຕົວຕ້ານທານ 220Ω -> LED anode (ຂາຍາວ)
// LED cathode (ຂາສັ້ນ) -> GND
```

---

### 5. Jumper Wires (Male-to-Female) (ສາຍຈໍາເປີແບບ ຊາຍ-ຍິງ)

**ຄໍາອະທິບາຍ:**
ສາຍທີ່ມີພິນຊາຍຢູ່ປາຍໜຶ່ງ ແລະ ຊ່ອງຍິງຢູ່ອີກປາຍໜຶ່ງ, ໃຊ້ເພື່ອເຊື່ອມຕໍ່ພິນ Arduino ເຂົ້າກັບອຸປະກອນ breadboard ຫຼື ເຊັນເຊີທີ່ມີ header ຊາຍ.

**ການເຮັດວຽກ:**
ປາຍຊາຍສອດເຂົ້າຮູ breadboard ຫຼື ຊ່ອງຍິງ, ໃນຂະນະທີ່ປາຍຍິງເຊື່ອມຕໍ່ກັບພິນຊາຍເທິງ Arduino ຫຼື ເຊັນເຊີ.

**ຮູບພາບຕົວຈິງ:**
![Male-to-Female Jumper Wires](https://components101.com/sites/default/files/inline-images/Male-to-Female-Jumper-Wire.jpg)

**ຕົວຢ່າງການນໍາໃຊ້:**
ເຊື່ອມຕໍ່ເຊັນເຊີທີ່ມີ header ຊາຍ (ເຊັ່ນ: DHT11, ເຊັນເຊີ ultrasonic) ໂດຍກົງກັບ Arduino ຫຼື breadboard ໂດຍບໍ່ຈໍາເປັນຕ້ອງວາງເຊັນເຊີເທິງ breadboard.

---

### 6. Jumper Wires (Female-to-Female) (ສາຍຈໍາເປີແບບ ຍິງ-ຍິງ)

**ຄໍາອະທິບາຍ:**
ສາຍທີ່ມີຊ່ອງຍິງທັງສອງປາຍ, ໃຊ້ເພື່ອເຊື່ອມຕໍ່ພິນ header ຊາຍເຂົ້າຫາກັນ, ເຊັ່ນ: ເຊື່ອມຕໍ່ສອງໂມດູນ ຫຼື Arduino ເຂົ້າກັບໂມດູນທີ່ມີ header ຊາຍ.

**ການເຮັດວຽກ:**
ຊ່ອງຍິງທັງສອງປາຍຍຶດພິນຊາຍເພື່ອສ້າງການເຊື່ອມຕໍ່ທາງໄຟຟ້າທີ່ໝັ້ນຄົງລະຫວ່າງອຸປະກອນທີ່ມີ header ຊາຍ.

**ຮູບພາບຕົວຈິງ:**
![Female-to-Female Jumper Wires](https://cdn.shopify.com/s/files/1/0025/5292/8119/products/2_8dc3dc8d-faef-4e1d-8da5-c78e5ce07d0c_1024x1024.jpg)

**ຕົວຢ່າງການນໍາໃຊ້:**
ເຊື່ອມຕໍ່ Arduino header ຊາຍໂດຍກົງເຂົ້າກັບໂມດູນເຊັນເຊີທີ່ມີ header ຊາຍ, ຫຼື ຂະຫຍາຍການເຊື່ອມຕໍ່ແບບຊາຍ-ຊາຍ.

---

### 7. 9V Battery Connector (ຕົວເຊື່ອມຕໍ່ແບັດເຕີຣີ 9V)

**ຄໍາອະທິບາຍ:**
ຄລິບແບັດເຕີຣີທີ່ມີຕົວເຊື່ອມຕໍ່ barrel jack ທີ່ອະນຸຍາດໃຫ້ແບັດເຕີຣີ 9V ໃຫ້ພະລັງງານ Arduino ຜ່ານຊ່ອງພະລັງງານພາຍນອກ.

**ການເຮັດວຽກ:**
ຕົວເຊື່ອມຕໍ່ຕິດກັບຂົ້ວຂອງແບັດເຕີຣີ 9V ແລະ ໃຫ້ພະລັງງານຜ່ານ barrel jack ຂະໜາດ 2.1mm. ຕົວປັບແຮງດັນພາຍໃນ Arduino ແປງ 9V ເປັນ 5V ສໍາລັບໄມໂຄຣຄອນໂທຣເລີ.

**ຮູບພາບຕົວຈິງ:**
![9V Battery Connector](https://m.media-amazon.com/images/I/61vGo0L0NFL._AC_UF894,1000_QL80_.jpg)

**Diagram ການເຊື່ອມຕໍ່:**
- **ສາຍສີແດງ:** ຂົ້ວບວກ → ພິນກາງຂອງ barrel jack
- **ສາຍສີດໍາ:** ຂົ້ວລົບ → ແຖບນອກຂອງ barrel jack

**ຕົວຢ່າງການນໍາໃຊ້:**
ໃຊ້ເມື່ອທ່ານຕ້ອງການໂຄງການ Arduino ແບບພົກພາທີ່ບໍ່ມີການເຊື່ອມຕໍ່ USB. ແບັດເຕີຣີ 9V ມີຄວາມຈຸປະມານ 400-600mAh, ເໝາະສໍາລັບໂຄງການທີ່ໃຊ້ພະລັງງານຕໍ່າໃຊ້ງານໄດ້ສອງສາມຊົ່ວໂມງ.

---

## 💡 ອຸປະກອນພື້ນຖານ

### 8. LEDs (Light Emitting Diodes) (ໄຟ LED)

**ຄໍາອະທິບາຍ:**
ອຸປະກອນເຊມິຄອນດັກເຕີທີ່ປ່ອຍແສງເມື່ອກະແສໄຟຟ້າໄຫຼຜ່ານ. ຊຸດມີ LED ສີແດງ (5), ສີເຫຼືອງ (5), ສີຟ້າ (5), ແລະ RGB (1). LED ມາດຕະຖານໂດຍທົ່ວໄປມີຂະໜາດ 5mm.

**ການເຮັດວຽກ:**
LED ແມ່ນໄດໂອດທີ່ປ່ອຍແສງເມື່ອມີແຮງດັນໄຟບວກ (anode ບວກ, cathode ລົບ). ວັດສະດຸເຊມິຄອນດັກເຕີແຕກຕ່າງກັນຜະລິດສີແຕກຕ່າງກັນ. ພວກມັນຕ້ອງການຕົວຕ້ານທານຈໍາກັດກະແສ (ໂດຍທົ່ວໄປ 220Ω ສໍາລັບ 5V) ເພື່ອປ້ອງກັນການເຜົາໄໝ້.

**ຮູບພາບຕົວຈິງ:**
![LEDs Various Colors](https://cdn.sparkfun.com/assets/parts/1/2/7/7/9/14563-LEDs_-_5mm_Diffused__25_pack_-01a.jpg)

**ໂຄງສ້າງ LED:**
![LED Diagram](https://upload.wikimedia.org/wikipedia/commons/thumb/f/f9/LED_symbol.svg/1200px-LED_symbol.svg.png)

**ການລະບຸພິນ:**
- **Anode (+):** ຂາຍາວກວ່າ, ເຊື່ອມຕໍ່ກັບບວກ
- **Cathode (-):** ຂາສັ້ນກວ່າ, ດ້ານແບນຂອງເລນສ໌, ເຊື່ອມຕໍ່ກັບກາວ
- **ແຮງດັນໄຟຟ້າໄປໜ້າ:** ແດງ ~1.8-2.2V, ເຫຼືອງ ~2.0-2.4V, ຟ້າ ~3.0-3.4V

**ຕົວຢ່າງການນໍາໃຊ້:**
```cpp
// ກະພິບ LED ເທິງພິນ 13
void setup() {
  pinMode(13, OUTPUT);
}

void loop() {
  digitalWrite(13, HIGH);  // ເປີດ LED
  delay(1000);
  digitalWrite(13, LOW);   // ປິດ LED
  delay(1000);
}
```

**Diagram ວົງຈອນ:**
Arduino ພິນ → ຕົວຕ້ານທານ 220Ω → LED Anode → LED Cathode → GND

---

### 9. RGB Module (ໂມດູນ RGB)

**ຄໍາອະທິບາຍ:**
ໂມດູນ LED RGB ລວມ LED ສີແດງ, ສີຂຽວ, ແລະ ສີຟ້າໃນຊຸດດຽວທີ່ມີ cathode ຫຼື anode ຮ່ວມກັນ. ສາມາດຜະລິດສີລ້ານສີໂດຍການຜະສົມຄວາມເຂັ້ມຂອງສີຕົ້ນຕໍທັງສາມ.

**ການເຮັດວຽກ:**
ໂມດູນ RGB ມີສີ່ພິນ: ໜຶ່ງພິນຮ່ວມ (cathode ຫຼື anode) ແລະ ສາມພິນສໍາລັບ R, G, ແລະ B. ໂດຍການໃຊ້ສັນຍານ PWM ເທິງສາມພິນສີ, ທ່ານສາມາດຄວບຄຸມຄວາມເຂັ້ມຂອງແຕ່ລະສີ (0-255) ເພື່ອສ້າງສີໃດກໍໄດ້ທີ່ມອງເຫັນໄດ້.

**ຮູບພາບຕົວຈິງ:**
![RGB LED Module](https://components101.com/sites/default/files/component_pin/RGB-LED-Module-Pinout.jpg)

**Pinout Diagram:**
![RGB Module Pinout](https://www.electronicshub.org/wp-content/uploads/2021/04/RGB-LED-Module-Pinout.jpg)

**ການຕັ້ງຄ່າພິນ:**
- **R:** ຄວບຄຸມ LED ສີແດງ (PWM)
- **G:** ຄວບຄຸມ LED ສີຂຽວ (PWM)
- **B:** ຄວບຄຸມ LED ສີຟ້າ (PWM)
- **GND/-:** Cathode ຮ່ວມ (ຫຼື VCC ສໍາລັບ anode ຮ່ວມ)

**ຕົວຢ່າງການນໍາໃຊ້:**
```cpp
int redPin = 9;
int greenPin = 10;
int bluePin = 11;

void setup() {
  pinMode(redPin, OUTPUT);
  pinMode(greenPin, OUTPUT);
  pinMode(bluePin, OUTPUT);
}

void loop() {
  // ສີມ່ວງ (ແດງ + ຟ້າ)
  analogWrite(redPin, 255);
  analogWrite(greenPin, 0);
  analogWrite(bluePin, 255);
  delay(1000);
  
  // ສີຟ້າອ່ອນ (ຂຽວ + ຟ້າ)
  analogWrite(redPin, 0);
  analogWrite(greenPin, 255);
  analogWrite(bluePin, 255);
  delay(1000);
}
```

---

### 10. Resistors (220Ω, 1kΩ, 10kΩ) (ຕົວຕ້ານທານ)

**ຄໍາອະທິບາຍ:**
ອຸປະກອນ passive ທີ່ຕ້ານການໄຫຼຂອງກະແສໄຟຟ້າ. ຊຸດມີສາມຄ່າທົ່ວໄປ: 220Ω (ແດງ-ແດງ-ນ້ຳຕານ), 1kΩ (ນ້ຳຕານ-ດຳ-ແດງ), ແລະ 10kΩ (ນ້ຳຕານ-ດຳ-ສົ້ມ).

**ການເຮັດວຽກ:**
ຕົວຕ້ານທານຈໍາກັດການໄຫຼຂອງກະແສຕາມກົດໝາຍ Ohm (V = I × R). ພວກມັນປົກປ້ອງອຸປະກອນເຊັ່ນ LED ຈາກກະແສທີ່ເກີນໄປ, ສ້າງ voltage divider, ແລະ ກໍານົດຄ່າເວລາໃນວົງຈອນ.

**ຮູບພາບຕົວຈິງ:**
![Resistors](https://upload.wikimedia.org/wikipedia/commons/thumb/e/e8/Resistors.jpg/1200px-Resistors.jpg)

**ຕາຕະລາງລະຫັດສີ:**
![Resistor Color Code](https://www.electronics-tutorials.ws/wp-content/uploads/2018/05/resistor-res1.gif)

**ການລະບຸຄ່າ:**
- **220Ω:** ແດງ-ແດງ-ນ້ຳຕານ-ຄຳ (ຈໍາກັດກະແສ LED)
- **1kΩ:** ນ້ຳຕານ-ດຳ-ແດງ-ຄຳ (ໃຊ້ງານທົ່ວໄປ)
- **10kΩ:** ນ້ຳຕານ-ດຳ-ສົ້ມ-ຄຳ (pull-up/pull-down resistors)

**ຕົວຢ່າງການນໍາໃຊ້:**
```cpp
// LED ດ້ວຍຕົວຕ້ານທານຈໍາກັດກະແສ
// ຄິດໄລ່ຄ່າຕົວຕ້ານທານ: R = (Vs - Vf) / If
// R = (5V - 2V) / 0.020A = 150Ω (ໃຊ້ 220Ω ເພື່ອຄວາມປອດໄພ)

// Pull-up resistor ສໍາລັບປຸ່ມກົດ
pinMode(2, INPUT);  // ໃຊ້ 10kΩ pull-up ພາຍນອກ
// ຫຼື
pinMode(2, INPUT_PULLUP);  // ໃຊ້ ~20kΩ pull-up ພາຍໃນ
```

**ການນໍາໃຊ້ຕົວຕ້ານທານແຕ່ລະຊະນິດ:**
- **220Ω:** ໃຊ້ຕໍ່ກັບ LED ເພື່ອຈໍາກັດກະແສ
- **1kΩ:** ໃຊ້ໃນວົງຈອນທົ່ວໄປ, ແບ່ງແຮງດັນ
- **10kΩ:** ໃຊ້ເປັນ pull-up ຫຼື pull-down resistor ສໍາລັບປຸ່ມກົດ ແລະ ສະວິດ

---

# ສິ້ນສຸດພາກທີ 1 (ອຸປະກອນ 1-10)

ພາກຕໍ່ໄປຈະປະກອບມີ:
- ອຸປະກອນ 11-20: Push Buttons, Potentiometer, Buzzer, LCD Display, ແລະອື່ນໆ
- ອຸປະກອນ 21-30: ເຊັນເຊີຕ່າງໆ (Temperature, Humidity, PIR, Ultrasonic, ແລະອື່ນໆ)
- ອຸປະກອນ 31-40: Remote Control, Motors, IC Modules, ແລະອື່ນໆ