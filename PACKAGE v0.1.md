# PACKAGE_v0.1

## Manifesto del pacchetto documentale
### Per la produzione di Analysis Practice e Design Practice

Versione pacchetto: 0.1
Data: 2026-09-12
Cartella di riferimento: `iteration_1.2`

---

## 1. Scopo del pacchetto

Il pacchetto raccoglie i documenti che, nel loro insieme, definiscono il
metodo di collaborazione tra un esperto progettista e un AI per produrre
documenti di *Analysis Practice* o *Design Practice*.

Il pacchetto include:
- documenti di specifica (struttura, regole, validazione);
- documenti di metodo (collaborazione, produzione contenuti);
- documenti di servizio (questo manifesto, file di stato delle sessioni).

---

## 2. Contenuto del pacchetto

### 2.1 Documenti di specifica (v1.1)

| File | Versione | Ruolo | Stato |
|---|---|---|---|
| `DOC-SPEC_design-document-specification_v1.1.md` | v1.1 | Struttura obbligatoria (12 capitoli) + regole R1–R8 | Adeguato, invariato |
| `DOC-SPEC_design-document-schema_v1.1.json` | v1.1 | JSON Schema per validazione automatica struttura | Adeguato, invariato |
| `DOC-SPEC_design-document-validation-checklist_v1.1.md` | v1.1 | Checklist per revisione manuale/assistita | Adeguato, invariato |
| `README_v1.1.md` | v1.1 | Descrizione pacchetto, versioning, glossario | Adeguato, invariato |

### 2.2 Documenti di metodo (v0.1, bozze)

| File | Versione | Ruolo | Stato |
|---|---|---|---|
| `METHOD_expert-ai-collaboration_v0.1.md` | v0.1 | Metodo di collaborazione Esperto Progettista + AI | Bozza, non validato |
| `METHOD_content-production_v0.1.md` | v0.1 | Metodo di produzione dei contenuti | Bozza, non validato |

### 2.3 Documenti di servizio

| File | Versione | Ruolo | Stato |
|---|---|---|---|
| `PACKAGE_v0.1.md` | v0.1 | Questo manifesto: elenca i file del pacchetto | Aggiornato a fine sessione |
| `STATUS_2026-09-12.md` | — | File di stato della sessione: decisioni, attriti, prossimi passi | Aggiornato a fine sessione |

---

## 3. Versioning

### 3.1 Regola

- Ogni documento ha la **sua versione** (v1.1, v0.1, ecc.).
- Il **pacchetto** ha una versione separata (`PACKAGE_vX.Y`).
- Il pacchetto è identificato anche dalla **cartella di iterazione**
  (es. `iteration_1.2`), che raggruppa i file validi per quella fase.

### 3.2 Come si legge una versione

| Prefisso | Significato |
|---|---|
| v1.x | Documento consolidato (specifica, schema, checklist, README) |
| v0.x | Documento in bozza (metodi, nuovi documenti) |

### 3.3 Quando si aggiorna la versione

- **Documento di specifica**: solo se cambiano struttura o regole.
- **Documento di metodo**: a ogni revisione sostanziale.
- **Pacchetto**: a ogni sessione che modifica il contenuto del pacchetto.

---

## 4. Coerenza tra i documenti

I documenti del pacchetto sono coerenti tra loro. In caso di conflitto:

1. Prevale `DOC-SPEC_design-document-specification_v1.1.md`.
2. Poi `DOC-SPEC_design-document-schema_v1.1.json`.
3. Poi `DOC-SPEC_design-document-validation-checklist_v1.1.md`.
4. Poi i documenti di metodo.

Ogni conflitto va registrato nel file di stato e risolto aggiornando il
documento di livello inferiore.

---

## 5. Come si usa il pacchetto

### 5.1 All'inizio di una sessione

1. L'utente rifornisce all'AI il pacchetto completo (tutti i file).
2. L'utente incolla o allega il file di stato più recente.
3. L'AI riprende dal punto indicato nel file di stato.

### 5.2 Durante la sessione

- Si producono o revisionano documenti del pacchetto.
- Si registrano gli attriti nel log.
- Si aggiornano i documenti modificati.

### 5.3 Alla fine di una sessione

1. Si aggiornano i documenti modificati.
2. Si aggiorna `PACKAGE_vX.Y.md` se cambia il contenuto del pacchetto.
3. Si produce un nuovo `STATUS_YYYY-MM-DD.md` con decisioni, attriti,
   prossimi passi.
4. L'utente salva tutto in una nuova cartella di iterazione (o aggiorna
   quella corrente).

---

## 6. Struttura della cartella di iterazione

iteration_1.2/
├── DOC-SPEC_design-document-specification_v1.1.md
├── DOC-SPEC_design-document-schema_v1.1.json
├── DOC-SPEC_design-document-validation-checklist_v1.1.md
├── README_v1.1.md
├── METHOD_expert-ai-collaboration_v0.1.md
├── METHOD_content-production_v0.1.md
├── PACKAGE_v0.1.md
└── STATUS_2026-09-12.md


---

## 7. Prossimi passi

| # | Passo | Stato |
|---|---|---|
| 1 | Analisi dei documenti esistenti | Fatto |
| 2 | Sviluppo dei due metodi (v0.1) | Fatto |
| 3 | Manifesto del pacchetto (`PACKAGE_v0.1.md`) | Fatto |
| 4 | File di stato (`STATUS_2026-09-12.md`) | In corso |
| 5 | Banco prova: Analysis Practice sul buckling della camera di combustione | Da fare |

---

*Fine del manifesto — PACKAGE_v0.1*
