![blue-pack_wiki_banner](https://github.com/glitched-nx/blue_pack_NX/raw/blue_pack/blue_pack_NX_wiki/pics/blue-pack_wiki_banner.png)

<div align="center">

## Punkt Nr.12 - Neufassung
</div>

### - Upgrade oder Wechsel von einem anderen oder älteren CFW Setup.
### - Download und Update der Switch Firmware. 

Willkommen zur ```Neufassung``` unserer ```Punkt Nr. 12```. Diese Anleitung unterstützt dich Schritt für Schritt bei der Durchführung eines ```CFW - emuMMC```-Upgrades oder -Wechsels zu unserem neuesten ```NX blue pack - All in One CFW Pack```, um deine Switch-Konsole mittels der saubersten Methode auf den neuesten Stand zu bringen. Ganz egal, ob deine Konsole noch ein älteres CFW-emuMMC-Setup von uns hat oder ein CFW-Setup von Dritten genutzt wurde.

Umfassender als die bisherige Punkt Nr. 12 und auf das aktuelle ```NX blue pack``` abgestimmt. Hier erfährst du, wie die SD-Karte richtig vorbereitet wird, welche alten CFW-Daten erhalten bleiben müssen und welche Daten gelöscht werden.

Außerdem enthält die ```Neufassung``` jetzt einen detaillierteren Leitfaden zum anschließenden Firmware-Update. Dieses kannst du ohne PC direkt an der Switch Konsole durchführen.

### ```Hinweise:```
- Punkt Nr. 12 war und ist ```nicht``` für die Ersteinrichtung geeignet!
- Eine mittels ```RCM/Payload``` oder ```ModChip``` gehackte Switch-Konsole ist Voraussetzung. Die Ersteinrichtung muss bereits abgeschlossen sein. Zudem sollte ```emuMMC``` entweder als ```RAW Partition``` oder als ```SD File``` eingerichtet sein, da unser NX blue pack darauf ausgelegt ist. Wenn diese Voraussetzungen erfüllt sind, ist Punkt Nr. 12 die richtige für dich.

### ```Vorsicht:```
- **Formatiere nicht die SD-Karte.** Dadurch werden alle Spieledaten, wie Spielstände und installierte Spiele unwiderruflich gelöscht.

- **```Wenn du dieser Anleitung folgst, bleiben deine Spiele und Spielstände erhalten.```**

## I.    SD-Karte vorbereiten und bereinigen!

1. Starte die Switch neu, um den Hekate Bootloader zu laden.
   - Falls die Switch ausgeschaltet ist, führe bei einer V1 Switch die RCM-Payload-Methode aus oder starte die Switch ganz normal, wenn ein ModChip eingebaut ist.
   - Verbinde deine Switch per USB-Kabel mit dem PC.
   - Aktiviere die ```Hekate UMS```-Funktion, um die SD-Karte deiner Switch als ```USB-Massenspeicher``` zu nutzen:
   - Navigiere dazu im Hekate-Menü zu ```Tools```, wähle ```USB Tools``` und dann ```SD Card```, um die Funktion zu aktivieren.

2. Auf deinem PC sollte nun ein Laufwerk mit dem Namen ```SWITCH SD``` erscheinen. 
   - Öffne dieses Laufwerk und positioniere das Fenster so, dass du den gesamten Inhalt im Blick hast.

3. Die ```Abbildungen``` unten zeigen den Inhalt der Switch SD-Karte vor und nach dem Bereinigen:
   - ```Hellgrau markierte Ordner und Dateien werden gelöscht.```
   - ```Wichtig:``` Die Ordner ```emuMMC``` und ```Nintendo``` ```NICHT löschen!```
   - ```Lösche nur die Ordner und Dateien, die entsprechend markiert sind.```
   - Dateien und Ordner, die auf deiner SD-Karte sind, aber in den Abbildungen nicht zu sehen sind, gehören nicht zur Grundstruktur des CFW-Setups. Lies dazu mehr im nächsten Punkt.

4. Weiter geht's im Ordner ```switch```:
   - Lösche darin ebenfalls alles, was in der Abbildung hellgrau markiert ist. ```tinfoil```, ```linkalho``` und ```JKSV``` bleiben erhalten, da sie wichtige Daten wie Backups und Shop-Adressen enthalten.

   - Ordner/Dateien, die sich zusätzlich auf der SD-Karte befinden, wie z.B. ```switchroot```, ```Android```, ```Lakka```, ```DBI```, ```RetroArch```, ```Roms```, ```Tinfoil```, ```TegraExplorer```, ```Themes``` etc., sind für das CFW-Upgrade nicht relevant und können/sollten auf der SD-Karte bleiben.

5. Kehre anschließend zum Hauptverzeichnis der SD-Karte zurück.

![blue-pack_wiki_guide_12_1](https://github.com/glitched-nx/blue_pack_NX/raw/blue_pack/blue_pack_NX_wiki/pics/guide_12_pic_1.png)

---

## II. Upgrade durchführen mit der aktuellen ZIP-Datei des ```NX blue pack - AIO CFW Pack```

1. Lade das neueste NX blue pack [hier](https://github.com/glitched-nx/blue_pack_NX/releases/latest) herunter.

2. Entpacke den gesamten Inhalt der Datei ```blue_pack_NX.zip``` in das Hauptverzeichnis der SD-Karte.
   - Es ist wichtig, alle Dateien vollständig und korrekt zu entpacken und gegebenenfalls zu ersetzen.

![blue-pack_wiki_guide_12_2](https://github.com/glitched-nx/blue_pack_NX/raw/blue_pack/blue_pack_NX_wiki/pics/guide_12_pic_2.png)

3. Die SD-Karte ist nun bereit und kann sicher vom PC entfernt werden.
   - Klicke dazu mit der rechten Maustaste auf das Switch-SD-Laufwerk.
   - Wähle "Auswerfen" aus dem Kontextmenü.
   - Entferne das USB-Kabel erst nach dem sicheren Auswerfen.

4. Wechsle in Hekate zurück zum ```Home```-Bildschirm und führe einen ```Reload``` durch, indem du den ```Reload```-Button unten im Hekate-Homescreen berührst und bestätigst.
   - Der Arbeitsspeicher wird durch den Reload mit den neuen Daten der SD-Karte geladen und Hekate wird neu gestartet.
   - Nach dem Reload muss die Uhrzeit in Hekate neu eingestellt werden.

5. Starte von Hekate Home aus ins Launch-Menü und wähle den Button ```atmosphere blue emu```, um in die CFW zu starten.
   - Achte darauf, dass die Systemuhrzeit korrekt eingestellt ist. Falls dies nicht der Fall ist, kannst du sie im Homebrew-Menü mit der App ```SwitchTime``` korrigieren. Starte die App und drücke nacheinander ```Y``` -> ```A``` -> ```+``` bei aktiver Internetverbindung.
   - Hinweis: Stelle die Uhrzeit nicht manuell ein, da Tinfoil sonst den Download verweigert, weil die Uhrzeit falsch ist.

---

## III. Firmware-Download und Update mit Daybreak Quick direkt über die Switch

#### Für das Firmware-Update kannst du deine Switch-Konsole direkt nutzen. Folge diesen Schritten:

1. Öffne im Hauptmenü das ```Homebrew-Menü```, indem du das Album auswählst.
2. Starte das Tool ```AIO Switch Updater - Switch```.
   - Navigiere zu ```Download Firmwares```.
   - Wähle die aktuelle Firmware auf der rechten Seite aus und bestätige die Auswahl. Für einen schnelleren Download empfehlen wir die Quelle ```mega.nz```.
   - Die Firmware wird heruntergeladen, automatisch entpackt und als Ordner namens ```firmware``` im Hauptverzeichnis der SD-Karte abgelegt.
3. Schließe das Tool und kehre mit der Taste ```+``` zum ```Homebrew-Menü``` zurück.
4. Starte nun ```Daybreak Quick```, um das Update durchzuführen.
   - Wähle ```Weiter```, um fortzufahren.
   - Wähle den Firmware-Ordner ```firmware``` aus dem vorherigen Download aus und bestätige mit der Taste ```A```.
   - Beginne das Firmware-Update mit ```Update jetzt durchführen``` nach erfolgreicher Überprüfung.
5. Nach Abschluss des Updatevorgangs ist ein Neustart erforderlich.
   - Wähle ```Switch neustarten```, um den Neustart einzuleiten. Nach dem Neustart wird Hekate gestartet.
6. Starte von Hekate aus über das Launch-Menü erneut mit dem Button ```atmosphere blue emu```, um das Firmware-Update abzuschließen.

---

### Glückwunsch, deine Switch läuft jetzt mit dem neuesten ```NX blue pack``` und der aktuellen ```Firmware```.

Um die aktuelle Version deiner System- oder Atmosphere-Software zu überprüfen, öffne die Systemeinstellungen. Scrolle ganz nach unten zu ```Konsole``` und wähle dann rechts ```System-Update``` aus.

---

<div align="center" style="font-size: 1.5em;">
  <img src="https://img.shields.io/github/v/release/THZoria/NX_Firmware?style=for-the-badge&label=Aktuelle%20Systemversion&labelColor=123ede&color=b3b9e8" alt="Aktuelle Systemversion" />
  | 
  <img src="https://img.shields.io/github/v/release/glitched-nx/atmo_blue?include_prereleases&style=for-the-badge&label=BLUE&labelColor=123ede&color=b3b9e8" alt="BLUE" />
  | E
  </p>
</div>

---

<div align="center">

![GitHub License](https://img.shields.io/github/license/Atmosphere-NX/Atmosphere?style=for-the-badge&labelColor=123ede&color=123ede)&emsp;
[![NX blue pack - AIO CFW PACK](https://img.shields.io/github/v/release/glitched-nx/blue_pack_nx?style=for-the-badge&label=NX%20blue%20pack%20-%20AIO%20CFW%20PACK&labelColor=123ede&color=b3b9e8)](https://github.com/glitched-nx/blue_pack_NX/releases/latest)&emsp;
[![NX blue pack DLs](https://img.shields.io/github/downloads/glitched-nx/blue_pack_nx/total?style=for-the-badge&label=NX%20blue%20pack%20Downloads&labelColor=123ede&color=b3b9e8)](https://github.com/glitched-nx/blue_pack_NX/releases/latest)


[![CFW - Homebrew - Modding Deutschland](https://img.shields.io/badge/CFW%20--%20Homebrew%20--%20Modding%20Deutschland-b3b9e8?style=for-the-badge&logo=facebook&logoColor=123ede)](https://facebook.com/groups/switchcfwde)&emsp;
[![NX blue pack WIKI](https://img.shields.io/badge/NX%20blue%20pack%20WIKI-b3b9e8?style=for-the-badge&logo=facebook&logoColor=123ede)](https://github.com/glitched-nx/blue_pack_NX/wiki)


</div>