# CHECKLIST DI VALIDAZIONE
## Design Document Specification v1.1

Questa checklist permette di verificare che un documento di progettazione
rispetti la specifica DOC-SPEC v1.1.

Istruzioni:
- Per ogni voce, segnare [x] se conforme, [ ] se non conforme.
- Se una voce non è conforme, annotare il motivo e il riferimento alla
  regola (R1–R8).

---

## A. STRUTTURA (R1, R2, R4)

- [ ] A.1  Il documento contiene il paragrafo 1 (Abstract).
- [ ] A.2  Il documento contiene il paragrafo 2 (Analysis Purpose).
- [ ] A.3  Il documento contiene il paragrafo 3 (Analysis Scope).
- [ ] A.4  Il documento contiene il paragrafo 4 (Analysis Requirements).
- [ ] A.5  Il documento contiene il paragrafo 5 (Analysis Concepts and Methods).
- [ ] A.6  Il documento contiene il sottoparagrafo 5.1 (Technical Background).
- [ ] A.7  Il documento contiene il sottoparagrafo 5.2 (Concepts and Methods for Simplified or Conceptual Design).
- [ ] A.8  Il documento contiene il sottoparagrafo 5.3 (Concepts and Methods for Accurate or Detailed Analysis).
- [ ] A.9  Il documento contiene il sottoparagrafo 5.4 (Method Advice).
- [ ] A.10 Il documento contiene il paragrafo 6 (Analysis Input).
- [ ] A.11 Il documento contiene il paragrafo 7 (Analysis Output).
- [ ] A.12 Il documento contiene il paragrafo 8 (Analysis Verification, Validation, Risk Assessment).
- [ ] A.12a Il documento contiene il sottoparagrafo 8.1 (Analysis Verification).
- [ ] A.12b Il documento contiene il sottoparagrafo 8.2 (Analysis Validation).
- [ ] A.12c Il documento contiene il sottoparagrafo 8.3 (Risk Assessment).
- [ ] A.13 Il documento contiene il paragrafo 9 (Experiences and Lessons Learned).
- [ ] A.14 Il documento contiene il paragrafo 10 (Recommendations).
- [ ] A.15 Il documento contiene il paragrafo 11 (Appendices).
- [ ] A.16 Il documento contiene il sottoparagrafo 11.1 (Tools).
- [ ] A.17 Il documento contiene il sottoparagrafo 11.2 (Literature).
- [ ] A.18 Il documento contiene il paragrafo 12 (Nomenclature).
- [ ] A.19 Nessun paragrafo è stato eliminato (R2).
- [ ] A.20 Nessun paragrafo è stato rinumerato (R2).
- [ ] A.21 Nessun paragrafo è stato rinominato (R2).
- [ ] A.22 Non sono presenti paragrafi di primo livello oltre il 12 (R4).

## B. COMPILAZIONE (R1)

- [ ] B.1 Ogni paragrafo contiene contenuto sostanziale.
- [ ] B.2 Le sezioni non applicabili contengono la stringa esatta `N/A`
         seguita da un separatore (—, :, oppure -) e da una motivazione
         sintetica.
- [ ] B.3 Nessuna sezione è vuota.

## C. AGGIUNTE (R3)

- [ ] C.1 Le eventuali aggiunte rispettano la numerazione `X.Y.Z` o `X.Y.Z.U`.
- [ ] C.2 Le eventuali aggiunte sono in coda a sottoparagrafi esistenti
         (non creano nuovi sottoparagrafi di primo livello come 5.5).
- [ ] C.3 Non sono presenti più di 4 livelli di annidamento.
- [ ] C.4 Non sono presenti sottoparagrafi con numerazione non progressiva
         (es. 5.1.3 senza 5.1.1 e 5.1.2).
- [ ] C.5 Le aggiunte sono presenti SOLO nei paragrafi consentiti:
         5.1, 5.2, 5.3, 6, 7, 8.1, 8.2, 8.3.
- [ ] C.6 NON sono presenti aggiunte in 5.4, 11.1, 11.2, 12, o in
         qualsiasi altro paragrafo non elencato in C.5.

## D. LINGUA E TERMINOLOGIA (R5)

- [ ] D.1 La lingua di lavoro è l'inglese.
- [ ] D.2 I termini tecnici consolidati sono usati senza spiegazione
         (es. abstract, scope, input, output, lessons learned).
- [ ] D.3 I termini non consolidati sono descritti nel paragrafo 12
         (Nomenclature).
- [ ] D.4 Eventuali deroghe sono state approvate dal revisore del documento.

## E. RIFERIMENTI INTERNI (R6)

- [ ] E.1 Tutti i riferimenti interni usano la numerazione definita nella
         Parte 1 e nella Parte 2 (R3).
- [ ] E.2 Non ci sono riferimenti a paragrafi inesistenti.
- [ ] E.3 Non ci sono riferimenti a numerazioni obsolete o alternative.

## F. MODIFICABILITÀ (R7)

- [ ] F.1 La struttura (numero, titolo, posizione) di tutti i paragrafi
         è invariata rispetto alla Parte 1.
- [ ] F.2 Il contenuto dei paragrafi è stato redatto, modificato o rimosso
         liberamente dal redattore.
- [ ] F.3 Nessun paragrafo è stato rinominato (es. "Abstract" → "Sintesi").
- [ ] F.4 Nessun paragrafo è stato spostato dalla sua posizione.

## G. NOTAZIONE MATEMATICA (R8)

- [ ] G.1 Tutte le formule matematiche sono scritte in plain-text
         algebraic notation (ASCII-only, inline, single-line).
- [ ] G.2 Non sono presenti formule in LaTeX (es. `\frac{...}{...}`,
         `\sqrt{...}`).
- [ ] G.3 Non sono presenti formule in Unicode (es. `σ`, `∫`, `√`, `×`).
- [ ] G.4 Non sono presenti formule in MathML.
- [ ] G.5 Le convenzioni di R8 sono rispettate:
         - moltiplicazione: `*`
         - divisione: `/`
         - potenza: `^`
         - radice quadrata: `sqrt(...)`
         - pedice: `_`
         - apice: `^`
         - lettere greche: nome esteso (es. `alpha`, `sigma`)
         - integrali: `integral(f(x), dx, a, b)`
         - sommatorie: `sum(i=1, n, x_i)`
         - derivate: `dy/dx`, `d^2y/dx^2`
- [ ] G.6 Gli operatori sono separati da spazi per chiarezza
         (es. `a * x + b`, non `a*x+b`).

## H. COERENZA GENERALE

- [ ] H.1 Il documento è conforme allo schema JSON
         `DOC-SPEC_design-document-schema_v1.1.json`.
- [ ] H.2 Il documento è conforme alla specifica narrativa
         `DOC-SPEC_design-document-specification_v1.1.md`.
- [ ] H.3 Non ci sono contraddizioni tra le sezioni.
- [ ] H.4 La tabella riepilogo R1–R8 è rispettata.

---

## ESITO DELLA VALIDAZIONE

- Data:
- Revisore:
- Esito complessivo: [ ] CONFORME  [ ] NON CONFORME
- Note:
