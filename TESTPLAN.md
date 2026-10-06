# NordicShop – Testplan 

**Release:** NordicShop 3.0
**Planerad release:** Vecka 12
**Testteam:** 1 testledare + 4 testare
**Utveckling:** 3 utvecklingsteam
**Övriga:** Product Owner, verksamhet och externa leverantörer



## 1 Beskrivning

Testplanen beskriver hur NordicShop Release 3.0 ska testas inför produktionssättning vecka 12.

Testningen omfattar främst:

* SIT
* systemtest
* E2E
* acceptanstest/UAT
* regression
* retest

## 1.3 Bakgrund

NordicShop består av webb, mobilapp, backend, Order Service, lagersystem samt externa tjänster för betalning, leverans och notifieringar.

Projektet har 12 veckor till release. Testningen behöver därför prioriteras utifrån risk.

## 1.4 Syfte och mål

Syftet är att säkerställa att de mest kritiska funktionerna fungerar inför release och att ge underlag för Go/No-Go.

### Viktigaste testmålen

1. Säkerställa att kunden kan genomföra köp via webb och mobil.
2. Säkerställa att betalning fungerar korrekt.
3. Säkerställa att order skapas, uppdateras och avbeställs korrekt.
4. Säkerställa att lagersaldot uppdateras korrekt.
5. Säkerställa att kritiska integrationer fungerar.
6. Säkerställa att inga kritiska regressioner finns inför release.

## 1.5 Viktiga termer

* **SIT:** Systemintegrationstest
* **E2E:** End-to-End-test
* **UAT:** Acceptanstest
* **Regression:** Kontroll av att tidigare fungerande funktionalitet fortfarande fungerar
* **Retest:** Test av en åtgärdad defekt

## 1.6 Hänvisningar

* NordicShop GitHub – Teststrategi
* NordicShop GitHub – Testobjekt och risker
* NordicShop GitHub – Kritiska affärsflöden
* Workshop – Resurs- och tidsplan
* Workshop – Entry/Exit Criteria

---
# Dokument och hänvisningar

Följande dokument och underlag behöver finnas eller användas i testarbetet.

| Dokument / underlag                       | Beskrivning                                                                                   |
| ----------------------------------------- | --------------------------------------------------------------------------------------------- |
| Kravspecifikation                         | Används för att förstå vilka funktioner NordicShop ska stödja.                                |
| Acceptanskriterier                        | Används för att avgöra när en funktion kan betraktas som godkänd.                             |
| Testanalys – Från projekt till testbehov  | Tidigare analys av testobjekt, risker, integrationer, stakeholders och kritiska affärsflöden. |
| Teststrategi                              | Detta dokument och tillhörande dokument beskriver den övergripande strategin för testarbetet. |
| Testplan                                  | Behöver senare beskriva mer detaljerat när och hur testningen ska genomföras.                 |
| Testfall                                  | Detaljerade instruktioner för specifika tester.                                               |
| Defect/Felrapporter                       | Används för att dokumentera upptäckta fel.                                                    |
| Arkitektur/systemlandskap                 | Används för att förstå hur NordicShops olika system hänger ihop.                              |
| API-dokumentation                         | Behövs för att förstå och testa kommunikationen mellan system.                                |
| Dokumentation för lagersystemet           | Viktigt eftersom lagersystemet är gammalt och 
# 2. Öppna frågor

Följande behöver besvaras innan testplanen kan färdigställas:

| Fråga                                                   | Varför viktig?                             |
| ------------------------------------------------------- | ------------------------------------------ |
| När är Payment Providers testmiljö tillgänglig?         | Påverkar betalning och E2E.                |
| Vilka exakta acceptanskriterier gäller för release?     | Krävs för UAT och Go/No-Go.                |
| Vilka prestandakrav gäller?                             | Behövs för att avgöra vad som ska testas.  |
| Vilken testdata behövs och vem ansvarar för den?        | Testerna kan annars blockeras.             |
| Vilka webbläsare och mobiler ska stödjas?               | Påverkar testomfattningen.                 |
| Vilka säkerhetskrav ska verifieras?                     | Påverkar behörighet och login.             |
| Vilka skillnader finns mellan testmiljö och produktion? | Påverkar testresultatens tillförlitlighet. |

---

# 3. Testobjekt

De viktigaste testobjekten är:

| Testobjekt       | Vad testas?                 |
| ---------------- | --------------------------- |
| Webbplats        | Kundens köpflöde            |
| Mobilapp         | Köp via mobil               |
| Backend          | Affärslogik och API         |
| Order Service    | Skapa och hantera order     |
| Payment Provider | Betalning och återbetalning |
| Lagersystem      | Lagerstatus                 |
| Behörighet       | Åtkomst och säkerhet        |
| E-post/SMS       | Orderbekräftelser           |

---

# 4. Omfattning – In Scope

De viktigaste områdena prioriteras utifrån risk.

| Område                      | Testnivå               | Prioritet | Kommentar                             |
| --------------------------- | ---------------------- | --------- | ------------------------------------- |
| Checkout                    | Systemtest / E2E       | MUST      | Centralt för försäljningen.           |
| Kortbetalning               | SIT / Systemtest / E2E | MUST      | Hög ekonomisk risk.                   |
| Swish                       | SIT / Systemtest / E2E | MUST      | Kritisk extern integration.           |
| Orderskapande               | SIT / Systemtest / E2E | MUST      | Fel påverkar hela orderflödet.        |
| Lager                       | SIT / Systemtest       | MUST      | Fel lagerstatus kan ge felaktiga köp. |
| Avbeställning/återbetalning | Systemtest / E2E       | MUST      | Påverkar order och pengar.            |
| Login/behörighet            | Systemtest             | MUST      | Säkerhetskritisk funktion.            |
| Kritiska integrationer      | SIT                    | MUST      | Externa beroenden innebär hög risk.   |
| Orderbekräftelse            | Systemtest / E2E       | SHOULD    | Viktigt kundflöde.                    |
| Rabatt                      | Systemtest             | SHOULD    | Prioriterade rabattregler testas.     |

---

# 5. Avgränsning

För att hinna med release fokuseras testningen på högsta risk.


### Alla rabattkombinationer

Endast viktigaste rabattreglerna testas.

**Varför:** Lägre risk än betalning, order och lager.

### Alla webbläsare och mobila enheter

Endast prioriterade plattformar testas.

**Varför:** Full kompatibilitetstestning kräver mer tid.

### Fullständigt prestandatest

**Varför:** Prestandakraven är ännu inte fastställda.

**Ansvar:** Projektledning/Product Owner behöver definiera kraven.

### Enhetstest av ny kod

**Varför:** Detta ligger på utvecklingsteamen.

---

# 6. Tillvägagångssätt

Testningen genomförs riskbaserat.

## SIT

Fokus på integrationer mellan:

* Webb/mobil → Backend
* Backend → Order Service
* Backend → Lager
* Backend → Payment Provider
* Backend → Delivery Provider

## Systemtest

Testa NordicShop som helhet med fokus på:

* login
* kundvagn
* checkout
* betalning
* order
* lager
* avbeställning
* behörighet

## E2E

De viktigaste flödena är:

1. Mobilkund genomför köp.
2. Webbkund genomför köp.
3. Order avbeställs och eventuell återbetalning hanteras.

## Defekthantering

Defekter registreras, prioriteras och följs upp.

**Critical/High** hanteras först.

## Retest

När en defekt är åtgärdad testas den igen för att verifiera fixen.

## Regression

Regression fokuserar på:

* betalning
* order
* lager
* login/behörighet
* kritiska E2E-flöden
* förändrad funktionalitet


---

# 7. Testomgångar

## Omgång 1 – Huvudtest

**Syfte:** Hitta de viktigaste felen tidigt.

Fokus:

* SIT
* systemtest
* integrationer
* kritiska E2E
* betalning
* order
* lager

---

## Omgång 2 – Retest och återstående tester

**Syfte:** Kontrollera fixade defekter och testa tidigare blockerade funktioner.

Fokus:

* retest
* kompletterande systemtest
* betalning
* E2E
* UAT

---

## Omgång 3 – Regression

**Syfte:** Säkerställa att ändringar inte har skapat nya kritiska fel.

Fokus:

* kritiska funktioner
* kritiska E2E
* betalning
* order
* lager
* behörighet

---

# 8. Entry och Exit

## Entry Criteria

Testning får starta när:

1. Testmiljön fungerar.
2. Testdata finns.
3. Relevant build är levererad.
4. Testfall är förberedda.
5. Berörda funktioner är tillräckligt färdiga.
6. Nödvändiga integrationer är tillgängliga.

## Exit Criteria

Testningen är klar när:

1. Prioriterade tester är genomförda.
2. Kritiska E2E-flöden fungerar.
3. Inga Critical-defekter är öppna.
4. Kritiska High-defekter är fixade eller riskaccepterade.
5. Kritisk regression är genomförd.
6. Testresultaten är rapporterade.

---

# 9. Avbrytande och återupptagande

## Avbryt testningen om:

1. Testmiljön ligger nere.
2. Minst 70 % av testerna är blockerade.
3. En Critical-defekt stoppar ett kritiskt affärsflöde.

## Återuppta när:

1. Testmiljön fungerar igen.
2. Blockerande defekt är åtgärdad eller workaround finns.
3. Tillräckligt många tester kan genomföras igen.

---

# 10. Testdokumentation

| Artefakt            | Ansvarig                    |
| ------------------- | --------------------------- |
| Testplan            | Testledare                  |
| Testfall            | Testare                     |
| Testdata            | Testare                   |
| Defektrapporter     | Testare                     |
| Teststatus          | Testledare                  |
| Testrapport         | Testledare                  |
| Regressionstestsvit | Testare                   |
| Go/No-Go-underlag   | Testledare + projektledning |

---

# 11. Testaktiviteter

| Aktivitet       | Ansvarig             |
| --------------- | -------------------- |
| Testanalys      | Testledare + Testare |
| Testplanering   | Testledare           |
| Testdesign      | Testare              |
| Testdata        | Testare             |
| SIT             | Testare             |
| Systemtest      | Testare             |
| E2E             | Testare             |
| Defekthantering | Testare + Utveckling |
| Retest          | Testare          |
| Regression      | Testare             |
| Rapportering    | Testledare           |

---

# 12. Testmiljö

## Viktigaste miljöerna

### NordicShop testmiljö

Innehåller bland annat:

* webb
* mobilapp
* backend
* Order Service
* lagersystem

### Payment Provider

Testas separat och är ett viktigt externt beroende.

Testa:

* godkänd betalning
* nekad betalning
* timeout
* återbetalning
* dubbeldebitering

### Inventory System

Testa framför allt:

* saldo före köp
* saldo efter köp
* lager vid avbeställning

### Viktiga integrationer

* Backend ↔ Payment Provider
* Backend ↔ Inventory System
* Backend ↔ Order Service
* Backend ↔ Delivery Provider
* Backend ↔ E-post/SMS

**Viktig skillnad mot produktion:** Testmiljö och externa testtjänster kan bete sig annorlunda än produktion.

**Öppen fråga:** Exakta skillnader behöver dokumenteras.

---

# 13. Ansvar

| Roll                           | Huvudansvar                                            |
| ------------------------------ | ------------------------------------------------------ |
| Testledare                     | Planering, prioritering, uppföljning och rapportering. |
| Testare                        | Testdesign, testgenomförande och defektrapportering.   |
| Utveckling                     | Enhetstest, tekniska tester och defektfixar.           |
| Product Owner                  | Krav, prioritering och verksamhetsmässig acceptans.    |
| Verksamhet                     | UAT och verifiering av verksamhetsprocesser.           |
| Release Manager/Projektledning | Releaseplanering och Go/No-Go.                         |

---

# 14. Resurser

## Testare A – API/integration

Fokus:

* SIT
* API
* integrationer
* teknisk retest

## Testare B – Systemtest/E2E/betalning

Fokus:

* systemtest
* E2E
* betalning
* kritiska kundflöden

## Testare C – Verksamhet/UAT/testdata

Fokus:

* testdata
* verksamhetstest
* UAT
* acceptanstest

## Testare D – Regression/automation

Fokus:

* regression
* automation
* behörighet

Testresurserna ska användas parallellt när aktiviteterna inte är beroende av varandra.

---

# 15. Tidplan – 12 veckor

| Vecka | Huvudaktivitet                         |
| ----- | -------------------------------------- |
| V1    | Testanalys och riskanalys              |
| V2    | Testdesign                             |
| V3    | Testdata + testmiljö                   |
| V4    | SIT                                    |
| V5    | SIT + systemtest                       |
| V6    | Systemtest + retest                    |
| V7    | Betalning + integrationer              |
| V8    | Systemtest + E2E                       |
| V9    | Acceptanstest/UAT                      |
| V10   | UAT + retest                           |
| V11   | Kritisk regression                     |
| V12   | Release readiness + Go/No-Go + release |

### Parallellt arbete

Följande ska ske parallellt där det är möjligt:

* testdesign + testdata
* SIT + utveckling/fix
* systemtest + retest
* UAT + systemtest
* regression + automation
* defektfix + retest

---

# 16. Risker

| Risk                                  | Konsekvens                      | Åtgärd                             | Ägare                  | Prioritet |
| ------------------------------------- | ------------------------------- | ---------------------------------- | ---------------------- | --------- |
| Payment Provider försenas             | Betalning/E2E försenas.         | Testa övriga delar parallellt.     | Projektledning         | Kritisk   |
| Testmiljön är instabil                | Testning blockeras.             | Miljöstabilisering och smoke test. | Utveckling             | Hög       |
| Lagersystemet fungerar felaktigt      | Fel lager och felaktiga order.  | Testa integration tidigt.          | Testare  / Utveckling | Hög       |
| Testdata saknas                       | Tester blockeras.               | Förbered data tidigt.              | Testare               | Hög       |
| Kritiska defekter hittas sent         | Lite tid för retest/regression. | Tidig riskbaserad testning.        | Testledare             | Hög       |
| Verksamheten inte är tillgänglig      | UAT försenas.                   | Boka verksamheten tidigt.          | Product Owner          | Hög       |
| Delar av regressionen måste reduceras | Fel kan missas.                 | Prioritera kritiska funktioner.    | Testare               | Medel/Hög |
| Krav är otydliga                      | Felaktig testning/acceptans.    | Eskalera öppna frågor till PO.     | Testledare / PO        | Hög       |

---

# 17. Go/No-Go

## GO

Release kan rekommenderas när:

* kritiska E2E-flöden fungerar
* betalning fungerar
* order och lager fungerar
* kritisk regression är genomförd
* inga Critical-defekter finns
* kvarstående High-defekter är riskaccepterade
* verksamhetens viktigaste flöden är godkända

## NO-GO

Release bör stoppas om:

* Critical-defekt finns
* betalning inte fungerar
* kritiskt köpflöde inte fungerar
* kritisk regression inte är genomförd
* testresultaten är för osäkra

---

# 18. Sammanfattning för presentation

## 1. Viktigast att testa

**Betalning, order, lager, integrationer och kritiska E2E-flöden.**

## 2. Vad har vi avgränsat?

Framför allt:

* full rabattkombinationstestning
* alla enheter/webbläsare
* full prestandatestning
* låg-risk-regression

## 3. Hur testar vi?

**Riskbaserat:**

SIT → Systemtest → E2E → UAT → Retest → Regression → Go/No-Go

## 4. Viktigaste Entry/Exit

**Entry:**

* fungerande miljö
* testdata
* stabil build
* förberedda tester

**Exit:**

* prioriterade tester klara
* kritiska E2E godkända
* inga Critical-defekter
* kritisk regression klar

## 5. Viktigaste resurser

* A = API/integration
* B = Systemtest/E2E/betalning
* C = UAT/testdata
* D = Regression/automation

## 6. Tre största risker

1. Payment Provider
2. Lagersystemet
3. Sena kritiska defekter

## 7. Viktigaste öppna frågor

| Fråga                                                   | Varför viktig?                             |
| ------------------------------------------------------- | ------------------------------------------ |
| När är Payment Providers testmiljö tillgänglig?         | Påverkar betalning och E2E.                |
| Vilka exakta acceptanskriterier gäller för release?     | Krävs för UAT och Go/No-Go.                |
| Vilka prestandakrav gäller?                             | Behövs för att avgöra vad som ska testas.  |
| Vilken testdata behövs och vem ansvarar för den?        | Testerna kan annars blockeras.             |
| Vilka webbläsare och mobiler ska stödjas?               | Påverkar testomfattningen.                 |
| Vilka säkerhetskrav ska verifieras?                     | Påverkar behörighet och login.             |
| Vilka skillnader finns mellan testmiljö och produktion? | Påverkar testresultatens tillförlitlighet. |


-


