# dotfiles

Desktop Wayland minimale: mangowm (layout scroller, animazioni leggere) con waybar, mako, foot e rofi.
Colori gruvbox dark ovunque.

## Installazione

1. Installare i pacchetti:

   ```
   mangowm waybar mako foot rofi swaybg grim slurp wl-clipboard
   brightnessctl networkmanager bluez-utils bluetui ttf-jetbrains-mono-nerd
   ```

2. Copiare `.config/*` in `~/.config/`.

Il font è JetBrainsMono Nerd Font (`ttf-jetbrains-mono-nerd`): le icone della barra sono suoi glifi.

## File

Ogni impostazione è spiegata da un commento subito sopra, nel file stesso.

| File                          | Programma               | Cosa controlla                                                             |
| ----------------------------- | ----------------------- | -------------------------------------------------------------------------- |
| `.config/mango/config.conf`   | mangowm (compositor)    | Monitor, avvio automatico, aspetto, animazioni, layout, input, scorciatoie |
| `.config/waybar/config.jsonc` | waybar (barra di stato) | Quali moduli mostra la barra e con che testo                               |
| `.config/waybar/style.css`    | waybar                  | Font, colori e spazi della barra                                           |
| `.config/mako/config`         | mako (notifiche)        | Posizione, colori e durata delle notifiche                                 |
| `.config/foot/foot.ini`       | foot (terminale)        | Font del terminale                                                         |
| `.config/rofi/config.rasi`    | rofi (launcher)         | Comportamento e aspetto del launcher                                       |

## Tasti

`SUPER` è il tasto Windows. Le direzioni sono `h` `j` `k` `l` oppure le frecce.

### Programmi

| Tasti                                  | Azione                    |
| -------------------------------------- | ------------------------- |
| `SUPER` + `Return`                     | Terminale (foot)          |
| `SUPER` + `d` oppure `SUPER` + `space` | Launcher delle app (rofi) |
| `SUPER` + `SHIFT` + `Return`           | Firefox                   |
| `SUPER` + `SHIFT` + `n`                | Gestore file (nautilus)   |

### Finestre

| Tasti                            | Azione                                |
| -------------------------------- | ------------------------------------- |
| `SUPER` + `w`                    | Chiude la finestra                    |
| `SUPER` + direzione              | Sposta il focus in quella direzione   |
| `SUPER` + `SHIFT` + direzione    | Scambia la finestra con quella vicina |
| `SUPER` + `f`                    | Schermo intero sì/no                  |
| `SUPER` + `SHIFT` + `space`      | Flottante sì/no                       |
| `SUPER` + `r`                    | Larghezza: 50% → 80% → 100%           |
| `SUPER` + `SHIFT` + `f`          | Larghezza 100%                        |
| `SUPER` + `Tab`                  | Panoramica di tutte le finestre       |
| `SUPER` + trascinamento sinistro | Sposta la finestra                    |
| `SUPER` + trascinamento destro   | Ridimensiona la finestra              |

### Tag

| Tasti                       | Azione                                              |
| --------------------------- | --------------------------------------------------- |
| `SUPER` + `1`…`9`           | Va al tag 1…9                                       |
| `SUPER` + `SHIFT` + `1`…`9` | Manda la finestra al tag 1…9                        |
| `SUPER` + rotellina         | Tag precedente / successivo tra quelli con finestre |

### Volume, luminosità, screenshot

| Tasti                  | Azione                                                                                 |
| ---------------------- | -------------------------------------------------------------------------------------- |
| Tasti del volume       | Volume ±5%, muto, muto del microfono                                                   |
| Tasti della luminosità | Schermo ±5%, tastiera ±10%                                                             |
| `Print`                | Screenshot di una regione, negli appunti                                               |
| `SHIFT` + `Print`      | Screenshot dello schermo, in `~/Pictures/Screenshots/` (la cartella deve già esistere) |

### Sessione

| Tasti                   | Azione                              |
| ----------------------- | ----------------------------------- |
| `SUPER` + `SHIFT` + `r` | Ricarica la configurazione di mango |
| `SUPER` + `SHIFT` + `e` | Esce da mango                       |

## Barra

| Modulo     | Mostra                    | Clic                         | Clic destro             | Rotellina |
| ---------- | ------------------------- | ---------------------------- | ----------------------- | --------- |
| Wi-Fi      | Nome della rete e segnale | Sceglie una rete (nmtui)     | Wi-Fi acceso/spento     |           |
| Bluetooth  | Dispositivo connesso      | Associa e connette (bluetui) | Bluetooth acceso/spento |           |
| Luminosità | Luminosità dello schermo  |                              |                         | ±5%       |
| Volume     | Volume di uscita          | Muto sì/no                   |                         | Volume    |
| CPU        | Carico della CPU          |                              |                         |           |
| Memoria    | RAM in uso                |                              |                         |           |
| Batteria   | Carica                    |                              |                         |           |

## Applicare le modifiche

| Programma  | Come                                                                                 |
| ---------- | ------------------------------------------------------------------------------------ |
| mango      | `SUPER` + `SHIFT` + `r`. Controllo errori: `mango -c ~/.config/mango/config.conf -p` |
| waybar     | `pkill waybar; waybar &`                                                             |
| mako       | `makoctl reload`                                                                     |
| foot, rofi | Basta aprirne uno nuovo                                                              |
