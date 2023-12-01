# Voorbereiding S3

<!-- toc -->

- [Voorbereiding S3](#voorbereiding-s3)
- [Opbouw van dit document](#opbouw-van-dit-document)
- [Geprioriteerde lijst met actuele TODO's](#geprioriteerde-lijst-met-actuele-todo's)
- [Wat eerste hoofdvragen](#wat-eerste-hoofdvragen)
- [Uitgangspunten](#uitgangspunten)
- [Mogelijke opsplitsing van de onderwerpen over S3 en S4 met minimale dependencies en voorbeelden van bijbehorende projecten](#mogelijke-opsplitsing-van-de-onderwerpen-over-s3-en-s4-met-minimale-dependencies-en-voorbeelden-van-bijbehorende-projecten)
  - [Semester 3 Real Time Advanced Coding](#semester-3-real-time-advanced-coding)
  - [Semester 4 Large Complex Systems](#semester-4-large-complex-systems)
  - [Projectideëen voor S3](#projectideëen-voor-s3)
    - [Lasergame](#lasergame)
    - [Project: Ontwikkeling van een Prototype Smart Laadstation (voor Alfen)](#project:-ontwikkeling-van-een-prototype-smart-laadstation-(voor-alfen))
    - [Een warmtepomp-systeem?](#een-warmtepomp-systeem?)
  - [Projectideëen voor S4](#projectideëen-voor-s4)
    - [PLC based besturingssysteem voor automatiseringsscenario's](#plc-based-besturingssysteem-voor-automatiseringsscenario's)
      - [VR simulatiegame](#vr-simulatiegame)
      - [Digital Twins](#digital-twins)
      - [AR assistent](#ar-assistent)
- [Organisatie](#organisatie)
  - [Team](#team)
  - [Bijeenkomsten S3](#bijeenkomsten-s3)

<!-- tocstop -->

# Opbouw van dit document

Dit document is een soort overzicht van "Samenvattingen/Belangrijkste topics/Huidige Stand van Zaken". Voor details wordt gelinkt naar andere documenten, zoals verslagen van meetings en andere documenten die er aan ten grondslag liggen..

Om te beginnen:

- Actuele TODO's
- Wat eerste hoofdvragen
- Uitgangspunten

# Geprioriteerde lijst met actuele TODO's

Onderstaand is een lijst met actuele TODO's voor de korte termijn (komende weken):

- Formulering beroepstaken en leeruitkomsten afronden voor S3
- Meteen ook formulering beroepstaken en leeruitkomsten afronden voor S4
- Zoeken naar geschikte projecten voor S3
- Leerdoelen opstellen
- Portfolio items maken
- S3 git creëeren naar analagon van de S2 site.
- Lesmateriaal etc. aan toevoegen

# Wat eerste hoofdvragen

- Wat moet de Technish Informaticus die de HU verlaat minimaal kunnen na S3 en S4 (zowel professioneel als technisch inhoudelijk)?
- Waarvoor is draagvlak binnen het docententeam?
- Hoe kunnen we het technisch inhoudelijke deel het best verdelen over S3 en S4?
- Welke projecten van welke bedrijven zijn geschikt voor S3?
- Welke projecten van welke bedrijven zijn geschikt voor S4?
- Hoe ziet het toplevel treintje van beroepstaken en leeruitkomsten, opgesplitst in tijd naar a en b er uit voor S3 en S4? (Studenten doen dus S3a S4b of S4a S3b).
- Hoe gaan we de S3 ontwikkeling organiseren?

# Uitgangspunten

Beschikbare uitgangspunten zijn onderstaand opgesomd.
In het document [S3_kickoff_27_nov_2023](../S3_kickoff_27_nov_2023/S3_kickoff_27_nov_2023.md) worden de er aan voorafgaande bulletpoints in meer detail samengevat en besproken. Ook de uitkomsten van de nabespreking van de betreffende kickofmeeting zijn er te vinden.

- [Toetsprogramma TI_2026.ppt (15 juni 2023)](../Bronnen/Toetsprogramma_TI_2026.pptx)

- [Document BrainStorm met Bedrijven (17 feb 2022).pdf](../Bronnen/Brainstorm_met_bedrijven_2022_02_17.pdf)

- [Vacature-onderzoek_2023_11_24](../Bronnen/VacatureOnderzoek_2023_11_24/VacatureOnderzoek_2023_11_24.md)

- [Vacatureonderzoek_ASML_2023_11_26](../Bronnen/Vacatureonderzoek_ASML_2023_11_26/Vacatureonderzoek_ASML_2023_11_26.md)

- [Workshop Op weg naar HBO ICT (ihb S2, 5 sept 2023)](../Bronnen/Workshop_Op_weg naar_HBO_ICT.pdf)

- [S3_kickoff_27_nov_2023](../S3_kickoff_27_nov_2023/S3_kickoff_27_nov_2023.md).

- [Initiele formulering van Beroepstaak van S3](https://github.com/HU-TI-DEV/TI-S3)

# Mogelijke opsplitsing van de onderwerpen over S3 en S4 met minimale dependencies en voorbeelden van bijbehorende projecten

## Semester 3 Real Time Advanced Coding

- Wat Python
- Basisprincipes van Networking, Server, Database, Docker,
  REST, TCP/IP, HTML, CSS
- Software architectuur: van UseCase Diagram tot Code
- Algoritmen, datastructuren, design patterns.
- Multithreading - RTOS
- Frontend - Javascript

Semester 3 is dus een stap omhoog vanaf Semester 2, met diepgaander netwerk component en software architectuur.

## Semester 4 Large Complex Systems

- System Engineering (met Waterval) & Software Architectuur
- Optioneel: Hardware-heavy pad:
  - Wat electrotechniek
  - Besturingstechniek & Integratie van Actuatoren en Sensoren
  - Motoren aansturen 
  - Sub-keuzepaden:
    - Digitale techniek en PLC Programmeren (met ook wat alg en ds)
    - Robotica
- Optioneel: 
  - (simulatie-) Game maken.
  - Opties:
    - XR, AR, VR
    - Unity3d based, Unreal engine based

## Projectideëen voor S3

### Lasergame

- Het normproject voor het vinden van andere projecten is een uitgebreide uitvoering van een "lasergame ":
  - De laserguns zijn ESP32-based (gebruikmakend van **FreeRtos**)
  - Communiceren onderling met NEC **infrarood protocol**
  - Communiceren via **WIFI** met een server op een pc.
  - De **server** draait op een **python flask** applicatie. 
  - Er is ook een **frontend**, geschreven in **javascript, HTML en CSS**, via welke de game parameters ingesteld kunnen worden en de lopende game progress gemonitord kan worden. 
  - De resultaten kunnen worden opgeslagen in een **database** en later nog eens worden bekeken.

Bij de lasergame zijn er relatief weinig actuatoren (alleen, trilling generators en ir-leds). Het zou nog mooier zijn als er wat basic robotica bij komt kijken(lopende banden, etc).

### Project: Ontwikkeling van een Prototype Smart Laadstation (voor Alfen)

- **Doel**: Ontwerpen en ontwikkelen van een geïntegreerde softwareoplossing voor een smart laadstation voor elektrische voertuigen. Dit project zou gericht zijn op het integreren van embedded systemen (met focus op C en Python), remote monitoring, en power management.
- **Details**: Studenten ontwikkelen software voor embedded systemen die communiceren met een centrale server voor statusupdates en controle. Het project omvat aspecten van netwerkprotocollen, databasebeheer en mogelijk een eenvoudige frontend-interface voor monitoring en beheer.
  <mark>-> TODO: Meer informatie daarover proberen in te winnen.</mark>

### Een warmtepomp-systeem?

- Ik heb het gevoel dat warmtepompen eerder werken met PLC's dan met microcontrollers. In dat geval zou het interessanter zijn voor S4. Enfin, goed om uit te zoeken.
  <mark>-> TODO: Meer informatie daarover proberen in te winnen.</mark>

## Projectideëen voor S4

Het vinden van Projectideëen van S4 heeft op dit moment niet de prioriteit maar is goed om tijdens het zoeken naar projecten voor S3 in het achterhoofd te houden.

### PLC based besturingssysteem voor automatiseringsscenario's

- Een PLC-controlled warmtepompsysteem
  -> kan interessant zijn. Maar eerste prioriteit heeft het vinden van projecten voor de routes die breed draagvlak hebben (gaming, simulatie).

#### VR simulatiegame

- Training met varen van een schip
- Training met het plegen van onderhoud
- Training met wat voor situatie dan ook die anders duur of lastig zou zijn.

#### Digital Twins

- Robot, productielijn of wat dan ook programmeren en optimaliseren dmv digital twin.

#### AR assistent

- Voor orderpicking
- Voor onderhoud
- Voor whatever..

# Organisatie

## Team

Het team dat (initieel) aan S3 gaat werken bestaat uit:

- Harm
- Hagen
- Marius
- Arno

## Bijeenkomsten S3

  We komen op dinsdagmiddag bij elkaar.
