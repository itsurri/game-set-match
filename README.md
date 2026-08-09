# Game, Set & Match!

App web (PWA) per tracciare e analizzare le tue partite di tennis — stile "SofaScore personale".
Ottimizzata per iPhone 15 Pro Max (6.7", safe area + Dynamic Island).

## File

| File | Ruolo |
|---|---|
| `index.html` | tutta l'app: UI, logica, grafici SVG, integrazione Firebase (login Google + sync) |
| `manifest.webmanifest` | installazione standalone sulla Home |
| `icon.svg` / `icon.png` | icona app |

## Uso su iPhone

1. Metti la cartella online (GitHub Pages, Netlify, o la stessa hosting di `index.html` del progetto).
2. Apri l'URL in **Safari** → Condividi → **Aggiungi a Home**.
3. Aprila dall'icona: parte a schermo intero, senza barre del browser.

Aprendola da file locale funziona comunque, ma senza modalità standalone.

## Dati

Di base tutto è salvato in `localStorage` **solo sul dispositivo**: niente account, niente server.
Da *Profilo* puoi anche **accedere con Google**: le partite vengono sincronizzate su Firebase Realtime Database e ritrovate su ogni dispositivo dove fai login con lo stesso account.
Da *Profilo* puoi inoltre caricare dati di esempio o cancellare tutto.

## Grafica

Stile **tabellone**: fondo scuro, numeri luminosi, dati incolonnati, card arrotondate con bordo chiaro.
Header con titolo **stencil** centrato, menù in **Liquid Glass** (Home · Stats · Storico · Profilo, con il `+` staccato nella sua pill).
Display **Bebas Neue**, testo **Work Sans**. Tema chiaro e scuro entrambi supportati.

## Funzioni

- **Registrazione partita**: data/ora, avversario, superficie (terra/cemento), **campo**, punteggio per set con tie-break, esito calcolato in tempo reale, note tattiche libere.
- **Suggerimenti**: avversari e campi già usati vengono proposti mentre scrivi, così non nascono doppioni.
- **Dashboard**: profilo, win/loss, striscia, forma delle ultime 10 con grafico cumulativo.
- **Statistiche**: filtri Mese / Anno / All-Time, anello win rate, barre per superficie, andamento.
- **Testa a testa**: scheda per ogni avversario con bilancio, ultimi incontri, rendimento per superficie e lista completa.
- **Record personali**: striscia più lunga, vittoria più netta, miglior mese, avversario più battuto.
- **Calendario dell'anno**: una griglia giorno per giorno — verde vinto, rosso perso, spento riposo.
- **Confronto periodi**: questo mese contro il precedente, quest'anno contro l'anno scorso.
- **Storico**: raggruppato per mese, filtri per superficie ed esito, ricerca avversario, scheda dettaglio per ogni match.
