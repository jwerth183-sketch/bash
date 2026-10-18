# 🎙️ Linux Voice-to-Text Diktier-Skript

Ein extrem schnelles, ressourcenschonendes und kostenloses Diktier-Skript für Linux. 
Es nimmt deine Stimme auf, wandelt sie über die schnelle **Groq API (Whisper-large-v3-turbo)** in Text um und **tippt das Ergebnis vollautomatisch** in dein aktives Fenster.

Perfekt optimiert für die Nutzung als **Tastenkürzel (Shortcut)** im Hintergrund, speziell unter Desktop-Umgebungen wie Cinnamon, Mint oder GNOME.

## ✨ Features
* **Rasend schnell:** Nutzt die Groq API für fast verzögerungsfreie Transkription.
* **Auto-Typing:** Fügt den erkannten Text wie von Geisterhand selbst in dein Dokument ein (via `xdotool`).
* **Toggle-Modus (Schalter):** Drücke dein Tastenkürzel, um die Aufnahme zu starten. Drücke es erneut, um sie sofort zu beenden und den Text zu generieren.
* **Smartes Zuhören:** Falls du den zweiten Tastendruck vergisst, stoppt die Aufnahme automatisch nach 1,5 Sekunden Stille.
* **Audio-Feedback:** Nutzt kurze, unaufdringliche **Signaltöne** (Start, Erfolg, Fehler), da Linux-Desktops visuelle Popups bei Hintergrund-Shortcuts oft blockieren.
* **Universell:** Unterstützt sowohl **X11** (`xclip`) als auch **Wayland** (`wl-copy`).

## 🛠️ Installation & Voraussetzungen

Damit das Skript Audios aufnehmen, Tastendrücke simulieren und die Zwischenablage nutzen kann, müssen ein paar kleine Linux-Pakete installiert werden.

Öffne dein Terminal und führe diesen Befehl aus:
```bash
sudo apt update && sudo apt install -y sox libsox-fmt-all curl jq wl-clipboard xclip xdotool
