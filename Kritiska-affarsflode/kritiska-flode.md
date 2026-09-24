# Kritiska affärsflöden

### 1. Kund via mobilapp genomför beställning
- Användare öppnar NordicShop mobilapp
- Navigerar produkter
- Produktsaldo hämtas och produktinfo visas
- Lägger till produkter i varukorg
- Genomför beställning
- Produktsaldo uppdateras i databas & appen
- Användare hänvisas till betalningstjänst
- Användare väljer betalningsmetod
- Betalning genomförs
- SMS tjänst skickar bekräftelse


### 2. Webbkund genomför beställning
- Användare går in på Nordischop hemsidan
- Filterar och söker efter produkt
- Kontrollerar saldo av produkt
- Lägger till produkt i varukorg
- Genomför beställning
- Lager uppdateras i klient och databas
- Redirect till betalningstjänst
- Val av betalningsmetod
- Betalning genomförs
- Användare får bekräftelsemail

### 3. Integrationer
- Mobilapp/Webbsida visar korrekt statisk information
- Information på frontend hämtas korrekt från backend
- Backend tar emot data och uppdaterar databasen
- Backend skickar vidare beställningsinfo till lagersystem
- Backend skapar leverans hos leveransansvarig
- Användare omdirigeras till betalningstjänst
- Betalningstjänst erbjuder betalningsmetoder
- Vid godkänd transaktion skickas bekräftelsemail
