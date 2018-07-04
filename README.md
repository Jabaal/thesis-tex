# thesis-tex
## Diplomarbeit Fakultät Elektrotechnik Hochschule für Technik und Wirtschaft (HTW) Dresden

### Corporate Design der HTW Dresden
[Hier](https://www.htw-dresden.de/intern/marketing/corporate-design.html) kann man Dateien zum Corporate Design der HTW Dresden finden. Dazu gehört unter anderem das Logo und ein Styleguide.
Dazu einfach mit
```
s-Nummer
Passwort
```
einloggen und lesen.

Alternativ gibt es [hier in GitHub](https://github.com/stura-htw-dresden/htw-logo) ein paar frei verfügbare Informationen vom Stura der HTW Dresden. Unter anderem auch das Logo der HTW Dresden.
Leider ist der dort verlinkte LaTex-Kurs nicht mehr verfügbar, da der Professor, der diesen Kurs an der TU Dresden zur Verfügung gestellt hat, leider verstorben ist.

### Installation und Ersteinrichtung für LaTex
[Hier](https://www.latex-project.org/get/#tex-distributions) gibt es LaTex zum Download.
Beschrieben wird die Installation und Einrichtung quick and dirty für einen Windows-Rechner:
  - [Miktex herunterladen](https://miktex.org/download) *meine Version: 2.9.6643 x64*
    - Miktex installieren für alle Nutzer und alle Pakete on-the-fly installieren.
    - auch in das übliche Verzeichnis installieren
    - Miktex Console als Administrator starten und Pakete updaten, danach *update DB* unter *Pakete* klicken und nochmal updaten
  - [Texmaker herunterladen](http://www.xm1math.net/texmaker/download.html) *meine Version: 5.0.2 x64*
    - Texmaker installieren
    - ebenso in das voreingestellte Verzeichnis installieren
    - schnell noch Konfigurieren:
      - erst auf Englisch umstellen (die deutsche Übersetzung ist einfach grauenvoll) unter *Optionen -> Sprache der Benutzeroberfläche -> en*
      - unter *Options -> Configure Texmaker* im Reiter *Quick Build* unbedingt *XeLaTex + View PDF* auswählen, damit auch die üblichen Schriftarten (wie z.B. *Arial*) verwendet werden können
      - Damit Glossare wie z.B. das Abkürzungsverzeichnis erstellt werden können, muss man noch unter *User > User commands > Edit User Commands* einen Eintrag hinzufügen und die Felder wie folgt ausfüllen:
        - Menu Item: `makeglossaries`
        - Command: `makeglossaries %`
      - Für Biblatex lauten die Felder wie folgt:
        - Menu Item: `biblatex`
        - Command:`biber %`
      - Folgende Befehle solltet ihr nun für das Zitieren unter *User -> User Tags -> Edit User Tags* hinzufügen. Diese Befehle ruft ihr anschließend mit `SHIFT+F1...F4` auf. Die Zeichen werden über eine Tastenkombination über ALT+NUMPAD-Zahlenreihe eingegeben oder aus diesem Text kopiert und eingefügt. Die folgenden Zeilen enthalten jeweils drei Teile in der entsprechenden Reihenfolge - *Menu Item* *Latex Content* *Tastenkombination*. Aus diesen solltet ihr insgesamt 4 *User Tags* erstellen:
        - `open guillemets` `»` `ALT+175`
        - `close guillemets` `«` `ALT+174`
        - `open single guillemets` `›` `ALT+0155`
        - `close single guillemets` `‹` `ALT+0139`        
  -[Active-Pearl herunterladen](https://www.activestate.com/activeperl/downloads) *meine Version:5.24.3.2404 x64* (sonst funktionieren die Glossare nicht)
    - Pearl installieren
    - Verzeichnis nicht ändern, *File extension* und *PATH* zum Pearl-Interpreter angekreuzt lassen
    - eventuelle Schwierigkeiten mittels [dieser Anleitung](https://tex.stackexchange.com/questions/158796/miktex-and-perl-scripts-and-one-python-script) korrigieren
Wer direkt anfangen möchte, kann das nächste Kapitel überspringen.

### Informationen zur Formatierung
- Viel geholfen haben mir auf jeden Fall [diese Einführung(**!**)](https://www.sharelatex.com/learn) und [diese Homepage](http://namsu.de/latex.html). Zusätzlich gibt es [hier](https://tobiw.de/tex-faq) noch eine tolle FAQ für verschiedene Dinge
- Im [Leitfaden für wissenschaftliche Dokumente](docs/Leitfaden_fuer_wiss_Dokumente.pdf) - welcher von der Fakultät Maschinenwesen ist, aber für die Fakultät Elektrotechnik genauso gut gilt - sind alle wichtigen Formatierungen für Abschlussarbeiten der HTW Dresden zusammengefasst. Diese wurden in das Template übernommen.
[Fakultät Maschinenwesen HTW Dresden - Informationen für Studierende](https://www.htw-dresden.de/fakultaet-maschinenbau/studium/infos-fuer-studierende.html)
- Im [Sündenregister](docs/l2tabu.pdf) sind verschiedene Sünden für LaTex aufgelistet. [LaTex Sündenregister Homepage](http://www.dante.de/CTAN/info/german/l2tabu/)
- Die Formatierung funktioniert größtenteils per [KOMA-Script](/docs/scrguide.pdf). [Link zum typearea-paket](https://ctan.org/pkg/typearea)
- Eine Übersicht zu den Glossar-Stilen gibt es [hier](https://www.dickimaw-books.com/gallery/)
- Eine tolle Linksammlung zu allen möglichen Themen gibt es [hier](https://tu-dresden.de/mn/math/stochastik/das-institut/beschaeftigte/jan-rudl/latex_win). Gerade zum hyperref-Paket findet man dort alles Wichtige.
- Eine Kurzanleitung zum hyperref-Paket gibt es [hier](http://www.pa.op.dlr.de/~PatrickJoeckel/pdflatex/index.html)
- Für eine Übersicht der Symbole habe ich [hier](/docs/symbols-a4.pdf) eine PDF hinterlegt. [CTAN Latex-Symbole](http://www.ctan.org/tex-archive/info/symbols/comprehensive/symbols-a4.pdf)

### Diplomarbeit beginnen
Informationen zu Abschlussarbeiten der Fakultät Elektrotechnik gibt es auf der [Seite der Fakultät Elektrotechnik der HTW Dresden](https://www.htw-dresden.de/fakultaet-elektrotechnik/fakultaet/studierende/abschlussarbeiten.html) und auch im [OPAL](https://bildungsportal.sachsen.de/opal/auth/RepositoryEntry/16966647814/CourseNode/97409953057309?5).
Nun noch das [Template](/template-htw-abschlussarbeit.tex) herunterladen und falls nötig die [Quick'n'Dirty Anleitung](/readme/quickndirty-anleitung.pdf) herunterladen, lesen und verinnerlichen.
Anschließend steht mit dem [Cheat-Sheet](/readme/cheatsheet-quickanddirty.pdf) eine Übersicht der wichtigsten Befehle zur Verfügung.

Autor und Titel werden automatisch in die PDF-Dokument-Informationen übernommen. Wer es ganz genau machen will, kann auch noch Stichworte und Subjekt hinzufügen - das geht in der Datei [pakete.tex](/style/pakete.tex). Einfach auskommentieren und Stichworte/Subjekt hinzufügen.



Eventuelle to-do's:
Kommando zum Kompilieren für alles erstellen. Mit xelatex, Glossaries, Biblatex, 2x Xelatex und view pdf.
Anschließend Readme aktualisieren, Links für die Dokumentation einfügen.

tabularx statt tabu verwenden? wenn ja, warum, wenn nein, warum nicht?
longtable unbedingt noch einfügen

eventuell das requirepackage einfügen von overleaf/uni stuttgart tex-file - um fehler zu verhindern. - link zum TUD/Uni-Stuttgart template einfügen

cheatsheet vollständig befüllen

eventuell seitenränder mit geometry anpassen


Befehle einfügen
u.a.
\tabularnewline
\midrule
\textwidth
command:
insert gfx
table außenumgebung
longtable
evtl. quotationmarks nur in öffnen und schließen hinzufügen
kleine quotationmarks löschen aus den user-commands