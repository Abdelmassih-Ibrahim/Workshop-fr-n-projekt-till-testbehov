

# Testnivaer för NordicShop:

NordicShop använder flera testnivåer eftersom systemet består av flera komponenter och integrationer.
och därför är De valda testnivåerna är:

1. Komponent-/enhetstest
2. Integrationstest
3. Systemintegrationstest
4. Systemtest
5. Acceptanstest

# 1. Enhetstest

## Syfte och mål
Syftet är att verifiera mindre delar av systemet individuellt.
Testnivån ska framför allt hitta all fel tidigt innan funktionaliteten integreras med andra system.

## Vad måste verifieras?
Till exempel: 

* affärslogik
* orderlogik
* rabattberäkning
* lagerlogik
* validering
* behörighetslogik

## Ansvariga
* Utvecklare
* Utvecklingsteam
Testledaren följer upp testresultat på en övergripande nivå.
## Omfattning
De viktigaste funktionerna och affärsreglerna i backend och Order Service bör ha enhetstester.


# 2. Integrationstest

## Syfte och mål
Syftet är att verifiera att två eller flera komponenter kan kommunicera korrekt.
Det är särskilt viktigt eftersom NordicShop är beroende av flera integrationer.
## Vad ska verifieras här?

Exempel:
* Webbplats till- Backend
* Mobilapp till- Backend
* Backend till- Order Service
* Backend till- Lagersystem
* Backend till- Betalning
* Backend till- Leverans
* Backend till- E-post/SMS

## Ansvariga
* Testare
* Utvecklare
* Testledare
* Externa leverantörer vid behov

## Omfattning
Testa bland annat:
* korrekta API-anrop
* rätt data skickas
* rätt svar tas emot
* felaktig data hanteras
* timeout hanteras
* system som är nere hanteras
* dubbla meddelanden hanteras


# 3. Systemintegrationstest

## Syfte och mål
Syftet är att verifiera att NordicShops olika system och externa tjänster fungerar tillsammans i större flöden.
## Vad ska verifieras?
Exempel:
Kund > Webb/Mobilapp > Backend > Order Service > Betalning > Lager > Leverans > E-post/SMS

Även avbeställning ska testas:
Kund > Order > Avbeställning > Återbetalning > Lager återställs > Bekräftelse

## Ansvariga
* Testare
* Testledare
* Utveckling
* Externa leverantörer vid behov

## Omfattning
Fokus ligger på systemens samspel.
Särskilt viktigt:
* betalning
* lager
* leverans
* order
* bekräftelser

# 4. Systemtest
## Syfte och mål
Syftet är att verifiera NordicShops funktionalitet som ett sammanhängande system.
## Vad behöver verifieras?
Exempel:

* skapa konto
* logga in
* söka produkter
* filtrera produkter
* se lagerstatus
* kundvagn
* rabatt
* betalning
* leverans
* order
* avbeställning
* behörigheter

## Ansvariga
* Testare
* Testledare
## Omfattning
Systemtest ska framför allt fokusera på de kritiska användarflödena och verksamhetskraven.



# 5. Acceptanstest

## Syfte och mål
Syftet är att verifiera att lösningen uppfyller verksamhetens behov innan release.
## Vad ska verifieras?
Exempel:

* kunden kan genomföra ett köp
* kunden kan avbeställa order
* kundservice kan hantera order
* administratör kan administrera produkter
* betalning fungerar
* lager uppdateras
* kunden får bekräftelse

## Ansvariga

* Product Owner
* Representanter från verksamheten
* Kundservice
* Testledare stödjer och samordnar

## Omfattning

Acceptanstestet fokuserar på verksamhetens viktigaste behov och användarflöden.



