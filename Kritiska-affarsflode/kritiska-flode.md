# Kritiska affärsflöden

### 1. Kund via mobilapp genomför beställning
- Användare öppnar NordicShop mobilapp
- Blir bemött av användargränssnitt
- Navigerar produkter
- Produktsaldo hämtas från backend databas
- Lägger till produkter i varukorg
- Genomför beställning
- Produktsaldo uppdateras i databas & appen
- Användare hänvisas till betalningstjänst
- Användare väljer betalningsmetod
- Betalning genomförs
- SMS tjänst skickar bekräftelse


### 2. Webbkund genomför beställning
- Användare går in på Nordischop hemsidan
- Kund blir bemött av frontend
- Filterar och söker efter produkt
- Kontrollerar saldo av produkt
- Lägger till produkt i varukorg
- Genomför beställning
- Lager uppdateras i klient och databas
- Redirect till betalningstjänst
- Val av betalningsmetod
- Betalning genomförs
- Användare får bekräftelsemail
