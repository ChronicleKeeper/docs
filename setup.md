# Installation

?> **Vor der Installation** Der Chronicle Keeper befindet sich in der Entwicklung. Bitte kontaktiere den Entwickler,
um den Chronicle Keeper im engen Austausch weiterzuentwickeln.

## Kontakt

Du kannst eine E-Mail an [contact@chronicle-keeper.com](mailto:contact@chronicle-keeper.com) schreiben.
Weitere Kontaktmöglichkeiten:

- [Twitter / X](https://x.com/DZunke)
- [GitHub Issues](https://github.com/ChronicleKeeper/ChronicleKeeper/issues)


## Vorraussetzungen

Der Chronicle Keeper benötigt ein Windows-Betriebssystem. Andere Betriebssysteme werden für die Desktop-Variante
derzeit nicht unterstützt. Zusätzlich wird ein [API Key von OpenAI](https://platform.openai.com/api-keys) benötigt.

Bitte beachte, dass der API Key nicht im "Free Tier" sein sollte, da die Limitierungen für eine reale Anwendung
ungeeignet sind. Mindestens das Tier 1 sollte vorliegen, was durch eine Einzahlung von mindestens 5$ auf das
OpenAI-Konto erreicht wird.

Falls nach 48 Stunden weiterhin nur das "Free Tier" aktiv ist, wende dich an den OpenAI Support.

?> Eine Übersicht über die Zugriffstufen von OpenAI findest du
[hier](https://platform.openai.com/docs/guides/rate-limits/usage-tiers?context=tier-one).


## Download & Setup

Die aktuellste Version des Chronicle Keepers kannst du auf GitHub herunterladen. In den Releases findest du zu jeder
Version ein entsprechendes ZIP-Archiv, das die vollständige Anwendung beinhaltet.

Die aktuellste Version kannst du hier herunterladen:
[Chronicle Keeper Releases](https://github.com/ChronicleKeeper/ChronicleKeeper/releases/latest)

Nachdem du das ZIP-Archiv heruntergeladen und entpackt hast, musst du noch einen OpenAI API Key manuell in einer
Datei hinterlegen. Diese findest du unter `www/.env`. Dort gibt es einen Eintrag `OPENAI_API_KEY`. Hast du deinen Key
dort hinterlegt, kannst du im entpackten Verzeichnis die Datei `ChronicleKeeper.exe` ausführen.

Es öffnet sich dann ein Fenster, das im ersten Moment ein wenig länger brauchen könnte, bis es geladen ist. Und schon
kannst du loslegen, den Chronicle Keeper in deine Rollenspielerfahrung zu integrieren.

## Upgrade

Hast du bereits eine Version des Chronicle Keepers am Laufen, musst du für das Upgrade auf eine neue Version die im
Download & Setup beschriebenen Schritte für die neue Version ausführen. Da deine neue Version dann keinerlei Daten
beinhaltet, musst du diese noch übertragen.

Dazu gehst du wie folgt vor:

1. Exportiere deine Daten aus der alten Version. Die Möglichkeit findest du in den [Einstellungen](settings.md).
2. Das gespeicherte ZIP-Archiv solltest du sicher verwahren, da es auch als Backup deiner Daten dient.
3. In deiner neuen Version des Chronicle Keeper gehst du in die [Einstellungen](settings.md) und kannst dort nun einen
4. "Import" ausführen.

Deine Daten sollten nun vollständig in die neue Version geladen sein. Sollte es dabei zu Problemen gekommen sein,
wende dich bitte an die Entwickler. Verloren gegangen ist nichts, da du auch die alte Version noch hast.

?> **Empfehlung** Aufgrund des Entwicklungsstandes des Chronicle Keepers solltest du regelmäßig Exporte ausführen, um
deine Daten vor Verlust zu sichern. Es wäre sehr schade, wenn die wunderbaren Geschichten und Erlebnisse verloren gehen
würden.
