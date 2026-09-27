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
- **La pagina non porta un numero di versione**, e nel repo non c'è un file che ne faccia da
  fonte: la regola universale (SlimVer, con una fonte sola visibile nel prodotto) qui non è ancora
  applicata. Di conseguenza non esiste nemmeno una sonda con cui verificare una pubblicazione.

## 🗂️ I file del repo

- **In uso da `index.html`**: `titolo.gif`, il font `BrainFlower.ttf` (dichiarato con
  `@font-face` e usato dall'elenco), le icone `apple-icon-*`, `android-icon-192x192.png`,
  `favicon-*.png`, `manifest.json` e i metadati `msapplication-*`. La favicon principale è un SVG
  scritto dentro `index.html`, sostituito il 2026-05-24 con la mano dell'emoji Noto a tono di pelle
  chiaro.
- **Non collegati da nessuna pagina**: `Parole_BCK.html` (una versione più corta della pagina,
  caricata insieme a lei nel primo commit) e `Labadessa.ttf`. `angolo_sinistro.png` e
  `angolo_destro.png` compaiono solo in un blocco commentato.
- **`ArialNarrow.ttf`** è dichiarato col nome `ArialNarrow`, mentre la riga del copyright chiede
  `'Arial Narrow'`: il nome non coincide, quindi quella riga non usa il file del repo.
