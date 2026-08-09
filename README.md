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

Gli esiti hanno tre colori in tutta l'app: **verde** vittoria, **giallo** pareggio, **rosso** sconfitta.

- **Registrazione partita**: data, ora (19:00 / 19:30), durata da 1 a 4 ore, avversario, superficie (terra/cemento), **campo**, punteggio per set con tie-break, esito calcolato in tempo reale, note tattiche libere.
- **Suggerimenti**: avversari e campi già usati vengono proposti mentre scrivi, così non nascono doppioni.
- **Home**: profilo con bandiera, dati anagrafici e livello; forma delle ultime 10 a colonne (tocca l'iniziale per il nome, l'esito per il risultato); superfici in una barra unica che sfuma verso il colore su cui hai giocato di più.
- **Statistiche** (all-time): tre anelli — vittorie, set, game — rendimento per superficie, andamento delle ultime 10 con esiti toccabili.
- **Testa a testa**: scheda per ogni avversario con bilancio, ultimi incontri, rendimento per superficie e lista completa.
- **Record personali**: strisce di vittorie e sconfitte con il periodo, vittoria e sconfitta più nette col punteggio, miglior mese, avversario più battuto.
- **Calendario dell'anno**: una griglia giorno per giorno — verde vittoria, giallo pareggio, rosso sconfitta, spento riposo.
- **Storico**: raggruppato per mese, filtri multipli per superficie ed esito, ricerca avversario, scheda dettaglio per ogni match.
- **Profilo**: nome, mano, età, altezza, livello, nazionalità e città; foto ritagliabile con zoom e trascinamento.
