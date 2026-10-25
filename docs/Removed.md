# Removed.md: le cose tolte da 'Ma che parola è', e come si recuperano

> **Cos'è questo file.** L'archivio di quello che è uscito dalla pagina: per ogni cosa tolta, che
> cosa faceva, quando è stata tolta, e da quale commit si recupera. Si legge su richiesta, quando
> qualcuno vuole riportare indietro un file o capire dove viveva.
> ⚠️ **Nei file di regole resta solo la decisione** (che la cosa non c'è più, e perché): ogni
> appunto su come recuperarla vive qui, corto o lungo che sia (regola universale in
> `rules/Roccobot.md` di `Roccobot/tools`, § '🗄️ Le cose tolte vivono in Removed.md').
> Le voci vanno dalla più recente alla più vecchia.

## 🤏 La favicon 🤏🏻 e le icone con la freccia TOP

- **Che cosa erano**: la favicon e le icone della pagina prima della 🤌🏻 di oggi.
  - La favicon era un SVG scritto dentro `index.html` come indirizzo `data:`, la 🤏🏻 (U+1F90F
    con la carnagione chiara, `emoji_u1f90f_1f3fb` di Google Noto Emoji), diversa da quella
    voluta: i commit che l'hanno messa, il 2026-05-24, la chiamavano 🤌🏻.
  - Le icone PNG e l'ICO (`apple-icon-*`, `android-icon-*`, `ms-icon-*`, `favicon-*.png`,
    `favicon.ico`) mostravano la freccia 'TOP' di Arda Top, copiate da là e caricate il
    2025-11-28, quando la pagina viveva ancora nella cartella `Parole/` dell'hub.
- **Sostituite il 2026-09-27**, su scelta dell'utente, dalla 🤌🏻 (U+1F90C U+1F3FB) di Google
  Noto Emoji, nella favicon SVG e in tutte le icone: la regola sulle icone di oggi resta in
  `Rules.md` § '🗂️ I file del repo'.
- **Si recuperano dal commit `36ccdc4^`**, cioè il genitore del commit di `main` che le ha
  sostituite (il repo non ha tag). Dove vivevano:
  - la favicon, nel `<link rel="icon">` in testa a `index.html`;
  - le icone, coi loro nomi di oggi alla radice del repo, richiamate dai `<link>` di
    `index.html`, da `manifest.json` e da `browserconfig.xml`.
- I comandi che le mostrano: `git show 36ccdc4^:index.html` per la favicon,
  `git show 36ccdc4^:apple-icon-180x180.png > apple-icon-180x180.png` per un'icona.

## 🗑️ I file che nessuna pagina usava

- **Che cosa facevano**: niente, ed è la ragione per cui sono usciti.
  - `Parole_BCK.html` era una seconda copia della pagina, con lo stesso titolo;
  - `Labadessa.ttf` era un font che nessun file dichiarava;
  - `angolo_sinistro.png` e `angolo_destro.png` erano due immagini fisse negli angoli in alto, a
    opacità 0,08, il cui blocco in `index.html` era già commentato.
- **Tolti il 2026-09-27**, su istruzione dell'utente, perché nessuna pagina li usava.
- **Si recuperano dal commit `36ccdc4^`**, cioè il genitore del commit di `main` che li ha tolti
  (il repo non ha tag). Dove vivevano:
  - i quattro file, alla radice del repo;
  - in `index.html`, il blocco commentato coi due `<div>` degli angoli e le regole CSS degli
    angoli (`.angle_tl`, `.angle_tr` e le loro immagini).
- Il comando che mostra la copia di riserva di allora: `git show 36ccdc4^:Parole_BCK.html`.
