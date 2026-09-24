# Limone Gym

Diario della palestra da installare sul telefono: serie, peso, ripetizioni, timer di recupero, calorie stimate, andamento settimanale e grafico dei progressi per ogni esercizio. Ogni persona ha i suoi dati, salvati solo sul proprio telefono.

## Cosa c'è nella cartella

| File | A cosa serve |
|---|---|
| `index.html` | L'app completa |
| `manifest.webmanifest` | Nome e icona dell'app installata |
| `sw.js` | Fa funzionare l'app anche senza internet |
| `icons/` | Icona: limone con bilanciere su verde |

## Metterla online gratis con GitHub Pages

1. Crea un account su github.com, se non l'hai già.
2. Crea un nuovo repository pubblico, per esempio `limone-gym`.
3. Tocca **Add file → Upload files** e trascina tutto il contenuto di questa cartella, compresa la cartella `icons`. Poi **Commit changes**.
4. Vai in **Settings → Pages**. In **Build and deployment** scegli **Deploy from a branch**, branch `main`, cartella `/ (root)`, e salva.
5. Dopo un paio di minuti l'app è online su `https://TUO-NOME-UTENTE.github.io/limone-gym/`.

Questo è il link da mandare agli amici.

## Installarla sul telefono

- **iPhone:** apri il link con Safari → tocca **Condividi** → **Aggiungi alla schermata Home** → **Aggiungi**.
- **Android:** apri il link con Chrome → menu ⋮ → **Installa app** (oppure **Aggiungi a schermata Home**).

Dopo la prima apertura funziona anche senza connessione.

## Backup

I dati stanno solo sul telefono di chi usa l'app. Nella pagina **Diario**, in fondo:

- **Salva backup** crea un file `limone-backup-DATA.json`. Su iPhone si apre il menu di condivisione: scegli **Salva in File** (o iCloud Drive).
- **Ripristina da file** ricarica un backup, anche su un telefono nuovo. Gli allenamenti già presenti non vengono cancellati: il backup aggiunge quelli mancanti.

Se passano più di 14 giorni senza backup, il riquadro diventa giallo per ricordarlo.

## Provarla sul computer

Dalla cartella dell'app:

```
python3 -m http.server 8000
```

Poi apri http://localhost:8000 nel browser.

## Aggiornare l'app

Dopo aver modificato `index.html`, apri `sw.js` e cambia `limone-v2` in `limone-v3` (e così via a ogni modifica). Carica i file aggiornati su GitHub: alla successiva apertura con internet, i telefoni prendono la nuova versione. I dati salvati non vengono toccati.
