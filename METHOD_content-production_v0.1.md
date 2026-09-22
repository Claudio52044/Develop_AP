# METHOD_content-production_v0.1

## Metodo di produzione dei contenuti
### Per documenti di Analysis Practice e Design Practice

Versione: 0.1 (bozza)
Data: 2026-09-12
Stato: in sviluppo, non validato

---

## 1. Scopo

Definire **come si scrive** il contenuto di un documento di *Analysis Practice*
o *Design Practice* conforme a `DOC-SPEC v1.1`.

Il metodo copre:
- come si struttura un paragrafo;
- come si gestiscono le fonti;
- come si separano fatti, ipotesi, esperienze;
- che tono usare;
- quali schemi adottare;
- come si chiude un paragrafo.

Il metodo **non** copre:
- chi fa cosa, quando, con quali responsabilità
  (→ `METHOD_expert-ai-collaboration_v0.1.md`);
- la conformità strutturale a `DOC-SPEC v1.1` (→ specifica + checklist);
- la validazione ultima (→ revisore ultimo);
- la formattazione finale (→ progettista, con editor).

---

## 2. Principi di produzione

| # | Principio | Descrizione |
|---|---|---|
| P1 | Schematismo bilanciato | Schemi per dati, relazioni, procedure, confronti. Testo per concetti, motivazioni, contesto, sfumature. Il testo resta breve e finalizzato. |
| P2 | Brevità | Frasi brevi. Un concetto per frase. Niente ridondanze. |
| P3 | Azionabilità | Ogni paragrafo dice cosa fare, non solo cosa pensare. |
| P4 | Tracciabilità | Ogni affermazione importante ha una fonte o è marcata come ipotesi/esperienza. |
| P5 | Separazione | Fatti, ipotesi, esperienze, opinioni sono tenuti distinti. |
| P6 | Coerenza terminologica | Un termine, un significato. Termini non consolidati → Nomenclature (par. 12). |
| P7 | Evolvibilità | Struttura stabile, contenuti separati, niente dipendenze nascoste tra paragrafi. |

---

## 3. Struttura di un paragrafo

Ogni paragrafo (a qualsiasi livello) è composto da elementi standard.
Non tutti sono obbligatori: dipende dal paragrafo.

| Elemento | Obbligatorio? | Descrizione |
|---|---|---|
| Titolo | Sì | Come da `DOC-SPEC v1.1` (per livelli 1–2) o libero (per sottoparagrafi aggiunti) |
| Obiettivo | Consigliato | Cosa deve permettere di fare al lettore |
| Contenuto | Sì | Testo, tabelle, elenchi, diagrammi |
| Fonti | Se applicabile | Riferimenti alle fonti delle affermazioni importanti |
| Note | Se applicabile | Avvertenze, limiti, casi particolari |
| Riferimenti interni | Se applicabile | Link ad altri paragrafi del documento |

**Regola:** i paragrafi predefiniti da `DOC-SPEC v1.1` non possono essere
eliminati, rinominati o fusi (R1, R2). Se un paragrafo non è applicabile al
caso specifico, NON deve essere eliminato né lasciato vuoto: deve essere
compilato con la stringa esatta `N/A` seguita da un separatore
(—, :, oppure -) e da una motivazione sintetica.

Esempio:
    5.4 Method Advice
    N/A — il metodo è imposto da normativa e non sono ammesse alternative.

Per i **sottoparagrafi aggiunti** (non predefiniti), vale la stessa disciplina
di `DOC-SPEC v1.1`: si aggiungono solo se motivati, si numerano come
`X.Y.Z` o `X.Y.Z.U`, max 4 livelli, e solo nei paragrafi consentiti
(5.1, 5.2, 5.3, 6, 7, 8.1, 8.2, 8.3). I sottoparagrafi aggiunti che si
rivelano inutili possono essere rimossi, purché la numerazione resti
progressiva e coerente (R3).

---

## 4. Schemi e testo: quando usarli

| Tipo di contenuto | Formato consigliato |
|---|---|
| Dati, parametri, proprietà | Tabella |
| Procedure passo-passo | Elenco numerato |
| Requisiti, vincoli, regole | Elenco puntato |
| Confronto tra opzioni | Tabella comparativa |
| Flusso di processo | Diagramma di flusso (o elenco sequenziale) |
| Relazioni causa-effetto | Testo breve + eventuale schema |
| Concetti, motivazioni, contesto | Testo breve |
| Sfumature, eccezioni, casi limite | Testo breve + nota |
| Checklist di verifica | Elenco con caselle |

**Regola:** se un contenuto può essere espresso in una tabella senza perdere
informazione, usa la tabella. Se la tabella perde informazione, usa il testo.
Se entrambi servono, usa entrambi.

---

## 5. Gestione delle fonti

### 5.1 Tipi di fonte

| Tipo | Esempio | Come si cita |
|---|---|---|
| Norma | ISO 1234, ASME VIII | Nome, numero, edizione, anno |
| Testo tecnico | Manuale, libro | Autore, titolo, edizione, anno |
| Paper | Articolo scientifico | Autore, titolo, rivista, anno, DOI |
| Web | Sito, pagina | URL + data di consultazione |
| Esperienza interna | Caso aziendale, test | Riferimento interno + descrizione sintetica |
| Comunicazione personale | Esperto, collega | Nome + data + contesto |

### 5.2 Marcatura delle affermazioni

Ogni affermazione importante è marcata con il tipo di fonte:

| Marcatore | Significato |
|---|---|
| `[FONTE: ...]` | Affermazione supportata da una fonte citata |
| `[IPOTESI]` | Affermazione non verificata, da validare |
| `[ESPERIENZA]` | Affermazione basata su esperienza diretta |
| `[OPINIONE]` | Affermazione soggettiva, non supportata |
| `[DA VALIDARE]` | Affermazione di cui non si conosce la fonte |

**Regola:** se non sai da dove viene un'affermazione, marcala `[DA VALIDARE]`.
Non inventare fonti.

### 5.3 Separazione fatti / ipotesi / esperienze

Nel testo, non mescolare:
- **Fatti**: ciò che è dimostrato o normato.
- **Ipotesi**: ciò che si assume vero in attesa di verifica.
- **Esperienze**: ciò che è stato osservato in pratica.
- **Opinioni**: ciò che si ritiene, senza supporto.

Se un paragrafo contiene più tipi, separali in sottoparagrafi o in sezioni
distinte.

---

## 6. Tono e stile

| Caratteristica | Regola |
|---|---|
| Tono | Tecnico, prescrittivo, neutro |
| Persona | Impersonale o terza persona |
| Tempo verbale | Presente per regole e procedure; passato per esperienze |
| Frasi | Brevi, un concetto per frase |
| Parole | Preferire termini tecnici consolidati; evitare sinonimi inutili |
| Ridondanze | Eliminare |
| Aggettivi | Solo se necessari e verificabili |
| Avverbi | Solo se necessari |
| Discorsività | Vietata: se un testo è discorsivo, va schematizzato o tagliato |

---

## 7. Ciclo di produzione di un paragrafo

### 7.1 Fasi

| Fase | Cosa si fa | Chi |
|---|---|---|
| 1. Preparazione | Definire obiettivo, input, output atteso, vincoli | Progettista + AI |
| 2. Bozza | Produrre una prima versione | AI, con input del progettista |
| 3. Critica | Analizzare la bozza: cosa manca, cosa è superfluo, cosa è sbagliato | Progettista + AI |
| 4. Revisione | Correggere e migliorare | AI, su indicazione del progettista |
| 5. Chiusura | Verificare conformità e coerenza con il resto del documento | Progettista |

### 7.2 Criteri di chiusura di un paragrafo

Un paragrafo è chiuso quando:
- ha contenuto sostanziale (o è `N/A` + motivazione, se non applicabile);
- ha un obiettivo chiaro;
- usa schemi e testo in modo bilanciato;
- le affermazioni importanti sono marcate;
- non ci sono contraddizioni con altri paragrafi;
- è conforme a `DOC-SPEC v1.1` (se applicabile);
- il progettista lo approva.

**Regola:** un paragrafo non chiuso non permette di aprire il successivo.

---

## 8. Criteri di successo

| # | Criterio | Come si verifica |
|---|---|---|
| 1 | Chiarezza | Un progettista esterno capisce senza chiedere chiarimenti |
| 2 | Schematismo bilanciato | Schemi per dati, testo per concetti, niente "discorsoni" |
| 3 | Azionabilità | Il progettista che usa il documento sa cosa fare |
| 4 | Tracciabilità | Ogni affermazione importante ha una fonte o è marcata |
| 5 | Coerenza | Terminologia, tono, formato sono coerenti in tutto il documento |
| 6 | Evolvibilità | Il contenuto può essere aggiornato senza riscrivere intere sezioni |

---

## 9. Errori da evitare

| # | Errore | Perché è un problema |
|---|---|---|
| E1 | Testo discorsivo | Rallenta la lettura, nasconde le informazioni |
| E2 | Affermazioni senza fonte | Non tracciabili, non verificabili |
| E3 | Mescolare fatti, ipotesi, esperienze | Confonde il lettore, mina la fiducia |
| E4 | Terminologia incoerente | Ambiguità, fraintendimenti |
| E5 | Paragrafi predefiniti senza obiettivo | Non rispettano R1 se compilati in modo non sostanziale; vanno compilati come `N/A` + motivazione, oppure riscritti con un obiettivo chiaro |
| E6 | Dipendenze nascoste tra paragrafi | Rende difficile l'aggiornamento |
| E7 | Ridondanze | Allungano il documento senza aggiungere informazione |
| E8 | Aggettivi e avverbi non necessari | Appesantiscono, spesso non verificabili |
| E9 | Formule in LaTeX/Unicode | Violano R8 |
| E10 | Contenuti inventati dall'AI | Non verificabili, pericolosi |

---

## 10. Cosa non è oggetto di questo metodo

- Chi fa cosa, quando, con quali responsabilità
  → `METHOD_expert-ai-collaboration_v0.1.md`
- Conformità strutturale a `DOC-SPEC v1.1` → specifica + checklist
- Validazione ultima → revisore ultimo
- Formattazione finale → progettista, con editor

---

## 11. Riferimenti

| Documento | Versione | Ruolo |
|---|---|---|
| `DOC-SPEC_design-document-specification_v1.1.md` | v1.1 | Struttura e regole R1–R8 |
| `DOC-SPEC_design-document-schema_v1.1.json` | v1.1 | Validazione struttura |
| `DOC-SPEC_design-document-validation-checklist_v1.1.md` | v1.1 | Checklist di conformità |
| `README_v1.1.md` | v1.1 | Descrizione pacchetto |
| `METHOD_expert-ai-collaboration_v0.1.md` | v0.1 | Metodo di collaborazione |

---

## 12. Coerenza con i documenti di livello superiore

| # | Regola |
|---|---|
| C1 | Ogni documento del pacchetto deve essere coerente con `DOC-SPEC v1.1` e con gli altri documenti del pacchetto. |
| C2 | La coerenza va verificata esplicitamente prima di considerare un documento chiuso. |
| C3 | In caso di conflitto tra documenti, prevale il documento di livello superiore (`DOC-SPEC v1.1`). |
| C4 | I conflitti vanno registrati nel log degli attriti e risolti aggiornando il documento di livello inferiore. |

---

*Fine del documento — bozza v0.1*
