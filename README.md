# dotfiles

Configurazione minimale di mangowm (layout scroller, animazioni leggere), waybar, mako, foot, rofi.
Font: JetBrainsMono Nerd Font (`ttf-jetbrains-mono-nerd`); le icone della barra sono glifi di questo font.

Pacchetti: `mangowm waybar mako foot rofi swaybg grim slurp wl-clipboard brightnessctl networkmanager bluez-utils bluetui ttf-jetbrains-mono-nerd`

Installazione: copiare `.config/*` in `~/.config/`.

## Cosa si trova dove

Ogni impostazione è spiegata da un commento subito sopra di essa, nel file stesso.

| File | Programma | Cosa controlla |
| --- | --- | --- |
| `.config/mango/config.conf` | mangowm (compositor) | Monitor, avvio automatico, aspetto, animazioni, layout, input, tutte le scorciatoie di tastiera e mouse |
| `.config/waybar/config.jsonc` | waybar (barra di stato) | Quali moduli mostra la barra e cosa scrivono |
| `.config/waybar/style.css` | waybar | Font, colori e spaziatura della barra |
| `.config/mako/config` | mako (notifiche) | Posizione, colori e durata dei popup di notifica |
| `.config/foot/foot.ini` | foot (terminale) | Font del terminale |
| `.config/rofi/config.rasi` | rofi (launcher) | Comportamento e aspetto del launcher |

I colori sono gruvbox dark in tutti i file.

## Tasti

`SUPER` è il tasto Windows. I tasti direzionali sono `h` `j` `k` `l` oppure le frecce.

| Tasti | Azione |
| --- | --- |
| `SUPER` + `Return` | Terminale (foot) |
| `SUPER` + `d` o `space` | Launcher delle app (rofi) |
| `SUPER` + `SHIFT` + `Return` | Firefox |
| `SUPER` + `SHIFT` + `n` | Gestore file (nautilus) |
| `SUPER` + `w` | Chiude la finestra |
| `SUPER` + direzione | Sposta il focus sulla finestra in quella direzione |
| `SUPER` + `SHIFT` + direzione | Scambia la finestra con quella vicina |
| `SUPER` + `f` | Schermo intero sì/no |
| `SUPER` + `SHIFT` + `space` | Finestra flottante sì/no |
| `SUPER` + `r` | Alterna la larghezza della finestra: 50% → 80% → 100% |
| `SUPER` + `SHIFT` + `f` | Larghezza della finestra al 100% |
| `SUPER` + `Tab` | Panoramica di tutte le finestre |
| `SUPER` + `1`…`9` | Va al tag 1…9 |
| `SUPER` + `SHIFT` + `1`…`9` | Manda la finestra al tag 1…9 |
| `SUPER` + rotellina | Tag precedente/successivo che contiene finestre |
| `SUPER` + trascinamento sinistro / destro | Sposta / ridimensiona la finestra |
| Tasti del volume | Volume ±5%, muto, muto del microfono |
| Tasti della luminosità | Schermo ±5%, retroilluminazione della tastiera ±10% |
| `Print` | Screenshot di una regione negli appunti |
| `SHIFT` + `Print` | Screenshot dello schermo in `~/Pictures/Screenshots/` (creare prima la cartella) |
| `SUPER` + `SHIFT` + `r` | Ricarica la configurazione di mango |
| `SUPER` + `SHIFT` + `e` | Esce da mango |

## Barra

| Modulo | Mostra | Mouse |
| --- | --- | --- |
| Wi-Fi | Nome della rete e segnale | Clic: sceglie una rete (nmtui). Clic destro: Wi-Fi acceso/spento |
| Bluetooth | Dispositivo connesso | Clic: associa/connette i dispositivi (bluetui). Clic destro: Bluetooth acceso/spento |
| Luminosità | Luminosità dello schermo | Rotellina: ±5% |
| Volume | Volume di uscita | Rotellina: volume. Clic: muto |
| CPU, memoria, batteria | Carico della CPU, RAM in uso, carica della batteria | |

## Applicare le modifiche

| Programma | Come |
| --- | --- |
| mango | `SUPER` + `SHIFT` + `r`; controllare gli errori con `mango -c ~/.config/mango/config.conf -p` |
| waybar | `pkill waybar; waybar &` |
| mako | `makoctl reload` |
| foot, rofi | Aprirne uno nuovo |
