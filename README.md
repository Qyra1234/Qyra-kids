# QYRA KIDS — prima versione

Questa cartella contiene una prima versione web statica e interattiva di QYRA KIDS.

## Contenuto
- `index.html`: interfaccia responsive, profili locali, quiz di vocaboli in italiano, inglese, albanese, spagnolo e tedesco.
- `wrangler.jsonc`: configurazione per pubblicare gli asset statici su Cloudflare Workers.

## Configurazione Cloudflare
Per il progetto Worker collegato a GitHub:
- Production branch: `main`
- Build command: lasciare vuoto
- Deploy command: `npx wrangler deploy`
- Root directory: `/`
- Build watch paths: `*`

Se Cloudflare richiede l'installazione delle dipendenze, usare `npm install -D wrangler` e committare anche `package.json` e `package-lock.json`. In alternativa, impostare il deploy command a `npx wrangler@latest deploy`.

## Limiti importanti della prima versione
I profili e i punteggi sono salvati nel browser tramite localStorage: non vengono sincronizzati fra dispositivi e non costituiscono account protetti. Non raccogliere dati identificativi o sensibili dei minori. Prima di un lancio commerciale o di un uso reale da parte di bambini, occorre implementare autenticazione genitori, database con regole di accesso, consenso e informativa privacy, sicurezza e conformità alle norme applicabili sui minori.
