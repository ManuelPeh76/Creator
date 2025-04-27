# Creator

Eine Spielwiese für HTML, CSS, Javascript und Typescript mit Live-Preview. Erstelle ein Projekt und gib ihm einen Namen. Von diesem Moment an ist das Projekt auch schon gesichert! Ganz lokal, in der indexedDB deines Browsers.
Startest du das Tool erneut, wird das zuletzt benutze Projekt automatisch geöffnet.
Alle bisher angelegten Projekte findest du ganz bequem in einem Dropdown-Menü, sowie im Kontext-Menü (Rechtsklick -> Projekt wählen).
Um deine Projekte ganz browser-unabhängig zu sichern, kannst du alle Projekte als eine einzige ZIP-Datei herunterladen. Kopierst du den Inhalt dieser ZIP in den /creations-Unterordner, kannst du beim Öffnen des Tools mit '...index.html?usedb=0' die zu ladenden Projekte auswählen. Alternativ klicke auf 'Projekt importieren' und wähle die ZIP-Datei selbst aus. Auch dann kannst du auswählen, welche Projekte aus der ZIP-Datei importiert werden sollen. 
Der Start mit ?usedb=0 führt dazu, dass keine Browser-Datenbank verwendet wird. Stattdessen sucht das Tool im creations-Ordner die Datei 'creations.txt' und lädt die dort eingetragenden Projekte aus dem /json-Ordner. Projekte können also nicht mehr automatisch gesichert werden! Du kannst aber alle geladenen Projekte als ZIP-Datei sichern, oder ein einzelnes Projekt als JSON. Alles Andere funktioniert ganz normal.

## Die Editoren

Der Creator basiert auf dem populären Ace-Editor von Cloud9.
Es gibt insgesamt sechs einzelne Editoren, von denen immer nur einer sichtbar ist. Die Auswahl des Editors geschieht bequem über Tabs direkt über dem Editor.
Die Editoren: HTML, Javascript, Typescript, CSS, Bilder und Assets.
Jeder Editor prüft die Eingabe auf syntaktische Korrektheit, hat Undo/Redo, sowie einen Beautifier und einen Minifier und macht Eingabevorschläge.

Die ersten vier Editoren sind selbsterklärend (HTML, CSS, JS, TS). Die Editoren 'Bilder' und 'Assets' speichern Inhalte im JSON-Format. 

### Assets-Editor
Beim Hochladen von Dateien kannst du wählen, wie diese verarbeitet werden sollen: Abhängig von der Dateierweiterung oder als Asset.
Wenn du Asset wählst, werden die hochgeladenen Dateien je nach Inhalt entweder als dataURI, als minifizierter Text oder in einen 8- oder 16-Bit-Arraybuffer konvertiert (dieses Verhalten kann beeinflusst werden, mehr dazu später).
Die Dateiinhalte werden anschließend in Strings umgewandelt und dem Asset-Editor hinzugefügt. Der Inhalt liegt im JSON-Format vor.
Beim Rendern des Projekts wird die globale Konstante '_assets_' erstellt, die alle Assets enthält, um sie per JavaScript zugänglich zu machen.

### Bilder-Editor
Klicke auf 'Upload' und wähle die zu ladenden Bilder. Diese werden zu dataURIs konvertiert und als Strings im Bilder-Editor gespeichert. Bei jedem Rendern des Projektes werden alle Pfadangaben zu Bildern innerhalb des HTML- und CSS-Quelltextes durch die dataURIs ersetzt, so dass die Bilder ganz normal angezeigt werden. Das gilt aber nicht für dynamische Inhalte, die erst während der Laufzeit nachgeladen werden sollen.

Die Inhalte der Bilder- und Assets-Editoren sollten nur von Hand editiert werden, wenn du weißt, was du tust! Aber zur Not gibt es ja noch die Undo-Funktion. ;)

## Die Editor-Funktionen

...
