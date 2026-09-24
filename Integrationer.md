# Integrationer

## Systemlandskap

graph TD
    %% Definition av noder
    Kund([KUND])

    subgraph NordicShop [NordicShop Ekosystem]
        Frontend[NordicShop <br> Webb / Mobilapp]
        Backend[Backend / <br> Order Service]
        Lager[Lagersystem]
        Notis[E-post / SMS Service]
    end

    subgraph Externa Tjänster [Externa Tjänster]
        Payment[Payment Provider]
        Delivery[Delivery Provider]
        Bank[Bank / Kort / Swish]
    end

    %% Relationer och flöden
    Kund --> Frontend
    Frontend --> Backend

    Backend --> Payment
    Backend --> Lager
    Backend --> Delivery

    Payment --> Bank

    %% Styling för att göra det tydligt i GitHub
    style Kund fill:#f9f9f9,stroke:#333,stroke-width:2px
    style Bank fill:#e1f5fe,stroke:#0288d1,stroke-width:1px

## Komponenter och ägarskap
| System / Komponent | Ägare |
|---|---|
| Webbplats | Nordicshop |
| Mobilapp | Nordicshop |
| Backend | Nordicshop | 
| Order service | Nordicshop |
| Lagersystem | Nordicshop |
| Betalningstjänst | Extern |
| SMS/E-post tjänst | Extern |
| Leveranstjänst | Extern |

## Integration - Vart och hur kan fel uppstå?

| Från | Till | Information | Risk |
|---|---|---|---|
| Mobilapp | Backend(Server) | Appen anropar backend som sköter logik | API anrop mellan komponenter misslyckas |
| Webbplats | Backend(DB) | Webbplats anropar lager som måste uppdateras | Webbplats skickar ogiltig data, databas uppdateras fel |
| Backend | Betaltjänst | Backend anropar betaltjänst vid transaktion | Betaltjänst är nere eller kan ej anropas, blir en SPOF |
| Betaltjänst | Swish | Betaltjänst anropar swish som betalningsmetod | Swish är nere, skapar beroende vi ej kan påverka |
| Backend | Leveranstjänst | Backend anropar leverans för transport | Leveranstjänst mottar fel information, varor stannar |
