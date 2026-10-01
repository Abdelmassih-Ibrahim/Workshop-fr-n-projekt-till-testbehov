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
| 1 | Registrera konto | Medel risk | Beror på ifall konto krävs för att utföra köp. |
| 2 | Login | Medel risk | Beror på ifall konto krävs för att utföra köp. |
| 3 | Lås konto efter tre felaktiga loginförsök | Hög risk | För att obehöriga inte ska kunna komma åt kundens information. |
| 4 | Återställ lösenord | Medel risk | För att kunden ska kunna komma åt sitt konto, dock brukar man inte byta lösenord för ofta. |
| 5 | Produktsökning | Låg risk | För man kan hitta produkten på andra sätt. |
| 6 | Produktfilter | Låg risk | För att man kan hitta produkten manuellt. |
| 7 | Produktinformation | Låg risk | Kunden kan fortfarande köpa produkten även om viss information skulle saknas. |
| 8 | Kundvagn | Medel risk | Viktig för att kunden ska kunna se och ändra sina val innan köp. |
| 9 | Rabattkod | Låg risk | Påverkar främst rabatten på köpet och kunden kan fortfarande genomföra köpet utan rabattkod. |
| 10 | Checkout | Hög risk | Ett viktigt steg i köpprocessen där kunduppgifter, leverans och betalning hanteras. |
| 11 | Kortbetalning | Hög risk | Hanterar betalningar och fel kan leda till att kunden inte kan genomföra sitt köp. |
| 12 | Swishbetalning | Hög risk | Är kopplad till betalning och en extern tjänst, vilket gör funktionen extra känslig. |
| 13 | Orderskapande | Hög risk | Om ordern inte skapas korrekt kan kunden förlora sitt köp eller ordern bli felaktig. |
| 14 | Lageruppdatering | Hög risk | Felaktigt lager kan leda till att kunder beställer produkter som inte finns i lager. |
| 15 | Leveransalternativ | Medel risk | Viktigt för att kunden ska kunna välja hur beställningen ska levereras. |
| 16 | Orderbekräftelse via e-post | Låg risk | Kunden kan fortfarande få sin order även om bekräftelsemejlet inte skickas. |
| 17 | Orderhistorik | Låg risk | Viktig för kunden men påverkar inte själva köpet. |
| 18 | Avbeställning | Medel risk | Påverkar ordern och kan även påverka lager och betalning. |
| 19 | Återbetalning | Hög risk | Hanterar pengar och fel kan leda till att kunden inte får tillbaka rätt belopp. |
| 20 | Behörigheter för kundservice och admin | Hög risk | Fel behörigheter kan göra att obehöriga får tillgång till känslig information eller funktioner. |

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
| Registrera konto | 0,5 |1 |1 |2 |0,5 |0,5 |5,5 |
| Login | 0,5 |1 |1 |2 |0,5 |0,5 |5,5 |
| Lås konto efter tre felaktiga loginförsök | 0,5 | 0,5 | 0,5  | 0,5 | 0,5 | 1 | 3,5 |
| Återställ lösenord | 0,5 | 1,5 | 1 | 1 | 0,5 | 1 | 5,5 |
| Produktsökning | 0,5 | 1 | 1 | 1 | 1 | 1 | 5,5 |
| Produktfilter | 0,5 | 1 | 1 | 0,5 | 1 | 1 | 5 |
| Produktinformation | 0,5 | 0,5 | 0,5 | 0,5 | 0,5 | 0,5 | 3 |
| Kundvagn | 1 | 2 | 1,5 | 1 | 1 | 1 | 7,5 |
| Rabattkod | 0,5 | 0,5 | 0,5 | 1 | 1 | 1 | 4,5 |
| Checkout | 1 | 1,5 | 1 | 1 | 1 | 1 | 6,5 |
| Kortbetalning | 1 | 2 | 2 | 1 | 1 | 1 | 8 |
| Swishbetalning | 2 | 2 | 1 | 3 | 2 | 1 | 11 |
| Orderskapande | 2 | 2 | 1 | 3 | 2 | 1 | 11 |
| Lageruppdatering | 2 | 2 | 2 | 3 | 2 | 1 | 12 |
| Leveransalternativ | 1 | 1 | 1 | 2 | 1 | 1 | 7 |
| Orderbekräftelse via e-post | 1 | 1 | 1 | 2 | 1 | 1 | 7 |
| Orderhistorik | 1 | 1 | 1 | 2 | 1 | 1 | 7 |
| Avbeställning | 2 | 2 | 1 | 3 | 2 | 1 | 11 |
| Återbetalning | 2 | 2 | 2 | 3 | 2 | 1 | 12 |
| Behörigheter för kundservice och admin | 1 | 1 | 2 | 1 | 1 | 1 | 7 |
| **TOTALT** | 21 | 26,5 | 23 | 33,5 | 22,5 | 18,5 | 145 |


---

## Uppgift 3 – Beskriv hur ni estimerade

Vi använde oss utav planning poker för att estimera storlek på tickets.
Därefter sorterade vi dom och estimerade tiden via Three-Point.

| Funktion | Estimeringsmetod | Motivering |
|---|---|---|
| Login | 3-point | Denna kändes tillräckligt simpel för att kunna estimera |
| Rabattkod| | 3-point | Rabattkod var vi överens om så vi använde 3-point för att få ett genomsnitt |
| Avbeställning | Planning-poker | Denna var vi lite osams om så alla argumenterade och tills vi var överens |
| Återbetalning | Planning-poker | Då återbetalning var svår att estimera hade vi en gemensam diskussion |
| Produktsökning | 3-point (4M) | Vi hade liknande estimeringar så vi gjorde 3-point med större vikt mot Most-Likely |
---

## Uppgift 4 – Three-Point Estimation

| Funktion | Optimistic (O) | Most Likely (M) | Pessimistic (P) | Viktat estimat |
|---|---:|---:|---:|---:|
|Checkout |2 |2 |2 |2 |
|Kortbetalning |2 |2 |2 |2 |
|Orderskapande |2 |3 |2 | 2.6|
**Formel:**

`(O + 4M + P) / 6`

---

## Uppgift 5 – Buffert


| Osäkerhet | Påverkan | Behövs buffert? | Kommentar |
|---|---|---|---|
| Externa integrationer |Hög |Ja |Idk |
| Gemensam testmiljö |Hög |Ja |Hålla varandra uppdaterade, bra spårbarhet |
| Gammalt lagersystem |Hög |Idk |Idk |
| Testdata |Hög |Idk |Idk |
| Många utvecklingsteam |Hög |idk |Overkill, bottleneck |
| Förväntade defekter |Låg | |Låg eftersom de var förväntde |
| Övrigt |idk |idk |idk |
### Buffertbeslut

| Fråga | Svar |
|---|---|
| Behöver vi en buffert? | Ja |
| Hur stor? | På cirka 20% av estimerad tid|
| Varför? | På grund av låg erfarenhet behövs buffert för att hantera felmarginal |
| Vilka osäkerheter ska bufferten hantera? | För låga estimeringar på tid och bugfixar |

---

## Uppgift 6 – Kapacitetsplanering

| Fråga | Beräkning | Svar |
|---|---|---|
| A. Hur många effektiva testtimmar har teamet per vecka? | 30 × 4 | 120 timmar/vecka ungefär |
| B. Hur många veckor krävs för testarbetet? | 120 / 145 | Cirka 6 dagar |
| C. Är planen realistisk? |  | Ja, om alla testare är tillgängliga och testmiljön fungerar som planerat. |
| D. Vilka antaganden bygger planen på? |  | Alla 4 testare har 30 timmar per vecka om dom inte sjukar sig, testmiljön är tillgänglig, testdata finns och utvecklingsteamen levererar funktionerna i tid. |
