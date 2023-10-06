# LogBoek week 2

# Cyberboswachters

## Cryptografie

### Encryptie en decryptie

Encryptie heel simpel uitgelegt is het versleutelen van onze data met behulp van een geheime sleutel.
Door deze te versleutelen wordt deze onleesbaar voor mensen die de geheime sleutel niet hebben
De moeilijkheid van een goed cryptografisch systeem is dat de data op een zodanige
manier moet versleuteld worden dat het quasi onmogelijk is om zonder sleutel de originele data terug
te vinden. We spreken hierbij over de originele data als de **plaintext** en de geëncrypteerde data als
**ciphertext**. De ontvanger van een ciphertext moet deze, als hij de juiste sleutel heeft, terug kunnen
omzetten naar de originele plaintext.

er word ook over decryptie gesproken in dit stuk namelijk cryptanalyse : dat is het
proberen ontcijferen van een ciphertext zonder dat je de geheime sleutel hebt en naar mate deze evolueerd moesten cryptografische algoritmes ook verbeteren.
maar dit betekent ook dat de machines waarop je decrypteerd ook duurder werden, want hoe sneller uw machine hoe sneller je de sleutel kon vinden.

Alle bestaande cryptografische systemen kunnen op verschillende manieren gekarakteriseerd worden
(bron Network Security Essentials, door William Stallings):

**• De acties die op de data wordt uitgevoerd om deze te encrypteren:**

- Substitutie: een teken door een ander teken vervangen.
- Transpositie: een teken op een andere plek in de tekst zetten.
- Product: een combinatie van meerdere substituties en transposities.

**• Het aantal sleutels dat nodig zijn:**

- 1 sleutel, ook wel “private encryption” genoemd.
- 2 sleutels, ook wel “public encryption” genoemd.

**• De manier waarop de data wordt verwerkt:**

- Als een blok data, blok per blok.
- Als een stream, teken per teken

### De eerste algoritmes

Het doel van ieder encryptie-algoritme is om data zodanig te versleutelen zodat enkel eigenaars van
de gebruikte sleutel de originele tekst kunnen terugvinden

#### Substitutie: Caesar encryptie

De Caesar encryptie (naar Julius Caesar) bestaat uit een eenvoudig substitutie algoritme. De sleutel is
een getal tussen 1 en 25 en geeft aan door welk element uit het alfabet een teken wordt aangepast, als
volgt:

- Ieder element wordt voorgesteld als een cijfer. A krijgt de waarde 1, B wordt 2,... Z wordt 26.
- Als de sleutel het getal 3 is, dan zal nu iedere letter A in de tekst vervangen worden door het
teken 1+3, dus D. Iedere B wordt een E, enzovoort.
- Indien er een “overflow” is achteraan komen we uiteraard terug naar voor in het alfabet. Iedere
Z wordt dus een C, iedere Y een B, enzovoort.

#### Transpositie: scytale encryptie

Bij transpositie-algoritmen gaan we de positie van de karakters veranderen. De sleutel kan hierbij
bepalen op welke manier dit moet gebeuren. De Oude Grieken gebruikten een zogenaamde scytale
om aan transpositie-encryptie te doen. Een scytale was een lange stok bestaande uit drie of meerdere
lange zijden.

#### Advanced Encryption Standard (AES)

is de facto standaard als het aankomt op symmetrische encryptie
Als we echter eens het algoritme opengooien en een enkele encryption round bekijken 
dan zien we dat de bits die bovenaan binnenkomen
(state) vervolgens een combinatie van substituties (sub) en transposities ondergaan

### Cryptanalyse

De term cryptanalyse is nu al enkele keren gevallen: de wereld van de cryptologie bestaat uit twee
delen, die elkaars tegengestelden zijn:

1. Cryptografie: de wetenschap van het versleutelen van informatie.
2. Cryptanalyse: de wetenschap van het ontcijferen van versleutelde informatie, zonder kennis
van de gebruikte sleutel.


voorbeelden zijn bruteforce, Dictionary attack

**Soorten cryptanalytische aanvallen:**

Deze aanvallen zijn afhankelijk van de
informatie die de cryptanalist bezit:

- Enkel de ciphertext: vanuit het standpunt van de cyberboswachters is dit het beste soort in-
formatie dat de aanvaller bezit. Hij heeft enkel een hoop geëncrypteerde informatie en moet
proberen daar de originele plaintext uit te krijgen. Vanuit het standpunt van de cryptanalist is dit
dus de minst goede situatie om vanuit te starten.
- Gekende plaintext: de cryptanalist heeft één of meerdere stukken informatie waarvan zowel de
ciphertext als de bijhorende plaintext gekend is.
- Gekozen plaintext: de cryptanalist kan zelf plaintext kiezen waarvan de bijhorende ciphertext
moet gemaakt worden. Dit zorgt ervoor dat de cryptanalist als het ware kan experimenteren.
- Gekozen ciphertext: het zelfde concept als gekozen plaintext maar deze keer kiest de cryptanalist
de ciphertext waarvan hij de bijhorende plaintext wil genereren.

### Symmetrische encryptie

Er zijn twee soorten encryptiesystemen als we kijken naar het aantal sleutels. Symmetrische systemen
zijn systemen waarbij maar één sleutel nodig is: zowel ontvanger als verzender gebruiken dezelfde
sleutel. 

- De symmetrische encryptiesystemen zijn de oudste vorm: alle klassieke algoritmes waren van
dit principe. Asymmetrische systemen zijn pas in de 20e eeuw ontwikkeld (circa 1970).
- Voorbeelden van bestaande symmetrische encryptiesystemen zijn: AES, DES, IDEA, RC4, Blowfish,
etc

Dit type encryptie is nog steeds het meest gebruikt en wordt overal gebruikt waar data op een veilige
manier (confidentiality) moet bewaard, verstuurd of verwerkt worden.

**Block en Stream ciphers**

Er zijn twee soorten symmetrische encryptieciphers als we kijken naar de manier waarop ze de te
encrypteren data verwerken:
- Streamciphers: hierbij wordt de data letterlijk als een stream van tekens beschouwd. Waarbij
teken per teken individueel geëncrypteerd wordt (het bekendste voorbeeld is RC4). Voor ieder
teken dat verwerkt wordt zal er exact één geëncrypteerd teken gegenereerd worden. Dit soort
algoritmes zijn over het algemeen sneller dan blockciphers.
- Blockciphers: de data wordt in blokken (van bijvoorbeeld 128 tekens) verwerkt. Bekendste
voorbeelden die we verderop behandelen zijn AES, DES, 3DES, etc.

### assymmetrische encryptie
symmetrische encryptie met meerdere mensen wilt communiceren zonder dat iedereen
elkaars berichten kan zien hebt per eindpunt een aparte sleutel nodig. Het aantal
sleutels dat je nodig hebt, zeker als ook alle gebruikers onderling nog eens willen communiceren wordt
snel erg groot. Je kan het aantal benodigde sleutels berekenen met de 
formule

    n ∗ (n−1)/2 

waarbij n het aantal gebruikers voorstelt

Publieke cryptografie
Publieke crypto oftewel asymmetrische encryptie zal het probleem met symmetrische encryptie
oplossen doordat er gebruikt wordt gemaakt van twee sleutels:

- Eén publieke sleutel.
- Eén private sleutel.
De publieke sleutel kan iedereen, vrij, gebruiken om versleutelde berichten mee aan te maken. Echter,
enkel de eigenaar van de bijhorende private sleutel zal deze berichten kunnen decrypteren.

## Nation-State Attacks

Het hoofdstuk "Nation-State Attacks" uit het boek "The Art of Cyberwarfare" (NoStarch Press, 2022) richt zich op een uiterst relevante en zorgwekkende kwestie in de moderne digitale wereld: cyberaanvallen uitgevoerd door nationale staten. Dit hoofdstuk biedt inzicht in de complexe en geavanceerde aard van dergelijke aanvallen, evenals de implicaties ervan voor de digitale beveiliging en geopolitieke verhoudingen.

Het hoofdstuk begint met een overzicht van wat nationale staten motiveert om cyberaanvallen uit te voeren. Dit kunnen politieke, economische of militaire redenen zijn. Het bespreekt ook hoe deze aanvallen vaak worden uitgevoerd door gespecialiseerde eenheden binnen de overheid, zoals cyberlegers, en hoe ze vaak in het geheim worden uitgevoerd om de bron ervan te verbergen.

Een belangrijk onderdeel van het hoofdstuk is de bespreking van de verschillende soorten cyberaanvallen die door nationale staten worden gebruikt. Dit omvat spionage, sabotage, desinformatie en zelfs aanvallen op kritieke infrastructuur. De auteurs benadrukken hoe deze aanvallen vaak zeer geavanceerd zijn en gebruik maken van zero-day kwetsbaarheden, geavanceerde malware en andere geheime technieken.

Het hoofdstuk behandelt ook enkele bekende voorbeelden van nationale staat-aanvallen, zoals de Stuxnet-worm die het Iraanse nucleaire programma saboteerde en de vermeende inmenging van Rusland in de Amerikaanse verkiezingen van 2016.

Een ander belangrijk punt dat in het hoofdstuk wordt behandeld, is de uitdagingen waarmee landen worden geconfronteerd bij het verdedigen tegen dergelijke aanvallen. Het wijst op het belang van internationale samenwerking en normen in het aanpakken van deze bedreigingen.

Ten slotte biedt het hoofdstuk enkele aanbevelingen voor organisaties en individuen om zich te beschermen tegen nationale staat-aanvallen, zoals het regelmatig bijwerken van software, het bewust zijn van phishing-pogingen en het implementeren van sterke beveiligingspraktijken.

Over het algemeen biedt het hoofdstuk "Nation-State Attacks" uit "The Art of Cyberwarfare" een diepgaand inzicht in een kritiek aspect van de hedendaagse cyberbeveiliging en benadrukt het belang van proactieve maatregelen om dergelijke dreigingen te bestrijden. Het onderstreept ook de voortdurende evolutie van cyberdreigingen en de noodzaak voor zowel overheidsinstanties als particulieren om zich voortdurend aan te passen en zich te verdedigen tegen deze geavanceerde aanvallen.

## understanding threat models

Het hoofdstuk "Understanding Threat Models" uit "The Car Hacker's Handbook" (NoStarch Press, 2016) biedt een essentieel inzicht in de wereld van autobeveiliging en de benadering van dreigingsmodellen in deze context. Dit hoofdstuk behandelt de volgende belangrijke punten:

1. **Inleiding tot dreigingsmodellen**: Het hoofdstuk begint met een introductie van wat dreigingsmodellen zijn en waarom ze cruciaal zijn voor het begrijpen van beveiligingsrisico's. Het benadrukt het belang van het identificeren en evalueren van potentiële bedreigingen voor voertuigsystemen.

2. **Aanvallers en hun motieven**: Het hoofdstuk bespreekt verschillende typen aanvallers, van nieuwsgierige onderzoekers tot kwaadwillende hackers. Het benadrukt de diverse motieven die deze aanvallers kunnen hebben, variërend van het vinden van kwetsbaarheden voor vermaak tot financieel gewin.

3. **Kritieke autocomponenten**: Het hoofdstuk biedt inzicht in de belangrijkste componenten van een auto die mogelijk doelwitten zijn voor aanvallers. Dit omvat elektronische regeleenheden (ECU's), infotainmentsystemen, draadloze communicatieprotocollen en meer.

4. **Vulnerabilities and Attack Surfaces**: Het benadrukt het belang van het identificeren van kwetsbaarheden en potentiële aanvalsvectoren in voertuigsystemen. Hierbij worden voorbeelden gegeven van bekende beveiligingsproblemen in auto's.

5. **Impact van aanvallen**: Het hoofdstuk behandelt de mogelijke gevolgen van succesvolle aanvallen op voertuigen, waaronder fysieke schade, diefstal, privacy-inbreuken en zelfs levensbedreigende situaties.

6. **Classificatie van dreigingen**: Het bespreekt verschillende categorieën dreigingen, zoals externe aanvallen via draadloze netwerken, fysieke toegang tot voertuigen en interne bedreigingen zoals kwaadwillende insiders.

7. **Risicobeoordeling en mitigatie**: Het hoofdstuk sluit af met het belang van het uitvoeren van een risicobeoordeling voor voertuigbeveiliging en het implementeren van passende maatregelen om risico's te verminderen. Dit omvat het up-to-date houden van firmware en het beperken van fysieke toegang tot voertuigen.

Kortom, het hoofdstuk "Understanding Threat Models" uit "The Car Hacker's Handbook" biedt een grondige basis voor het begrijpen van de beveiligingsaspecten van moderne voertuigen. Het benadrukt het belang van dreigingsmodellering en bewustwording bij het beoordelen en verbeteren van de beveiliging van voertuigen tegen potentiële aanvallen en risico's.

# specialicatie

Mijn specialisatie valt in het thema van AI en de gevaren van AI in de toekomst.
Een idee waar ik veel aandacht aan heb besteed was de creatie van een Verdedigings AI dat verschillende hacker / gevaarlijke AI's tegen kan gaan
natuurlijk moet deze heel beveiligd worden en gelimiteerd worden tot een kleine groep.

dit idee kwam van United States national missile defense dat Amerika verdedigt tegen raketen.
