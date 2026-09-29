# Datenschutz

Morrow verbindet dein Gerät direkt mit Hörbuch-Servern, die du selbst auswählst und betreibst. Diese Seite beschreibt genau, was die App speichert und wo, auf Grundlage der aktuellen Umsetzung, und stimmt mit der offiziellen Datenschutzerklärung im App Store überein.

Dies ist eine Übersetzung der [englischen Fassung](https://liftbridgelabs.app/products/morrow/privacy). Bei Abweichungen gilt die englische Fassung.

## Kurz gesagt

Morrow hat keine Benutzerkonten, keine Analyse, keine Werbung, kein Tracking und keine SDKs für Absturzberichte oder Werbung. Die App sendet deine Daten nie an Liftbridge Labs. Wir erhalten nur dann etwas, wenn du uns selbst eine E-Mail schreibst, etwa mit einer Diagnosedatei, die du selbst exportiert und angehängt hast. Der Netzwerkverkehr läuft zwischen deinem Gerät und den Servern, die du einrichtest. Auf Apple-Geräten kannst du zusätzlich eine Sicherung im iCloud-Schlüsselbund einschalten.

## Server-Zugangsdaten

- Auf Apple-Geräten werden Server-Passwörter, Werte eigener Proxy-Header und Audiobookshelf-API-Schlüssel im Schlüsselbund von iOS gespeichert.
- Unter Android werden diese Geheimnisse mit einem Schlüssel verschlüsselt, den der Android Keystore verwahrt. Server-Einstellungen, die nicht geheim sind, liegen im app-eigenen DataStore-Speicher.
- Zugangsdaten verlassen das Gerät nur, um sich bei dem Server anzumelden, für den du sie eingerichtet hast (zum Beispiel eine Anmeldung bei deinem eigenen BookOrbit-Server). Sie werden nirgendwohin sonst gesendet.

## iCloud-Sicherung (optional, nur Apple)

- „In iCloud sichern“ in den Einstellungen ist **standardmäßig ausgeschaltet**.
- Wenn du es einschaltest, wird deine Serverliste (Servername, Adresse, Benutzername, Anmeldeart und das Passwort oder der API-Schlüssel) als synchronisiertes Objekt in deinem **iCloud-Schlüsselbund** gespeichert, den Apple Ende-zu-Ende verschlüsselt. In iCloud Drive erscheint keine Datei, und Liftbridge Labs kann die Sicherung nicht lesen.
- Die Sicherung bleibt erhalten, wenn du die App löschst, damit eine Neuinstallation deine Einrichtung wiederherstellen kann. Schaltest du die Option aus, wird die Sicherung für alle Geräte aus iCloud gelöscht.
- Diese Sicherung im iCloud-Schlüsselbund enthält nur die Serverliste. Die Liste der zuletzt gespielten Titel, der Hörverlauf und anderer geräteübergreifender Zustand werden getrennt davon über deine private iCloud-Datenbank behandelt, wie im nächsten Abschnitt beschrieben. Die sichere Sicherung unter Android ist derzeit deaktiviert.

## Synchronisierung zwischen deinen Apple-Geräten (optional)

Dieselbe Einstellung „Server und ‚Als Nächstes‘ synchronisieren“, die die iCloud-Sicherung oben steuert, hält auch einen kleinen Teil des Zustands zwischen deinen Apple-Geräten gleich, einschließlich Apple TV. Der iCloud-Schlüsselbund allein kann das nicht, weil Apple TV keinen Zugriff darauf hat. Das betrifft nur Apple-Geräte; Android behält die entsprechenden Einträge auf dem Gerät.

- Dafür wird deine **private iCloud-Datenbank (CloudKit)** in deinem eigenen iCloud-Account verwendet. Liftbridge Labs hat keinen Zugriff darauf und erhält nichts.
- Alles, was Morrow dort speichert, steht in **Ende-zu-Ende verschlüsselten Feldern**, sodass nur deine eigenen Geräte es lesen können. Das umfasst deine Server-Passwörter und API-Schlüssel, deine Serveradressen und Benutzernamen und jede unten beschriebene Liste. Apple speichert die Daten, kann sie aber nicht lesen.
- Was dort gespeichert wird: deine Serverliste (wie oben beschrieben), deine Liste „Als Nächstes“, welche Bücher du aus „Weiterhören“ weggewischt hast, deine kurze Liste zuletzt gespielter Titel, das Wiedergabetempo pro Buch, die Anordnung deiner Regale auf Home und dein Hörverlauf pro Buch. Nur Buchkennungen, Titel, Autoren und Zeitstempel. Kein Audio und keine Zugangsdaten außer den oben bereits beschriebenen Server-Anmeldedaten.
- Die Geräte prüfen auf Änderungen, während die App geöffnet ist, sowie beim Öffnen und Schließen. Im Hintergrund wird nichts geprüft, auch nicht während der Audiowiedergabe im Hintergrund.
- Schaltest du die Einstellung aus, werden diese Einträge aus iCloud gelöscht.

## Hördaten

- Der Wiedergabefortschritt wird **auf deinen eigenen Servern** gespeichert, mit den normalen Fortschrittsfunktionen des jeweiligen Servers, also denselben Einträgen, die auch deren Web-Player verwenden.
- Morrow speichert außerdem Positionseinträge auf dem Gerät, damit ein erneuter Import auf dem Server deine Stelle nicht verliert. Android sichert zusätzlich etwa alle fünf Sekunden die genaue aktuelle Position, damit sie nach einem Beenden der App durch das System erhalten bleibt.
- Kennungen zuletzt gespielter Titel und der Verlauf der Hörsitzungen pro Buch bleiben auf dem Gerät. Auf Apple-Geräten können diese Einträge wie oben beschrieben synchronisiert werden; Android behält sie auf dem Gerät.

## Daten auf dem Gerät

- Cover und Bibliothekslisten werden auf dem Gerät zwischengespeichert, damit die App schnell startet.
- Geladene Bücher bleiben auf dem Gerät, bis du sie entfernst.
- Der automatische Wiedergabe-Cache speichert gestreamte Bücher bis zu dem von dir festgelegten Limit auf dem Gerät und ist von Gerätesicherungen ausgenommen. Du kannst ihn jederzeit in den Einstellungen ansehen und leeren.
- Löschst du die Android-App, werden ihre lokalen Daten und die Geheimnisse im Android Keystore entfernt. Auf Apple-Geräten werden lokale Dateien entfernt, während Einträge im Schlüsselbund dem üblichen Verhalten von Apple folgen; die optionale iCloud-Sicherung bleibt bestehen, bis du sie ausschaltest.

## Diagnose und Dritte

- Morrow enthält **keine** SDKs für Analyse, Absturzberichte oder Werbung, und kein Drittanbieter erhält Daten aus der App. Die App sendet von sich aus nie Diagnosedaten, weder automatisch noch im Hintergrund.
- Apple oder Google können je nach Einstellungen deines Geräts und Accounts übliche Diagnosedaten des Betriebssystems oder Stores erfassen. Diese von der Plattform gesteuerten Datenflüsse werden von Morrow nicht an Liftbridge Labs gesendet.

## Diagnosedaten, die du selbst sendest

Morrow führt einige kleine Diagnoseprotokolle auf dem Gerät, damit sich ein Wiedergabe- oder Download-Problem im Nachhinein erklären lässt. Sie bleiben auf dem Gerät, solange du sie nicht sendest.

- **„Diagnose exportieren“** in den Einstellungen unter „Über“ fasst diese Protokolle in einer Textdatei zusammen. Serveradressen, Serverkennungen, Buchtitel und Bibliotheksnamen werden beim Schreiben der Datei entfernt, sodass sie weder beschreibt, was du hörst, noch wo deine Server stehen. Übrig bleiben App- und Systemversionen, Wiedergabe- und Download-Ereignisse, Dateiformate, Größen und Längen, Fehlercodes und Zeitstempel. Passwörter, Tokens und Benutzernamen werden in diese Protokolle gar nicht erst geschrieben.
- **Du entscheidest, wohin die Datei geht.** Du kannst sie zuerst lesen, speichern oder an eine E-Mail an den Support anhängen. Nur das Senden per E-Mail schickt sie irgendwohin.
- **Wenn du uns eine E-Mail schreibst,** erhalten wir die angehängte Datei und die Adresse, von der du geschrieben hast, wie bei jeder E-Mail. Wir verwenden sie, um dir zu antworten und das Problem zu beheben, und für nichts anderes.

## Aufbewahrung und Löschung von Daten

- Liftbridge Labs erhält aus der App selbst nichts, daher gibt es nichts aufzubewahren. Die Ausnahme sind E-Mails, die du uns selbst schickst: Eine Support-Nachricht und ihre Anhänge bewahren wir nur so lange auf, wie es dauert, dir zu antworten und das beschriebene Problem zu beheben. Sie werden nie verkauft, weitergegeben oder für Werbung verwendet.
- Deine Server bewahren den Hörfortschritt, den du an sie sendest, unter deiner Kontrolle auf.
- Daten auf dem Gerät werden durch das Löschen der App entfernt, vorbehaltlich des üblichen Verhaltens des Apple-Schlüsselbunds; die optionale iCloud-Sicherung entfernst du, indem du die Option zur Sicherung ausschaltest.

## Kontakt

Bei Fragen zum Datenschutz schreib an **support@liftbridgelabs.app** oder eröffne eine Support-Anfrage (gib in einer öffentlichen Anfrage niemals Passwörter, Tokens oder private URLs an).
