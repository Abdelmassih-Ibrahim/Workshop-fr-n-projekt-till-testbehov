### Stakeholder-analyse

| Stakeholder[cite: 1] | Vad behöver testledaren från dem?[cite: 1] | Vad behöver de från testledaren?[cite: 1] |
|---|---|---|
| **Utvecklingsteam** | Kunskap för att svara på tekniska frågor[cite: 3]. | Information om teststatus[cite: 3]. |
| **Product Owner** | Hjälp att prioritera[cite: 3] samt djup kunskap om verksamheten[cite: 3]. | Uppdaterad teststatus[cite: 3] och att involveras inför release[cite: 3]. |
| **Projektledare** | Projektstyrning och resursallokering. | Övergripande teststatus[cite: 3] och att involveras inför release[cite: 3]. |
| **Testare** | Utförande av det praktiska testarbetet. | Tydlig testledning, planering och daglig teststatus[cite: 3]. |
| **Representanter från kundservice**[cite: 2] | Insikter från de som känner verksamheten[cite: 3] och slutanvändarnas behov. | Att informeras och involveras inför release[cite: 3]. |
| **Externa leverantörer** | Att de ansvarar för externa system[cite: 3]. | Relevanta uppdateringar om teststatus[cite: 3] för systemintegrationer. |

---

### Mermaid-diagram

```mermaid
graph TD
    TL[Testledare]

    subgraph Stakeholders
        DEV[3 Utvecklingsteam]
        PO[1 Product Owner]
        PL[1 Projektledare]
        TEST[4 Testare]
        CS[Kundservice]
        EXT[Externa Leverantörer]
    end

    TL -->|Teststatus| DEV
    DEV -->|Teknisk kunskap| TL

    TL -->|Teststatus & Releaseinvolvering| PO
    PO -->|Prioritering & Verksamhetskunskap| TL

    TL -->|Övergripande teststatus| PL
    PL -->|Projektstyrning & Resurser| TL

    TL -->|Testledning & Planering| TEST
    TEST -->|Praktiskt testarbete| TL

    TL -->|Releaseinformation| CS
    CS -->|Verksamhetsinsikter| TL

    TL -->|Integrationsteststatus| EXT
    EXT -->|Ansvar för externa system| TL
