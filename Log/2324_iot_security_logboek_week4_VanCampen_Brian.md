# logboek week4

# cyberboswachters

Een certificaat is een digitaal document dat de identiteit van een gebruiker koppelt aan een openbare sleutel. Dit certificaat wordt ondertekend door een vertrouwde derde partij om de echtheid ervan te waarborgen. Certificaten worden beschreven in de X.509-standaard en worden aangemaakt door een registratieautoriteit (RA) die de identiteit van de gebruiker verifieert. Vervolgens wordt het certificaat ondertekend door een certificeringsinstantie (CA). De echtheid van het certificaat kan worden geverifieerd door de openbare sleutel van de CA te gebruiken. Dit proces is essentieel voor het beveiligen van communicatie, bijvoorbeeld bij HTTPS-verbindingen.

Certificaten vormen een vertrouwensketen, waarbij bovenaan een root CA staat. Als deze wordt vertrouwd, kunnen alle onderliggende CA's ook worden vertrouwd. Het is van cruciaal belang dat de integriteit van een CA wordt gehandhaafd, aangezien een inbreuk kan leiden tot ongeldigverklaring van alle certificaten, inclusief sub-CA's.

Browsers stellen gebruikers in staat om certificaten te bekijken en de geldigheidsduur en CA-informatie te controleren. Persoonlijke certificaten kunnen worden gebruikt voor identiteitsverificatie in e-mailcommunicatie, terwijl code-ondertekeningscertificaten de authenticiteit van applicaties bevestigen. Een waarschuwing van een tool zoals SmartScreen betekent niet automatisch dat software onveilig is, maar het vereist extra waakzaamheid.


HTTPS (HTTP-Secure) is een protocol dat zorgt voor een veilige, geëncrypteerde communicatie tussen je browser en een website. Het maakt gebruik van het TLS-protocol (Transport Layer Security) om een beveiligde encryptietunnel op te zetten. TLS gebruikt certificaten om de identiteit van de website te verifiëren en een gemeenschappelijke sleutel te genereren voor encryptie. Hierdoor wordt het voor derden onmogelijk om de verkeer tussen jou en de website af te luisteren. TLS combineert asymmetrische en symmetrische cryptografie om de sterke punten van beide te benutten en de zwakke punten te minimaliseren.

Hoewel HTTPS de verbinding veiliger maakt, heeft het nadelen voor internetproviders en websites, omdat de gegevens zijn versleuteld en caching niet meer mogelijk is. Mitmproxy is een krachtige tool die een man-in-the-middle aanval op HTTPS mogelijk maakt. Het stelt een aanvaller in staat zich tussen jou en het internet te positioneren en HTTPS-verbindingen te onderscheppen en zelf TLS-tunnels met de website op te zetten. Dit stelt de aanvaller in staat om verkeer te lezen en aan te passen, hoewel moderne browsers waarschuwingen zouden moeten genereren vanwege ongeldige certificaten.
