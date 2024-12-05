# Einstellungen

In den Einstellungen stehen dir umfangreiche Möglichkeiten zur Verfügung, das Verhalten des Chronicle Keepers an deine
eigenen Bedürfnisse anzupassen. Einige Einstellungen können das Verhalten des Chronicle Keepers in Gesprächen auch
gefühlt negativ beeinflussen. Es ist daher zu empfehlen, ab und an [Sicherungen](backup) anzulegen, damit du
jederzeit deine Einstellungen wiederherstellen kannst.

## Gespräche

In diesem Bereich findest du Einstellungen, die deine Gespräche mit dem Chronicle Keeper direkt beeinflussen.

### Allgemein

**Name des Chatbots** und **Name des Benutzers**

In Gesprächen wird angezeigt, welche Nachrichten von dir eingegeben wurden und welche Nachrichten als Antwort gekommen
sind. Dabei wird ein Name ausgegeben. Diesen Namen kannst du hier für jeden "Beteiligten" anpassen. Deine Nachrichten
bekommen eine Änderung hat keinen funktionalen Einfluss auf eure Gespräche, sondern dient mehr dem Gefühl.

Du wirst jedoch feststellen können, dass der "Name des Chatbots" sich auch auf das Menü auswirkt, denn der Name wird
dort als Titel für den Gesprächsbereich verwendet.

**Maximale Kontextdokumente** und **Maximale Kontextbilder**

Im Hintergrund der Gespräche wird ChatGPT immer wieder nach Wissen aus deiner Bibliothek fragen, um dir gute Antworten
auf deine Fragen zu geben. Das läuft vollständig automatisch ab. Da es auf Seiten von ChatGPT aber Beschränkungen für
die Länge von Inhalten gibt, kannst du hier einstellen, wie viele Dokumente bzw. wie viele Bilder maximal als Antwort
auf eine Anfrage von ChatGPT an deine Bibliothek gegeben werden sollen. Die Einstellung hängt sehr davon ab, wie groß
deine Dokumente und Bildbeschreibungen in der Regel sind. Hast du Inhalte, die eher in Länge von Büchern sind, wird
eine Suche mit Stichworten auf diese wohl wenig ausspielen, aber dafür sehr lange Texte. Hast du deine Inhalte stark
aufgeteilt und spezialisiert, wird die Suche wohl sehr spezifische Daten für ChatGPT finden, die auch nicht zu lang
sind, und so kannst du diese Zahlen erhöhen.

Es ist wichtig, hier eine Balance zu finden, die auf deine Bibliothek passt. So ist dies eine sehr individuelle
Einstellung. Mehr Dokumente und Bilder können auch zu schlechteren Ergebnissen führen oder aber zu besseren. Das
wirst du selbst ein wenig herausfinden müssen.

**Zusätzliche Angaben im Chat**

Wenn du Interesse daran hast, welche Dokumente und Bilder aus deiner Bibliothek für Antworten herangezogen wurden,
kannst du hier einschalten, dass dir diese Informationen angezeigt werden. Eine lokale Aufzeichnung dieser Informationen
findet immer statt, sodass du die Einstellungen auch ausgeschaltet lassen kannst und bei Bedarf aktivieren. So ist es
dann auch möglich, dir für alle bisherigen Gespräche diese zusätzlichen Angaben anzeigen zu lassen.

Du findest die Ausgabe jeweils direkt unter den Antworten deines Chronicle Keepers, wenn die Einstellungen aktiviert sind.

### Tuning

?> Neu ab **v0.4-alpha**: Diese Einstellungen sind nur Standardeinstellungen. Sie können für jedes Gespräch individuell
eingestellt werden. So kannst du in verschiedenen Gesprächen auch verschiedene Einstellungen ausprobieren und dich an die
für dich besten Werte herantasten.

Diese Einstellungen sind sehr technischer Natur und dennoch ist es wichtig, sie zu verstehen, da sie dir ermöglichen,
deine Ergebnisse mit dem Chronicle Keeper deutlich zu verbessern, wenn du unzufrieden bist.

**Temperatur**

Die Temperatur ist eine Einstellung, die die Kreativität von ChatGPT definiert. Sie entscheidet darüber, ob der
Chronicle Keeper mehr oder weniger versucht, deine Anfragen mit kreativen Antworten zu beantworten. Der Wert muss
irgendwo zwischen 0,1 und 2,0 liegen. Im Standard liegt dieser bei 0,7. Egal wie der Wert ist, wird deine Bibliothek
ausgewertet. Der Wert bestimmt aber, inwiefern die Daten mit kreativen Aussagen belebt werden. Sowohl ein hoher als
auch ein niedriger Wert können sich als nützlich erweisen. Im technischen Sinne definiert die Temperatur die
Wahrscheinlichkeit, in der die Rückgabe von Antworten die realen Worte auseinander liegen dürfen.

Das heißt, bei einem niedrigen Wert ist ein Wort wie "Natürlich" immer ein "Natürlich". Bei einem höheren Wert könnte
daraus auch ein "Sicher" werden. Bei einem sehr hohen Wert könnte aber auch absoluter Schwachsinn wie "Wieso?" entstehen.
Die Wahrscheinlichkeit für sinnlose Antworten steigt mit einem höheren Wert. Muss es aber nicht. Spätestens aber bei
einem Wert von 2,0 wirst du wahrscheinlich keine sinnvoll formulierten Antworten mehr bekommen.

Wenn du also eine Geschichte ausarbeiten, einen Charakter weiter ausgestalten oder gezielt Ideen haben möchtest, ist
es naheliegend, einen Wert um die 1,0 herum zu verwenden. Willst du jedoch nur an vorhandenen Fakten orientierte
Antworten haben, wie vorhandene Charakterbögen oder was in den letzten Tagen in deiner Welt passiert ist, liegt ein
Wert von um die 0,2 vielleicht eher in dem Bereich, den du haben möchtest.

**Maximale Distanz bei Dokumentensuche** und **Maximale Distanz bei Bildersuche**

Deine Anfragen an deinen Chronicle Keeper werden von ChatGPT analysiert und bei Bedarf Funktionen im Hintergrund
aufgerufen, die Kontext aus deiner Bibliothek bereitstellen. Dabei liefert ChatGPT den Funktionen einen oder mehrere
Suchbegriffe, für die mehr Wissen aus deiner Bibliothek gebraucht wird. Diese Suchbegriffe werden mit einer
Vergleichssuche auf deine hinterlegten Dokumente und Bilder ausgeführt. Die Vergleichssuche ist dabei nicht dumm und
erkennt auch Synonyme und Bedeutungen, da die Daten in einem mathematischen Format, sogenannten Vektoren, vorliegen.
Diese Werte wurden mit der Funktion [Chat Refresh aus deiner Bibliothek](library) errechnet und stellen deine Texte in
mathematischer Bedeutung dar.

Unter der Verwendung eines [Cosine Distance](https://de.wikipedia.org/wiki/Kosinus-%C3%84hnlichkeit) Algorithmus wird
die Wahrscheinlichkeit errechnet, in der die gegebenen Suchbegriffe in einem Dokument oder einem Bild vorhanden sind.
Diese Wahrscheinlichkeit nennt man "Distanz". Entsprechend kannst du hier granular einstellen, wie nah deine Texte oder
Bilder an den gesuchten Phrasen sein müssen.

Ein hoher Wert von 1,0 würde bedeuten, dass so ziemlich alle deine Dokumente und Bilder gute Funde für jeden Suchbegriff
sind. Es würde also, egal was gesucht wird, fast deine gesamte Bibliothek als gültig gelten. Ein niedriger Wert von 0,1
würde schon sehr exakte Treffer bedürfen. Weder der hohe noch der niedrige Wert sind in der Regel geeignet für eine
reale Verwendung.

Um die für dich perfekten Werte zu finden und deine Ergebnisse zu verbessern, kannst du in den Funktionseinstellungen
eine Checkbox finden, um erweiterte Ausgaben im Gespräch zu ermöglichen. Dir werden dann für jede Antwort des Chronicle
Keepers erweiterte Informationen zu den Funktionsanfragen angezeigt. Dabei wirst du auch herausfinden können, welche
Begriffe ChatGPT als passend für eine Anfrage erachtete und auf welchen Distanzen basierend die Dokumente oder Bilder
aus deiner Bibliothek als Kontextwissen zu dieser Anfrage gegeben wurden.

Es kann etwas dauern, den perfekten Wert zu finden, wenn man unzufrieden ist mit den Ergebnissen.

### System Prompt

Ein System Prompt ist eine spezielle Anweisung, die an ChatGPT gegeben wird, bevor das eigentliche Gespräch beginnt.
Diese Anweisung legt fest, wie ChatGPT auf Anfragen reagieren soll. Es beeinflusst den Ton, die Art der Antworten und
welche Informationen bevorzugt verwendet werden. Durch das Anpassen des System Prompts kann man sicherstellen, dass
Gespräche in der gewünschten Art geführt werden.

So wirst du bei den Standardeinstellungen feststellen können, dass der Chronicle Keeper in seinen Gesprächen als
Spielleiter deiner Spielrunde agieren soll. Es wird auch festgelegt, in welcher Spielwelt ihr unterwegs seid und
welchem Regelwerk ihr folgen wollt.

Du kannst auch vieles näher beschreiben. So auch nochmal zusätzliche Anweisungen geben, welche Funktionen genutzt
werden sollen. Wenn du einen speziellen Charakter spielst und dein Chronicle Keeper nur für diesen einen Charakter
vorhanden ist, kannst du auch direkt hier definieren, dass dein Spielleiter dich als diesen Charakter kennt. Das
würde Anfragen wie "Was weißt du über mich?" ermöglichen, da du bereits definiert hast, wer du bist. Erweiterte
Informationen zu dir würden dann aus der Datenbank geladen werden, ohne nach dem Wort "mir" zu suchen, sondern
dem Namen deines Charakters.

?> **Tipp!** Solltest du mit geändertem oder erweitertem System Prompt deutlich bessere Ergebnisse erzielen als mit
dem Standard, könntest du diesen auch mit anderen teilen, um den Chronicle Keeper eventuell für alle Nutzer zu verbessern.

### Funktionen

In diesem Bereich kannst du sehen, welche Funktionen für ChatGPT, den fleißigen Bot im Hintergrund des Chronicle Keepers,
zur Verfügung stehen, um Kontextinformationen aus dem Programm bereitzustellen. Anhand der aufgeführten Beschreibungen
ist ChatGPT in der Lage zu entscheiden, welche Funktionen zu Rate gezogen werden müssen, um eine passende Antwort auf
eine Anfrage zu geben.

Diese Übersicht ermöglicht es dir, Funktionsnamen auch in deinen Anfragen unterzubringen oder im System Prompt direkt
Anweisungen zu geben, wann welche Funktionen genutzt werden sollen. So kannst du auch, wenn du das Gefühl hast, dass
deine Daten nicht ausreichend beachtet wurden, eine Anfrage wie "Erzähle mir etwas über den Charakter Fidelbus unter
Verwendung der Funktion novalis_background." stellen. Die Dokumente aus deiner Bibliothek werden dann auf jeden
Fall zu Rate gezogen.

Neben der reinen Übersicht über die vorhandenen Funktionen kannst du hier auch aktivieren, dass die ausgeführten
Funktionsaufrufe mit erweiterten Informationen im Gesprächsverlauf angezeigt werden. Das ermöglicht dir ein aktives
Verfolgen, inwiefern deine Einstellungen sich auf deine Gespräche auswirken.

?> Neu ab **v0.5-alpha**

Was dir aber wirklich helfen kann, deine Ergebnisse mit dem Chronicle Keeper zu verbessern, ist, dass du die Beschreibungen
der einzelnen Funktionen auch anpassen kannst. ChatGPT wird diese dann erhalten, statt der Standardbeschreibungen.

?> **Tipp!** Solltest du mit geänderten Beschreibungen deutlich bessere Ergebnisse erzielen als mit den Standardbeschreibungen,
könntest du diese auch mit anderen teilen, um den Chronicle Keeper eventuell für alle Nutzer zu verbessern.

## Kalender

?> Beachte bitte, dass es sich bei den Kalendereinstellungen um sehr **experimentelle Funktionen** handelt. Wenn du
herausfinden willst, wie der Chronicle Keeper deinen Kalender besser verstehen kann, wirst du um ein Gespräch mit
Fragen wie "Wie kann ich den Kalender, gegeben mit der Funktion calendar, verständlicher machen?" nicht herumkommen.
Wenn du herausgefunden hast, wie eine gute Definition eines Kalenders aussieht, wäre eine Rückmeldung an den Entwickler
des Chronicle Keepers sehr freundlich.

Der Kalender teilt sich in drei Bereiche, um dir genug Raum zu geben, deinen Kalender zu definieren. In einer Spielwelt
verläuft in der Regel die Zeit nicht mit der echten Zeit. Entsprechend ist das heutige Kalenderdatum selten das
Datum in deiner Spielzeit. Auch verläuft die Zeit anders. Eine Spielrunde an einem Tag im Spiel kann sich auch schon
einmal über mehrere Tage im echten Leben verteilen. So ist unser realer Kalender wahrscheinlich auch auf deine Spielrunde
nicht anwendbar. Im Chronicle Keeper gibt es so immer ein statisches Datum, auf dessen Basis gearbeitet wird. Habt ihr
in eurer Spielrunde einen neuen Tag erreicht, musst du diesen auch in deinem Chronicle Keeper eintragen.

**Allgemein**

Im allgemeinen Kalenderbereich kannst du zum Ersten das aktuelle Datum in deiner Spielwelt setzen. Bitte trage das
vollständige Datum inklusive Monat und Jahr ein. Ein Beispiel wäre der "12. Jubilar im 1443. Zyklus des Lebens".
Erreicht ihr in eurer Spielrunde einen neuen Tag, müsstest du dann, um beim Beispiel zu bleiben, aus dem 12. den 13.
machen oder spezifischer den Tag, der in eurem Spielkalender auf den 12. folgt.

In der Textbox kannst du dann noch lang und breit ausführen, wie der Kalender in eurer Spielwelt funktioniert. Bitte
sei so genau wie möglich und versuche es einem Kind zu erklären, da ChatGPT versucht, diese Informationen zu
interpretieren und fortan auf Basis eures Kalenders zu rechnen oder dir Auskunft zu erteilen.

Ein Hinweis: Der Kalender sollte in Textform beschrieben werden. Große Tabellen können zu Problemen in der Auswertung
führen aufgrund der Funktionalitäten des Chronicle Keepers. Wenn du also eine Reihenfolge der Monate aufführen möchtest,
dann sollte dies in einer Form wie "Der erste Monat eines Zyklus ist der Jubilar. Darauf folgt als zweiter Monat
der Zebra. [...]".

**Feiertage** und **Mondkalender**

Diese beiden Einstellungsbereiche erlauben, was die Namen verraten. Eine Formulierung, welche Feiertage es gibt und wie
der Mondkalender funktioniert. Du kannst in den Texten auch die Funktion "calendar" als Referenz benennen, wenn du
weiteren Kontext erzwingen willst. Insgesamt gibt es wenige Hinweise aktuell, wie man die Beschreibungen gut zusammen
bringen kann. Teilweise hat ChatGPT im Hintergrund ein paar Halluzinationen zu den ganzen Informationen.

Mehr Informationen werden in Zukunft folgen.

## Anwendung

Die Import- und Export-Funktionen des Chronicle Keepers ermöglichen es dir, alle Daten aus der Bibliothek, die
Einstellungen und die gespeicherten Gespräche zu sichern und wiederherzustellen. Diese Funktionen sind essenziell,
um deine Daten zu sichern und bei Bedarf wiederherzustellen.

**Allgemein**

In diesem Bereich kannst du deinen [API Key von OpenAI](https://platform.openai.com/api-keys) eintragen oder ändern. Der API Key wird benötigt, um die
Kommunikation mit ChatGPT zu ermöglichen. Ohne einen gültigen API Key kann der Chronicle Keeper keine Gespräche
führen.

**Export**

Der Export erstellt ein ZIP-Archiv, das alle relevanten Daten des Chronicle Keepers enthält. Dies umfasst:

- Alle Dokumente, Bilder und Gespräche aus der Bibliothek
- Alle Favoriten
- Alle Einstellungen
- Alle gespeicherten Gespräche

Speichere das erstellte ZIP-Archiv an einem sicheren Ort.

?> **Tipp:** Es ist ratsam, regelmäßig Exporte durchzuführen, um deine Daten vor Verlust zu schützen.

**Import**

Der Import ermöglicht es dir, eine zuvor exportierte Version des Chronicle Keepers wiederherzustellen. Du solltest
nur Archive verwenden, die mit dieser Anwendung erstellt wurden. Diese Funktion kann auch genutzt werden, um
Datenbestände oder -sicherungen von älteren Versionen einzuspielen.

<ins>Import-Optionen</ins>

- **Überschreiben der Einstellungen:** Diese Option überschreibt alle aktuellen Einstellungen mit den Einstellungen aus dem Import-Archiv.
- **Überschreiben vorhandener Daten (ohne leeren):** Diese Option überschreibt vorhandene Daten in der Bibliothek, ohne diese vorher zu leeren.
- **Leeren der Bibliothek vor dem Import:** Diese Option leert die Bibliothek vollständig, bevor die Daten aus dem Import-Archiv eingespielt werden.

Mit diesen Funktionen kannst du sicherstellen, dass deine Daten im Chronicle Keeper stets gesichert und bei Bedarf wiederhergestellt werden können.

