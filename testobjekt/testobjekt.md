# Testanalys för NordicShop

| Testbbjekt | Vad måste vi verifiera  i objektet | Prioritet? |
|------|------:|------|
| Backend | affärslogiken ska fungera korrekt | HÖ´G |
| Mobilappen | Samma kundflöde som på webben ska visas | HÖG |
| order service | ordrar ska dels kunna skapas/ändras men även avrbyts. Rätt status ska visas | HÖG |
| Webbplatsen | Produkter/ kundvagn/ rabatt/ köp/ inloggning/ leverans samt ordrar ska verifieras| HÖG |
| Betalningsintegration | Betalningen ska fungera som det bör, ingen dubbeldebitering. | HÖG |
| Lagersystem | Lagersaldot uppdateras på ett korrekt sätt | HÖG |
| E-post/SMS | Orderbekräftelse skickas med rätt information | MEDEL |
| Behörigheter | Kundservice och administratörer endast kan göra det de har rätt till inget mer. | MEDEL |
| Rabatt | Giltighet på rabatten och minsta ordervärde | LÅG |

## Testansvar

Vi ansvarar för att verifiera NordicShops egna system:
- Webbplats
- Mobilapp
- Backend
- Order Service

Men vi behöver även testa [integrationerna](../Integrationer.md) mot:
- Betalningsleverantör
- Lagersystem
- Leveranstjänst
- E-post/SMS-tjänst

Vi testar att integrationerna fungerar som det ska, men ansvarar inte för hur externa systemen är byggda internt.

