# Sitzungsnotiz – Einrichtung und Hotfixes

## Kurzüberblick

Die App kann über GitHub Pages oder ohne GitHub über Netlify Drop veröffentlicht werden. Die Webseite ist öffentlich erreichbar, aber die App enthält keinen Dienst zum Hochladen deiner Sitzungsdaten: Protokolle und Teilnehmendenlisten werden im lokalen Speicher des jeweiligen Browsers abgelegt.

Für die erste Installation und für spätere Aktualisierungen braucht das Gerät Internet. Nach dem ersten vollständigen Aufruf kann die App dank Offline-Cache auch ohne Internet starten. iPhone und iPad synchronisieren ihre Sitzungen nicht miteinander.

## GitHub Pages: Änderungen und Hotfixes

Wenn die App bereits über dein Repository `sitzungsnotiz-spvgg` veröffentlicht wird:

1. Öffne im Repository den Ordner `Sitzungsnotizen`.
2. Wähle **Add file → Upload files** und lade die aktualisierte App-Datei hoch. Für eine Änderung an der Oberfläche reicht meist `index.html`; bei Änderungen an Symbolen, Offline-Verhalten oder App-Einstellungen lade alle Dateien aus dem Startpaket hoch.
3. Bestätige unten mit **Commit changes**. GitHub Pages veröffentlicht den Stand nach dem erfolgreichen Deployment unter derselben Website-Adresse.
4. Öffne die App auf dem iPad mit Internetverbindung erneut und lade die Seite neu. Danach kann sie wieder offline verwendet werden.

Lösche nicht die Safari-Websitedaten, um ein Update zu erzwingen: Dadurch könnten lokal gespeicherte Sitzungen verloren gehen. Die Adresse der App sollte gleich bleiben, damit die Sitzungen im lokalen Browser-Speicher erhalten bleiben.

## Netlify Drop: erste Einrichtung

1. Öffne [Netlify Drop](https://app.netlify.com/drop) auf dem PC.
2. Melde dich an oder erstelle ein Netlify-Konto, damit du die Webseite dauerhaft verwalten und später Hotfixes veröffentlichen kannst.
3. Ziehe `Sitzungsnotiz-PWA-Startpaket.zip` auf die Upload-Fläche. Alternativ entpacke die ZIP-Datei und ziehe den entpackten Ordner hinein.
4. Netlify veröffentlicht die Seite und zeigt eine Adresse mit der Endung `.netlify.app` an. Notiere diese Adresse und öffne sie einmal in einem Browser mit Internetverbindung.

## 2. Auf iPhone und iPad hinzufügen

1. Öffne die Netlify-Adresse auf dem Gerät in Safari.
2. Tippe auf **Teilen** und dann auf **Zum Home-Bildschirm**.
3. Aktiviere **Als Web-App öffnen** und tippe auf **Hinzufügen**.
4. Öffne die App einmal mit Internetverbindung, damit die Offline-Dateien gespeichert werden.

Danach kannst du die App über das neue Symbol starten. Die Sitzungen bleiben lokal auf dem jeweiligen Gerät.

## Datenschutz und Öffentlichkeit

Die Netlify-Adresse ist öffentlich erreichbar. Dort liegen nur die App-Dateien und das Vereinswappen. Die App überträgt weder Protokolle noch Teilnehmerlisten an Netlify; sie verwendet den lokalen Browser-Speicher. Wer die Adresse kennt, kann allerdings die leere App-Seite öffnen. Wenn auch die App-Seite selbst nicht öffentlich sein darf, brauchst du einen privaten HTTPS-Webhost.

## Hotfixes veröffentlichen

Die Netlify-Adresse dauerhaft beibehalten, da der lokale Sitzungsverlauf an diese Browser-Adresse gebunden ist. Für einen Hotfix die aktualisierten Dateien in eine neue ZIP-Datei packen, in Netlify das Projekt öffnen und unter **Deploys** die neue ZIP-Datei hochladen. Beim nächsten Öffnen mit Internetverbindung erhält die installierte App die neue Version. Offline startet sie mit der zuletzt zwischengespeicherten Version.
