# Hilfe zu Morrow

Die App gibt es auf Deutsch. Die ausführlichen Anleitungen sind derzeit auf Englisch; die häufigsten Fragen sind unten auf Deutsch beantwortet. Bei allem anderen hilft dir der Support gern, auch auf Deutsch: **support@liftbridgelabs.app**.

## Anleitungen (Englisch)

- [Getting started](https://liftbridgelabs.app/products/morrow/docs/getting-started): Morrow installieren und den ersten Server hinzufügen
- [BookOrbit setup](https://liftbridgelabs.app/products/morrow/docs/bookorbit-setup), [Audiobookshelf setup](https://liftbridgelabs.app/products/morrow/docs/audiobookshelf-setup), [Grimmory setup](https://liftbridgelabs.app/products/morrow/docs/grimmory-setup): die Einrichtung für deinen Server
- [Troubleshooting](https://liftbridgelabs.app/products/morrow/docs/troubleshooting): wenn eine Verbindung, Wiedergabe oder ein Download nicht klappt
- [FAQ](https://liftbridgelabs.app/products/morrow/docs/faq): alle Fragen und Antworten

## Häufige Fragen

### Ist Morrow ein Hörbuch-Server?

Nein. Morrow ist ein Player, der sich mit einem BookOrbit-, Audiobookshelf- oder Grimmory-Server verbindet, den du bereits betreibst. Morrow enthält, hostet oder verkauft keine Hörbücher.

### Kann ich mehr als einen Server verbinden?

Die kostenlose Version verbindet einen Server. Morrow Unlock hebt diese Grenze auf, sodass du mehrere hinzufügen und auf Home zwischen ihnen wechseln kannst. Jeder Server bleibt dabei völlig eigenständig: Morrow führt nichts zwischen ihnen zusammen und synchronisiert nichts, auch wenn dasselbe Hörbuch auf mehreren liegt.

### Was ist kostenlos, und was bringt Morrow Unlock?

Die kostenlose Version ist ein vollständiger Player: Wiedergabe mit Kapiteln, einstellbarem Tempo und Schlaftimer, CarPlay, das Widget, die Steuerung im Sperrbildschirm, die Warteschlange mit automatischem Weiterspielen, ein verbundener Server und bis zu drei geladene Bücher.

Morrow Unlock ist ein einmaliger Kauf (einzeln oder für die Familie) mit unbegrenzten Downloads, automatischem Laden des nächsten Buchs der Warteschlange, Akzentfarben und beliebig vielen Servern. Es gibt kein Abo.

### Funktioniert Morrow offline?

Ja, auf zwei Wegen:

- **Downloads**: Der Download-Knopf auf der Detailseite eines Buchs (oder in der Wiedergabe) speichert das ganze Buch auf dem Gerät, bis du es entfernst. Ein vollständig geladenes Buch spielt ohne Verbindung zum Server, auch im Flugmodus.
- **Wiedergabe-Cache**: Während ein Buch gestreamt wird, kann Morrow es automatisch auf dem Gerät speichern, damit es beim nächsten Mal sofort startet. Das Limit legst du in den Einstellungen fest.

Über Mobilfunk wird standardmäßig nichts geladen; in den Einstellungen gibt es dafür einen eigenen Schalter.

### Was wird zwischen meinen Geräten synchronisiert?

**Deine Stelle im Buch überall**, weil der Fortschritt auf deinem eigenen Server gespeichert wird: iPhone, iPad, Apple TV, Android und der Web-Player deines Servers sehen dieselbe Position.

**Alles andere nur innerhalb einer Plattform.** Die Liste „Als Nächstes“, aus „Weiterhören“ weggewischte Bücher, zuletzt gespielte Titel, das Tempo pro Buch, die Anordnung der Regale und der Hörverlauf werden über deine private iCloud-Datenbank zwischen iPhone, iPad und Apple TV synchronisiert, wenn du „Server und ‚Als Nächstes‘ synchronisieren“ einschaltest. Alles ist Ende-zu-Ende verschlüsselt.

### Zählt mein Hören in der Statistik von BookOrbit?

Ja, ab BookOrbit 3.2.0. Morrow sendet jede Hörsitzung an BookOrbit, sobald du aufhörst zu hören. Deine Statistiken, Serien und das Leseprotokoll jedes Buchs in BookOrbit enthalten dann auch, was du in Morrow hörst. Als Quelle steht dort „iOS app“.

Deinen Hörverlauf von vor Morrow 1.10.1 kannst du nachträglich senden: Öffne die **Einstellungen**, wähle deinen BookOrbit-Server und tippe unter **Hörverlauf** auf **Bisherigen Hörverlauf an BookOrbit senden**.

- Gesendet werden die Sitzungen, die Morrow auf diesem Gerät gespeichert hat, bis zu den letzten 20 pro Buch.
- Sie zählen als Hörzeit, ohne Position, deshalb ändert sich der Status eines Buchs dabei nie.
- Jede Sitzung wird nur einmal gezählt, egal wie oft du tippst.
- Hast du ein Buch auf diesem Gerät auch mit einem anderen Konto oder Server gehört, hält Morrow diese Sitzungen zurück und fragt vorher. Ältere Sitzungen speichern nicht, zu welchem Konto sie gehören, deshalb zählen sie nach dem Senden alle als Hörzeit dieses Kontos.

### Unterstützt Morrow CarPlay?

Ja: Home, Sammlungen, die ganze Bibliothek von A bis Z, Offline-Downloads, Serverwechsel und die Steuerung unter „Jetzt läuft“.

### Mein Server liegt hinter Cloudflare oder einem anderen Proxy, der einen Header verlangt

Öffne den Server in den **Einstellungen**, scrolle zu **Erweitert** und füge die Header hinzu, die dein Proxy erwartet. Die Vorlage **Cloudflare Access** trägt `CF-Access-Client-Id` und `CF-Access-Client-Secret` mit einem Tipp ein; füge dort die Werte deines Cloudflare-Service-Tokens ein.

### Kann ich Morrow außerhalb meines Heimnetzes nutzen?

Ja, sofern dein Server sicher von deinem Gerät aus erreichbar ist. Empfohlen ist HTTPS über einen korrekt eingerichteten Reverse-Proxy.

### Wo melde ich einen Fehler?

Am einfachsten per E-Mail an **support@liftbridgelabs.app**, gern mit einer Diagnosedatei: **Einstellungen > Über > Diagnose per E-Mail**. Sie enthält keine Titel, Adressen oder Kontodaten. Du kannst Fehler auch im [Fehlerformular](https://github.com/LiftbridgeLabs/Morrow-Docs/issues/new?template=bug-report.yml) auf GitHub melden (auf Englisch).

## Datenschutz

Die [Datenschutzerklärung auf Deutsch](https://liftbridgelabs.app/products/morrow/privacy/de).
