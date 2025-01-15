# 🛰️SI-2024-CubeSat-SU

🗄️ Repository for summer internship 2024 "intro to CubeSat and Satellite Communication"

![cube-1024x661](https://github.com/DonaldB2003/SI-2024-CubeSat-SU/assets/173866002/1522ad85-2467-4c02-b384-0174fc47d0be)

# ℹAbstract
The report encapsulates the comprehensive learning journey of the Summer Internship 2024 on Introduction to CubeSat and Satellite Communication, providing a deep dive into CubeSat fundamentals, satellite communication principles, LoRa protocol applications, and antenna design. Participants engaged in hands-on experiences including programming ESP32 platforms, configuring TinyGS ground stations, and simulating antenna designs using 4NEC2 software. Led by expert instructors from Silicon University and the Indian Institute of Space Science and Technology, alongside industry guidance from ToSpace, the internship fostered a practical understanding of aerospace technologies. Culminating in a project to design and implement ground stations, participants showcased their skills in a poster presentation, reinforcing their readiness for future endeavors in satellite engineering and space technology.

# Introduction📒

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
  <li>Mass=1.33kg </li>
  <li>allows for cost-effective development and deployment </li>
  <li>CubeSats have lower costs compared to large satellites.</li>
  <li>Shorter development times (CubeSats can be built within two years.)</li>
  <li>Flexible services(CubeSats can be used for different missions and purposes).</li>
</ul>

## History📖
The CubeSat concept originated in the late 1990s as a collaborative effort between Stanford University's Space Systems Development Laboratory (SSDL) and California Polytechnic State University (Cal Poly). Professors Bob Twiggs (Stanford) and Jordi Puig-Suari (Cal Poly) proposed the idea of a standardized, small satellite format to enable affordable space access for universities and other entities.

## CubeSat dispenser system
![nasa_iss_on_orbit_status_report_image_030617_945](https://github.com/DonaldB2003/SI-2024-CubeSat-SU/assets/173866002/45e17908-a8a4-44ae-afc5-d33e8230039e)

A CubeSat dispenser system is a critical component used to deploy CubeSats into orbit from a host satellite or launch vehicle. These systems are designed to securely hold CubeSats of various sizes, conforming to standard dimensions like 1U, 2U, or 3U, and ensure their safe release once the host satellite reaches its designated orbit. Integrated into the payload configuration of the launch vehicle, CubeSat dispensers typically employ mechanisms such as springs, pneumatic actuators, or mechanical latches to eject CubeSats at specified velocities and orientations. This controlled deployment process not only facilitates efficient utilization of launch vehicle payload capacity but also enables multiple CubeSats to be deployed in sequence, supporting diverse mission objectives including scientific research, Earth observation, technology demonstration, and educational initiatives. By simplifying and standardizing the deployment process, CubeSat dispenser systems contribute significantly to the accessibility and cost-effectiveness of space missions involving CubeSats.


## **Layers of CubeSat**
![Screenshot 2024-07-11 160347](https://github.com/DonaldB2003/SI-2024-CubeSat-SU/assets/173866002/d08f1305-1be7-4f56-8325-a75a60d7d034)
<ul>
  <li>layer 1-Antenna</li>
  <li>layer 2-communication radio</li>
  <li>layer 3-On Board Computer</li>
  <li>layer 4-Attitude control rods</li>
  <li>layer 5-power management system</li>
  <li>layer 6-magnet and battery</li>
</ul>

## Development Process Overview 📊

The overall timeframe can vary depending on the launch vehicles selected and what you are trying to accomplish with your CubeSat.
A CubeSat can be designed,bulit,tested and delivered in as little as 6 months,but it takes typically,18 to 24 months to complete. Once your CubeSat is delivered,the typical time to launch is anywhere from few months to few years.This is obviously affected by the availability of launch oppurtunities,but also by the feasibilty of your orbital requirements-the more flexible,the easier to manifest,and therefore the shorter wait.
Launch vehicles will usually require you to deliver your finished CubeSat between 4 to 6 months,prior to launch.
The project phases are as follows:
-  Concept Development(1-6 Months)
-  Securing Fundings (1-12 Months)
-  Merit and Feasibility Review(1-2 Months)
-  CubeSat Design(1-6 Months)
-  Development and Submittal of Proposal in response to CLSI call.(3-4 Months)
-  Selection and Manifesting(1-36 Months)
-  Mission Co-ordination(9-18 Months)
-  Licensing(4-6 Months)
-  Flight Specific Documentation and Development and Submittal(10-12 Months)
-  Groundstation Designs Development and Testing(2-12 Months)
-  CubeSat Hardware Fabrication and Testing(2-12 Months)
-  Mission Readiness Review(1/2 Day)
-  CubeSat to Dispenser Integration and Testing(1 Day)
-  Launch(1 Day)
-  Mission Operation(variable,upto 20 years)

## Block Diagram For communication

![communication](https://github.com/user-attachments/assets/a0ed18d1-cb8b-40e6-948e-94b4ebe79033)


## SPI Protocol🎩

**SPI** (Serial Peripheral Interface) is a synchronous serial communication protocol used for short-distance communication primarily between microcontrollers, sensors, and peripheral devices. Here are some key points about SPI:


**Basic Operation:** SPI operates in full-duplex mode, meaning data can be sent and received simultaneously. It uses four lines:

  -  SCLK (Serial Clock): Clock signal generated by the master device.
  -  MOSI (Master Out Slave In): Master sends data to slave.
  -  MISO (Master In Slave Out): Slave sends data to master.
  -  SS/CS (Slave Select/Chip Select): Used by the master to select which slave device to communicate with.
    
  
**Master-Slave Relationship:** In SPI communication, there is typically one master device that controls the communication and one or more slave devices that respond to the master.
  
**Clock and Data Transmission:** Data is transmitted in synchronized fashion with the clock. Each clock pulse (rising edge or falling edge, depending on configuration) typically corresponds to one bit of data being transmitted.

**Data Transfer Modes:** SPI can operate in different modes (0 through 3), which determine the polarity and phase of the clock signal. The modes are defined by:

**Clock Polarity (CPOL):** Determines the idle state of the clock (high or low).

**Clock Phase (CPHA):** Determines whether data is sampled on the leading or trailing edge of the clock pulse.

![phpcyBPrf](https://github.com/user-attachments/assets/2cd8e3ca-968f-4e12-8fae-2cf9d917a402)

**Advantages:**

- High speed: SPI can achieve high data transfer rates compared to other serial communication protocols.
- Simple hardware implementation: Requires minimal pins for communication.
- Full-duplex communication: Allows simultaneous data transmission and reception.
- Applications: SPI is commonly used in embedded systems, IoT devices, sensors, memory devices (like EEPROMs), ADCs (Analog-to-Digital Converters), DACs (Digital-to-Analog Converters), and many other peripherals where fast and reliable 
 serial communication is needed.

*SPI is a versatile and widely used protocol due to its simplicity, speed, and flexibility in connecting multiple devices. However, it is designed for communication over short distances within a single PCB or between closely located devices due to the lack of inherent noise immunity and clock synchronization mechanisms over longer distances.*


# MICRO PROCESSOR VS MICRO CONTROLER
![Difference-Microprocessor-vs-Microcontroller](https://github.com/DonaldB2003/SI-2024-CubeSat-SU/assets/173866002/ef18fda0-0041-48e6-9dc7-d66584efd79a)

## MICROCONTROLLER = MICROPROCESSOR+PERIPHERAL 

## PERIPHERAL
<ul>
<li>SPI/I2C/I2S/UART: Digital Serial data.</li>
<li>PWM: Pulse-Width Modulation</li>
<li>Touch Sensor: Capacitive touch screens, etc.</li>
<li>Timers</li>
<li>ADC: Analog to Digital Converter</li>
<li>DAC: Digital to Analog converter</li>
<li>Bluetooth</li>
<li>WiFi</li>
</ul>


ESP-32

![ESP32 BLOCK](https://github.com/DonaldB2003/SI-2024-CubeSat-SU/assets/173866002/5ec3834a-2b5e-4f80-9f7a-1f6c9c4a9648)



# Electromagnetic Spectrum

The electromagnetic spectrum refers to the entire range of wavelengths or frequencies of electromagnetic radiation, which includes all types of light. This spectrum ranges from very low-frequency radio waves to very high-frequency gamma rays. Here are the key segments of the electromagnetic spectrum, ordered from longest to shortest wavelengths (or lowest to highest frequencies):

![radio-frequency-bands](https://github.com/DonaldB2003/SI-2024-CubeSat-SU/assets/173866002/ac2d60d7-b8f9-4115-b2af-bab1424c9d72)




## EM Waves

![istockphoto-1194626452-612x612](https://github.com/DonaldB2003/SI-2024-CubeSat-SU/assets/173866002/5ed674c5-9d36-4051-8763-5a913fdb5083)

ν = c/λ
<ul>
  ν = 433MHz
  <li>λ=c/ν</li>
  <li>λ=0.692m</li>
</ul>


### VHF (Very High Frequency):
Refers to radio frequencies ranging from 30 MHz to 300 MHz. VHF frequencies are commonly used for FM radio broadcasting, television broadcasting (channels 2-13), maritime communication, air traffic control, and some military and government communication.

### UHF (Ultra High Frequency):
Refers to radio frequencies ranging from 300 MHz to 3 GHz. UHF frequencies are used for a variety of purposes including television broadcasting (channels 14-83 and above), satellite communication, cell phones, Wi-Fi, Bluetooth, and many two-way radios (walkie-talkies).


# Atmospheric attenuation

"Atmospheric attenuation refers to the reduction in electromagnetic radiation intensity as it travels through Earth's atmosphere. This occurs due to absorption, scattering (like Rayleigh and Mie scattering), and reflection by gases, aerosols, and water vapor. It affects various applications such as satellite communication, weather forecasting, and remote sensing, influencing the choice of frequencies used in these technologies."


![636541236646532654-Loss_V_Freq_Air](https://github.com/DonaldB2003/SI-2024-CubeSat-SU/assets/173866002/ddede805-3562-4e5e-a2e1-19576789e9cf)



## Carrier Frequency Selection Criteria
<ul>
  <li>Power Efficiency</li>
  <li>Bandwidth Efficiency</li>
  <li>System Complexity</li>
  <li>Frequency Allocation & Radiation</li>
</ul>


# Orbits🚀

## 4 Types of Orbit

There are several types of orbits that objects can follow around celestial bodies such as planets or stars.

![image](https://github.com/DonaldB2003/SI-2024-CubeSat-SU/assets/173866002/58fa41f0-29e9-4ad9-97f9-1c96d9a23d9c)

### Here are four common types of orbits:

-  **Low Earth Orbit (LEO):**
Orbits at altitudes typically between 160 kilometers (100 miles) and 2,000 kilometers (1,200 miles) above the Earth's surface. LEO is used by many satellites for Earth observation, communication, and scientific research.

-  **Geostationary Orbit (GEO):**
Orbits at an altitude of approximately 35,786 kilometers (22,236 miles) above the equator. Satellites in GEO orbits remain fixed relative to a point on Earth's surface, making them ideal for communication and weather satellites.

-  **Polar Orbit:**
Passes over Earth's poles, allowing satellites to observe the entire surface of the Earth over time as the planet rotates beneath the orbit. Polar orbits are used for Earth observation, mapping, and scientific research.

-  **Heliocentric Orbit:**
Orbits around the Sun rather than a planet. Planets, comets, and asteroids follow heliocentric orbits within our solar system. Spacecraft such as those sent to explore other planets or to study the Sun also follow heliocentric orbits.

"These different orbits serve various purposes depending on the mission objectives, including communication, Earth observation, scientific exploration, and more"

# Antenna

Antennas are devices used to transmit and receive electromagnetic waves, typically in the radio frequency (RF) range. They come in various types, each designed for specific applications based on factors like frequency range, directivity, and physical size

## Radiation
![OIP](https://github.com/user-attachments/assets/2609d44a-ab6f-49f1-b424-11b3af1949d1)

Radiation refers to energy that travels through space in the form of waves or particles. It can be categorized into ionizing radiation (such as X-rays and gamma rays) and non-ionizing radiation (like radio waves and visible light). Ionizing radiation has enough energy to remove tightly bound electrons from atoms, potentially causing damage to living tissues and DNA. Understanding and managing exposure to radiation is crucial in fields such as medicine, energy production, and space exploration.

## Mechanism Of Radiation

-  If a charge is not moving, current is not created and there is no radiation.
-  If charge is moving with a uniform velocity:
-  There is no radiation if the wire is straight, and infinite in extent.
-  There is radiation if the wire is curved, bent, discontinuous, terminated, or truncated.
-  If charge is oscillating in a time-motion, it radiates. even if the wira is straight.

## Two Wire Antenna and free space

![image](https://github.com/user-attachments/assets/4366861b-fa24-4596-b5c8-79e2557cdaeb)

## Formafion and detachment of free-wave from a Dipole Antenna

![image](https://github.com/user-attachments/assets/36a99b98-e329-47f6-bd60-9b5503755a80)


## Types Of Antennas

![OIP](https://github.com/user-attachments/assets/e2704399-78f4-4756-a47c-f152ce06c322)

-  **Dipole Antenna:**
  
![3ba1d7c4-a7f7-43bf-b5c1-a931ddcbce63](https://github.com/user-attachments/assets/b7508f4c-2fbd-45d5-a023-916cfb11c375)

Consists of two conductive elements (rods or wires) oriented in a straight line.
Simple and widely used for radio and television broadcasting, as well as in Wi-Fi routers.

-  **Yagi-Uda Antenna:**
  
![download](https://github.com/user-attachments/assets/b8078ef3-373a-405e-b790-2e4fedcd30b5)

Consists of multiple parallel elements (one driven element, one or more reflectors, and one or more directors).
Directional antenna used for long-distance communication, such as TV reception and amateur radio.

-  **Horn Antenna:**
  
![download](https://github.com/user-attachments/assets/bc3245d0-c6be-41c5-877b-d64b0c47176a)

Shaped like a pyramidal or conical horn.
Used for microwave frequencies, radar systems, and satellite communication due to its wide bandwidth and high gain.

-  **Parabolic Reflector Antenna:**
  
![OIP](https://github.com/user-attachments/assets/422e3142-1616-412e-9487-1265bc695318)

Consists of a large dish-shaped reflector and a small feed antenna at the focal point.
Provides high gain and is used for satellite communication, radio telescopes, and radar.

-  **Patch Antenna:**
 
![OIP](https://github.com/user-attachments/assets/4d8acfa9-ef49-4adb-8583-e41d66c230df)

Flat, rectangular antenna made on a printed circuit board.
Commonly used in mobile devices (like cell phones) and Wi-Fi routers due to their compact size and ease of integration.

-  **Loop Antenna:**
 
![OIP](https://github.com/user-attachments/assets/1b9aff37-3ceb-423f-bb0c-e5be18560d3b)

Consists of a loop of wire or conductor.
Used for receiving signals in AM radios and magnetic field sensing applications.

-  **Log-Periodic Antenna:**
  
![download](https://github.com/user-attachments/assets/d9d858ce-08a8-443e-89a1-afa62242a68b)

Consists of multiple dipole elements of varying lengths.
Provides a wide bandwidth and is used in broadband communication systems and television antennas.

-  **Helical Antenna:**
  
![OIP](https://github.com/user-attachments/assets/f402acba-fd52-4a29-8ca0-02c3718ebd4c)

Consists of a helix-shaped wire or conductor wound in a coil.
Used in satellite communication, GPS, and amateur radio due to its circular polarization and compact size.

-  **Microstrip Antenna:**
  
![OIP](https://github.com/user-attachments/assets/edc265ac-ac75-4a22-adca-b2acb1186258)

Made from a thin metal patch on a dielectric substrate.
Used in mobile phones, GPS devices, and wireless communication systems due to their low profile and ease of integration.



# Lab Exercises

## Lab-1 Introduction to ESP32:
<ul>
  <li>Install and configure Arduino IDE</li>
  <li>Introduction to ESP32 development kit.</li>
  <li>Write and execute a C-code to blink an LED on the dev board.</li>
</ul>

-[Datasheet ESP32](https://github.com/silicon-sat/SI-2024-CubeSat/blob/main/docs/Datasheet-ESP32.pdf)

**ESP-32**
The ESP32 is a powerful microcontroller with built-in Wi-Fi and Bluetooth capabilities, ideal for IoT projects. It features:
<ul>
<li>Dual-core processor: Runs at up to 240 MHz.</li>
<li>Low power consumption: Great for battery-operated devices.</li>
<li>Variety of GPIO pins: Supports various interfaces like SPI, I2C, UART, PWM, etc.</li>
<li>Rich development environment: Compatible with Arduino IDE, PlatformIO, and ESP-IDF.</li>

![347949728-5ec3834a-2b5e-4f80-9f7a-1f6c9c4a9648](https://github.com/user-attachments/assets/ed259ecf-81e2-40d7-897c-a7137e76329a)
</ul>


```C
#define LED_BUILTIN 2
void setup() {
  // initialize digital pin LED_BUILTIN as an output.
  pinMode(LED_BUILTIN, OUTPUT);
}

// the loop function runs over and over again forever
void loop() {
  digitalWrite(LED_BUILTIN, HIGH);  // turn the LED on (HIGH is the voltage level)
  delay(1000);                      // wait for a second
  digitalWrite(LED_BUILTIN, LOW);   // turn the LED off by making the voltage LOW
  delay(1000);                      // wait for a second
}
```



## Lab 2: Intro to GPIO programming

In this Lab exercise, students learn to configure a GPIO as an output and control an LED with it.

![esp32-devkit-v1-pinout-imicon-01-copy](https://github.com/user-attachments/assets/5817401d-406e-4832-806f-188978cfb6bd)


-[SOURCE FILE](LED/Aurdino/)

```C
#define LED 2
void setup() {
  // initialize digital pin LED_BUILTIN as an output.
  pinMode(LED_BUILTIN, OUTPUT);
}

// the loop function runs over and over again forever
void loop() {
  digitalWrite(LED, HIGH);  // turn the LED on (HIGH is the voltage level)
  delay(1000);                      // wait for a second
  digitalWrite(LED, LOW);   // turn the LED off by making the voltage LOW
  delay(1000);                      // wait for a second
}
```

## Lab -3(Dimming LED using PWM)💡
-In this exercise we used the ESP32 to control the light intensity of an external LED using PWM signal.
From the [LED Datasheet](https://github.com/silicon-sat/SI-2024-CubeSat/blob/main/docs/Datasheet-LED-XLMR01DE.pdf) tabulate the following data:
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






## Lab 4: Dimming multiple LEDs💡💡

ESP32 GPIO pins were used to dim multiiple LEDs with different delays.

![d2360516-8034-4558-91b5-4f4b3313295e](https://github.com/user-attachments/assets/816c42e8-678d-4443-aa0a-1899a5a82114)

Parameter for the LED Datashet

| parameters | value |
|------------|-------|
|MAX Forward Current|30mA|
|Forward Voltage|1.85V|
|Dominant Wavelength|640nm|
|Colour|Red|
|Total Capacitance|  45pF |
|Operating Range|-45 to 85C|

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

## Lab 5: Printing data in the serial monitor

-**Serial Monitor** is an essential tool when creating projects with Arduino. It can be used as a debugging tool, testing concepts, or communicating directly with the Arduino board.

-The **Arduino IDE 2** has the Serial Monitor tool integrated with the editor, which means that no external window is opened when using the Serial Monitor. This means that you can have multiple windows open, each with its own Serial Monitor.
```c
#include <Arduino.h>

void setup() {
  // Initialize Serial Monitor
  Serial.begin(115200);
}

void loop() {
  // Print "Hello" to Serial Monitor
  Serial.println("Hello");

  // Delay for 1 second (1000 milliseconds)
  delay(1000);
}

```


## Lab 6: Controlling an LED through serial monitor

Controlling an LED connected to ESP32 by reading commands from the serial monitor and turning the LED on or off based on those commands.

```c
//ESP32 TO serial monitor
#define LED 2

void setup(){
  Serial.begin(9600);
pinMode(LED, OUTPUT);
}

void loop(){
  if(Serial.available()){
    String command = Serial.readStringUntil('\n');
    
    if(command == "ON"){
      digitalWrite(LED, HIGH);
      Serial.println("Turn LED ON ");
    }
    else if (command == "OFF"){
      digitalWrite(LED, LOW);
      Serial.println("Turn LED OFF");

    }
  }

  
}
```

## Lab 7: I2C-based OLED Display control

I2C-based OLED pin details. Importing OLED libraries. Structure of the OLED. Displaying simple Text and Scrolling Text in different ways.

![cc4428ab-5a48-4624-ba07-d3a0e69c871d](https://github.com/user-attachments/assets/20e2e48b-122f-42df-bcb7-cf429225e76f)

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




## Lab 8: Introduction Signal Processing using Python
You can use lab1-fft.py and lab2-fsk.py as reference for the following exercises:
Write a python program to create a cosine wave of frequency 2MHz with 256 samples per cycle.
Plot it with proper annonation and axis labeling.
Compute the FFT of the above signal and plot it.
You will notice the FFT resolution is very limited for a single cycle.
Create another a signal of frequency 3MHz, add it to above signal and do FFT for the resultant signal.
Simulate lab2-fsk.py and anlayze the plot to understand FSK modulation.
Change the code such that the modulation frequency for 1 is 4MHz and for 0 it is 3MHz.
Change the above code to simulate ASK modulation.
Add demodulation to the above code and plot the time-domain waveform, as well as the FFT of the demodulated signal.
Add a moving average filter to remove the high-frequency component from the demodulated signal.

### sine wave

![lab-fsk](https://github.com/user-attachments/assets/58df6f40-b9b0-467f-bd31-57e3e06bcbbb)

![fftsin](https://github.com/user-attachments/assets/b73f870f-4485-4439-9b65-15f2b836a168)

```py
import numpy as np
import matplotlib.pyplot as plt

#Parameters
f_signal = 2e6  # 2 MHz signal frequency
fs = 0.5e9     # Sampling frequency (0.5 GHz)
num_samples = 256  # Number of samples
total_time = 500e-9  # Total time duration (500 ns)
time_period = 0.5e-6  # Time period of the signal (0.5 microseconds)

#Time vector
t = np.linspace(0, total_time, num_samples, endpoint=False)

#Generate sine wave
signal = np.sin(2 * np.pi * f_signal * t)

#Plotting
plt.figure(figsize=(10, 6))
plt.plot(t * 1e9, signal)  #, marker='o')
plt.title('2 MHz Sine Wave')
plt.xlabel('Time (ns)')
plt.ylabel('Amplitude')
plt.grid(True)
plt.show()

plt.tight_layout()
plt.show()
plt.savefig("lab-fsk.png")
```

### Modulation
```py
#!/usr/bin/env python3

import numpy as np
import matplotlib.pyplot as plt
from scipy.fft import fft, fftfreq
## For saving plots to a file. Just couldn't get it to work from commandline
import matplotlib
matplotlib.use('Agg')

# Parameters
fc0 = 4e6        # 1 Carrier Frequency
fc1 = 2e6        # 0 Carrier Frequency
fs = 256*4e6    # Sampling frequency
ncycl = 512          # No of cycles of fc 
nfc0 = 8        # number of fc0 cycles for one symbol
Tsim = ncycl/fc0       # Total Simulation time
t = np.arange(0, Tsim, 1/fs)  # Time vector

# Message signal (binary data)
data = np.random.randint(0, 2, int(ncycl/nfc0))  # Random binary data
nupData = int(t.size/data.size) 
data = np.repeat(data, nupData)  # Upsample binary data

# FSK Modulation
modulated_signal = np.zeros_like(t)
for i in range(len(t)):
    if data[i] == 0:
        modulated_signal[i] = np.cos(2 * np.pi * fc0 * t[i])
    else:
        modulated_signal[i] = np.cos(2 * np.pi * fc1 * t[i])

# FFT of the modulated signal
N = len(modulated_signal)
yf = fft(modulated_signal)
xf = fftfreq(N, 1 / fs)

# modulation
# Parameters for modulation
threshold = 0  # Decision threshold for modulation

# modulated data array
modulated_data = np.zeros_like(data)

# modulation loop
for i in range(len(t)):
    if np.cos(2 * np.pi * fc0 * t[i]) > threshold:
        modulated_data[i] = 0
    else:
        modulated_data[i] = 1

# Ensure demodulated data has the correct length (may be longer due to upsampling)
modulated_data = modulated_data[:data.size]

# Plotting
fig, axs = plt.subplots(4, 1, figsize=(10, 16))

axs[0].plot(t, data)
axs[0].set_title('Original Binary Data')
axs[0].set_xlim([0, Tsim])
axs[0].set_ylim([-0.2, 1.2])

axs[1].plot(t, modulated_signal)
axs[1].set_title('FSK Modulated Signal')
axs[1].set_xlim([0, Tsim])

axs[2].plot(xf, np.abs(yf))
axs[2].set_title('FFT of Modulated Signal')
axs[2].set_xlim([0, 2*fc0])
axs[2].set_xlabel('Frequency (Hz)')

axs[3].plot(t, modulated_data, marker='o', linestyle='-', color='b')
axs[3].set_title('modulated Binary Data')
axs[3].set_xlabel('Time (s)')
axs[3].set_ylabel('Binary Value')
axs[3].set_xlim([0, Tsim])
axs[3].set_ylim([-0.2, 1.2])
axs[3].grid(True)

plt.tight_layout()
plt.savefig("fsk-lab2.png")
plt.show()
```
![demodulation](https://github.com/user-attachments/assets/f42470f5-bce1-44cc-8887-c178199f7a58)

## Demodulation
```py

# Parameters
fc0 = 4e6        # 1 Carrier Frequency
fc1 = 2e6        # 0 Carrier Frequency
fs = 256*4e6    # Sampling frequency
ncycl = 512          # No of cycles of fc
nfc0 = 8        # number of fc0 cycles for one symbol
Tsim = ncycl/fc0       # Total Simulation time
t = np.arange(0, Tsim, 1/fs)  # Time vector

# Message signal (binary data)
data = np.random.randint(0, 2, int(ncycl/nfc0))  # Random binary data
nupData = int(t.size/data.size)
data = np.repeat(data, nupData)  # Upsample binary data

print(data.size, t.size)

# FSK Modulation
modulated_signal = np.zeros_like(t)
for i in range(len(t)):
    if data[i] == 0:
        modulated_signal[i] = np.cos(2 * np.pi * fc0 * t[i])*np.cos(2 * np.pi * fc0 * t[i])
    else:
        modulated_signal[i] = np.cos(2 * np.pi * fc1 * t[i])*np.cos(2 * np.pi * fc0 * t[i])

# FFT of the modulated signal
N = len(modulated_signal)
yf = fft(modulated_signal)
xf = fftfreq(N, 1 / fs)

# Plotting
fig, axs = plt.subplots(3, 1, figsize=(10, 12))

axs[0].plot(t, data)
axs[0].set_title('Original Binary Data')
axs[0].set_xlim([0, Tsim])
#axs[0].set_ylim([-0.2, 1.2])

axs[1].plot(t, modulated_signal)
axs[1].set_title('FSK DeModulation')
axs[1].set_xlim([0, Tsim])
                                                                                                                                                        axs[2].plot(xf, np.abs(yf))
axs[2].set_title('FFT of DeModulated Signal')
axs[2].set_xlim([0, 2*fc0])
axs[2].set_xlabel('Frequency (Hz)')

plt.tight_layout()
plt.savefig("fsk-demodulation-lab2.png")
plt.show()
```

![fsk-demodulation-lab2](https://github.com/user-attachments/assets/7835a516-0691-4310-8959-ea1308133588)




## Lab 9: I2C temperature sensor interface

![cf5729a0-1bd2-4b48-b892-6fc4948ee1ed](https://github.com/user-attachments/assets/65251995-6613-4899-8ec7-0e96cfb8c69b)

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





## Lab 10: Introduction to LoRa module

Introduction to architecture and pin configuration of Ra-02 Lora transceiver module and SPI (Serial Peripheral Interface) communication.

Key Features
-Long Range: Achievable distances from several kilometers up to 15 km or more.
-Low Power: Suitable for battery-operated devices, often using deep sleep modes.
-Low Data Rate: Typically supports data rates from 0.3 kbps to 50 kbps, which is sufficient for many IoT applications.

**Connect the LoRa module to your ESP32 (e.g., using SPI pins).**

|Module Pin	|Arduino Pin|
|-----------|-----------|
|VCC|3.3V|
|GND|GND|
|SCK|Pin 13|
|MOSI|Pin 11|
|MISO|Pin 12|
|NSS|Pin 10|
|RESET|Pin 9|
|DIO0|Pin 2|

**Ra-02 (SX1278)**

Frequency: 433/868/915 MHz
Range: Up to 15 km in rural areas
Interface: SPI
Commonly used with Arduino and ESP32.





## Lab 12: Communication between two LoRa nodes

Sending Text packets and receiving the text packets with *RSSI (Received Signal
Strength Indicator)* and SNR through Serial monitor.
Sending Temperature and humidity packets and receiving the same packets with RSSI (Received Signal Strength Indicator) and SNR through a Serial monitor as well as an OLED display.

### Programming for Transmitter Station

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
### Programming for Reciever Station
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
|Sl No.|Transmission Power|RSSI|🔺RSSI|
|------|------------------|----|-------|
|1|0|62.3|0|
|2|1|5|51.4|10.9|
|3|7|50.6|11.7|

## Lab 13: LoRa one-to-many communication setup

Sending data packets from one Lora transmitter to multiple Lora receivers and retracing the same packets.

![d2727fe6-5d07-46f3-9c0b-39a2f445ded9](https://github.com/user-attachments/assets/50f08491-6c53-44ea-8836-33d0de2a9624)


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






## Lab 14: Introduction to antenna modeling and simulation software 4NEC2.

**4NEC2** is a popular antenna modeling and simulation tool based on the Numerical Electromagnetics Code (NEC). It allows users to design, analyze, and optimize antennas by simulating their performance in various configurations.

### Key Features
  -  **Easy to Use:** User-friendly interface suitable for beginners and experienced users alike.

  -  **Versatile Modeling:** Supports various antenna types, including dipoles, Yagi-Uda, and more complex designs.

  -  **Visual Representation:** Provides graphical visualization of antenna geometry and radiation patterns.

  -  **Post-Processing:** Allows for in-depth analysis of results, including gain, radiation patterns, and impedance.






## Lab 15: Physical design of Dipole and V-dipole antennas

Tune it to 433MHz with the help of NanoVNA-A Portable VNA Antenna Analyzer Kit with 10KHz-1.5GHz, 2.8 Inch Digital LCD Display Touching Screen Standing Wave Measuring Instrument.

```txt
CM Example new :	Loaded dipole in free space
CM 		antenna design.txt
CE 					' End of comment
'


SY ylen=.1392				' Symbol: Length for WL/2
SY zlen=.0975
SY ysma=.004095
SY zsma=.002867	
'

GW  1  9  0  -ylen   zlen   0  -ysma  zsma   .0001	' Wire 1, 9 segments, halve wavelength long.
GW  2  9  0   ysma   zsma   0   ylen  zlen   .0001	' Wire 2, 9 segments, halve wavelength long.
GW  3  1  0  -ysma   zsma   0   ysma  zsma   .0001	' Wire 3, 9 segments, halve wavelength long
GE  0					' End of geometry
'


LD 5 1 0 0 5.8001E7			' Wire conductivity
LD 5 2 0 0 5.8001E7			
LD 5 3 0 0 5.8001E7			


'


EX 0 3 1 0 1 0				' Voltage source (1+j0) at wire 1 segment 5.


FR 0 1 0 0 433 0			' Set design frequency (433 Mc).

EN					' End of NEC input

```
![image](https://github.com/user-attachments/assets/bf7da8ba-95b8-4a00-b354-6a23631f242a)

![image](https://github.com/user-attachments/assets/5b4f47b9-ff8a-4d6e-a8b4-667a1a91bc43)



## Lab 16: Introduction to TinyGS

![images](https://github.com/user-attachments/assets/20129486-6c79-44f9-bf88-08e56c100df8)

https://tinygs.com/

**TinyGS** is a lightweight, open-source ground station software designed for receiving LoRaWAN and other types of satellite signals. It allows users to connect easily and manage their own ground station for satellite communication.

![image](https://github.com/user-attachments/assets/382cf837-3f2b-450d-bc98-c34d0015dd49)


### Key Features

   **Lightweight:** Optimized for performance on small hardware platforms.
   
   **Open Source:** Community-driven, enabling contributions and modifications.
   
   **Flexible Configuration:** Easily configure to work with different satellites and protocols.
   
   **Real-time Monitoring:** Provides live data reception and monitoring capabilities.
   






## Lab 17: Setting up a TinyGS ground station

![38e6e159-a341-4461-8edb-87557fabbab5](https://github.com/user-attachments/assets/0d9f3674-97c7-43f7-ab3b-f135bef59055)

1.**Hardware Requirements**
  1. **LoRa Module:** Common options include Ra-02.
  2. **Microcontroller:** Arduino, Raspberry Pi, or ESP32.
  3. **Antenna:** Compatible antenna for your LoRa module.
  4. **Power Supply:** Ensure stable power for your setup.


2.**Steps**
  1. Construct design of antenna using **4NEC2**
  2. Resister yourself in Tiny GS website
  3. Install algorithm from TinyGS website in **ESP-32**
  4. Tune it with the help of **VNA** and cutting plier
  5. setup your Ground Station
  6. wait till you recieve a data

### Packet recieved from the Satellite
we recieved around 61 packets from different satellites.
the data are given below:-

![image](https://github.com/user-attachments/assets/2d1c9958-ffb2-458d-80e9-63edfa376866)

**details:-**
[TinyGS_Record.1.xlsx](https://github.com/user-attachments/files/16200976/TinyGS_Record.1.xlsx)








## Lab 18: Processing TLE data with Python

**Using genAI tool (ChatGPT, CoPilot, etc) find out the detail about the satellite Two-Line Element (TLE) format.**

https://api.tinygs.com/v1/tinygs_supported.txt

**Write a Python programm to conver a TLE of satellite into a Lat/Long location.**

```py
rom skyfield.api import EarthSatellite, load
from datetime import datetime
import time
import webbrowser

def generate_maps_url(latitude, longitude):
    return f"https://www.google.com/maps/search/?api=1&query={latitude},{longitude}"

def main():
    try:
        # Prompt user to input TLE data
        print("Enter TLE data:")
        line1 = input("Enter line 1: ").strip()
        line2 = input("Enter line 2: ").strip()

        # Extract satellite name from line 1 if available
        satellite_name = line1.split()[1]

        # Load TLE data into a satellite object
        satellite = EarthSatellite(line1, line2, name=satellite_name)

        # Load timescale
        ts = load.timescale()

        while True:
            # Get current UTC time
            now = datetime.utcnow()

            # Compute satellite position at the current time
            t = ts.utc(now.year, now.month, now.day, now.hour, now.minute, now.second + now.microsecond / 1e6)
            position = satellite.at(t)

            # Get GeographicPosition object
            geo_position = position.subpoint()

            # Extract latitude, longitude, and altitude in degrees and kilometers
            latitude = geo_position.latitude.degrees
            longitude = geo_position.longitude.degrees

            print(f" ")
            print(f"{satellite_name}")
            print(f"Latitude, Longitude: {latitude}, {longitude}")

            # Calculate altitude (height above Earth's surface)
            distance_from_earth_center = position.distance().km
            radius_of_earth = 6371.0  # Radius of the Earth in kilometers
            altitude = distance_from_earth_center - radius_of_earth

            print(f"Altitude: {altitude} km")

            # Generate Google Maps URL
            maps_url = generate_maps_url(latitude, longitude)
            print(f"Google Maps URL: {maps_url}")

            # Open Google Maps in the default web browser
            webbrowser.open(maps_url)

            # Delay for a while before fetching the next position
            time.sleep(10)  # Fetch position every 10 seconds (adjust as needed)

    except KeyboardInterrupt:
        print("\nTerminated by user.")
    except Exception as e:
        print(f"Error occurred: {e}")

if _name_ == "_main_":
    main()
```


**Enter TLE data: TIANQI-23**

    Enter line 1: 1 57794U 23135C   24193.84851663  .00000031  00000-0  84750-4 0  9998

    Enter line 2: 2 57794  49.9717 238.8296 0014532 317.7298  42.2493 14.22337202 44201

**Generate the output as an URL that you can paste in a browser and get the satellite location.**

https://www.google.com/maps/place/25%C2%B024'17.5%22N+30%C2%B015'50.8%22W/@25.4048723,-30.2641009,17z/data=!3m1!4b1!4m4!3m3!8m2!3d25.4048723!4d-30.2641009?entry=ttu

![image](https://github.com/user-attachments/assets/ef600973-5b49-40b0-8bfb-035cf8087903)


And modify the above program such the TLE data file can be given as input with the two line numbers to process.


🙏 Acknowledgments:
This program would not have been possible without the guidance and support of my mentors *Dr. Saroj Rout* and teammates .Your expertise and encouragement have been instrumental in my learning and development.
Here is the link of full course described by Dr. Saroj Rout https://github.com/silicon-sat/SI-2024-CubeSat?tab=readme-ov-file


🚀 Looking Ahead:
While this internship marks the end of one chapter, it also ignites my enthusiasm for further exploration in aerospace technology and communication systems. This repository will remain a testament to the skills and knowledge I've gained, and I hope it serves as a helpful resource for others venturing into the field.

Thank you for visiting! 🌍🌌
