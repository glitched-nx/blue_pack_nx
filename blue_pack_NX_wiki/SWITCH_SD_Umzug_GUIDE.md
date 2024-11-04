## Umzug/Wechsel auf eine andere/größere SD-Karte

Das Ziel dieses Vorgangs ist es, den Speicherplatz der Switch-SD-Karte zu erweitern, um mehr Spiele speichern zu können. Dabei soll sichergestellt werden, dass installierte Spiele, Spielstände und Profile korrekt auf die neue, größere SD-Karte übertragen werden.


Unser [blue pack NX - AIO CFW PACK](https://github.com/glitched-nx/blue_pack_NX/releases/latest) ist, wie die meisten anderen CFW-Packs, auf die Einrichtung einer emuMMC-Partition ausgelegt. Daher sollten die meisten Nutzer bereits eine emuMMC-Partition eingerichtet haben.

### **Anleitung:**

Zuerst solltest du überprüfen, ob du ein dateibasiertes oder partitioniertes emuMMC hast:

1. Starte deine Switch neu um den Hekate Bootloader zu laden.
   - Ist die Switch ausgeschaltet, mittels RCM Payload Methode bzw. ganz normal anschalten bei eingebautem ModChip.

2. Gehe zu `emuMMC Info & Selection` und überprüfe den Text neben `Type`.
   - Wenn du ein emuMMC hast, sollte dort entweder `SD Raw Partition` oder `SD File` stehen.

-----

### Umzug auf eine neue SWITCH microSD, mit einem `SD-File` basierten emuMMC Setup.

Starte deine Switch neu um den Hekate Bootloader zu laden.
   - Ist die Switch ausgeschaltet, mittels RCM Payload Methode bzw. ganz normal anschalten bei eingebautem ModChip.
   - Ist Hekate gestartet, verbinde deine Switch per USB-Kabel mit dem PC.
   - Aktiviere die `Hekate UMS`-Funktion, um die SD-Karte deiner Switch als `USB-Massenspeicher` zu nutzen:
   - Navigiere im Hekate-Menü zu `Tools`, wähle `USB Tools` und dann `SD Card`, um die Funktion zu aktivieren.
   - Auf deinem PC sollte nun ein Laufwerk mit dem Namen `SWITCH SD` erscheinen. 
   - Öffne dieses Laufwerk und positioniere das Fenster so, dass du den gesamten Inhalt im Blick hast.
   - Kopiere den Inhalt der SD-Karte entweder zuerst auf den  auf deinen PC oder (On th fly) auf die andere/neue SD-Karte.
   - Greife mit einem SD-Kartenleser oder Ähnlichem auf die neue SD-Karte zu.
   - Formatiere die `neue SD-Karte` in FAT32 (Clustergröße 64Kb) mit einem `Partition Manager` oder einem kleinen Tool wie [SD Formatter](https://www.sdcard.org/downloads/formatter_4/).
   - Kopiere die Dateien vom PC oder direkt von der alten SD-Karte auf die neue SD-Karte.
   - Entferne das `UMS`-Gerät sicher über das Betriebssystem deines Computers.
   - Lege die neue SD-Karte in die Switch und starte wieder in den Hekate Bootloader.

-----

### Umzug auf eine neue SWITCH microSD, einem emuMMC `Raw Partition` Setup.

1. Im Hauptmenü von Hekate, tippe auf `Tools`, dann auf `Backup eMMC`. Stelle sicher, dass `SD emuMMC Raw Partition` unten auf dem Bildschirm auf `ON` gesetzt ist.
 Wie im foldendem Bild nummerierten Reihenfolge.

 ![emuMMC_Raw_backup](https://github.com/glitched-nx/blue_pack_NX/raw/blue_pack/blue_pack_NX_wiki/pics/emuMMC_Raw_backup.png)

2. Sichere sowohl `SD emuMMC BOOT0 & BOOT1` als auch `SD emuMMC RAW GPP`.
- Dieser Vorgang wird ein weicheb#n dauern. Ca. 20 Min


![emuMMC_backup_raw_b1_b2](https://github.com/glitched-nx/blue_pack_NX/raw/blue_pack/blue_pack_NX_wiki/pics/emuMMC_backup_raw_b1_b2.png)

3. Sobald beide Sicherungen abgeschlossen sind, kehre zum Hauptmenü zurück. Navigiere zu `Tools` > `USB Tools` > `SD Card` und verbinde die Switch über USB mit deinem PC.

- **Hinweis:** 
    - Falls Windows dich auffordert, ein Laufwerk zu formatieren, **ignoriere dies**. 
    - Öffne stattdessen das zugängliche Laufwerk mit dem Inhalt der alten SD-Karte.

4. Navigiere auf der SD-Karte zu `sdmc:/backup/<abcd1234>/`. Verschiebe das Verzeichnis `emummc` direkt über das `/restore` Verzeichnis.
Die Bildfolge, zeigen dir die schritte
![sd_partition_erista_oled](https://github.com/glitched-nx/blue_pack_NX/raw/blue_pack/blue_pack_NX_wiki/pics/sd_partition_erista_oled.png)

![sd_partition_erista_oled](https://github.com/glitched-nx/blue_pack_NX/raw/blue_pack/blue_pack_NX_wiki/pics/sd_partition_erista_oled.png)

5. Sichere anschließend die Ordner **backup**, **emuMMC** und **Nintendo**, der alten SD-Karte auf dem PC.

-----

### Die neue SD-Karte wie bei der Ersteinrichtung vorbereiten

- Formatiere die neue microSD in FAT32/exfat. Nagelneue microSD's sind bereits in exfat formatiert und brauchen nicht formatiert werden, da während der Partionierung später die Hauptpartition der SD Karte in FAT32 formatiert wird.

   - `By the Way` kannst du direkt die CFW aktualisieren und `blue pack NX` von [diesem Link](https://github.com/glitched-nx/blue_pack_NX/releases/latest) downloaden.
   - Entpacke den vollstände Zip-Datei `blue_pack_NX.zip` in das Hauptverzeichnis der neuen SD-Karte.
   - **Beachte:** Kopiere jetzt noch **KEINE** Daten der alten SD-Karte auf die neue, außer den CFW-Daten aus der ZIP-Datei. Du kannst [blue_pack_nx.zip](https://github.com/glitched-nx/blue_pack_NX/releases/latest/download/blue_pack_nx.zip) oder ein anderes CFW-Paket verwenden, das du bevorzugst.

#### Folge den Anweisungen im nächsten Abschnitt, um eine   emuMMC Partition neue microSD zu erstellen..
-----
## Partitionieren der SD-Karte für ein emuMMC (Raw Partition - Setup)

Starte deine Switch neu um den Hekate Bootloader zu laden.

- Ist die Switch ausgeschaltet, mittels RCM Payload Methode bzw. ganz normal anschalten bei eingebautem ModChip.

**Achtung:** Die Partitionierung *löscht* alle Daten auf der SD-Karte, *wenn* der Inhalt 2 GB überschreitet! Bleibt er darunter, werden alle Daten zwischengespeichert und nach der Partitionierung wiederhergestellt. Die Ordner `emuMMC` und `Nintendo` werden daher erst nach der Partitionierung auf die neue SD-Karte kopiert.

## Partitionierung mit Hekate

1. Navigiere zu `Tools` > `Partition SD card`.
2. Stelle den `emuMMC (RAW)`-Schieberegler in der Mitte der Leiste auf `29 FULL`.
   - Wenn du eine OLED-Switch verwendest, stelle den `emuMMC (RAW)`-Schieberegler auf `58 FULL`.
   - Falls du später Android und/oder Linux installieren möchtest, partitioniere die SD-Karte hier entsprechend, indem du die Schieberegler während dieses Schritts verschiebst. Wir empfehlen, die Schieberegler für `Android (USER)` und `Linux (EXT4)` auf mindestens 16 GB einzustellen.
3. Navigiere unten rechts zu `Next Step` und wähle im erscheinenden Menü `Start` aus.
   - Für Android: Wähle `Legacy`-Partitionierung für Android 10/11 und `Dynamic`-Partitionierung für Android 13+. Beachte, dass Legacy- und Dynamic-Partitionierung **nicht** miteinander kompatibel sind.

![sd_partition_erista_oled](https://github.com/glitched-nx/blue_pack_NX/raw/blue_pack/blue_pack_NX_wiki/pics/sd_partition_erista_oled.png)

-----

### Kopieren des auf dem PC gesicherten emuMMC Backups und der CFW Daten der alten microSD, auf die neue SD-Karte

- Nachdem dies abgeschlossen ist, starte Hekate und navigiere zu `Tools` > `USB Tools` > `SD Card`. Verbinde dann die Switch über USB mit deinem PC.

- Kopiere das Backup von `sdmc:/backup`, das du zuvor von der alten SD-Karte mit Hekate erstellt und auf deinem PC gespeichert hast, auf die neue SD-Karte.

BILDER SErie

-----

11. Entferne das `UMS`-Gerät sicher über das Betriebssystem deines Computers.

12. Gehe zu `Tools` und wähle `Restore eMMC`. Stelle sicher, dass die Option `SD emuMMC Raw Partition` unten auf dem Bildschirm auf `ON` gesetzt ist.

![emuMMC_Raw_restore](https://github.com/glitched-nx/blue_pack_NX/raw/blue_pack/blue_pack_NX_wiki/pics/emuMMC_Raw_restore.png)

13. Beginne mit der Wiederherstellung des Backups, indem du sowohl `SD emuMMC BOOT0 & BOOT1` als auch `SD emuMMC RAW GPP` auswählst. Beachte, dass die Wiederherstellung von `SD emuMMC RAW GPP` etwas länger dauern kann.
    - Es ist entscheidend, dass die Option `SD emuMMC Raw Partition` bei beiden aktiviert ist, um zu vermeiden, dass du versehentlich den sysMMC veränderst.

14. Dein emuMMC ist nun erfolgreich auf der neuen SD-Karte wiederhergestellt. Du kannst es über `Launch` -> `Atmosphere FSS0 emuMMC` in Hekate starten.
