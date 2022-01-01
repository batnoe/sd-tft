# -------------------- SD-TFT ----------------------------
 
Essai de fonctionnement d'une carte sd sur un écran tft 3.5 (9486)

Enregistrement de la température extérieur toutes les 5 minutes sur la carte sd

                  DATE        HEURE       TEMPERATURE

// Pour ESP32 DEVKIT Wroom et TFT 3.5 ILI9486

// Test avec carte sd et sonde bme280

#define ESP32_PARALLEL

#define ILI9486_DRIVER

#define TFT_CS 33 // Chip select control pin (library pulls permanently low

#define TFT_DC 15 // Data Command control pin - must use a pin in the range 0-31

#define TFT_RST 32 // Reset pin, toggles on startup

#define TFT_WR 4 // Write strobe control pin - must use a pin in the range 0-31

#define TFT_RD 2 // Read strobe control pin

#define TFT_D0 12 // Must use pins in the range 0-31 for the data bus

#define TFT_D1 13 // so a single register write sets/clears all bits.

#define TFT_D2 26 // Pins can be randomly assigned, this does not affect

#define TFT_D3 25 // TFT screen update performance.

#define TFT_D4 17

#define TFT_D5 16

#define TFT_D6 27

#define TFT_D7 14

#define LOAD_GLCD   // Font 1. Original Adafruit 8 pixel

#define LOAD_FONT2  // Font 2. Small 16 pixel high font

#define LOAD_FONT4  // Font 4. Medium 26 pixel high

#define LOAD_FONT6  // Font 6. Large 48 pixel
#define LOAD_FONT7  // Font 7. 7 segment 48 pixel
#define LOAD_FONT8  // Font 8. Large 75 pixel
#define LOAD_GFXFF  // FreeFonts.

#define SMOOTH_FONT

--------------- SD card -------------------

SD SS  D5 CS

SD DI D23 MOSI

SD DO D19 MISO

SD SCK  D18 CLK