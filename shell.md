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
- `ctrl + c` : wenn terminal hängt oder `esc + z z` oder shift + z + z
- `man [Befehl]` : zeigt wie man Befehle für die Shell anwendet
- `clear` or `⌃L` : Clear screen
- `exit` or `⌃D` : Exit terminal

## Shortcuts

- `⌃C` Get out of trouble
- `⌃A` Move to beginning of line
- `⌃E` Move to end of line
- `⌃U` Delete to beginning of line

## GIT

- Pull: mit dem Terminal in Ordner gehen, dann `git pull`
- `git status`: zeigt an, ob Ordner aktuell ist (kurz: gst)
- Hilfe hier: [Git und VS Code](https://herwig.de/anleitungen/entwicklung/gitlab/workflow-vscode-git-gitlab.html#branch-von-mehreren-standorten-bearbeiten)
- Branch auf Github erstellen: Über iTerm in Projekt gehen, dann `git checkout -b my-new-feature` eingeben, dann push auf Github mit `git push origin [name_of_your_new_branch]``
- Branches anzeigen lassen: `git branch -a`
- mehr Infos zu Branches : [Git branches help](https://github.com/Kunena/Kunena-Forum/wiki/Create-a-new-branch-with-git-and-manage-branches) oder [Git branch change](https://backlog.com/git-tutorial/branching/switch-branch/)

### Neues Projekt anlegen per Terminal local --> remote

- neue Directory anlegen mit `mkdir`
- git Projekt initieren: in Ordner gehen, dann `git init`im Terminal
- neuer Ordner mit `touch`

* `git status`zeigt, wo Dateien stehen (Workflow, ob gestaged oder nicht usw)
* **Staging** `git add datei` oder für alles: `git add .` (gaa)
* **committing** `git commit -m "message"` Beim ersten Commit ist die Message "Initial Commit" (kurz: gcmsg "blabla")
* `git log` zeigt Verlauf an, `q`um da rauszukommen
* neues Repository in Github oder Gitlab erstellen
* dann Link kopieren `git remote add origin Projektname`
* `git remote -v` überprüfen, ob Verbindung zu Git erfolgreich war
* **pushen** immer einmal upstream festlegen: `git push --set-upstream origin ...` (Befehl bekommt man durch `git push`als Fehlermeldung) , dann `git push`
* **Branch** anlegen: `git branch name`
* in branch wechseln `git checkout name` (kurz: gco)
* **Merge** `git merge branch-name` (vorher muss man im Master bzw Branch sein, in den man hinein mergen möchte)
* **Ohne Merge Konflikt** dann Version in VS auswählen, die richtig ist, danach stagen, committen
* Bei **Merge Konflikt** erst Master in Branch mergen, um sauberen Stand zu haben, dann Konflikte beheben --> Konflikte werden also nur im Branch und lokal behoben
* und dann wieder in Master mergen, dann push auf Remote, Merge Request stellen und daraufhin mergen
* **Merge Konflikt bei Merge Request** (z.B. bei verschiedenen Master-Versionen)
* Master auswählen `git checkout master`, Master auf lokal pullen `git pull`, Problem-branch in Terminal auswählen `git checkout branch`, master in branch mergen `git merge master`, Konflikte in VS Code beheben, stagen, committen, pushen, Merge Request in Gitlab/Github beenden
* Wenn Merge Request abgeschlossen, den Stand wieder auf Lokal holen (`git pull`) und Branches lokal aufräumen, siehe Branch löschen
* **Branch löschen** `git branch -d name`

### User Name und E-Mail in Git konfigurieren

- `config --global user.name "Vanessa Harbeck"`
- `config --global user.email vanessa.harbeck@web.de`
- im Nachhinein ändern: `commit --amend --reset-author`
-

Für Aufgabe:
@import für css
bug Speichern: in Index Datei aktualisieren, da sonst nicht Aktualisierung angezeigt wird
jede Hauptseite sollte aus drei MOdulen bestehen. Seiten: Index, create, profile, settings
npm muss eventuell mit `npm start` neu gestartet werden, dann in anderem TErminal-Tab arbeiten

color scheme als variable speichern und dann vierfach benutzen!! mit SASS

- cmd + d für neues Tab im TErminal
