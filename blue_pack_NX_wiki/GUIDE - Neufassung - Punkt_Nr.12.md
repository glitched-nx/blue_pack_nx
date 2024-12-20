![blue-pack_wiki_banner](https://github.com/glitched-nx/blue_pack_NX/raw/blue_pack/blue_pack_NX_wiki/pics/blue-pack_wiki_banner.png)

<div align="center">

## **`GUIDE Punkt Nr. 12 - Neufassung`**
### **`Upgrade/Wechsel von einem bestehenden CFW-Setup + emuMMC zum NX blue pack - AIO CFW PACK`**

</div>

### **`Im Guide enthalten:`**

- **Bereinigen der Switch SD-Karte von alten CFW-Dateien**
- **Herunterladen und Entpacken des `NX blue pack - AIO CFW PACK`**
  
- **Herunterladen der `Switch NX-Firmware` über die Konsole**
- **Durchführung eines Up- oder Downgrades der Firmware` mit Daybreak Quick**

---

### **`Berücksichtige folgende Hinweise:`**

- Dieser Guide ist **NICHT** für die `Ersteinrichtung` geeignet.

- Die Switch-Konsole muss bereits mit ModChip/RCM-Payload Hack modifiziert sein und ein fertiges CFW-Setup mit einem `Raw Partition` oder `SD File based` `emuMMC` eingerichtet sein.
- Das NX blue pack ist für `CFW - emuMMC Setups` ausgelegt.

- **Formatiere die SD-Karte **NICHT** einfach:**
  - Dadurch werden `emuMMC Partition` inkl. `deiner Profile`, alle `Spieledaten` wie `Spielstände` und `installierte Spiele` unwiderruflich gelöscht.
  - **Folge diesem Guide, und deine Daten sicher zu behalten.**

- Führe **KEIN** Firmware-Update durch, ohne vorab zu prüfen, ob die aktuellste `NX blue pack` noch kompatibel ist.
  - Dies ist über die [Release Notes](https://github.com/glitched-nx/blue_pack_NX/releases/latest) des `NX blue pack` CFW-Packs überprüfbar.
  - Die höchste kompatible Firmware-Version steht in den Release Notes:
    - **...kompatibel mit NX-Firmware 1x.x.x und niedriger.**


---

<div align="center">

### **`SD-Karte vorbereiten und bereinigen`**

</div>

1. Starte die Switch neu, um den Hekate Bootloader zu laden.
   - Falls die Switch ausgeschaltet ist, führe bei einer V1 Switch die RCM-Payload-Methode aus oder starte die Switch ganz normal, wenn ein ModChip eingebaut ist.
   - Verbinde deine Switch per USB-Kabel mit dem PC.
   - Aktiviere die ```Hekate UMS```-Funktion, um die SD-Karte deiner Switch als ```USB-Massenspeicher``` zu nutzen:
   - Navigiere dazu im Hekate-Menü zu ```Tools```, wähle ```USB Tools``` und dann ```SD Card```, um die Funktion zu aktivieren.
     - Alternativ kannst du die Switch auch ganz ausschalten, die SD-Karte aus der Konsole herausnehmen und mit einem SD-Kartenleser am PC auf die SD-Karte zugreifen und sie bearbeiten.

2. Auf deinem PC sollte nun ein Laufwerk mit dem Namen ```SWITCH SD``` erscheinen. 
   - Öffne dieses Laufwerk und positioniere das Fenster so, dass du den gesamten Inhalt im Blick hast.

#### **`Beachte:` Falls Windows beim Einhängen bzw. Anschließen der Switch-SD-Karte eine Fehlermeldung ausgibt und eine Formatierung empfiehlt, führe diese auf KEINEN FALL durch!**

1. Die ```Abbildungen``` unten zeigen den Inhalt der Switch SD-Karte vor und nach dem Bereinigen:
   - ```Hellgrau markierte Ordner und Dateien werden gelöscht.```
   - ```Wichtig:``` Die Ordner ```emuMMC``` und ```Nintendo``` ```NICHT löschen!```
   - ```Lösche nur die Ordner und Dateien, die entsprechend markiert sind.```
   - Dateien und Ordner, die auf deiner SD-Karte sind, aber in den Abbildungen nicht zu sehen sind, gehören nicht zur Grundstruktur des CFW-Setups. Lies dazu mehr im nächsten Punkt.

2. Weiter geht's im Ordner ```switch```:
   - Lösche darin ebenfalls alles, was in der Abbildung hellgrau markiert ist. ```tinfoil```, ```linkalho``` und ```JKSV``` bleiben erhalten, da sie wichtige Daten wie Backups und Shop-Adressen enthalten.

   - Ordner/Dateien, die sich zusätzlich auf der SD-Karte befinden, wie z.B. ```switchroot```, ```Android```, ```Lakka```, ```DBI```, ```RetroArch```, ```Roms```, ```Tinfoil```, ```TegraExplorer```, ```Themes``` etc., sind für das CFW-Upgrade nicht relevant und können/sollten auf der SD-Karte bleiben.

3. Kehre anschließend zum Hauptverzeichnis der SD-Karte zurück.

![blue-pack_wiki_guide_12_1](https://github.com/glitched-nx/blue_pack_NX/raw/blue_pack/blue_pack_NX_wiki/pics/guide_12_pic_1.png)

---

<div align="center">

### **`NX blue pack - AIO CFW PACK - Herunterladen und Entpacken`**

</div>

1. Lade das neueste NX blue pack [hier](https://github.com/glitched-nx/blue_pack_NX/releases/latest) herunter.

2. Entpacke den gesamten Inhalt der Datei ```blue_pack_NX.zip``` in das Hauptverzeichnis der SD-Karte.
   - Es ist wichtig, alle Dateien vollständig und korrekt zu entpacken und gegebenenfalls zu ersetzen.

![blue-pack_wiki_guide_12_2](https://github.com/glitched-nx/blue_pack_NX/raw/blue_pack/blue_pack_NX_wiki/pics/guide_12_pic_2.png)

3. Die SD-Karte ist nun bereit und kann sicher vom PC entfernt werden.
   - Klicke dazu mit der rechten Maustaste auf das Switch-SD-Laufwerk.
   - Wähle `Auswerfen` aus dem Kontextmenü.
   - Entferne das USB-Kabel erst nach dem sicheren Auswerfen.

4. Wechsle in Hekate zurück zum ```Home```-Bildschirm und führe einen ```Reload``` durch, indem du den ```Reload```-Button unten im Hekate-Homescreen berührst und bestätigst.
   - Der Arbeitsspeicher wird durch den Reload mit den neuen Daten der SD-Karte geladen und Hekate wird neu gestartet.
   - Nach dem Reload muss die Uhrzeit in Hekate neu eingestellt werden.

5. Starte von Hekate Home aus ins Launch-Menü und wähle den Button ```atmo blue - emummc```, um in die CFW zu starten.
   - Achte darauf, dass die Systemuhrzeit korrekt eingestellt ist. Falls dies nicht der Fall ist, kannst du die Uhrzeit mit der App ```DBI```im Homebrew-Menü synchronisieren. Starte ```DBI``` und öffne  ```Tools```, wähle `NTP time sync`. `NTP time sync` ist nur bei aktiver Internetverbindung im Menü sichtbar.
   - Hinweis: Versuche die Uhrzeit nicht manuell einzustellen, da Tinfoil sonst den Download verweigert, weil die Uhrzeit falsch ist.

---

<div align="center">

### **`NX - Firmware über die Switch-Konsole herunterladen`**

</div>

 
**`Download über AIO Switch Updater - Switch`**

1. Öffne das Homebrew-Menü im Switch-Hauptmenü, indem du das Album auswählst.
2. Starte das Tool `AIO Switch Updater - Switch`.
3. Navigiere zu `Download Firmwares`.
4. Wähle die aktuelle Firmware auf der rechten Seite aus und bestätige die Auswahl.
   - Tipp: Lade die Firmware über den `mega.nz`-Link herunter. Der Download ist deutlich schneller als über `archive.org`.
   - Die Firmware wird heruntergeladen, automatisch entpackt und als Ordner namens `firmware` im Hauptverzeichnis der SD-Karte abgelegt.
5. Schließe das Tool mit der `+` Taste.

6. Falls die neueste NX-Firmware im `AIO Switch Updater` nicht zur Verfügung steht, lade sie alternativ über das `Ultrahand-Overlay` herunter.

**`Download über Ultrahand-Overlay - Paket-Menü`**

7. Drücke die `L+R+PLUS` Tastenkombination gleichzeitig, um das Ultrahand-Overlay-Menü zu öffnen.
2. Navigiere mit den Richtungstasten zum Pakete-Menü und wähle dort das Paket `NX-Firmware Downloader` aus.
3. Wähle die aktuelle Firmware zum Download mit der `A` Taste aus.
   - Der Download wird durchgeführt und die Firmware anschließend entpackt im Hauptverzeichnis der SD-Karte abgelegt.
   - **Hinweise zum Download- und Entpackvorgang:**
      - Der angezeigte Prozentwert zählt während des Vorgangs zweimal bis auf 100% hoch, bis er im zweiten Durchlauf bei 100% stehen bleibt.
   - Die Firmware wurde nun fertig entpackt im Hauptverzeichnis der SD-Karte, als Ordner `Firmware 1x.x.x` abgelegt.
   - Schließe `NX-Firmware Downloader` und verlasse `Ultrahand Overlay`, jeweils mit der `B` Taste.
  
  ---

<div align="center">

### **`Up- oder Downgrade mit Daybreak Quick`**

</div>

1. Öffne das Homebrew-Menü.
2. Starte `Daybreak Quick`.
   - Wähle `Weiter`, um fortzufahren.
   - Wähle den Firmware-Ordner `firmware` aus dem vorherigen Download aus und bestätige mit der `A` Taste.
   - Beginne nach erfolgreicher Überprüfung das Firmware-Update mit `Update jetzt durchführen`.
3. Wähle `Switch neustarten`, um den Neustart einzuleiten. Nach dem Neustart wird Hekate gestartet.
4. Starte von Hekate aus über das Launch-Menü erneut mit dem Button `atmo blue - emummc`, um das Firmware-Update abzuschließen.

---

<div align="center">

### **`Glückwunsch, du hast das Upgrade erfolgreich durchgeführt!`**

</div>

Um die aktuelle Version deiner System- oder Atmosphere-Software zu überprüfen, öffne die Systemeinstellungen. Scrolle ganz nach unten zu ```Konsole``` und wähle dann rechts ```System-Update``` aus. 


<div align="center" style=`font-size: 1.5em;`>
  <img src="https://img.shields.io/github/v/release/THZoria/NX_Firmware?style=for-the-badge&label=Aktuelle%20Systemversion&labelColor=123ede&color=b3b9e8" alt="Aktuelle Systemversion" />
  | 
  <img src="https://img.shields.io/github/v/release/glitched-nx/atmo_blue?include_prereleases&style=for-the-badge&label=BLUE&labelColor=123ede&color=b3b9e8" alt="BLUE" />
  | E
  </p>
</div>

---

<div align="center">

### **Hilfe & Support**

</div>

- Du hast Fragen, Probleme oder möchtest anderen Mitgliedern deine Hilfe zu den Themen CFW - Homebrew - Modding anbieten? Tritt unseren Communities bei, um unter anderem Hilfe für das NX blue pack - AIO CFW PACK zu erhalten.
- Tritt bei unter folgende `Buttons`:

<div align="center">

[![CFW - Homebrew - Modding Deutschland](https://img.shields.io/badge/CFW%20--%20Homebrew%20--%20Modding%20Deutschland-b3b9e8?style=for-the-badge&logo=facebook&logoColor=123ede)](https://facebook.com/groups/switchcfwde)&emsp;&emsp;&emsp;&emsp;&emsp;&emsp;
[![Niklas Discord Server](https://img.shields.io/badge/Niklas%20Discord%20Server-b3b9e8?style=for-the-badge&logo=discord&logoColor=123ede)](https://discord.gg/niklas-discord-server-733728731432091648)

</div>

---
---
---

<div align="center">

![GitHub License](https://img.shields.io/github/license/Atmosphere-NX/Atmosphere?style=for-the-badge&labelColor=123ede&color=123ede)&emsp;
[![NX blue pack - AIO CFW PACK](https://img.shields.io/github/v/release/glitched-nx/blue_pack_nx?style=for-the-badge&label=NX%20blue%20pack%20-%20AIO%20CFW%20PACK&labelColor=123ede&color=b3b9e8)](https://github.com/glitched-nx/blue_pack_NX/releases/latest)&emsp;
[![NX blue pack DLs](https://img.shields.io/github/downloads/glitched-nx/blue_pack_nx/total?style=for-the-badge&label=NX%20blue%20pack%20Downloads&labelColor=123ede&color=b3b9e8)](https://github.com/glitched-nx/blue_pack_NX/releases/latest)


[![CFW - Homebrew - Modding Deutschland](https://img.shields.io/badge/CFW%20--%20Homebrew%20--%20Modding%20Deutschland-b3b9e8?style=for-the-badge&logo=facebook&logoColor=123ede)](https://facebook.com/groups/switchcfwde)&emsp;
[![NX blue pack WIKI](https://img.shields.io/badge/NX%20blue%20pack%20WIKI-b3b9e8?style=for-the-badge&logo=facebook&logoColor=123ede)](https://github.com/glitched-nx/blue_pack_NX/wiki)

</div>

---

<div align="center">

![glitched_nx_logo](https://github.com/glitched-nx/blue_pack_NX/raw/blue_pack/blue_pack_NX_wiki/pics/glitched_nx_metal_logo.png)

</div>