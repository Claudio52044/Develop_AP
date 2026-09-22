# Design Document Specification — Pacchetto v1.1

Questo pacchetto contiene la specifica, lo schema e gli strumenti di
validazione per la produzione di documenti di progettazione conformi
alla specifica DOC-SPEC v1.1.

---

## Contenuto del pacchetto

| File | Descrizione | A chi serve |
|------|-------------|-------------|
| `DOC-SPEC_design-document-specification_v1.1.md` | Specifica narrativa: struttura obbligatoria (12 capitoli) e regole di compilazione (R1–R8) | Umani (redattori, revisori) e AI |
| `DOC-SPEC_design-document-schema_v1.1.json` | JSON Schema per la validazione automatica della struttura | AI e tool automatici |
| `DOC-SPEC_design-document-validation-checklist_v1.1.md` | Checklist operativa per la revisione manuale o automatica | Umani (revisori) e AI |
| `README.md` | Questo file: descrive il pacchetto e come usarlo | Tutti |

---

## Come si usa il pacchetto

### 1. Redazione del documento
Il redattore segue la specifica narrativa
(`DOC-SPEC_design-document-specification_v1.1.md`) e produce il
documento di progettazione rispettando:
- la struttura obbligatoria (Parte 1);
- le regole di compilazione e numerazione (Parte 2, R1–R8).

### 2. Validazione automatica (opzionale)
Se il documento è rappresentato in formato JSON o YAML, uno strumento
automatico (linter) può validarlo contro il JSON Schema
(`DOC-SPEC_design-document-schema_v1.1.json`).

### 3. Revisione manuale o assistita
Il revisore (umano o AI) usa la checklist
(`DOC-SPEC_design-document-validation-checklist_v1.1.md`) per
verificare la conformità del documento, voce per voce.

### 4. Esito
- Se tutte le voci della checklist sono conformi → documento approvato.
- Se ci sono non conformità → il documento torna al redattore con
  l'elenco delle violazioni e il riferimento alla regola (R1–R8).

---

## Versioning

La versione è indicata nel nome del file (`_v1.1`).
Quando la specifica cambia, tutti i file del pacchetto vengono
aggiornati con la stessa versione.

| Versione | Data | Modifiche |
|----------|------|-----------|
| 1.0 | (inserire data) | Prima emissione |
| 1.1 | (inserire data) | Aggiunte R7 (modificabilità) e R8 (notazione matematica); aggiunti sottoparagrafi 8.1, 8.2, 8.3; corretto refusi |

---

## Coerenza tra i file

I tre file (specifica, schema, checklist) sono coerenti tra loro:
- la specifica definisce le regole R1–R8;
- lo schema le traduce in vincoli formali verificabili;
- la checklist le rende operative per la revisione.

Se un file viene modificato, gli altri due vanno aggiornati di
conseguenza.

---

## Glossario delle regole

| ID  | Regola |
|-----|--------|
| R1  | Obbligo di compilazione (tutti i paragrafi presenti e compilati; `N/A` + motivazione se non applicabile) |
| R2  | Divieto di eliminazione, rinumerazione, rinomina |
| R3  | Aggiunta di sottoparagrafi come `X.Y.Z` o `X.Y.Z.U`, max 4 livelli, solo nei paragrafi consentiti |
| R4  | Struttura di primo livello chiusa (paragrafi 1–12) |
| R5  | Lingua inglese; termini consolidati ammessi; altri → paragrafo 12 |
| R6  | Coerenza dei riferimenti interni |
| R7  | Modificabilità dei paragrafi (struttura fissa, contenuto modificabile) |
| R8  | Notazione matematica in plain-text algebraic notation (ASCII-only, inline, single-line) |

---

## Terminologia

Nel pacchetto si usa la seguente terminologia:

| Termine | Significato |
|---------|-------------|
| **Paragrafo** | Termine generico per qualsiasi sezione del documento |
| **Capitolo** | Paragrafo di primo livello (1–12) |
| **Sottocapitolo** | Paragrafo di secondo livello (es. 5.1) |
| **Sottoparagrafo** | Paragrafo di terzo o quarto livello (es. 5.1.1) |
