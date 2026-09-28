# Testmiljö

NordicShop behöver testmiljöer som gör det möjligt att testa både företagets egna system och integrationerna mot externa tjänster.

## Miljö 1 – Gemensam testmiljö

| Egenskap              | Beskrivning                                            |
| --------------------- | ------------------------------------------------------ |
| Miljö                 | Gemensam testmiljö                                     |
| Syfte                 | Testa NordicShops funktionalitet och integrationer     |
| Användare             | Tre utvecklingsteam och testteam                       |
| System                | Webb, mobilapp, backend, Order Service och lagersystem |
| Externa integrationer | Behöver kunna anslutas till externa testtjänster       |
| Testdata              | Separat testdata behövs                                |
| Viktig risk           | Flera team kan påverka varandras tester                |

### Vad måste då testas här?

* funktionalitet
* integrationer
* order
* lager
* kundvagn
* inloggning
* behörigheter
* E2E-flöden


# Miljö 2 – Betalningsleverantörens testmiljö

| Egenskap          | Beskrivning                                     |
| ----------------- | ----------------------------------------------- |
| Miljö             | Extern testmiljö                                |
| Syfte             | Testa betalningsintegration                     |
| Ägare             | Extern betalningsleverantör                     |
| Betalningsmetoder | Visa, Mastercard och Swish                      |
| Viktig risk       | Testmiljön kan ha andra beteenden än produktion |

### Vad ska testas?

* betalningsförfrågan
* godkänd betalning
* nekad betalning
* timeout
* avbruten betalning
* betalningsstatus
* återbetalning
* att samma order inte debiteras två gånger



# Testdata

Testmiljön behöver testdata för bland annat:

* kunder
* produkter
* lager
* rabattkoder
* order
* betalningar
* leveranser

Testdata behöver även innehålla negativa scenarier.
Exempel:
* produkt utan lager
* ogiltig rabattkod
* utgången rabattkod
* tre felaktiga lösenord
* nekad betalning
* order som redan skickats


# Miljörisker
De viktigaste riskerna är:

1. Tre utvecklingsteam delar samma miljö.
2. Testdata kan påverkas av andra tester.
3. (Fortsätter sen)
4. 
5. 


