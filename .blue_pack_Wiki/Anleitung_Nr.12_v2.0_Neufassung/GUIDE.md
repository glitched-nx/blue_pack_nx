<div style="text-align: center;">
  <h2 style="color: #0055EE;"><strong><em>blue pack NX - Anleitung Nr. 12 v2.0</em></strong></h2>
  <p style="color: #0055FF;"><em>Upgrade/Wechsel von einem anderen/älteren CFW-Pack auf das blue pack NX - Firmware Download & Update</em></p>
  <p style="color: #0055FF;"><em></em></p>
</div>

---

*Willkommen zur Neufassung unserer* ***Anleitung Nr. 12*** *gehen wir Schritt für Schritt mit dir durch, wie du das CFW-Setup, auf deiner Switch manuell auf das neueste* ***blue pack NX*** *upgraden kannst.* ***Anleitung Nr. 12 ist umfassender*** *als die bisherige und auf das aktuelle blue pack NX abgestimmt.*

*Zur vorbereitung der SD-Karte vor den Upgrade, erfährst du wie richtig von alten CFW-Daten bereinigt wird und welche dabei Daten verschont bleiben müssen. Egal, ob du von einem älteren oder anderen CFW-Pack zum blue pack NX wechseln möchtest - hier in* ***Anleitung Nr. 12 v2.0*** *findest du die notwendigen Schritte.*

*Außerdem führt* ***Anleitung Nr. 12 v2.0*** *jetzt detaillierter durch das anschließende Firmware-Update, dass du direkt über deine Konsole herunterzuladen und zu aktualisieren kannst.*

---

<div align="left">

<p style="color: #FF0000;"><em>Vorsicht: Formatiere die SD-Karte nicht, dadurch wird dein CFW-Setup, alle Spielstände und installierte Spiele unwiderruflich gelöscht.</em></p>
</div>

- ***Alle Spiele und Spielstände bleiben erhalten, wenn du dieser Anleitung folgst.***

- ***Um die Schritte in Anleitung Nr. 12 durchzuführen, wird eine gehackte Switch (mit ModChip oder RCM Bug) benötig, die bereits eine Custom Firmware mit emuMMC Partition/SD File eingerichtet hat.***

---

<div style="text-align: center;">
  <h3 style="color: #0055FF;"><strong><em>SD-Karte bereinigen - Upgrade / Wechsel durchführen</em></strong></h2>
</div>

1. *Starte den Hekate Bootloader und verbinde deine Switch per USB-Kabel mit dem PC.*

2. *Aktiviere die `Hekate UMS`-Funktion, um die SD-Karte deiner Switch als `USB-Massenspeicher` zu nutzen:*
   - *Navigiere im Hekate-Menü zu `Tools`, wähle `USB Tools` und dann `SD Card`, um die Funktion zu aktivieren.*

3. *Auf deinem PC sollte nun ein Laufwerk mit dem Namen `SWITCH SD` erscheinen. Öffne dieses Laufwerk und positioniere das Fenster so, dass du den gesamten Inhalt im Blick hast.*

4. *Die folgende bildliche Darstellung zeigt die Dateistruktur der SD-Karte:*
   - *Markierungen geben an, welche Dateien und Ordner gelöscht werden sollen. Diese entsprechen der Grundstruktur der `blue_pack_NX.zip`-Datei.*
   - ***Wichtig:*** *Die Ordner `emuMMC` und `Nintendo`* ***nicht löschen!***
   - *Lösche nur die Ordner und Dateien, die entsprechend markiert sind.*

   ---

<style>
  /* Dark Mode Bild */
  .lightmode { display: none; }
  @media (prefers-color-scheme: dark) {
    .darkmode { display: inline; }
    .lightmode { display: none; }
  }
  /* Light Mode Bild */
  @media (prefers-color-scheme: light) {
    .darkmode { display: none; }
    .lightmode { display: inline; }
  }
</style>

<!-- Bilder für Light- und Darkmode -->
<img src="https://github.com/glitched-nx/blue_pack_NX/raw/blue_pack/.blue_pack_Wiki/Anleitung_Nr.12_v2.0_Neufassung/pix/guide_12-1_light.png" class="lightmode" alt="Guide Bild Lightmode">
<img src="https://github.com/glitched-nx/blue_pack_NX/raw/blue_pack/.blue_pack_Wiki/Anleitung_Nr.12_v2.0_Neufassung/pix/guide_12-1_dark.png" class="darkmode" alt="Guide Bild Darkmode">

---

5. *Öffne den Ordner* ***switch:***
   -  *lösche alles außer `tinfoil`, `linkalho` und `JKSV`. Diese enthalten wichtige Daten wie Backups und Shop-Adressen.*

   - *Ordner/Dateien, die sich zusätzlich auf der SD-Karte befinden, wie z.B. `switchroot`, `Android`, `Lakka`, `DBI`, `RetroArch`, `Roms`, `Tinfoil`, `TegraExplorer`, `Themes` etc., sind für ein Upgrade nicht relevant und sollten auf der SD-Karte bleiben.*

5. *Kehre anschließend zum Hauptverzeichnis der SD-Karte zurück.*

6. *Lade das neueste blue pack NX [HIER](https://github.com/glitched-nx/blue_pack_NX/releases/latest) herunter.*

7. *Entpacke den gesamten Inhalt der Datei `blue_pack_NX.zip` in das Hauptverzeichnis der SD-Karte. Bestätige die Aufforderung zum Ersetzen von Dateien mit "Ja".*

---

<style>
  /* Dark Mode Bild */
  .lightmode { display: none; }
  @media (prefers-color-scheme: dark) {
    .darkmode { display: inline; }
    .lightmode { display: none; }
  }
  /* Light Mode Bild */
  @media (prefers-color-scheme: light) {
    .darkmode { display: none; }
    .lightmode { display: inline; }
  }
</style>

<!-- Bilder für Light- und Darkmode -->
<img src="https://github.com/glitched-nx/blue_pack_NX/raw/blue_pack/.blue_pack_Wiki/Anleitung_Nr.12_v2.0_Neufassung/pix/guide_12-2_light.png" class="lightmode" alt="Guide Bild Lightmode">
<img src="https://github.com/glitched-nx/blue_pack_NX/raw/blue_pack/.blue_pack_Wiki/Anleitung_Nr.12_v2.0_Neufassung/pix/guide_12-2_dark.png" class="darkmode" alt="Guide Bild Darkmode">

---


8. *Die SD-Karte ist nun bereit und kann sicher vom PC entfernt werden.* 
    - *Klicke dazu mit der rechten Maustaste auf das Switch-SD-Laufwerk.*
    - *Wähle "Auswerfen" aus dem Kontextmenü.*
    - *Entferne das USB-Kabel erst nach dem sicheren Auswerfen.*

9. *Wechsle in Hekate zurück zum `Home`-Bildschirm und führe einen Reload durch, indem du den `Reload`-Button unten im Hekate-Homescreen berührst und bestätigst.*

10. *Der Arbeitsspeicher wird durch den Reload mit den neuen Daten der SD-Karte geladen und Hekate wird neu gestartet.*
    - *Nach dem Reload muss die Uhrzeit in Hekate neu eingestellt werden.*

11. *Starte über das Launch-Menü `atmosphere blue emu`.*
    - *Achte darauf, dass die Systemuhrzeit korrekt eingestellt ist. Falls dies nicht der Fall ist, kannst du sie im Homebrew-Menü mit der App `SwitchTime` korrigieren. Starte die App und drücke nacheinander `Y` -> `A` -> `+`, bei aktiver Internetverbindung.*
    - *Hinweis: Stelle die Uhrzeit nicht manuell ein, da Tinfoil sonst den Download verweigert, weil die Uhrzeit falsch ist.*

---

<div style="text-align: center;">
  <h3 style="color: #0055FF;"><strong><em>Firmware-Download und Update mit Daybreak Quick</em></strong></h2>
</div>

1. Lade die aktuelle Switch-Firmware mit dem Tool `AIO Switch Updater` im Homebrew-Menü herunter.
   - Gehe zu `Download Firmwares`.
   - Wähle auf der rechten Seite die aktuelle Firmware aus und bestätige die Auswahl. Für einen schnelleren Download empfehlen wir die Quelle `mega.nz`.
   - Die Firmware wird heruntergeladen, automatisch entpackt und als Ordner namens `firmware` im Hauptverzeichnis der SD-Karte abgelegt.

2. Schließe den ***`AIO Switch Updater`*** mit der Taste **`+`**.

3. Kehre zum ***`Homebrew-Menü`*** zurück.

4. Starte `Daybreak Quick`, um das Update durchzuführen.
   - Wähle ***`Weiter`***, um fortzufahren.
   - Wähle den Firmware-Ordner `firmware` aus dem vorherigen Download aus und bestätige mit der ***`A`***-Taste.
   - Beginne das Firmware-Update mit ***`Update jetzt durchführen`*** nach erfolgreicher Überprüfung.

5. Nach Abschluss des Updatevorgangs ist ein Neustart erforderlich.
   - Wähle `Switch neustarten`, um den Neustart einzuleiten.
   - Hekate wird gestartet.

6. Starte über das Launch-Menü erneut ***`atmosphere blue emu`***, um das ***`Firmware-Update abzuschließen`***.

---

<div style="text-align: center;">
  <h2 style="color: #0088FF;"><strong><em>Glückwunsch!</em></strong></h2>
</div>



Deine Switch läuft jetzt mit dem neuesten `blue pack NX` und der aktuellen `Firmware`.

*Um die aktuelle Version deiner System- oder Atmosphere-Software zu überprüfen, öffne die Systemeinstellungen. Scrolle ganz nach unten zu "Konsole" und wähle dann rechts "System-Update" aus.*

## Aktuelle Systemversion [**1x.x.x**](*) | blue [**1.x.x**](*) | *E*  <img alt="" src="https://img.shields.io/github/v/tag/glitched-nx/blue_pack_nx?style=social&logoSize=auto&labelColor=%23abc4ff&color=%230d3ce6">

```
https://github.com/glitched-nx/blue_pack_NX/releases/latest
```

