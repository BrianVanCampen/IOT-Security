# Logboek Week5

# Optie 2: technisch labo

Je bouwt zelfstandig een Wifi scanner in Python met behulp van de Scapy library (https://scapy.net/)

! Reconnaissance, GEEN hacking. Wees voorzicht, geen illegale handelingen stellen.

Scapy is een krachtige netwerkbibliotheek voor Python die toelaat om, met enkele regels code, netwerkpakketten te creëren, te versturen, te onderscheppen en te analyseren. Het is als het ware een Zwitsers zakmes voor netwerkonderzoek en -testen. De leercurve is aanwezig, net omdat het zo'n uitgebreide mogelijkheden geeft. Maar mits wat opzoekwerk moet je in staat zijn een eenvoudige tekst-based scanner te maken.

Concreet: je schrijft een eenvoudige Wi-Fi scanner die beacon frames (https://en.wikipedia.org/wiki/Beacon_frame) snifft en decodeert die door AP's worden uitgezonden. Deze beacon frames worden uitgezonden om de aanwezigheid van een Wi-Fi netwerk aan te kondigen.

Je probeert vervolgens ook zoveel mogelijk informatie in te winnen over de beveiliging van de netwerken die je vindt. 

Extra punten om de tool (via de terminal) gebruiksvriendelijk te maken en de bekomen gegevens op te slaan in een bestand.


**Ik ga hieronder een korte uitleg geven van hoe mijn code werkt en wat ik heb geleerd tijdens deze opdracht**

Het script begint door netwerkinterfaces op te halen en deze op het scherm weer te laten zien, zodat u de juiste interface kan kiezen.
Na u een interface heeft geselecteerd, begint de code met het vastleggen van Wi-Fi-beacon frames op die interface. 
Beacon frames worden uitgezonden door Wi-Fi-toegangspunten om hun aanwezigheid aan te kondigen.

Voor elk gedetecteerd beacon frame, wordt de informatie geëxtraheerd, waaronder de SSID (naam van het netwerk), het BSSID (MAC-adres van het toegangspunt), het kanaal en de beveiligingsstatus van het netwerk.

De beveiligingsstatus wordt bepaald door het inspecteren van informatie-elementen in het beacon frame. Het programma controleert op WEP- en WPA/WPA2-beveiligingsinformatie-elementen en past de beveiligingsstatus  aan.

De verzamelde informatie wordt opgeslagen in een bestand dat door de gebruiker wordt opgegeven.

Het programma waarschuwt de gebruiker dat de gevonden Wi-Fi-netwerken zijn opgeslagen in het opgegeven bestand.
