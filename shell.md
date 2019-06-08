# Shell Commands

## Befehle, mit denen man sich in Ordnern bewegen kann

- `ls` : listet Dateien (files)/Ordner (directories) auf
- `pwd` : print working directory - zeigt an, wo ich mich grade befinde (mein "working directory")
- `cd [file]` : change directory - in anderen Ordner springen
- `cd ..` : einen Ordner zurück gehen
- `cd ../[directory]` : einen Ordner zurück gehen und dann in einen bestimmten Unterordner gehen
- `mkdir [directory]` : erstellt einen neuen Ordnernamen
- `mkdir [Ordner/Unterordner]` Unterordner erstellen
- `mkdir -p [Ordner/Unterordner/Unterunterordner/...]` Ordnerpfad wird erzeugt
- `touch [file.xy]` : neue DAtei wird erstellt im aktuellen Ordner
- `ls -a` : zeigt versteckte Dateien an, die mit _._ beginnen
- `ls -l` : Inhalte der directory im Langformat
- `ls -t` : zeigt Inhalte und Ordner nach Bearbeitungszeitpunkt an
- `ls -alt` : zeigt alle drei oben genannten Optionen gleichzeitig an
- `z neu` = `cd ~/neuefische` z lernt oft benutzte Ordner und bietet so Abkürzung
- `tree` Verzeichnisbaum anzeigen

## Kopieren / Löschen / Verschieben

- `cp [file.xy] [directory]` : kopiert DAteien oder Ordner. Argument 1 = sourcefile , Argument 2 = destination directory
- `cp * [directory]` : Wählt alle Dateien im working directory aus und kopiert sie. \* = wildcard
- `cp m*.txt [directory]` : kopiert alle Dateien mit dem Anfangsbuchstaben "m" und dem Ende ".txt" in den angegebenen Ordner
- `cp -R [src-directory] [target-directory]` kopiert alles aus dem Quellverzeichnis in das Zielverzeichnis
- `mv [file.xy] [directory]` : Datei in Ordner verschieben - funktioniert auch mit mehreren Dateien gleichzeitig
- `mv [file.xy] [file2.xy]` : Datei umbenennen, Argument 1 = alter Name , Argument 2 = neuer Name
- `mv [Ordner] *` verschieben des Ordners in den aktuellen Ordner
- `rm [file.xy]` : löscht Datei
- `rm -r [directory]` : löscht Ordner und alle Unterordner
- `rm -rf` Ordner löschen; `r` = rekursiv (alles in allen Unterordnern); `f` = force (nicht jede Datei einzeln bestätigen); auch **Rimraf** genannt
- `rm -rf *` löschen aller Ordner und Dateien im aktuellen Ordner

## Zusatzbefehle

- `echo "abc"` : gibt Text aus
- `echo "abc" >> [file.xy]` : schreibt Text/Zeichenfole in Datei
- `pbcopy` speichert Eingabe in die Zwischenablage (Bsp.: `cat ~/.ssh/id_rsa.pub | pbcopy`)
- `cat` = gibt Inhalt einer Datei aus
- `open` = öffnet eine Datei im Standardprogramm eines Betriebssystems
- `open .` : öffnet ORdner im Finer/Explorer
- `.code` = zeigt Datei in VS Code an
- `ctrl + c` : wenn terminal hängt
- `man [Befehl]` : zeigt wie man Befehle für die Shell anwendet
- `clear` or `⌃L` : Clear screen
- `exit` or `⌃D` : Exit terminal

## Shortcuts

- `⌃C` Get out of trouble
- `⌃A` Move to beginning of line
- `⌃E` Move to end of line
- `⌃U` Delete to beginning of line

## Push und Pull

- Pull: mit dem Terminal in Ordner gehen, dann `git pull`
- `git status`: zeigt an, ob Ordner aktuell ist
- Hilfe hier: [Git und VS Code](https://herwig.de/anleitungen/entwicklung/gitlab/workflow-vscode-git-gitlab.html#branch-von-mehreren-standorten-bearbeiten)
- Branch auf Github erstellen: Über iTerm in Projekt gehen, dann `git checkout -b my-new-feature` eingeben, dann push auf Github mit `git push origin [name_of_your_new_branch]``
- Branches anzeigen lassen: `git branch -a`
- mehr Infos zu Branches : [Git branches help](https://github.com/Kunena/Kunena-Forum/wiki/Create-a-new-branch-with-git-and-manage-branches) oder [Git branch change](https://backlog.com/git-tutorial/branching/switch-branch/)
