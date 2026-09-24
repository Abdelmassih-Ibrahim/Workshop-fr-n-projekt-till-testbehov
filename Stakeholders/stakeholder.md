### Stakeholder-analyse

| Stakeholder | Vad behöver testledaren från dem?[cite: 1] | Vad behöver de från testledaren? |
|---|---|---|
| **Utvecklingsteam** | Kunskap för att svara på tekniska frågor. | Information om teststatus. |
| **Product Owner** | Hjälp att prioritera samt djup kunskap om verksamheten | Uppdaterad teststatus och att involveras inför release. |
| **Projektledare** | Projektstyrning och resursallokering. | Övergripande teststatus och att involveras inför release. |
| **Testare** | Utförande av det praktiska testarbetet. | Tydlig testledning, planering och daglig teststatus. |
| **Representanter från kundservice** | Insikter från de som känner verksamheten och slutanvändarnas behov. | Att informeras och involveras inför release |
| **Externa leverantörer** | Att de ansvarar för externa system. | Relevanta uppdateringar om teststatus för systemintegrationer. |

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
