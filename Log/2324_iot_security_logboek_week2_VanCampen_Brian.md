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
