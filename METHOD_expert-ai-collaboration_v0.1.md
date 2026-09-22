# METHOD_expert-ai-collaboration_v0.1

## Metodo di collaborazione Esperto Progettista + AI
### Per la produzione di Analysis Practice e Design Practice

Versione: 0.1 (bozza)
Data: 2026-09-12
Stato: in sviluppo, non validato

---

## 1. Scopo

Definire come un **esperto progettista** e un **AI collaboratore** lavorano
insieme per produrre un documento di *Analysis Practice* o *Design Practice*
conforme alla specifica `DOC-SPEC v1.1`.

Il metodo copre:
- chi fa cosa (ruoli e responsabilità);
- quando lo fa (fasi);
- con quali input e output;
- con quali criteri di successo;
- con quali vincoli.

Il metodo **non** copre:
- come si scrive il contenuto (→ `METHOD_content-production_v0.1.md`);
- come si valida il documento finale (→ revisore ultimo);
- come si gestiscono fonti, lessons learnt, versioning (→ responsabilità
  dell'esperto progettista, descritte nel documento finale).

---

## 2. Attori e responsabilità

| Attore | Ruolo | Responsabilità | Non fa |
|---|---|---|---|
| **Esperto progettista** | Autore e decisore | Porta conoscenza tecnica, decide contenuti, valida, consegna al revisore | Non delega le decisioni tecniche all'AI |
| **AI collaboratore** | Assistente | Aumenta produttività, propone bozze, esegue check, segnala problemi | Non decide, non valida, non approva |
| **Revisore ultimo** | Terza parte | Verifica che il documento soddisfi gli scopi, sia corretto, chiaro, utilizzabile, memoria storica aziendale | Non interviene nella produzione |

**Regola d'oro:** l'AI propone, il progettista dispone, il revisore approva.

---

## 3. Input della collaborazione

| Input | Chi lo fornisce | Note |
|---|---|---|
| Titolo del documento | Esperto progettista | Concordato con chi commissiona |
| Scopo del documento | Esperto progettista | Cosa deve permettere di fare |
| Destinatario | Esperto progettista | Chi userà il documento |
| Struttura dei paragrafi | `DOC-SPEC v1.1` | Fissa, non negoziabile |
| Materiale grezzo | Esperto progettista | Conoscenza tecnica, esperienze, lessons learnt, fonti, vincoli |
| Criteri di accettazione | Esperto progettista | Definiti all'inizio, non alla fine |

---

## 4. Output della collaborazione

| Output | Formato | Note |
|---|---|---|
| Documento di Analysis/Design Practice | Markdown o plain-text | Conforme a `DOC-SPEC v1.1` |
| Elenco dei check eseguiti con esito | Lista | Opzionale, utile al revisore ultimo |

**Nota:** la verifica di qualità **non produce un documento separato**.
Produce correzioni al documento e, se utile, un elenco dei check eseguiti.

---

## 5. Fasi della collaborazione

### 5.1 Panoramica

| Fase | Nome | Obiettivo | Output |
|---|---|---|---|
| F0 | Preparazione | Definire scopo, destinatario, struttura, criteri, raccogliere materiale | Brief di progetto |
| F1 | Produzione a blocchi | Scrivere il documento un paragrafo alla volta | Bozza dei paragrafi |
| F2 | Verifica di conformità | Controllare rispetto a `DOC-SPEC v1.1`, correggere | Documento conforme + elenco check |
| F3 | Consegna | Passare al revisore ultimo | Documento + elenco check |

### 5.2 F0 – Preparazione

**Chi:** esperto progettista, con supporto AI.

**Cosa si fa:**
- Definire titolo, scopo, destinatario.
- Definire i criteri di accettazione.
- Raccogliere il materiale grezzo.
- Confermare la struttura (`DOC-SPEC v1.1`).

**Output:** brief di progetto (1 pagina max).

**Criterio di uscita:** il brief è approvato dall'esperto progettista.

### 5.3 F1 – Produzione a blocchi

**Chi:** esperto progettista + AI.

**Cosa si fa:**
- Per ogni paragrafo della struttura:
  1. Definire obiettivo, input, output atteso, vincoli.
  2. Produrre bozza (AI, con input del progettista).
  3. Criticare la bozza (progettista, con supporto AI).
  4. Revisionare (AI, su indicazione del progettista).
  5. Chiudere il paragrafo (progettista).

**Regola:** non si apre un paragrafo finché il precedente non è chiuso.

**Output:** bozza dei paragrafi.

**Criterio di uscita:** tutti i paragrafi obbligatori hanno contenuto sostanziale.

### 5.4 F2 – Verifica di conformità

**Chi:** esperto progettista + AI.

**Cosa si fa:**
- Applicare la checklist `DOC-SPEC_design-document-validation-checklist_v1.1.md`.
- Verificare conformità a R1–R8.
- Correggere le non conformità.
- Produrre l'elenco dei check eseguiti con esito.

**Output:** documento conforme + elenco check.

**Criterio di uscita:** nessuna non conformità bloccante.

### 5.5 F3 – Consegna

**Chi:** esperto progettista.

**Cosa si fa:**
- Consegnare al revisore ultimo: documento + elenco check.
- Attendere l'esito.

**Output:** consegna effettuata.

**Criterio di uscita:** il revisore ultimo riceve il materiale.

---

## 6. Criteri di successo

La collaborazione è riuscita se il documento prodotto soddisfa **tutti** i
seguenti criteri:

| # | Criterio | Come si verifica |
|---|---|---|
| 1 | Velocità | Tempo di produzione inferiore a una redazione senza AI |
| 2 | Chiarezza e usabilità | Un progettista esterno capisce senza chiedere chiarimenti |
| 3 | Evolvibilità | Struttura stabile, contenuti separati, niente "discorsoni" |
| 4 | Conformità | Rispetto di `DOC-SPEC v1.1` |
| 5 | Accettazione finale | Il revisore ultimo approva |

---

## 7. Vincoli e assunzioni

| Vincolo | Descrizione |
|---|---|
| Lingua | Inglese (R5) |
| Formato | Markdown o plain-text, notazione matematica ASCII (R8) |
| Memoria | L'AI non ha memoria tra sessioni: serve file di stato esterno |
| Fallibilità | L'AI può sbagliare: ogni output va verificato dal progettista |
| Conoscenza | La conoscenza tecnica è del progettista: l'AI organizza, non inventa |

---

## 8. Regole operative

| # | Regola |
|---|---|
| RO1 | Un blocco alla volta: mai "scrivi tutto il documento" |
| RO2 | Ogni paragrafo si chiude prima di aprire il successivo |
| RO3 | La conoscenza tecnica viene dal progettista, non dall'AI |
| RO4 | Ogni affermazione importante ha una fonte o è marcata come ipotesi |
| RO5 | Le fonti sono separate dai contenuti |
| RO6 | Il documento è schematico bilanciato: schemi per dati, testo per concetti |
| RO7 | Log degli attriti in tempo reale |
| RO8 | File di stato a fine sessione, salvato fuori dalla chat |
| RO9 | A inizio sessione, il pacchetto completo viene rifornito all'AI |
| RO10 | La formattazione finale è a carico del progettista, con editor di testo |
| RO11 | Ogni documento del pacchetto deve essere coerente con i documenti di livello superiore (`DOC-SPEC v1.1` in primis). La coerenza va verificata esplicitamente prima di considerare un documento chiuso. |

---

## 9. Log degli attriti (riferito a questo metodo)

| # | Attrito | Lezione |
|---|---|---|
| A1 | "Verifica di qualità" ambigua | Esplicitare sempre se un output è un documento o un artefatto leggero |
| A2 | "Attrito" usato senza definizione | Definire i termini prima di usarli |
| A3 | Sovrapposizione tra i due metodi | Separare scope: chi fa cosa vs come si scrive |
| A4 | Regola incompatibile con `DOC-SPEC v1.1` introdotta nel Metodo di produzione | Verificare sempre la coerenza con i documenti di livello superiore. Aggiunta RO11. |

---

## 10. Cosa non è oggetto di questo metodo

- Metodo di produzione dei contenuti → `METHOD_content-production_v0.1.md`
- Validazione ultima → revisore ultimo
- Gestione fonti, lessons learnt, versioning → esperto progettista
- Formattazione finale del documento → progettista, con editor

---

## 11. Riferimenti

| Documento | Versione | Ruolo |
|---|---|---|
| `DOC-SPEC_design-document-specification_v1.1.md` | v1.1 | Struttura e regole R1–R8 |
| `DOC-SPEC_design-document-schema_v1.1.json` | v1.1 | Validazione struttura |
| `DOC-SPEC_design-document-validation-checklist_v1.1.md` | v1.1 | Checklist di conformità |
| `README_v1.1.md` | v1.1 | Descrizione pacchetto |
| `METHOD_content-production_v0.1.md` | v0.1 | Metodo di produzione contenuti |

---

*Fine del documento — bozza v0.1*
