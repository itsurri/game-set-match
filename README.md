# Game, Set & Match!

App web (PWA) per tracciare e analizzare le tue partite di tennis — stile "SofaScore personale".
Ottimizzata per iPhone 15 Pro Max (6.7", safe area + Dynamic Island).

## File

| File | Ruolo |
|---|---|
| `index.html` | tutta l'app: UI, logica, grafici SVG (nessuna dipendenza esterna) |
| `manifest.webmanifest` | installazione standalone sulla Home |
| `icon.svg` / `icon.png` | icona app |

## Uso su iPhone

1. Metti la cartella online (GitHub Pages, Netlify, o la stessa hosting di `index.html` del progetto).
2. Apri l'URL in **Safari** → Condividi → **Aggiungi a Home**.
3. Aprila dall'icona: parte a schermo intero, senza barre del browser.

Aprendola da file locale funziona comunque, ma senza modalità standalone.

## Dati

Tutto è salvato in `localStorage` **solo sul dispositivo**: niente account, niente server.
Da *Profilo* puoi esportare/importare un backup JSON e caricare dati di esempio.

## Funzioni

- **Registrazione partita**: data/ora, avversario, superficie (erba/terra/cemento/indoor), punteggio per set con tie-break, esito calcolato in tempo reale.
- **Metriche facoltative**: aces, doppi falli, % prime, vincenti, errori gratuiti, break point convertiti, note tattiche.
- **Live**: segui il match game per game; il punteggio resta visibile nella pill sotto la Dynamic Island e a fine partita precompila il form.
- **Dashboard**: profilo, win/loss, striscia, forma delle ultime 10 con grafico cumulativo.
- **Statistiche**: filtri Mese / Anno / All-Time, anello win rate, barre per superficie, medie per partita, avversari frequenti.
- **Storico**: raggruppato per mese, filtri per superficie ed esito, ricerca avversario, scheda dettaglio per ogni match.
