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
