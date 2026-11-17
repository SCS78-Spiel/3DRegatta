# Regatta 3D – Mehrspieler-Version für GitHub Pages

Ein 3D-Segelspiel im Browser. Bis zu 12 Leute segeln live gegeneinander; der Host zeigt einen QR-Code, alle anderen scannen ihn.

## Online stellen (ca. 5 Minuten)

1. Auf https://github.com ein Konto anlegen bzw. einloggen.
2. Oben rechts **+ → New repository**: Name z. B. `regatta`, **Public**, dann **Create repository**.
3. Im neuen Repository **Add file → Upload files**, die Datei `index.html` hineinziehen, unten **Commit changes**.
4. **Settings → Pages**: bei *Source* „Deploy from a branch“, Branch `main` und Ordner `/ (root)` wählen, **Save**.
5. Nach 1–2 Minuten ist das Spiel erreichbar unter `https://scs78-spiel.github.io/3DRegatta/`.

## Spielen

1. Am Laptop/Beamer (oder Handy) die Seite öffnen, im Menü Klasse, Kurs, Runden und KI-Stärke wählen.
2. **Mehrspieler (QR-Code) → Rennen hosten**. Es erscheint ein QR-Code und ein 5-stelliger Code.
3. Mitspieler scannen den QR-Code, geben ihren Namen ein und tippen **Beitreten**
   (oder Seite öffnen → Mehrspieler → Code eingeben).
4. Sind alle in der Liste, startet der Host mit **Rennen starten**. Freie Plätze bis 6 Boote füllen KI-Boote auf (abschaltbar).

## Regattaleitung & Analyse

- Im Mehrspieler-Menü **„Ich segle nicht mit – Regattaleitung“** ankreuzen: Der Host segelt nicht mit, sieht das ganze Feld in der Totalen (Rangliste antippen = Boot verfolgen, ziehen = drehen, Mausrad/＋－ = Zoom) und das Rennen wird aufgezeichnet.
- **Beenden & analysieren** öffnet die Rennanalyse: alle Kurse auf der Karte, Zeitleiste zum Abspielen, Tabelle mit Zeiten, Ø-/Max-Speed, Strecke, Wenden/Halsen, Strafen und Schenkelzeiten je Boot.
- **3D-Wiedergabe ab hier** spielt das Rennen in 3D nach (1×–16×, Totale oder einzelnes Boot verfolgen).
- **Aufzeichnung speichern** lädt eine .json-Datei herunter; über **Aufzeichnung laden** im Hauptmenü lässt sie sich später wieder analysieren. Jedes Rennen (auch Einzelspieler) wird automatisch aufgezeichnet – „Letztes Rennen analysieren“ im Menü.

## Gut zu wissen

- Der **Host muss das Spiel offen und im Vordergrund lassen** – sein Browser steuert die KI-Boote und verteilt die Positionen.
- Die Verbindung läuft direkt zwischen den Browsern (WebRTC). Zum Verbindungsaufbau wird der kostenlose PeerJS-Dienst (peerjs.com) genutzt; es entstehen keine Kosten und es wird kein eigener Server gebraucht.
- In manchen Firmen-/Schul-WLANs oder Mobilfunknetzen werden direkte Verbindungen blockiert. Dann hilft meist ein anderes Netz (z. B. Handy-Hotspot).
- Testen ohne zweites Gerät: zwei Tabs mit `…/3DRegatta/?net=local` öffnen – dann läuft der Mehrspieler-Modus lokal über den Browser.

## In eine bestehende Website einbauen

```html
<iframe src="https://scs78-spiel.github.io/3DRegatta/" style="width:100%;height:85vh;border:0;border-radius:12px" allow="fullscreen; autoplay"></iframe>
```
Der QR-Code zeigt dann auf die GitHub-Pages-Adresse des Spiels – Mitspieler landen direkt im Spiel.
