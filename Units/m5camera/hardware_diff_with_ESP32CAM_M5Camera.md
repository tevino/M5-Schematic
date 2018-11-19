# Schematic difference with ESP32CAM and M5Camera

## PinMap

**Camera Interface PinMap**

| *Interface*             | *Camera Pin*| *Alternate ESP32 Pin Mapping* | *ESP32Cam*    | *M5Camera*  |
| :-------------------  | :--------:| :-------------------------: | :--------:  | :------:  |
| SCCB Clock            | SIOC      | IO23                        | IO23        |IO23       |
| SCCB Data             | SIOD      | IO25                        | IO25        |IO25       |
| System Clock          | XCLK      | IO27                        | IO27        |IO27       |
| Vertical Sync         | VSYNC     | IO22                        | IO22        |IO22       |
| Horizontal Reference  | HREF      | IO26                        | IO26        |IO26       |
| Pixel Clock           | PCLK      | IO21                        | IO21        |IO21       |
| Pixel Data Bit 0      | D2        | IO35                        | IO17        |IO32       |
| Pixel Data Bit 1      | D3        | IO17                        | IO35        |IO35       |
| Pixel Data Bit 2      | D4        | IO34                        | IO34        |IO34       |
| Pixel Data Bit 3      | D5        | IO5                         | IO5         |IO5        |
| Pixel Data Bit 4      | D6        | IO39                        | IO39        |IO39       |
| Pixel Data Bit 5      | D7        | IO18                        | IO18        |IO18       |
| Pixel Data Bit 6      | D8        | IO36                        | IO36        |IO36       |
| Pixel Data Bit 7      | D9        | IO19                        | IO19        |IO39       |
| Camera Reset          | RESET     | IO15                        | IO15        |IO15       |
| Camera Power Down     | PWDN      | *see Note 3*                | *see Note 3* | *see Note 3* |
| Power Supply 3.3V     | 3V3       | 3V3                         | 3V3         | 3V3       |
| Ground                | GND       | GND                         | GND         | GND       |

Notes:

3. **Camera Power Down** pin does not need to be connected to ESP32 GPIO. Instead it may be pulled down to ground with 10 kOhm resistor.

**GROVE Interface**

| *Grove*         | *ESP32Cam*    | *M5Camera*  |
| :-----------: | :--------:  | :------:  |
| G13           | IO12        | IO13      |
| G13           | IO12        | IO12      |
| 5V            | 5V          | 5V        |
| GND           | GND         | GND       |

**BME280 Interface**

| *BME280*         | *ESP32Cam*    | *M5Camera*  |
| :-----------: | :--------:  | :------:  |
| SCL           | IO4         | IO23      |
| SDA           | IO13        | IO22      |


**MPU6050 Interface**

| *MPU6050*         | *ESP32Cam*    | *M5Camera*  |
| :-----------: | :--------:  | :------:  |
| SCL           | IO4         | IO23      |
| SDA           | IO13        | IO22      |

**MIC(SPM1423) Interface**

| *MPU6050*            | *M5Camera*  |
| :-----------: | :------:  |
| SCL           | IO2      |
| SDA           | IO4      |

**MIC(SPQ2410) Interface**

| *MPU6050*            | *ESP32Cam*  |
| :-----------: | :------:  |
| SCL           | IO32      |

**LED Interface**

| *LED*         | *ESP32Cam*    | *M5Camera*  |
| :-----------: | :--------:  | :------:  |
| LED_Pin           | IO16        | IO14      |