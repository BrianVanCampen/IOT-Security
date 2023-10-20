# Logboek Week4

# cyberboswachters

De opkomst van wifi-netwerken heeft geleid tot meer vrijheid voor gebruikers, maar heeft ook beveiligingsproblemen met zich meegebracht. Deze problemen omvatten:

- Eavesdropping: In tegenstelling tot bekabelde netwerken, waar de communicatie via fysieke kabels verloopt, kan iedereen in de buurt draadloze signalen oppikken en bekijken wat er wordt verzonden.
- Invasie: Als een wifi-netwerk onvoldoende beveiligd is, kunnen ongeautoriseerde gebruikers eenvoudig verbinding maken met het netwerk, wat niet mogelijk is bij bekabelde netwerken zonder fysieke toegang.
- Man-in-the-Middle-aanvallen: Dit is een ernstig beveiligingsrisico waarbij een aanvaller zich tussen de communicatie van twee partijen plaatst om gegevens te onderscheppen of te wijzigen.
- Backdoors: Rogue access points worden vaak onbedoeld geïnstalleerd door werknemers die het bereik van het netwerk willen uitbreiden. Deze access points hebben meestal zwakkere beveiligingsinstellingen dan het bedrijfsnetwerk en kunnen een ideale ingang zijn voor kwaadwillende gebruikers.
- Denial-of-Service (DoS) op fysiek niveau: Bij wifi wordt de 'kabel' gevormd door de frequentiebanden in de lucht. Een aanvaller kan legitieme gebruikers de toegang tot het netwerk ontzeggen door de frequentieband te vullen met storende signalen, waardoor legitieme communicatie wordt verstoord.

Kortom, wifi-netwerken bieden flexibiliteit, maar ook beveiligingsuitdagingen die moeten worden aangepakt om de integriteit van de communicatie te waarborgen.


De IEEE 802.11-standaard beschreef oorspronkelijk beveiligingshiaten in wifi-netwerken, met name het gebruik van de WEP-encryptie die in de vroege dagen van wifi een aanzienlijk zwakke beveiliging bood. Hier volgt een samenvatting van de relevante informatie:

De oorspronkelijke IEEE wifi-standaard uit 1999 besteedde weinig aandacht aan beveiliging, en hoofdstuk 8 getiteld "Authentication and privacy" was slechts tien pagina's lang in een document van 528 pagina's.

Om verbinding te maken met een wifi-netwerk, doorloopt een gebruiker vier stappen: scannen, verbinden, authenticatie en associatie.

- **Scannen**: De client zoekt actief of passief naar beschikbare netwerken in de omgeving, waarbij netwerken hun SSID (Service Set Identifier) uitzenden, samen met fysieke parameters die de client nodig heeft.

- **Verbinden**: De wifi-netwerkkaart wordt geconfigureerd met de juiste fysieke parameters om verbinding te maken met het gekozen netwerk.

- **Authenticatie**: Gebruikers moeten bewijzen dat ze toegang hebben tot het netwerk. Er waren drie mogelijke authenticatiemethoden, namelijk Open-system authentication, Shared-key authentication en MAC Address Authentication met een MAC-ACL.

  - **Open-system authentication**: Deze modus vereist geen authenticatie en stelt effectief "geen authenticatie nodig" in. Dit houdt in dat elk apparaat verbinding kan maken met het netwerk, tenzij WEP-encryptie wordt toegepast.

  - **Shared-key authentication**: In deze modus moet de gebruiker bewijzen dat hij in het bezit is van de juiste WEP-sleutel door een challenge-response-authenticatieproces te doorlopen.

Na een succesvolle authenticatie krijgt de client een associatie-ID toegewezen, waarmee het netwerk weet met welk toegangspunt (AP) de client is verbonden. Op dit punt kan de gebruiker de bronnen van het netwerk beginnen gebruiken, en het is belangrijk om de communicatie te beveiligen, tenzij het om een openbare hotspot gaat waarin alles zichtbaar is voor iedereen.

Samengevat, de oorspronkelijke wifi-standaard had aanzienlijke beveiligingsproblemen, met name gerelateerd aan zwakke WEP-encryptie, waardoor het mogelijk was om snel toegang te krijgen tot bijna elk wifi-netwerk rond de eeuwwisseling.

In de vroege jaren 2000 werd duidelijk dat wifi-netwerken dringend betere beveiliging nodig hadden vanwege de wijdverspreide adoptie in zowel particuliere huishoudens als bedrijven. Twee oplossingen werden ontwikkeld om zowel bestaande apparaten als toekomstige producten te beveiligen:

1. **WPA1 (WiFi Protected Access 1):** Dit was een tijdelijke oplossing om de beveiligingsproblemen aan te pakken zonder de bestaande apparaten onbruikbaar te maken. WPA1 introduceerde enkele beveiligingsprotocollen, maar had enkele beperkingen.

2. **WPA2 (WiFi Protected Access 2):** Dit werd beschouwd als de "ultieme oplossing" en omvatte een geheel nieuwe reeks beveiligingsprotocollen voor toekomstige wifi-producten. Het was echter niet compatibel met oudere apparaten.

Beide oplossingen maakten gebruik van de IEEE 802.1X-standaard voor sleutelbeheer en gebruikersauthenticatie in combinatie met nieuwe encryptie- en integriteitsoplossingen.

Om rekening te houden met de behoeften van verschillende gebruikers, werden zowel WPA1 als WPA2 in twee versies uitgebracht:

- **Personal:** Dit was bedoeld voor gewone gebruikers, waarbij een gedeelde sleutel of wachtwoord (pre-shared key of PSK) werd gebruikt. Deze versie maakte geen gebruik van 802.1X.

- **Enterprise:** Dit was de versie voor grote bedrijven waar sleutelbeheer en 802.1X-authenticatie belangrijk waren.

Kortom, WPA1 en WPA2 waren reacties op de beveiligingsproblemen van wifi, met WPA2 als de meer geavanceerde en veiligere optie voor toekomstige wifi-producten, terwijl WPA1 een tijdelijke oplossing bood voor bestaande apparaten.


In 2018 lanceerde de Wifi Alliance de opvolger van WPA2, genaamd WPA3 (ook wel Wifi 6 genoemd). WPA3 was state-of-the-art op het gebied van beveiliging en hield rekening met de behoeften van moderne draadloze netwerken, zoals Internet of Things apparaten en beveiligde openbare hotspots. De Wifi Alliance zorgde ervoor dat producten conform IEEE-standaarden waren door ze te testen en het label "Wifi Alliance compatibel" toe te kennen.

WPA3 had twee modi: personal en enterprise. Enkele belangrijke verbeteringen waren Simultaneous Authentication of Equals (SAE) voor veiligere authenticatie in de personal mode, resistentie tegen offline dictionary-aanvallen, forward secrecy om oude wifi-sleutels te beschermen, Wifi Easy Connect voor eenvoudige IoT-apparaatverbindingen, Wifi Enhanced Open voor veilige openbare hotspots, geauthenticeerde encryptie met "256-bit Galois/Counter Mode Protocol (GCMP-256)", en moderne authenticatie- en sleuteldistributiemethoden binnen 802.1X, zoals HMAC, HMAC-SHA384 en ECDH.
