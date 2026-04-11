# HCS CRM Mobile — PWA per iPhone

## Cosa è incluso
- `index.html` — L'app completa (React + CSS + JS tutto in un file)
- `manifest.json` — Configurazione PWA per installazione su home screen
- `icon.svg` — Icona dell'app (da convertire in PNG 192x192 e 512x512)

## Deploy su GitHub Pages

### Passo 1 — Crea repository
1. Vai su github.com/new
2. Nome: `hcs-crm-mobile` (o quello che preferisci)
3. Seleziona "Private" se vuoi tenerlo riservato
4. Clicca "Create repository"

### Passo 2 — Carica i file
1. Clicca "uploading an existing file"
2. Trascina tutti i file da questo ZIP
3. Clicca "Commit changes"

### Passo 3 — Attiva GitHub Pages
1. Vai su Settings → Pages (menu a sinistra)
2. Source: "Deploy from a branch"
3. Branch: main, folder: / (root)
4. Clicca Save
5. Aspetta 2-3 minuti

### Passo 4 — URL dell'app
L'app sarà disponibile su:
```
https://TUO_USERNAME.github.io/hcs-crm-mobile/
```

## Installazione su iPhone

1. Apri Safari su iPhone
2. Vai all'URL dell'app
3. Tocca l'icona "Condividi" (quadrato con freccia in su)
4. Scorri e tocca "Aggiungi alla schermata Home"
5. Dai un nome (es. "HCS CRM") e tocca "Aggiungi"

L'app apparirà sulla home screen come un'app nativa!

## Funzionalità

### Schermata principale
- **Banner GPS** — Mostra l'hotel più vicino alla tua posizione
- **Barra ricerca** — Cerca per nome, città, indirizzo
- **Filtri stage** — Lead, Contattato, Demo, Proposta, Chiuso, Perso
- **Lista hotel** — Cards con semaforo, distanza, rating

### Semaforo automatico
- 🟢 Verde — Inserito da meno di 7 giorni O data ricontatto lontana
- 🟠 Arancione — Tra 7-15 giorni O data ricontatto entro 3 giorni
- 🔴 Rosso — Scaduto (>15gg senza azione O data passata)

### Scheda dettaglio
- **Azioni rapide** — Chiama, Naviga, Sito Web, Giro Vicini
- **Form aggiornamento** — Stage, Referente, Data ricontatto, Valore, Note
- **Strutture vicine** — Lista delle 5 più vicine con distanza e navigazione

### Import database
1. Tocca "📥 Import" nella barra in basso
2. Seleziona il file XLSX con le strutture
3. Le strutture vengono importate come Lead

## Prossimi passi

Questo è il **Core mobile UI** — la prima versione funzionante.

Prossime funzionalità da aggiungere:
1. **Google Sheets sync** — Salvataggio bidirezionale in tempo reale
2. **Vista "Vicini"** — Tab dedicata solo alle strutture vicine
3. **Statistiche** — Dashboard con pipeline €, chiusi, tassi conversione
4. **Notifiche** — Reminder per ricontatti scaduti

## Note tecniche

- L'app usa localStorage per salvare i dati localmente
- Il GPS richiede HTTPS (GitHub Pages lo fornisce automaticamente)
- Testato su iOS Safari 15+ e Chrome mobile
