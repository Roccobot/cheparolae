# Rules.md: regole del progetto 'Ma che parola è' (repo `Roccobot/cheparolae`)

> **Cos'è questo file.** Il testo completo delle regole del progetto **'Ma che parola è'**, la
> pagina che elenca parole in colonna. Vale per **tutti gli agenti**: il nucleo, cioè ogni regola
> in una riga, vive in `AGENTS.md`, e questo file ne dà il perché. Claude Code lo carica da sé,
> perché `CLAUDE.md` lo importa; gli altri agenti lo leggono quando il lavoro tocca una sua
> sezione. Le regole trasversali vivono nelle regole dell'hub `Roccobot/roccobot.github.io`
> (`AGENTS.md` e `Rules.md`), quelle universali in `rules/Roccobot.md` di `Roccobot/tools`.
> ⚠️ **Il repo non aveva un `CLAUDE.md`**: questo file nasce il 2026-09-27 e porta solo i fatti
> verificati nel repo quel giorno. Quello che il repo non dice non è scritto qui.

## 🧭 Che cos'è

- **Una pagina sola e statica**, `index.html`, col titolo `Ma che parola è`: un'immagine di
  testata (`titolo.gif`) e sotto un elenco di parole in colonna, diviso da righe vuote in quattro
  gruppi (gli ultimi due sono nomi di persona e nomi di luogo), chiuso dalla riga
  `© 2017 FDPA & gulpegaspe`. Non c'è build: l'unico script ricarica la pagina quando cambia
  l'orientamento del telefono.
- **Da dove viene**: è nata nella cartella `Parole/` del repo `Roccobot/roccobot.github.io` (primo
  caricamento il 2025-11-28, col file `Parole.html` poi rinominato `index.html`), e il
  **2026-09-26** è passata in un repo suo, con la cronologia di quella cartella. Il commit che crea
  il repo (`7e1a870`) la dice servita da GitHub Pages, e aggiunge `.nojekyll` come nel sito di base.
- **W3C**: il 2026-07-14, ancora nell'hub, `index.html` e `Parole_BCK.html` sono stati portati a
  0 errori e 0 warning (commit `b4cabb3` e `9c308c5`).

## 🌿 Ramo e versione

- **Ramo principale `main`**, l'unico, in locale e sul remoto.
- ⚠️ **La pagina resta senza numero di versione, per scelta dell'utente** (2026-09-27: *resta
  senza, è una paginetta statica che potrei anche aggiornare a mano e non la tocco praticamente
  mai*). È una deroga dichiarata alla regola universale (SlimVer, con una fonte sola visibile nel
  prodotto), e vale solo qui. Di conseguenza non c'è una sonda di versione: una pubblicazione si
  verifica con un `curl` su `index.html` (con `Cache-Control: no-cache`) cercando la modifica
  appena fatta.

## 🗂️ I file del repo

- **In uso da `index.html`**: `titolo.gif`, i font `BrainFlower.ttf` (l'elenco) e
  `ArialNarrow.ttf` (la riga del copyright), le icone `apple-icon-*`, `android-icon-*`,
  `ms-icon-*`, `favicon-*.png` e `favicon.ico`, `manifest.json` e `browserconfig.xml`.
- **Favicon e icone sono la 🤌🏻 (U+1F90C U+1F3FB) di Google Noto Emoji**, per scelta
  dell'utente (2026-09-27). La favicon principale è l'SVG di Noto scritto dentro `index.html`; le
  icone PNG e l'ICO sono lo stesso disegno reso a 1024 pixel e ridotto, in RGBA senza palette, con
  lo sfondo bianco nelle sole `apple-icon-*`, perché iOS riempie di nero la trasparenza. Fino a
  quel giorno la favicon era la 🤏🏻 (U+1F90F), diversa da quella voluta, e le icone PNG mostravano la
  freccia 'TOP' di Arda Top, copiate da là. ⚠️ **L'SVG viene dal set `noto` di Iconify**
  (`@iconify-json/noto`, su jsDelivr), cioè le emoji Noto di Google convertite: il repo
  `googlefonts/noto-emoji` non si raggiunge da jsDelivr, e i raw di quei file rispondono 404.
- **`manifest.json` e `browserconfig.xml` usano percorsi relativi dal 2026-09-27**: prima
  cominciavano con `/`, cioè puntavano alla radice del dominio, dove quelle icone non ci sono. Il
  manifest si chiama come la pagina, `Ma che parola è`, e non più `App`.
- **Tolti il 2026-09-27, su istruzione dell'utente, perché nessuna pagina li usava**:
  `Parole_BCK.html`, `Labadessa.ttf`, `angolo_sinistro.png` e `angolo_destro.png`, con il
  blocco commentato e le regole CSS degli angoli.
- **`ArialNarrow.ttf` è dichiarato col nome `'Arial Narrow'` dal 2026-09-27**, quello che la
  riga del copyright chiede: prima il nome era `ArialNarrow`, e quella riga non usava il file.
