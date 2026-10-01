# Uppgift 7 – Planera om

## 1. Hur mycket kapacitet hade ni tidigare?

**Beräkning:**  

vi hade 6 dagar tidigare

## 2. Hur mycket kapacitet har ni nu?

**Beräkning:**  

8 dagar blir vår nya kapacitet. 

## 3. Hur många timmar saknas för att genomföra ursprunglig plan?

**Beräkning:**  

2 dagars arbete. 


## 4. Hur påverkas tidsplanen?

**Svar:**  

Vi behöver göra en avgränsning.
---

# Uppgift 8 – Prioritera om

Nr | Funktion | Prioritet |
|---|---|---|
|1 |Registrera konto |SHOULD|
|2 |Login |SHOULD|
|3 |Lås konto efter tre felaktiga loginförsök | MUST|
|4 |Återställ lösenord |SHOULD|
|5 |Produktsökning |COULD|
|6 |Produktfilter |COULD|
|7 |Produktinformation |COULD|
|8 |Kundvagn |SHOULD|
|9 |Rabattkod |COULD|
|10| Checkout |MUST|
|11 |Kortbetalning |MUST|
|12 |Swishbetalning |MUST|
|13 |Orderskapande |MUST|
|14 |Lageruppdatering | MUST|
|15 |Leveransalternativ |SHOULD|
|16 |Orderbekräftelse via e-post | COULD |
|17 |Orderhistorik |COULD |
|18 |Avbeställning |SHOULD |
|19 |Återbetalning |MUST |
|20 |Behörigheter för kundservice och admin | MUST |

**MUST:**  

**SHOULD:**  

**COULD:**  

---

# Uppgift 9 – Vad reducerar ni?

Vi måste nu bestämma om ni reducerar:
● analys
● testdesign
● testdata
● testgenomförande
● regression
● felomtest

**Vad kan faktiskt reduceras utan att skapa oacceptabel risk**

| Område | Vad reducerar vi? |
|---|---|
| Analys | Samma mängd, annars riskerar vi missa större del |
| Testdesign | Samma mängd |
| Testdata | Lägre mängd testdata |
| Testgenomförande | Ej affärskritiskt |
| Regression | Stor reduktion |
| Felomtest | Behåller samma mängd |

### Sammanfattning



# Uppgift 10 – Presentera för projektledaren

Projektledaren säger:
**Releasedatumet ligger fast. Kan ni fortfarande hinna?**

| Område | Beskrivning |
|---|---|
| Vad har förändrats? | En mindre testare innebär förändrad riskanalys och avgränsning |
| Hur påverkas kapaciteten? | -25% -> från 6 dagar till 8 dagar |
| Vad kan inte längre genomföras enligt ursprunglig plan? | Några låg prio / SHOULD funktioner |
| Vad prioriterar vi? | Allt affärskritiskt och beroenden. |
| Vad reducerar vi? | Kosmetiskt och låg-prioriterade aspekter i drift/användbarhet |
| Vilka risker skapar det? | Hög funktionalitet men bristfällig kvalitet inom prestanda/GUI |
| Vilka alternativ finns? | Anställ konstult / kontrollera Acceptanskriterier |
| Rekommendation | Conditional-Go ifall MUST + COULD funktioner är godkända |

