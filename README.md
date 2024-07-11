# 🛰️SI-2024-CubeSat-SU
🗄️ Repository for summer internship 2024 "intro to CubeSat and Satellite Communication"

![cube-1024x661](https://github.com/DonaldB2003/SI-2024-CubeSat-SU/assets/173866002/1522ad85-2467-4c02-b384-0174fc47d0be)

# Abstractℹ
The report encapsulates the comprehensive learning journey of the Summer Internship 2024 on Introduction to CubeSat and Satellite Communication, providing a deep dive into CubeSat fundamentals, satellite communication principles, LoRa protocol applications, and antenna design. Participants engaged in hands-on experiences including programming ESP32 platforms, configuring TinyGS ground stations, and simulating antenna designs using 4NEC2 software. Led by expert instructors from Silicon University and the Indian Institute of Space Science and Technology, alongside industry guidance from ToSpace, the internship fostered a practical understanding of aerospace technologies. Culminating in a project to design and implement ground stations, participants showcased their skills in a poster presentation, reinforcing their readiness for future endeavors in satellite engineering and space technology.

# Introduction

CubeSat and Satellite Communication offers a structured learning path covering fundamental aspects of embedded systems, communication systems, LoRa technology, antenna design, and the deployment of a TinyGS ground station. Participants begin by mastering ESP32 embedded systems through practical exercises in the Arduino IDE, learning GPIO programming, PWM control for LED dimming, and interfacing with sensors. They then delve into the basics of communication systems, understanding modulation techniques, digital communication principles, and the electromagnetic spectrum.

Next, the course focuses on LoRa basics, exploring spread-spectrum modulation, LoRa radio architecture, and practical implementation using ESP32 with the RA-02 LoRa module. Participants engage in hands-on labs to establish communication between two ESP32 boards equipped with LoRa modules, measuring signal strength and quality using RSSI and SNR metrics.

Antenna fundamentals follow, where participants learn about radiation mechanisms, antenna types, and design principles. Using simulation software like 4NEC2, they simulate antenna configurations, optimizing performance through practical tuning with tools like the NanoVNA. This segment equips participants with essential skills for designing and refining antennas suitable for satellite communication applications.

The culmination of the course involves the deployment of a TinyGS ground station. Participants apply their acquired knowledge to set up and configure ground stations using ESP32 platforms, establishing bidirectional communication with CubeSats or other satellites. Through collaborative project work, they demonstrate proficiency in satellite communication systems, antenna deployment, and operational management of ground stations, preparing them for real-world applications in the burgeoning field of CubeSats and satellite communication technologies.

# What are CubeSats?
CubeSats are a class of nanosatellites that use a standard size and form factor.  The standard CubeSat size uses a “one unit” or “1U” measuring 10x10x10 cms and is extendable to larger sizes; 1.5, 2, 3, 6, and even 12U. Originally developed in 1999 by California Polytechnic State University at San Luis Obispo (Cal Poly) and Stanford University to provide a platform for education and space exploration.  The development of CubeSats has advanced into its own industry with government, industry and academia collaborating for ever increasing capabilities.  CubeSats now provide a cost effective platform for science investigations, new technology demonstrations and advanced mission concepts using constellations, swarms disaggregated systems.
![electronics-09-00482-g001](https://github.com/DonaldB2003/SI-2024-CubeSat-SU/assets/173866002/e431567e-3d6b-4a38-ae62-3e4b1ca073a9)

## Why CubeSats  ? 
<ul>
  <li>size 4x4x4 inches </li>
  <li>mass Mass=1.33kg </li>
  <li>allows for cost-effective development and deployment </li>
  <li>CubeSats have lower costs compared to large satellites.</li>
  <li>Shorter development times (CubeSats can be built within two years.)</li>
  <li>Flexible services(CubeSats can be used for different missions and purposes).</li>
</ul>

## History
The CubeSat concept originated in the late 1990s as a collaborative effort between Stanford University's Space Systems Development Laboratory (SSDL) and California Polytechnic State University (Cal Poly). Professors Bob Twiggs (Stanford) and Jordi Puig-Suari (Cal Poly) proposed the idea of a standardized, small satellite format to enable affordable space access for universities and other entities.

## CubeSat dispenser system
![nasa_iss_on_orbit_status_report_image_030617_945](https://github.com/DonaldB2003/SI-2024-CubeSat-SU/assets/173866002/45e17908-a8a4-44ae-afc5-d33e8230039e)

A CubeSat dispenser system is a critical component used to deploy CubeSats into orbit from a host satellite or launch vehicle. These systems are designed to securely hold CubeSats of various sizes, conforming to standard dimensions like 1U, 2U, or 3U, and ensure their safe release once the host satellite reaches its designated orbit. Integrated into the payload configuration of the launch vehicle, CubeSat dispensers typically employ mechanisms such as springs, pneumatic actuators, or mechanical latches to eject CubeSats at specified velocities and orientations. This controlled deployment process not only facilitates efficient utilization of launch vehicle payload capacity but also enables multiple CubeSats to be deployed in sequence, supporting diverse mission objectives including scientific research, Earth observation, technology demonstration, and educational initiatives. By simplifying and standardizing the deployment process, CubeSat dispenser systems contribute significantly to the accessibility and cost-effectiveness of space missions involving CubeSats.


## Layers of CubeSat
![Screenshot 2024-07-11 160347](https://github.com/DonaldB2003/SI-2024-CubeSat-SU/assets/173866002/d08f1305-1be7-4f56-8325-a75a60d7d034)
<ul>Chassis
  <li>layer 1-Antenna</li>
  <li>layer 2-communication radio</li>
  <li>layer 3-On Board Computer</li>
  <li>layer 4-Attitude control rods</li>
  <li>layer 5-power management system</li>
  <li>layer 6-magnet and battery</li>
</ul>

## Block Diagram For communication


## SPI Protocol


### PID

# MICRO PROCESSOR
![image](https://github.com/DonaldB2003/SI-2024-CubeSat-SU/assets/173866002/c30d280f-926a-4fe3-9fc5-a3395cf9067a)

# MICRO CONTROLER
![image](https://github.com/DonaldB2003/SI-2024-CubeSat-SU/assets/173866002/1f1990d8-c247-4f3a-b7c9-80c1f6f6b671)
<ul>
  <li>MICROCONTROLLER = MICROPROCESSOR+PERIPHERAL</li>
PMW = Pulse ...........
</ul>
ESP-32


# WAVE GENERATION
|x|e^-x|1-e^-x|
|-|----|------|
|0.001|0.99|9.95x10^-3|
|0.1|0.90|0.095|
|1|0.36|0.63|
|10|4.53x10^-5|0.99|
|100|3.72x10^-44|1|

# Electromagnetic Spectrum

VHF
UHF

ν = c/λ
<ul>ν = 433MHz
<li>λ=c/ν</li>
<li>λ=</li>
</ul>
# Atmospheric Attoination
![636541236646532654-Loss_V_Freq_Air](https://github.com/DonaldB2003/SI-2024-CubeSat-SU/assets/173866002/e62cac79-4d0f-42bd-acc6-e277a31597a6)

## Carrier Frequency Selection Criteria
<ul>
  <li>Power Efficiency</li>
  <li>Bandwidth Efficiency</li>
  <li>System Complexity</li>
  <li>Frequency Allocation & Radiation</li>
</ul>

# SATELLITE FUNDAMENTALS 
## Satellite Orbit Kepeler`s Law
## veleocity from the centre of earth
## Path Loss(dB)








# Lab Exercises

## Lab-1 Introduction to ESP32

-[Datasheet ESP32](https://github.com/silicon-sat/SI-2024-CubeSat/blob/main/docs/Datasheet-ESP32.pdf)

## Lab-2 Blinking LED

-[SOURCE FILE](LED/Aurdino/)

Description of writing a list of item:
-To display the current directory type 'pwd'
  -This is a subsection
  -Another
 -Start the second list item 

```C
#define LED1 2
#define LED2 4
#define LED3 5
#define LED4 18
#define LED5 19

// Array to hold LED pin numbers
int leds[] = {LED2, LED3, LED4, LED5};

// Corresponding delays for each LED
int delays[] = {1000, 700, 100, 500};

void setup() {
  pinMode(LED1, OUTPUT); // LED1 is not used in loop, so just initialized here
  for (int i = 0; i < sizeof(leds) / sizeof(leds[0]); i++) {
    pinMode(leds[i], OUTPUT);
  }
}

void loop() {
  for (int i = 0; i < sizeof(leds) / sizeof(leds[0]); i++) {
    digitalWrite(leds[i], HIGH);
    delay(delays[i]);
    digitalWrite(leds[i], LOW);
    delay(50); // Common delay after each LED blinks
  }
}
```

## Lab -3(Dimming LED)

Parameter for the LED Datashet

| parameters | value |
|------------|-------|
|MAX Forward Current|30mA|
|Forward Voltage|1.85V|
|Dominant Wavelength|640nm|
|Colour|Red|
|Total Capacitance|  45pF |
|Operating Range|-45 to 85C|

```c
int led = 13;
int led2 = 2;
int brightness=0;
int fadeAmount=5;

void setup() {
  //initialize digital pin LED_BUILTIN as an output.
  pinMode(led, OUTPUT);
  pinMode(led2, OUTPUT);
 
}

// the loop function runs over and over again forever
void loop() {
 analogWrite(led,brightness);
 analogWrite(led2,brightness);

 brightness=brightness + fadeAmount;

 if( brightness<=0 || brightness>=255 ){
  fadeAmount=-fadeAmount;
 }
 delay(30);
 }
```

## Lab-4(OLED)

```C
#include<SPI.h>
#include<Wire.h>
#include<Adafruit_GFX.h>
#include<Adafruit_SSD1306.h>

#define SCREEN_WIDTH 128 //OLED DISPLAY WIDTH
#define SCREEN_HEIGHT 64
#define OLED_RESET 4
#define SCREEN_ADDRESS 0X3C
Adafruit_SSD1306 display(SCREEN_WIDTH,SCREEN_HEIGHT,&Wire,OLED_RESET);

void setup(){
  Serial.begin(9600);
  if(!display.begin(SSD1306_SWITCHCAPVCC,SCREEN_ADDRESS)){
    Serial.println(F("SSD1306 allocation failed"));
    for(;;);
  }

delay(100);
display.clearDisplay();
display.setTextSize(1);
display.setTextColor(SSD1306_WHITE);
display.setCursor(0,0);
display.println(F("HELLO SILICONITES!!!"));
display.display();
delay(2000);
}
void loop(){}
```
## Lab-5(Temperature Sensor)
```c
#include<Wire.h>
#include<Adafruit_GFX.h>
#include<Adafruit_SSD1306.h>
#include<Adafruit_Sensor.h>
#include "DHT.h"

#define SCREEN_WIDTH 128 //128OLED DISPLAY WIDTH
#define SCREEN_HEIGHT 64

Adafruit_SSD1306 display(SCREEN_WIDTH,SCREEN_HEIGHT,&Wire,-1);

#define DHT11PIN 4

#define DHTTYPE DHT11
DHT dht(DHT11PIN, DHTTYPE);

void setup(){
  Serial.begin(9600);
  dht.begin();

  if(!display.begin(SSD1306_SWITCHCAPVCC,0X3C)){
    Serial.println(F("SSD1306 allocation failed"));
    for(;;);
  }
  delay(2000);
  display.clearDisplay();
  display.setTextColor(WHITE);
}

void loop(){
  delay(5000);

  float humi = dht.readHumidity();
  float temp = dht.readTemperature();
  if(isnan(humi)||isnan(temp)){
    Serial.println("Failed to read from DHT sensor!");
  }

  display.clearDisplay();

display.setTextSize(1);
display.setTextColor(SSD1306_BLACK,SSD1306_WHITE);
display.setCursor(0,0);
display.print("temperature");
display.setTextSize(2);
display.setTextColor(SSD1306_BLACK,SSD1306_WHITE);
display.setCursor(0,10);
display.print(temp);
display.print(" ");
display.setTextSize(2);
display.print("C");


display.setTextSize(1);
display.setTextColor(SSD1306_BLACK,SSD1306_WHITE);
display.setCursor(0,35);
display.print("HUMIDITY");
display.setTextSize(2);
display.setTextColor(SSD1306_BLACK,SSD1306_WHITE);
display.setCursor(0,45);
display.print(humi);
display.print(" %");

display.display();
}
```

## Lab-6(Introduction to LoRa )
### Programming for transmission
```c
#include<SPI.h>
#include<LoRa.h>

//std configuration
//#define DIO0 2
//#define RST 14
//#define NSS 3
//#define MOSI 23
//#define MISO 19
//#define SCLK 18

#define DIO0 26
#define RST 14
#define NSS 18
#define MOSI 27
#define MISO 19
#define SCLK 5

int counter=0;

void setup(){
  //initiliazing serial monitor
  Serial.begin(115200);
  while(!Serial);
  Serial.println("LoRa Sender");

  //setup LoRa tranceiver module
  SPI.begin(SCLK,MISO,MOSI,NSS);
  LoRa.setPins(NSS,RST,DIO0);

  //replace the lora.begin(---E-)
  // 433E6 FOR ASIA
  // 866E6 FOR EUROPE
  // 915E6 FOR NORTH AMERICA
while(!LoRa.begin(433E6)){
  Serial.println(".");
  delay(500);
}
//change sync word 0xF3 to match reciever
//the sync word assures you dont gets LoRa message from other LoRa transceiver
//ranges from 0-0xFF
LoRa.setSyncWord(0XF3);
Serial.println("LoRa Initializing OK !");
}

void loop(){
  Serial.println("sending packet");
  Serial.println(counter);

  //send LoRa packet to recieve

  LoRa.beginPacket();
  LoRa.print("hello...");
  LoRa.print(counter);
  LoRa.endPacket();

  counter++;

  delay(1000);
}

```
### Programming for reciever
```c
#include<SPI.h>
#include<LoRa.h>

//std configuration
//#define DIO0 2
//#define RST 14
//#define NSS 3
//#define MOSI 23
//#define MISO 19
//#define SCLK 18

#define DIO0 26
#define RST 14
#define NSS 18
#define MOSI 27
#define MISO 19
#define SCLK 5


void setup(){
  //initiliazing serial monitor
  Serial.begin(115200);
  while(!Serial);
  Serial.println("LoRa Sender");

  //setup LoRa tranceiver module
  SPI.begin(SCLK,MISO,MOSI,NSS);
  LoRa.setPins(NSS,RST,DIO0);

  //replace the lora.begin(---E-)
  // 433E6 FOR ASIA
  // 866E6 FOR EUROPE
  // 915E6 FOR NORTH AMERICA
while(!LoRa.begin(433E6)){
  Serial.println(".");
  delay(5000);
}
//change sync word 0xF3 to match reciever
//the sync word assures you dont gets LoRa message from other LoRa transceiver
//ranges from 0-0xFF
LoRa.setSyncWord(0XF3);
Serial.println("LoRa Initializing OK !");
}

void loop() {
  // try to parse packet
  int packetsize = LoRa.parsePacket();
  if(packetsize){
    Serial.println("Recieving Packet:");
  }
  while(LoRa.available()){
    String LoRaData = LoRa.readString();
    Serial.print(LoRaData);
  }
    Serial.print("`with RSSI");
    // RSSI - recieved signal strength indicator
    Serial.print(LoRa.packetRssi());
    Serial.println("C");
  }
```
