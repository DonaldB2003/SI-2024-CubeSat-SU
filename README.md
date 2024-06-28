# SI-2024-CubeSat-SU
Repository for summer internship 2024 "intro to CubeSat and Satellite Communication"

# Lab Exercises

## Lab-1 Introduction to ESP32

## Lab-2 Blinking LED

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
|MAXforward Current|30mA|
|Forward Voltage|1.85V|
|Dominant Wavelength|640nm|
|Colour|Red|
|Total Capacitance|  45pF |
|Operating Range|-45 to 85C|
