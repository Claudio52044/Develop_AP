# SPECIFICA DEL DOCUMENTO DI PROGETTAZIONE
## Parte 1 — Struttura obbligatoria
## Parte 2 — Regole di compilazione e numerazione

Versione: 1.1

---

## PARTE 1 — STRUTTURA OBBLIGATORIA

Il documento DEVE contenere i seguenti paragrafi, con questa esatta
numerazione e denominazione:

1  Abstract
2  Analysis Purpose
3  Analysis Scope
4  Analysis Requirements
5  Analysis Concepts and Methods
    5.1 Technical Background
    5.2 Concepts and Methods for Simplified or Conceptual Design
    5.3 Concepts and Methods for Accurate or Detailed Analysis
    5.4 Method Advice
6  Analysis Input
7  Analysis Output
8  Analysis Verification, Validation, Risk Assessment
    8.1 Analysis Verification
    8.2 Analysis Validation
    8.3 Risk Assessment
9  Experiences and Lessons Learned
10 Recommendations
11 Appendices
    11.1 Tools
    11.2 Literature
12 Nomenclature

---

## PARTE 2 — REGOLE DI COMPILAZIONE E NUMERAZIONE

### R1 — Obbligo di compilazione
Tutti i paragrafi elencati nella Parte 1 DEVONO essere presenti e
compilati con contenuto sostanziale.

Se un paragrafo non è applicabile al caso specifico, NON deve essere
eliminato né lasciato vuoto: deve essere compilato con la stringa
esatta `N/A` seguita da un separatore (—, :, oppure -) e da una
motivazione sintetica.

Esempio:
    5.4 Method Advice
    N/A — il metodo è imposto da normativa e non sono ammesse alternative.

### R2 — Divieto di eliminazione e rinumerazione
Nessun paragrafo della Parte 1 può essere:
    - eliminato;
    - rinumerato;
    - rinominato.

### R3 — Aggiunta di sottoparagrafi
È consentito aggiungere sottoparagrafi SOLO in coda a un paragrafo
esistente, usando la numerazione `X.Y.Z` o `X.Y.Z.U` dove l'ultimo
numero è progressivo e parte da 1.

Sono consentiti al massimo 4 livelli di annidamento
(esempio: `5.1.1`, `5.1.1.1`, non `5.1.1.1.1`).

È consentito aggiungere sottoparagrafi SOLO ai seguenti paragrafi:
    - 5.1, 5.2, 5.3
    - 6, 7
    - 8.1, 8.2, 8.3

Esempi PERMESSI:
    - aggiungere `5.1.1` dentro `5.1`
    - aggiungere `5.1.1.1` dentro `5.1.1`
    - aggiungere `7.1` dentro `7`
    - aggiungere `8.1.1` dentro `8.1`

Esempi VIETATI:
    - aggiungere `5.5` (nuovo sottoparagrafo di 5)
    - aggiungere `13` (nuovo paragrafo di primo livello)
    - aggiungere `5.1.1.1.1` (quinto livello)
    - aggiungere `5.4.1` (5.4 non è nella lista dei paragrafi consentiti)
    - aggiungere `11.1.1` (11.1 non è nella lista dei paragrafi consentiti)
    - aggiungere `12.1` (12 non è nella lista dei paragrafi consentiti)

### R4 — Struttura di primo livello chiusa
I paragrafi di primo livello sono fissi da 1 a 12.
Non è possibile aggiungere paragrafi di primo livello
(es. 13, 14, …).

### R5 — Lingua e terminologia
La lingua di lavoro è l'inglese.
Sono ammessi termini tecnici consolidati nella pratica ingegneristica
(es. abstract, scope, input, output, lessons learned).

Un termine è considerato consolidato se compare in almeno una norma
o testo di riferimento riconosciuto nel settore.
Eventuali deroghe sono ammesse solo dal revisore del documento.
Gli altri termini devono essere descritti nel paragrafo 12 (Nomenclature).

### R6 — Coerenza dei riferimenti
Ogni riferimento interno al documento DEVE usare la
numerazione definita nella Parte 1 e nella Parte 2 (R3).

### R7 — Modificabilità dei paragrafi

La struttura dei paragrafi è fissa; il contenuto è modificabile.
In dettaglio:

**Struttura NON modificabile**:
- numero, titolo e posizione sono invariabili;
- non possono essere eliminati, rinumerati o rinominati;
- appartengono a questa categoria: TUTTI i paragrafi elencati nella
  Parte 1.

**Contenuto modificabile**:
- il contenuto testuale è redatto dal redattore;
- il contenuto può essere aggiunto, modificato o rimosso;
- l'unico vincolo è che il paragrafo non sia vuoto (R1).

**Esempi:**

| Paragrafo | Cosa si può fare | Cosa NON si può fare |
|-----------|------------------|----------------------|
| 1 Abstract | Scrivere il testo dell'abstract | Rinominarlo "Sintesi" |
| 5 Analysis Concepts and Methods | Scrivere il contenuto del paragrafo | Eliminarlo o spostarlo |
| 5.1 Technical Background | Scrivere il contenuto | Rinumerarlo 5.5 |
| 5.1.1 (aggiunto) | Aggiungere un sottoparagrafo | Aggiungerlo come 5.5 |
| 12 Nomenclature | Elencare i termini | Rinominarlo "Glossario" |

### R8 — Notazione matematica

Tutte le formule matematiche presenti nel documento DEVONO essere
scritte in **plain-text algebraic notation** (ASCII-only, inline,
single-line).

Definizione:
- solo caratteri ASCII (codici 32–126);
- notazione algebrica classica (non RPN, non notazione polacca);
- inline (dentro il testo, non in blocchi separati);
- single-line (una sola riga, senza frazioni impilate).

Esempi PERMESSI:
    x = (-b + sqrt(b^2 - 4*a*c)) / (2*a)
    sigma = M / W
    E * I * d^4w/dx^4 = q(x)
    w_tip = P * L^3 / (3 * E * I)
    integral(f(x), dx, a, b)
    sum(i=1, n, x_i)

Esempi VIETATI:
    x = \frac{-b + \sqrt{b^2 - 4ac}}{2a}    (LaTeX)
    σ = M/W                                  (Unicode)
    ∫_a^b f(x) dx                            (Unicode)
    <math><mi>x</mi>...</math>               (MathML)

Convenzioni:
- moltiplicazione: `*`
- divisione: `/`
- potenza: `^`
- radice quadrata: `sqrt(...)`
- pedice: `_` (es. `x_1`, `sigma_max`)
- apice: `^` (es. `x^2`, `10^-3`)
- lettere greche: nome esteso (es. `alpha`, `sigma`)
- integrali: `integral(f(x), dx, a, b)`
- sommatorie: `sum(i=1, n, x_i)`
- derivate: `dy/dx`, `d^2y/dx^2`
- spazi: usare spazi attorno agli operatori per chiarezza
  (es. `a * x + b`, non `a*x+b`)

Le violazioni di R8 sono considerate non conformità bloccanti:
il documento non può essere approvato finché non sono corrette.

---

## RIEPILOGO VINCOLI (per verifica automatica)

| ID  | Vincolo                                                    | Tipo      |
|-----|------------------------------------------------------------|-----------|
| R1  | Tutti i paragrafi presenti e compilati                     | Obbligo   |
| R1  | Sezioni non applicabili → `N/A` + separatore + motivazione | Obbligo   |
| R2  | Nessuna eliminazione, rinumerazione, rinomina              | Divieto   |
| R3  | Aggiunte come `X.Y.Z` o `X.Y.Z.U`, max 4 livelli, solo nei paragrafi consentiti | Permesso |
| R4  | Nessun nuovo paragrafo di primo livello                    | Divieto   |
| R5  | Inglese + termini tecnici consolidati; altri → par. 12     | Regola    |
| R6  | Riferimenti interni coerenti con la numerazione            | Obbligo   |
| R7  | Struttura fissa, contenuto modificabile                    | Obbligo   |
| R8  | Notazione matematica in plain-text algebraic notation      | Obbligo   |
