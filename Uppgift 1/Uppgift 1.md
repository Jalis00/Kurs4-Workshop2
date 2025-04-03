Mål
Ta reda på vad som behövs för att skapa lösningen på problemet.
Identifiera relevanta portar, bibliotek och alternativa lösningar.

1. Simulering av temperatursensorn
För att få temperatursensorn TMP36 att ge olika värden i en simulering kan vi:
Använda en potentiometer i TinkerCAD för att simulera temperaturvariation.
Manuellt justera spänningen till sensorn i TinkerCAD.
Programmera en slumpgenerator i koden för testsyfte (ej realistiskt, men bra för debug).
Exempel: Simulerad temperatur med slumpgenerering
float getSimulatedTemperature() {
    return random(200, 350) / 10.0; // Simulerar 20.0 till 35.0 grader C
}

2. Portar för komponenter
Förslag på anslutningar:
Komponent
Porttyp
Rekommenderad port
LCD 16x2 (I2C)
Digital
A4 (SDA), A5 (SCL)
Temperatursensor (TMP36)
Analog
A0
Numpad
Digital
2, 3, 4, 5, 6, 7, 8, 9

Följdfråga: Räcker portarna?
Arduino UNO har 14 digitala portar och 6 analoga portar, vilket räcker för denna uppgift.
Alternativ lösning om portar saknas:
Multiplexer (t.ex. 74HC4051) för att expandera analoga portar.
Shift register (74HC595) för fler digitala utgångar.
Använda en I2C-kompatibel Numpad för att spara digitala portar.

3. Bibliotek som behövs
Interna bibliotek (finns i Arduino IDE)
Bibliotek
Användning
LiquidCrystal
Styrning av LCD-display
Keypad
Hantering av Numpad

Externa bibliotek (behöver installeras)
Bibliotek
Användning
Adafruit_Sensor
Generisk sensorhantering
Adafruit_GFX
Grafiska funktioner för display
Adafruit_LiquidCrystal
Alternativ LCD-kontroll

Installera bibliotek i Arduino IDE:
Gå till Sketch > Include Library > Manage Libraries.
Sök efter biblioteket och klicka Install.
Installera bibliotek i PlatformIO:
Kör följande i terminalen:
pio lib install "Adafruit GFX Library"
pio lib install "Adafruit LiquidCrystal"

4. Bättre referenslistor för bibliotek
Interna (Arduino) bibliotek
Arduino Libraries Official Docs
Built-in Libraries List
Externa bibliotek och resurser
PlatformIO Library Manager
Adafruit Libraries

Sammanfattning
Vi kan simulera temperaturändringar i TinkerCAD med en potentiometer eller kod.
Rekommenderade portar har valts för varje komponent.
Om portar inte räcker kan vi använda en multiplexer eller I2C-kompatibla enheter.
Lista över både interna och externa bibliotek har sammanställts.
Instruktioner för att installera bibliotek i både Arduino IDE och PlatformIO.
