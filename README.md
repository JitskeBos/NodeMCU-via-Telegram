# NodeMCU-via-Telegram
Door Jitske Bos Laatste update 2 oktober 2024 20:02

## Introductie
Met deze manual leer je hoe je een NodeMCU kan aansturen via Telegram. Hiervoor heb je de volgende dingen nodig:
1. Een Telegram account
2. NodeMCU Arduino Board, ESP8266

Wanneer je al een Telegram account hebt, kan je stap 1 overslaan.

## Stap 1: Telegram account aanmaken
Download Telegram op je mobiele telefoon

Volg de aanwijzingen in de app

## Stap 2: Maak een bot aan
Open in jouw brower de onderstaande link naar de chatbot van Telegram

https://telegram.me/BotFather

Klik vervolgens op Send Message

<img width="1440" alt="Scherm­afbeelding 2024-10-02 om 20 36 15" src="https://github.com/user-attachments/assets/310a7a38-826a-47d8-808a-ca370b5c25dd">

Druk onderaan het scherm op Start

<img width="878" alt="Scherm­afbeelding 2024-10-02 om 20 37 50" src="https://github.com/user-attachments/assets/6d54a862-8750-43ac-bc81-ff396e4a4385">

### Creëer een nieuwe bot

Typ in de chatbalk onderin

/newbot

<img width="569" alt="Scherm­afbeelding 2024-10-02 om 20 57 03" src="https://github.com/user-attachments/assets/e27bf65b-f624-4ce2-88ac-e4ab00e6acb6">

Verzin een leuke naam voor jouw chatbot!

Vul de naam van jouw chatbot in in de chatbalk

_Voor deze manual heb ik de naam JanMan gebruikt_

<img width="567" alt="Scherm­afbeelding 2024-10-02 om 21 01 59" src="https://github.com/user-attachments/assets/bd692787-c695-482c-a453-e9ce2f2ffdb0">

Geef je Bot een gebruikersnaam

**Let op:** deze gebruikers naam moet eindigen op _Bot_

Het kan zijn dat je meerdere keren een naam moet bedenken. Sommige gebruikersnamen zijn al in gebruik

<img width="567" alt="Scherm­afbeelding 2024-10-02 om 21 02 30" src="https://github.com/user-attachments/assets/8efe8fe6-ede5-4648-b778-c5d260046cf4">

## Stap 3: Arduino Libraries downloaden
Open de Arduino applicatie

Klik onder File op _New Sketch_

<img width="371" alt="Scherm­afbeelding 2024-10-02 om 21 20 02" src="https://github.com/user-attachments/assets/9253139f-db4a-4a96-bd53-44dbc96ca622">

Klik vervolgens op Tools -> Manage Libraries

<img width="778" alt="Scherm­afbeelding 2024-10-02 om 21 22 36" src="https://github.com/user-attachments/assets/9885d032-56ef-4f15-becc-b5adc866cb31">

Typ onder Library Manager _universaltelegrambot_ in

Installeer de onderstaande library die overeen komt met de ingevulde naam

<img width="275" alt="Scherm­afbeelding 2024-10-02 om 21 29 46" src="https://github.com/user-attachments/assets/d123e16a-7bbb-4f41-9bf5-f78aef059494">

Wanneer je op _Install_ hebt geklikt komt er een melding in beeld. Installeer ook de Library die wordt aangeboden

Dit doe je door op _Install All_ te klikken

<img width="633" alt="Scherm­afbeelding 2024-10-02 om 21 32 53" src="https://github.com/user-attachments/assets/f5a05a38-e5d0-4fa6-87a1-66edfc49e698">

De library is succesvol gedownload als de melding _Succesfully installed library UniversalTelegramBot:1.3.0_ rechts onder in beeld verschijnt

<img width="542" alt="Scherm­afbeelding 2024-10-02 om 21 41 44" src="https://github.com/user-attachments/assets/45801bc6-1a3d-47ec-8055-0b03f2453d31">

## Stap 4: WiFi connecten
Klik op File -> Examples

Scroll hier helemaal omlaag richting _UniversalTelegramBot_

Klik vervolgens op ESP8266 -> Echobot

<img width="1440" alt="Scherm­afbeelding 2024-10-02 om 21 37 53" src="https://github.com/user-attachments/assets/649f4cdc-9ea2-45ff-82a9-40a8904fbb0e">

Pas in de Arduino code de wifi instellingen aan

WIFI_SSID = de naam van je wifi netwerk

WIFI_PASSWORD = het wifi wachtwoord

<img width="636" alt="Scherm­afbeelding 2024-10-02 om 21 48 25" src="https://github.com/user-attachments/assets/6ab40bb9-98f7-4a62-8025-b91460388352">

Pas ook de BOT_TOKEN aan

Plak hier de persoonlijke API token die je chatbot in Telegram je heeft gegeven

Er staat nu geen place holder tekst meer in dit gedeelte van de code

### Verbinding checken
Upload je code met de 2e blauwe knop in de linker bovenhoek

<img width="165" alt="Scherm­afbeelding 2024-10-02 om 21 55 16" src="https://github.com/user-attachments/assets/6c057045-84c8-49fa-8e75-dbd1cefe6fbe">

De code wordt nu eerst gecontroleerd

<img width="554" alt="Scherm­afbeelding 2024-10-02 om 21 56 38" src="https://github.com/user-attachments/assets/d7336175-7212-4d17-ae83-4279c709839b">

Daarna wordt het geupload

<img width="825" alt="Scherm­afbeelding 2024-10-04 om 15 45 34" src="https://github.com/user-attachments/assets/c61ff0ea-8487-4f6e-a967-9b1109ab22f1">

### Serial Monitor uitlezen
Open de Serial Monitor door op de knop rechts boven in het scherm te klikken

<img width="217" alt="Scherm­afbeelding 2024-10-02 om 22 16 06" src="https://github.com/user-attachments/assets/73d1eeff-98f1-4c9a-97f2-7575bf9ef20f">

Wanneer je geen duidelijke taal te zien krijgt in je Serial Monitor, zoals in het voorbeeld hieronder, moet je de baud aanpassen

<img width="883" alt="Scherm­afbeelding 2024-10-04 om 15 51 24" src="https://github.com/user-attachments/assets/c07009ff-f9fa-4033-a66c-785e050da26a">

Klik op _9600 baud_, scroll omlaag en klik op _115200 baud_

<img width="180" alt="Scherm­afbeelding 2024-10-04 om 15 51 39" src="https://github.com/user-attachments/assets/49938d2a-3437-4cd4-96ab-4e4647dc688d">

Upload de code opnieuw

Nu zal er in de Serial Monitor weergeven worden dat er verbinding wordt gemaakt met de wifi die je net hebt ingesteld

<img width="883" alt="Scherm­afbeelding 2024-10-04 om 15 55 34" src="https://github.com/user-attachments/assets/e9cdf064-4523-4675-ac03-55438cc83f7f">

## Stap 5: Bot koppelen
Wanneer je nu een bericht stuurt naar jouw Bot in Telegram, zal deze dit bericht terugkaatsen

Doet het dit niet? Kijk dan of je je BOT_TOKEN goed hebt overgenomen

<img width="568" alt="Scherm­afbeelding 2024-10-04 om 16 00 09" src="https://github.com/user-attachments/assets/63d00666-61e0-43e4-8e29-2e13a0c9772a">

### Gesprek weergeven in Monitor
Voeg in de _void handleNewMessages_ de volgende code toe

```Inline
Serial.print(bot.messages[i].text);
```
Nu wordt de imput die jij stuur naar je Bot weergeven in de Serial Monitor

<img width="531" alt="Scherm­afbeelding 2024-10-04 om 16 12 47" src="https://github.com/user-attachments/assets/83e0d5cc-0c42-420d-a88c-c064712b961e">

<img width="278" alt="Scherm­afbeelding 2024-10-04 om 16 12 53" src="https://github.com/user-attachments/assets/cac6d4ae-d65e-419c-bef2-79c6c44b1b14">

### Antwoord toevoegen
Om je Bot een specifiek antwoord te laten geven op jouw input voeg je de volgende code toe aan de  _void handleNewMessages_

```Inline
bot.sendMessage(bot.messages[i].chat_id, "Alles goed kameraad?", "");
```

_De teksts tussen de "" kan vervangen worden door wat je zelf wilt. In dit voorbeeld gebruik ik "Alles goed kameraad?"_

<img width="530" alt="Scherm­afbeelding 2024-10-04 om 16 19 17" src="https://github.com/user-attachments/assets/8403e727-12a2-44f0-ab20-09549533f1a7">

## Stap 6: LED aansturen
Voeg aan de _void setup_ de volgende code toe

```Inline
pinMode(LED_BUILTIN, OUTPUT);  // Initialize the LED_BUILTIN pin as an output
```

Nu kan je het blauwe lampje op je NodeMCU aansturen

### Aan / uit
Om te zorgen dat het blauwe lampje aan en uit kan gaan moet er een _if statement_ toegevoegd worden aan de _void handleNewMessages_

```Inline
if (bot.messages[i].text == "Licht aan") {
      digitalWrite(LED_BUILTIN, LOW);
    }

else if (bot.messages[i].text == "Licht uit") {
      digitalWrite(LED_BUILTIN, HIGH);
    }
```

Stuur je je bot "Licht aan" dan zal het lampje aan gaan. Stuur je "Licht uit" dan gaat het uit.

Om zeker te weten dat de code goed wordt ontvangen kan je dit controleren in de Serial Monitor

Voeg dan de onderstaande code toe onder de _digitalWrite_ code

```Inline
Serial.print("...");
```

Vul op de "..." de tekst neer die weergeven moet worden als het statement wordt aangeroepen

<img width="638" alt="Scherm­afbeelding 2024-10-04 om 16 33 58" src="https://github.com/user-attachments/assets/611c015d-4846-45ec-8980-aeebf019f5cd">

Opload je code en test het met de Serial Monitor. Zie je dat het lampje aan en uit gaat?

<img width="533" alt="Scherm­afbeelding 2024-10-04 om 16 36 23" src="https://github.com/user-attachments/assets/338f09a6-50fa-4095-a1ab-c0f1a9104462">

<img width="452" alt="Scherm­afbeelding 2024-10-04 om 16 36 30" src="https://github.com/user-attachments/assets/d33f1656-19e8-4dc9-8cac-53bb0bbc056a">

## Stap 7: LED strip koppelen
Sluit je LED strip aan zoals je gewend bent

Zorg ervoor dat je de LED strip verbind met de code door de onderstaande code boven aan bij de andere #include in het bestand te zetten

```Inline
#include <Adafruit_NeoPixel.h>
#ifdef __AVR__
#include <avr/power.h>  // Required for 16 MHz Adafruit Trinket
#endif
#define PIN D1  // On Trinket or Gemma, suggest changing this to 1

// How many NeoPixels are attached to the Arduino?
#define NUMPIXELS 12  // Popular NeoPixel ring size

Adafruit_NeoPixel pixels(NUMPIXELS, PIN, NEO_GRB + NEO_KHZ800);
```
Hiermee kan je de LED strip gaan aanroepen

### Nieuwe code
In de if statement die we in de vorige stap hebben toegevoegd gaan we de LED strip aanroepen

Dat doe je door de de volgende code toe te voegen aan je _if statement_

```Inline
 for (int i = 0; i < NUMPIXELS; i++) {
        pixels.setPixelColor(i, pixels.Color(0, 150, 0));  // Stel elke pixel in op groen (RGB: 0, 150, 0)
      }
      pixels.show();
```
En deze code aan je _else if statement_

```Inline
      pixels.clear();
      pixels.show();
```

<img width="692" alt="Scherm­afbeelding 2024-10-04 om 17 43 25" src="https://github.com/user-attachments/assets/e7a9de43-1404-4414-ae69-735e49b59b3c">

Vergeet je code niet te valideren om te checken of alles goed is aangeroepen

Upload je code, en speel met je nieuwe licht aan licht uit systeem!
