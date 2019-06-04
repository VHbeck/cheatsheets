# Shell Commands

## Befehle, mit denen man sich in Ordnern bewegen kann
* ls : listet Dateien (files)/Ordner (directories) auf 
* pwd : print working directory - zeigt an, wo ich mich grade befinde (mein "working directory")
* cd *file* : change directory - in anderen Ordner springen
* cd .. : einen Ordner zurück gehen
* cd ../*directory* : einen Ordner zurück gehen und dann in einen bestimmten Unterordner gehen
* mkdir *directory* : erstellt einen neuen Ordnernamen
* touch *file.xy* : neue DAtei wird erstellt im aktuellen Ordner
* ls -a : zeigt versteckte Dateien an, die mit *.* beginnen
* ls -l : Inhalte der directory im Langformat
* ls -t : zeigt Inhalte und Ordner nach Bearbeitungszeitpunkt an
* ls -alt : zeigt alle drei oben genannten Optionen gleichzeitig an

## Kopieren / Löschen / Verschieben
* cp *file.xy* *directory* : kopiert DAteien oder Ordner. Argument 1 = sourcefile , Argument 2 = destination directory
* cp * *directory* : Wählt alle Dateien im working directory aus und kopiert sie. * = wildcard
*cp m*.txt *directory* : kopiert alle Dateien mit dem Anfangsbuchstaben "m" und dem Ende ".txt" in den angegebenen Ordner
* mv *file.xy* *directory* : Datei in Ordner verschieben - funktioniert auch mit mehreren Dateien gleichzeitig
* mv *file.xy* *file2.xy* : Datei umbenennen, Argument 1 = alter Name , Argument 2 = neuer Name
* rm *file.xy* : löscht Datei
* rm -r *directory* : löscht Ordner und alle Unterordner

## Zusatzbefehle
* echo "abc" : gibt Text aus
* echo "abc" >> *file.xy* : schreibt Text/Zeichenfole in Datei
* cat = gibt Inhalt einer Datei aus
* open = öffnet eine Datei in VS Code
* .code = zeigt Datei in VS Code an