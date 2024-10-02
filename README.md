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

## Stap 4: 
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

<img width="502" alt="Scherm­afbeelding 2024-10-02 om 21 51 54" src="https://github.com/user-attachments/assets/17aecf89-b122-4141-a7fd-2e109f7f1761">

Er staat nu geen place holder tekst meer in dit gedeelte van de code

<img width="625" alt="Scherm­afbeelding 2024-10-02 om 21 48 35" src="https://github.com/user-attachments/assets/028ac1a6-a079-4524-b5b9-269d15ac9b19">

### Verbinding checken
Upload je code met de 2e blauwe knop in de linker bovenhoek

<img width="165" alt="Scherm­afbeelding 2024-10-02 om 21 55 16" src="https://github.com/user-attachments/assets/6c057045-84c8-49fa-8e75-dbd1cefe6fbe">


