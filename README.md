# Workshop 02: Moduler & Bibliotek

## Kursinformation
**Kurs:** Systemutvecklare C/C++ Extended 2024  
**Klass:** SUVx24  
**Teknikområde:** Systemutveckling i Inbyggda system - Moduler & Bibliotek  

## Learning Target
- Förklara grunderna i hårdvarukomponenter och deras interaktion med mjukvarulösningar i inbyggda system.
- Använda mjukvarubibliotek för att få komponenter eller moduler att fungera med det inbyggda systemet.

---

## Introduktion
För att få olika komponenter eller moduler att fungera med Arduino-systemet behövs mjukvara som antingen följer med Arduino IDE eller som tillverkaren förser oss med i form av ett bibliotek (library) vi kan lägga till vår programkod.

## Förberedelse
1. Skapa en ny projektmapp i den projektmapp du använder för kodning:  
   ```sh
   mkdir -p C:/Chas/SUVx24/kurs4/Workshop2/
   ```
2. Alternativt använd GitHub och skapa ett repository för denna workshop.
3. Spara alla relaterade filer till workshopen antingen i denna mapp eller på repot.
4. Skapa gärna en MD-fil (`README.md`) för att:
   - Anteckna viktiga saker
   - Spara bra länkar
   - Göra en ToDo-lista

## Installation
🔹 Steg 1: Klona repot (om du inte redan gjort det)
Om du inte har repot på din dator ännu, klona det:

sh
Kopiera
Redigera
git clone https://github.com/Jalis00/Kurs4-Workshop2.git
cd Kurs4-Workshop2
2. Öppna projektmappen i Arduino IDE eller PlatformIO.

## Workshop: Använda mjukvarubibliotek för att programmera en hårdvarulösning

### Problembeskrivning
Skapa en TinkerCAD-lösning för:
- En Arduino UNO med en temperatursensor (typ TMP36), LCD 16x2 och en Numpad.
- Visa temperatur på displayen.
- Möjlighet att växla mellan temperatur i Celsius, Fahrenheit och Kelvin.
- Displayen och Numpad ska användas för att interagera med systemet.

### Uppgift 1: Research
**Mål:** Identifiera vad som behövs för att skapa lösningen.

**Att göra:**
- Hur kan vi simulera olika temperaturvärden i TinkerCAD?
- Vilka portar ska användas för:
  - LCD 16x2
  - Temperatursensor
  - Numpad
  - Räcker Arduinons portar? Om inte, finns alternativa lösningar?
- Vilka bibliotek behöver vi?
  - Lista de interna och externa biblioteken.
  - Hitta en bättre referenslista än Arduino Docs.
  - Finns motsvarande installationsguide för PlatformIO?

| Komponent       | Anslutning         |
|----------------|------------------|
| LCD 16x2      | Digitala portar  |
| TMP36 Sensor  | Analog port A0   |
| Numpad        | Digitala portar  |

### Uppgift 2: Skapa hårdvarulösningen i TinkerCAD
**Mål:** Koppla ihop komponenterna i TinkerCAD.

**Att göra:**
- Koppla samman:
  - Arduino UNO
  - LCD 16x2
  - Numpad
  - Temperatursensor
  - Komponent för att simulera temperaturvariation

![Projektbild](bilder/workshop2-setup.png)

### Uppgift 3: Programmera lösningen i TinkerCAD
**Mål:** Skapa mjukvarulösningen.

**Att göra:**
- Programmera och använd nödvändiga bibliotek för att få komponenterna att fungera.
- UI-design:
  - Hur gör vi systemet självförklarande utan användarmanual?

### Uppgift 4: Extra (Om tid finns)
- Vad finns det för vidareutvecklingsmöjligheter för denna lösning?

## TODO
- [ ] Skapa en TinkerCAD-simulation
- [ ] Programmera lösningen
- [ ] Dokumentera användning av bibliotek
- [ ] Utvärdera UI/UX för användarvänlighet
- [ ] Utforska vidareutvecklingsmöjligheter

## Referenser
- [Arduino Docs](https://docs.arduino.cc/)
- [PlatformIO Documentation](https://docs.platformio.org/)
- [TinkerCAD](https://www.tinkercad.com/)

