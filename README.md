# TFT
ESP32 + RPi  LCD (A) v3 demo XPT2046 base on ILI9486 DRIVER

## Wire connection

```mermaid
graph LR;
    XPT2046-->2[[+5V 2]];
    XPT2046-->14[[GND 14]];
    XPT2046-->18[[DC 18]];
    XPT2046-->22[[RST 22]];
    XPT2046-->24[[CS 24]];
    XPT2046-->26[[T_CS 26]];
    XPT2046-->19[[MOSI 19]];
    XPT2046-->21[[MISO 21]];
    XPT2046-->23[[SLK 23]];
    XPT2046-->25[[GND 25]];
    XPT2046-->1[[3V 1]];
    
    VIN[[VIN +5V]]-->ESP32
    GND1[[GND]]-->ESP32
    GND2[[GND]]-->ESP32
    G19[[GPIO19]]-->ESP32
    G23[[GPIO23]]-->ESP32
    G22[[GPIO22]]-->ESP32
    G18[[GPIO18]]-->ESP32
    G15[[GPIO15]]-->ESP32
    G2[[GPIO2]]-->ESP32
    G4[[GPIO4]]-->ESP32
    3V3[[3V3]]-->ESP32
    
    14 o--o GND1
    25 o--o GND2
    2 o--o VIN
    18 o--o G2
    22 o--o G4
    24 o--o G15
    26 o--o G22
    19 o--o G23
    21 o--o G19
    23 o--o G18
    1 o-.-o |Optional| 3V3
    
```


# PinOut

## ESP32
![image](images/esp32wroom-32_pinout.png)

## XPT2046
![image](images/XPT2046.png)

Key Parameters
SKU 	MPI3501
LCD Type 	TFT
LCD Interface 	SPI(Fmax:32MHz)
Touch Screen Type 	Resistive
Touch Screen Controller 	XPT2046
Colors 	65536
Driver IC 	ILI9486
Backlight 	LED
Resolution 	320*480 (Pixel)
Backlight Current 	120ma
Power Dissipation 	0.13A*5V
Operating Temp. (℃) 	-20~60
Active Area 	48.96x73.44(mm)
Product Size 	85.42*55.60(mm)
Package Size 	118*72*34 (mm)
Rough Weight(Package containing) 	75 (g) 

![image](https://user-images.githubusercontent.com/5806935/178270347-23dba539-70a3-4037-b3df-91a2340550ac.png)


# Sources
## XPT2040

[LCD Wiki](http://www.lcdwiki.com/3.5inch_RPi_Display)
[Another LCD shares](https://www.waveshare.com/wiki/3.5inch_RPi_LCD_(C))
[XPT2046 tough arduino libray](https://github.com/PaulStoffregen/XPT2046_Touchscreen)

## ESP32

[ESP32 pinout](https://www.studiopieters.nl/esp32-pinout/)
[XPT2046 Touch with ESP32](https://www.hackster.io/nash-ali/using-the-ili9341-tft-xpt2046-touch-with-esp32-arduino-ac8eed)
