# Sito Market Digital: guida

## Messa online (una volta sola, circa 15 minuti)

### 1. Carica il sito su GitHub
1. Crea un account gratuito su https://github.com
2. In alto a destra: **+** → **New repository**. Nome: `marketdigital`. Lascia tutto com'è e clicca **Create repository**.
3. Nella pagina che si apre clicca **uploading an existing file**.
4. Apri la cartella `marketdigital` che hai scompattato, seleziona **tutto il suo contenuto** e trascinalo nella pagina. Clicca **Commit changes**.
5. Nell'elenco dei file apri `pages.yml`, clicca la matita (Edit), e nel nome del file in alto aggiungi un punto all'inizio: `.pages.yml`. Clicca **Commit changes**.
   (Serve al pannello del blog. Il punto non è incluso nello zip perché i file che iniziano col punto sono invisibili su Mac e Windows.)

### 2. Pubblica con Cloudflare
1. Entra su https://dash.cloudflare.com → **Workers e Pages** → **Crea** → scheda **Pages** → **Importa un repository Git** (o "Connect to Git").
2. Collega il tuo account GitHub e scegli il repository `marketdigital`.
3. Impostazioni di build:
   - Framework preset: **Astro**
   - Build command: `npm run build`
   - Build output directory: `dist`
   - Variabili d'ambiente: aggiungi `NODE_VERSION` = `22`
4. Clicca **Salva e distribuisci**. Dopo un paio di minuti il sito è online su un indirizzo tipo `marketdigital.pages.dev`.

### 3. Collega il dominio
Nel progetto appena creato: **Domini personalizzati** → **Configura un dominio** → scrivi `marketdigital.it` → conferma. Ripeti con `www.marketdigital.it`. Essendo il dominio già su Cloudflare, fa tutto da solo.

### 4. Collega il pannello del blog
1. Vai su https://app.pagescms.org ed entra con GitHub.
2. Autorizza l'accesso al repository `marketdigital` e aprilo.

Fatto.

---

## Uso quotidiano

### Scrivere un articolo
1. Vai su https://app.pagescms.org → progetto `marketdigital` → **Articoli del blog** → **Aggiungi**.
2. Compila titolo, riassunto, data, immagine di copertina e testo.
3. Clicca **Salva**. Dopo circa un minuto l'articolo è online.

Per preparare un articolo senza pubblicarlo, attiva **Bozza**. Quando è pronto, disattivala e salva.

### Cambiare email, telefono o social
Nel pannello apri **Contatti e social**, modifica e salva. Si aggiornano in tutto il sito.

### Cambiare testi, pagine o grafica
Chiedi a Claude caricando il file da modificare, oppure modificalo direttamente su GitHub (matita → Commit changes). Ogni modifica va online da sola in un minuto.
