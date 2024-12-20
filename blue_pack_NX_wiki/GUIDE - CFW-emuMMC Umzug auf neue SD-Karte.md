CFW Setup mit emuMMC (Raw Partition / SD File-based) auf neue SD-Karte übertragen.
GUIDE - CFW-emuMMC Umzug auf neue SD-Karte


***Benutzeranfrage:***

***Jo Leute,*** 
***ich hab mir ne neue, fettere SD-Karte für meine Switch geordert, weil ich mehr Speicher für Games brauch. Auf der alten SD ist schon ein komplettes CFW-Setup mit diesem emuMMC Dings . Wie kann ich jetzt am besten die Daten von der alten auf die neue SD-Card transferieren, mit allem Drum und Dran - also installierte Games, Savegames, Profile, System Settings, einfach alles?***

****Wär nice, wenn mir einer von den weiterhelfen könnte, wie man das am smoothesten handlen kann. Step-by-Step Guide wären optimal.***

***Danke im Voraus!***


<div align="center">

### GUIDE

</div>

Zuerst solltest du überprüfen, ob du eine `SD Raw Partition` oder ein `SD File`-basiertes emuMMC eingerichtet hast.

1. Boote deine Switch neu, um in den Hekate Bootloader zu kommen.
   - Bei ausgeschalteter Konsole entweder per RCM Payload Methode oder ganz normal hochfahren, wenn ein ModChip verbaut ist.

2. Navigiere zu `emuMMC Info & Selection` und schau dir den Text neben `Type` an.
   - Wenn ein emuMMC vorhanden ist, sollte dort entweder `SD Raw Partition` oder `SD File` stehen.


Unser [blue pack NX - AIO CFW PACK](https://github.com/glitched-nx/blue_pack_NX/releases/latest) ist, wie die meisten anderen CFW Packs auch, auf die Einrichtung einer emuMMC Partition ausgelegt. Daher sollte dein CFW-Setup mit einer emuMMC-Partition eingerichtet sein.

-----


### Umzug auf eine neue SWITCH SD, einem emuMMC `Raw Partition` Setup.

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

### Die neue SD-Karte wie bei der **`Ersteinrichtung`** vorbereiten

- Formatiere die neue microSD in FAT32/exfat. Nagelneue microSD's sind bereits in exfat formatiert und brauchen nicht formatiert werden, da während der Partionierung später die Hauptpartition der SD Karte in FAT32 formatiert wird.

   - `By the Way` kannst du direkt die CFW aktualisieren und `blue pack von [diesem Link](https://github.com/glitched-nx/blue_pack_NX/releases/latest) downloaden.
   - Entpacke den vollstände Zip-Datei `blue_pack_NX.zip` in das Hauptverzeichnis der neuen SD-Karte.
   - **Beachte:** Kopiere jetzt noch **KEINE** Daten der alten SD-Karte auf die neue, außer den CFW-Daten aus der ZIP-Datei. Du kannst [blue_pack_nx.zip](https://github.com/glitched-nx/blue_pack_NX/releases/latest/download/blue_pack_nx.zip) oder ein anderes CFW-Paket verwenden, das du bevorzugst.

#### Folge den Anweisungen im nächsten Abschnitt, um eine   emuMMC Partition neue microSD zu erstellen..
-----
## Partitionieren der SD-Karte für ein emuMMC (Raw Partition - Setup)

Starte deine Switch neu um den Hekate Bootloader zu laden.

- Ist die Switch ausgeschaltet, mittels RCM Payload Methode bzw. ganz normal anschalten bei eingebautem ModChip.

**`Achtung:`** Die Partitionierung *löscht* alle Daten auf der SD-Karte, *wenn* der Inhalt 2 GB überschreitet! Bleibt er darunter, werden alle Daten zwischengespeichert und nach der Partitionierung wiederhergestellt. Die Ordner `emuMMC` und `Nintendo` werden daher erst nach der Partitionierung auf die neue SD-Karte kopiert.

## Partitions Manager mit Hekate

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


### Umzug auf eine neue Switch SD-Karte mit einem `SD-File` basierten emuMMC Setup

   1. Führe einen Reboot in den `Hekate Bootloader` durch:
      - Bei `unpatched-V1` Modellen schalte die Switch aus und starte Hekate per `RCM-Payload` Methode.
      - Bei Modellen mit `eingebautem ModChip` schalte die Switch ganz normal ein.
   2. Sobald Hekate gestartet ist, verbinde deine Switch per USB-Kabel mit dem PC.
   3. Aktiviere die `Hekate UMS`-Funktion, um auf die SD-Karte deiner Switch als `USB-Massenspeicher` zuzugreifen:
      - Navigiere im Hekate-Menü zu `Tools`, wähle `USB Tools` und dann `SD Card`.
   4. Auf deinem PC sollte nun ein Laufwerk namens `SWITCH SD` erscheinen.
   5. Öffne dieses Laufwerk und positioniere das Fenster so, dass du den gesamten Inhalt gut im Blick hast.
   6. Kopiere den kompletten Inhalt der SD-Karte entweder zuerst auf deinen PC oder direkt (on-the-fly) auf die neue SD-Karte.
   7. Greife mit einem SD-Kartenleser oder ähnlichem Gerät auf die neue SD-Karte zu.
   8. Formatiere die neue SD-Karte mit FAT32 (Clustergröße 64KB) mithilfe eines `Partition Managers` oder eines Tools wie [SD Formatter](https://www.sdcard.org/downloads/formatter_4/).
   9. Kopiere alle Dateien vom PC oder direkt von der alten SD-Karte auf die neu formatierte SD-Karte.
   10. Entferne das `UMS`-Gerät sicher über dein Computer-Betriebssystem.
   11. Lege die neue SD-Karte in deine Switch ein und starte erneut in den Hekate Bootloader.
   
-----
