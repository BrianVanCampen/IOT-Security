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
