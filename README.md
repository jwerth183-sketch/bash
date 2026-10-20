# Linux Voice-to-Text Diktier-Skript

Ein Bash-Skript für Linux zur systemweiten Spracheingabe. Es nimmt gesprochenes Audio auf, transkribiert es über die Groq-API (Whisper-large-v3-turbo) und fügt den generierten Text automatisch in das aktuell fokussierte Fenster ein. 

Das Skript ist für die Ausführung über eine systemweite Tastenkombination im Hintergrund konzipiert (z. B. unter Cinnamon, Linux Mint oder GNOME).

## Funktionen
- **Transkription:** Nutzt die Groq-API für eine zügige Textgenerierung.
- **Automatisches Einfügen:** Übergibt den erkannten Text über `xdotool` an die aktive Anwendung.
- **Toggle-Steuerung:** Die Audioaufnahme lässt sich über denselben Tastendruck starten und wieder manuell beenden.
- **Silence Detection:** Alternativ stoppt die Aufnahme automatisch, sobald für 1,5 Sekunden Stille erkannt wird.
- **Akustisches Feedback:** Verwendet kurze Signaltöne zur Statusrückmeldung (Start, Erfolg, Fehler), da visuelle Benachrichtigungen bei Hintergrundskripten oft von der Desktop-Umgebung blockiert werden.
- **Zwischenablage:** Kompatibel mit X11 (`xclip`) und grundlegend mit Wayland (`wl-copy`).

## Voraussetzungen

Für die Audioaufnahme, das Auslesen der Zwischenablage und die Simulation der Tastendrücke werden folgende Kommandozeilenwerkzeuge benötigt. Unter Debian/Ubuntu-basierten Systemen lassen sich diese über das Terminal installieren:

```bash
sudo apt update && sudo apt install -y sox libsox-fmt-all curl jq wl-clipboard xclip xdotool
