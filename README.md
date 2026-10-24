# Sound Visual Art

Trasforma qualsiasi immagine in arte   **animata e interattiva**, direttamente nel browser.
I segni cambiano di continuo, reagiscono al cursore e possono vibrare a ritmo di musica
o della tua voce. Puoi salvare un fotogramma come PNG o registrare un video.

**Provala online:** https://nicobule.github.io/sound_visual_art/

> Le immagini e l'audio che usi restano sul tuo dispositivo: la pagina non invia nulla a nessun server.

## Come si usa (online)

1. Apri il link e premi **Carica un'immagine** (JPG, PNG, WebP o GIF).
2. Muovi il cursore sopra l'immagine per scompigliare i segni; clicca per un'onda d'urto.
3. Dal pannello a sinistra scegli stile, palette, effetti e suono.
4. Per usare il microfono premi **Microfono** e consenti l'accesso quando il browser lo chiede.

Funziona anche su telefono e tablet.

## Cosa puoi fare

- **11 stili**
  - a caratteri: ASCII, Braille, Testo (una frase a tua scelta), Contorni, Matrix;
  - a forme: Retino, Dithering, Pixel, Tratteggio, Puntini, Linee ondulate.
- **5 palette**: Originale, Fosforo, Ambra, Duotone (due colori a scelta), Game Boy.
- **Effetti finali**: CRT, Glitch, Bloom.
- **Suono**: dal microfono o da un file audio, l'immagine vibra. Gli effetti sono Spettro, Onda (bassi / medi / alti), sobbalzo sui bassi e caos dal volume.
- **Regolazioni**: raggio e spinta del cursore, velocità, variazione, grandezza e quantità dei segni.
- **Salva PNG** e **Registra** un video (MP4 o WebM, con l'audio se è acceso).
- **Prestazioni**: qualità bassa / media / piena, anche automatica, e statistiche dal vivo (FPS, tempi di disegno, risoluzione).

### Scorciatoie da tastiera

| Tasto | Azione |
|---|---|
| `1`–`9`, `←` `→` | cambia stile |
| `I` | carica un'immagine |
| `S` | salva PNG |
| `R` | avvia / ferma la registrazione |
| `M` | accende / spegne il microfono |
| `H` | mostra / nasconde il pannello dei controlli |
| `F` | mostra / nasconde le statistiche |
| `Spazio` | pausa |

## Usarlo dal computer con Python (facoltativo)

Serve [Python 3](https://www.python.org/) con la libreria Pillow:

```bash
pip install -r requirements.txt
```

Esempi:

```bash
# pagina HTML vuota: l'immagine si sceglie nella pagina
python ascii_art_finale.py --color --html risultato.html

# pagina HTML che parte già con una foto
python ascii_art_finale.py foto.jpg -w 150 --color --html risultato.html

# ASCII art nel terminale, oppure salvata in un file di testo
python ascii_art_finale.py foto.jpg --color
python ascii_art_finale.py foto.jpg -w 120 -o risultato.txt
```

Opzioni principali: `-w` larghezza in caratteri (1–1000), `--color` colori originali,
`--invert` inverte chiari e scuri, `-c semplice|dettagliato|blocchi` set di caratteri.

> Nota: una pagina generata **con** una foto contiene una copia di quella foto.
> Per pubblicarla online usa la versione senza foto (`index.html` di questo repository).

## Pubblicare una tua copia

Fai un **Fork** di questo repository, poi in **Settings → Pages** scegli
**Deploy from a branch**, branch `main`, cartella `/ (root)`.
Dopo un minuto il sito sarà online su `https://TUO-NOME.github.io/NOME-REPOSITORY/`.
