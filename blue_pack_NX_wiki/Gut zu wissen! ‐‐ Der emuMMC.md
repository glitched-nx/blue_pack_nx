## **emuMMC (emulierter NAND)**

Ein emuMMC ermöglicht eine saubere Trennung zwischen der offiziellen Firmware (OFW) und der Custom Firmware (CFW). Dieses Verfahren ist essenziell, um die beiden Systeme voneinander zu isolieren und somit die Sicherheit und Flexibilität der Konsole zu gewährleisten.

### Was ist emuMMC?  
Der emuMMC ist eine exakte Kopie des internen Speichers der Konsole (sysMMC), auch NAND genannt, die auf eine Partition der SD-Karte geschrieben wird. Sobald der emuMMC aktiviert ist, läuft die Konsole vollständig von dieser kopierten Umgebung auf der SD-Karte, anstatt den internen Speicher zu nutzen. Dadurch wird sichergestellt, dass alle Änderungen, Installationen oder Eingriffe im Rahmen der CFW ausschließlich im emuMMC stattfinden und der sysMMC unverändert bleibt.

### Warum ist die Einrichtung von emuMMC wichtig?  
Die Einrichtung eines emuMMC bietet mehrere entscheidende Vorteile:  

1. **Saubere Trennung zwischen OFW und CFW**  
   - Die OFW (Stock) bleibt unangetastet und kann sicher für Online-Aktivitäten genutzt werden.  
   - Alle Modifikationen, Homebrew-Apps oder Installationen von Spielen finden ausschließlich im emuMMC statt, was das Risiko minimiert, dass unautorisierte Inhalte im sysMMC landen.  

2. **Minimierung des Bannsrisikos**  
   - Nintendo überwacht Konsolen, die mit modifizierter Software online gehen. Mit einem korrekt eingerichteten emuMMC bleibt die OFW unmodifiziert und kann sicher für Online-Zwecke verwendet werden, während der emuMMC für Offline-Homebrew und modifizierte Inhalte genutzt wird.  

3. **Flexibilität und Sicherheit**  
   - Da der emuMMC auf der SD-Karte liegt, können Backups davon erstellt werden, um einen früheren Zustand wiederherzustellen.  
   - Änderungen und Tests innerhalb der CFW betreffen nur den emuMMC und haben keine Auswirkungen auf die OFW.  

4. **Erweiterte Nutzungsmöglichkeiten**  
   - Der emuMMC ermöglicht es, alternative Setups zu betreiben, ohne die Originaldaten zu gefährden. Beispielsweise können experimentelle Firmware-Versionen oder neue Homebrew-Apps getestet werden.  

### Wie funktioniert der emuMMC im Detail?  
- Beim Einrichten eines emuMMC wird eine Kopie des sysMMC auf die SD-Karte geschrieben, in der Regel auf eine speziell dafür angelegte Partition.  
- Beim Booten über Hekate oder ähnliche Payloads kann gezielt zwischen sysMMC (OFW) und emuMMC (CFW) gewechselt werden.  
- Während der Nutzung des emuMMC werden sämtliche Schreib- und Leseoperationen auf die SD-Karte umgeleitet. Dadurch bleibt der sysMMC unverändert.  

### Fazit  
Die Nutzung eines emuMMC ist ein unverzichtbarer Bestandteil für alle, die sowohl die Vorteile einer CFW genießen möchten, als auch ihre Konsole sicher online mit der OFW betreiben wollen. Mit dieser sauberen Trennung wird eine optimale Balance zwischen Funktionalität, Sicherheit und Flexibilität erreicht. Wer Homebrew nutzen oder seine Konsole modifizieren möchte, sollte stets auf die korrekte Einrichtung eines emuMMC achten.