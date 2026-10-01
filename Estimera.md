# Workshop – Estimera NordicShop

VI är testledningsteam för NordicShop.
Projektet har:
● 1 testledare
● 4 testare
● 3 utvecklingsteam
● gemensam testmiljö
● externa integrationer
● fast planerad release

# De 20 funktionerna
1. Registrera konto
2. Login
3. Lås konto efter tre felaktiga loginförsök
4. Återställ lösenord
5. Produktsökning
6. Produktfilter
7. Produktinformation
8. Kundvagn
9. Rabattkod
10. Checkout
11. Kortbetalning
12. Swishbetalning
13. Orderskapande
14. Lageruppdatering
15. Leveransalternativ
16. Orderbekräftelse via e-post
17. Orderhistorik
18. Avbeställning
19. Återbetalning
20. Behörigheter för kundservice och admin


## Uppgift 1 – Riskklassificering

varje funktion som:
● Hög risk
● Medel risk
● Låg risk 

| Nr | Funktion | Risk | Motivering |
|---:|---|---|---|
| 1 | Registrera konto |GIGANTISK risk | |
| 2 | Login |Hög risk | |
| 3 | Lås konto efter tre felaktiga loginförsök |Hög risk | |
| 4 | Återställ lösenord |Medel risk | |
| 5 | Produktsökning |Låg risk  | |
| 6 | Produktfilter |Låg risk  | |
| 7 | Produktinformation | Medel risk  | |
| 8 | Kundvagn |Medel risk | |
| 9 | Rabattkod |Låg risk | |
| 10 | Checkout | Hög risk | |
| 11 | Kortbetalning |Hög risk | |
| 12 | Swishbetalning |Hög risk | |
| 13 | Orderskapande |Hög risk | |
| 14 | Lageruppdatering |Hög risk | |
| 15 | Leveransalternativ | Medel risk | |
| 16 | Orderbekräftelse via e-post |Låg risk  | |
| 17 | Orderhistorik |Låg risk  | |
| 18 | Avbeställning | Medel risk| |
| 19 | Återbetalning | Hög risk| |
| 20 | Behörigheter för kundservice och admin | Hög risk| |

---

## Uppgift 2 – Estimera varje funktion

varje funktion estimera vi:
● Analys
● Testdesign
● Testdata
● Genomförande
● Regression
● Felomtest
Ange estimatet i timmar.

| Funktion | Analys | Testdesign | Testdata | Genomförande | Regression | Felomtest | Totalt |
|---|---:|---:|---:|---:|---:|---:|---:|
| Registrera konto | | | | | | | |
| Login | | | | | | | |
| Lås konto efter tre felaktiga loginförsök | | | | | | | |
| Återställ lösenord | | | | | | | |
| Produktsökning | | | | | | | |
| Produktfilter | | | | | | | |
| Produktinformation | | | | | | | |
| Kundvagn | | | | | | | |
| Rabattkod | | | | | | | |
| Checkout | | | | | | | |
| Kortbetalning | | | | | | | |
| Swishbetalning | | | | | | | |
| Orderskapande | | | | | | | |
| Lageruppdatering | | | | | | | |
| Leveransalternativ | | | | | | | |
| Orderbekräftelse via e-post | | | | | | | |
| Orderhistorik | | | | | | | |
| Avbeställning | | | | | | | |
| Återbetalning | | | | | | | |
| Behörigheter för kundservice och admin | | | | | | | |
| **TOTALT** | | | | | | | |

---

## Uppgift 3 – Beskriv hur ni estimerade

För minst fem funktioner ska vi beskriva vilken metod ni använde.
Exempel:
## Kortbetalning
- Vi använde Expert Estimation eftersom en gruppmedlem har erfarenhet av
- betalningsintegrationer.
## Login
- Vi använde Historical Data eftersom vi jämförde med tidigare liknande
funktionalitet.
## Lagerintegration
Vi använde Three-Point Estimation eftersom området har stor osäkerhet. 

| Funktion | Estimeringsmetod | Motivering |
|---|---|---|
| | | |
| | | |
| | | |
| | | |
| | | |

---

## Uppgift 4 – Three-Point Estimation

| Funktion | Optimistic (O) | Most Likely (M) | Pessimistic (P) | Viktat estimat |
|---|---:|---:|---:|---:|
| | | | | |
| | | | | |
| | | | | |

**Formel:**

`(O + 4M + P) / 6`

---

## Uppgift 5 – Buffert


| Osäkerhet | Påverkan | Behövs buffert? | Kommentar |
|---|---|---|---|
| Externa integrationer | | | |
| Gemensam testmiljö | | | |
| Gammalt lagersystem | | | |
| Testdata | | | |
| Många utvecklingsteam | | | |
| Förväntade defekter | | | |
| Övrigt | | | |

### Buffertbeslut

| Fråga | Svar |
|---|---|
| Behöver vi en buffert? | |
| Hur stor? | |
| Varför? | |
| Vilka osäkerheter ska bufferten hantera? | |

---

## Uppgift 6 – Kapacitetsplanering

| Fråga | Beräkning | Svar |
|---|---|---|
| A. Hur många effektiva testtimmar har teamet per vecka? | | |
| B. Hur många veckor krävs för testarbetet? | | |
| C. Är planen realistisk? | | |
| D. Vilka antaganden bygger planen på? | | |
