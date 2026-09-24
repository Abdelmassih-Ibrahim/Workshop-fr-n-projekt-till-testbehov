# Kritiska affärsflöden

### 1. Kund via mobilapp genomför beställning
#### Verksamhetsmål: Färre avbrutna order & förenkla för kunder att handla
#### Berörda system: Samtliga, förutom webbsida. Positivt E-2-E test
#### Om flöde ej fungerar: Affärskritiskt, förlust av stor kundkrets
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
#### Verksamhetsmål: Färre avrutna order & förenkla för kunder att handla
#### Berörda system: Samtliga, förutom mobilapp. Positivt E-2-E
#### Om flöde ej fungerar: Affärskritist, förlust av stor kundkrets
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

### 3. Integrationer mellan system - Vardera komponents roll
#### Verksamhetsmål: Automatisera lager & minska manuellt arbete för Kundservice
#### App/Webbsida -> Backend(Server/DB) -> leverans / lager / betalsystem -> SMS / E-post tjänst
#### Vid bristande flöde: Affärskritiskt, alla komponenter är beroende av varandra
- Mobilapp/Webbsida visar korrekt statisk information
- Information på frontend hämtas korrekt från backend
- Backend tar emot data och uppdaterar databasen
- Backend skickar vidare beställningsinfo till lagersystem
- Backend skapar leverans hos leveransansvarig
- Användare omdirigeras till betalningstjänst
- Betalningstjänst erbjuder betalningsmetoder
- Vid godkänd transaktion skickas bekräftelsemail
