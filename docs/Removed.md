# Removed.md: le cose tolte da 'Ma che parola è', e come si recuperano

> **Cos'è questo file.** L'archivio di quello che è uscito dalla pagina: per ogni cosa tolta, che
> cosa faceva, quando è stata tolta, e da quale commit si recupera. Si legge su richiesta, quando
> qualcuno vuole riportare indietro un file o capire dove viveva.
> ⚠️ **Nei file di regole resta solo la decisione** (che la cosa non c'è più, e perché): ogni
> appunto su come recuperarla vive qui, corto o lungo che sia (regola universale in
> `rules/Roccobot.md` di `Roccobot/tools`, § '🗄️ Le cose tolte vivono in Removed.md').
> Le voci vanno dalla più recente alla più vecchia.

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
