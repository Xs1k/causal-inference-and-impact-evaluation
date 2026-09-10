# Syllabi

Sito statico pubblicato con GitHub Pages. HTML/CSS puri, nessun framework, nessuna build.

## Struttura

| File | Cosa fa |
|---|---|
| `index.html` | Hub: una card per materia |
| `causal-inference.html` | Syllabus Causal Inference (7 sezioni) |
| `logistics-scm.html` | Syllabus Logistics & SCM (8 sezioni) |
| `style.css` | Foglio di stile condiviso dalle pagine nuove |
| `MHE_Chapter_*.html` | Visore dei capitoli MHE con barra di avanzamento |
| `MHE_Chapter_*.pdf` | I capitoli estratti dal libro |
| `.nojekyll` | Dice a GitHub di servire i file così come sono |

## Come aggiungere una materia

1. Duplica `logistics-scm.html` e rinominalo (es. `microeconomics.html`).
2. Dentro: cambia `<title>`, l'`<h1>`, e sostituisci i blocchi `<section id="topicN">`.
3. Per ogni sezione serve la voce corrispondente nella `<ul>` della sidebar:
   `<li><a href="#topic3">3. Titolo</a></li>`
4. In `index.html` aggiungi una card:

```html
<a href="microeconomics.html" class="course-card">
    <h2>Nome della materia</h2>
    <div class="meta">N SEZIONI</div>
    <p>Una riga di descrizione.</p>
</a>
```

## Come aggiungere una sezione a una materia esistente

Copia un blocco `<section id="topicN" class="section">...</section>`, cambia `id` e
contenuto, e aggiungi la voce nella sidebar. Gli `id` devono combaciare con gli `href`
della sidebar, altrimenti lo scroll spy non evidenzia la sezione attiva.

## Modificare dal browser

Su GitHub: apri il file, icona della matita in alto a destra, modifica, "Commit changes".
Il sito si aggiorna da solo in un minuto o due. Se non vedi il cambiamento, ricarica
con Ctrl+F5 (cache).
