# bash
# 🎙️ Linux Voice-to-Text Diktier-Skript

Ein extrem schnelles, ressourcenschonendes und kostenloses Diktier-Skript für Linux. 
Es nimmt deine Stimme auf, wandelt sie über die pfeilschnelle **Groq API (Whisper-large-v3-turbo)** in Text um und legt das Ergebnis direkt in deine Zwischenablage. 

Perfekt optimiert für die Nutzung als **Tastenkürzel (Shortcut)** im Hintergrund, speziell unter Desktop-Umgebungen wie Cinnamon, Mint oder GNOME.

## ✨ Features
* **Rasend schnell:** Nutzt die Groq API für fast verzögerungsfreie Transkription.
* **Audio-Feedback:** Da Linux-Desktops (wie Cinnamon) visuelle Popups bei Hintergrund-Shortcuts oft blockieren, nutzt dieses Skript kurze, unaufdringliche **Signaltöne** (Start, Erfolg, Fehler).
* **Smartes Zuhören:** Stoppt die Aufnahme automatisch nach 2 Sekunden Stille.
* **Universell:** Unterstützt sowohl **X11** (`xclip`) als auch **Wayland** (`wl-copy`).
* **Kostenlos:** Benötigt lediglich einen kostenlosen API-Key von Groq.

## 🛠️ Installation & Voraussetzungen

Damit das Skript Audios aufnehmen und die Zwischenablage nutzen kann, müssen ein paar kleine Linux-Pakete installiert werden.

Öffne dein Terminal und führe diesen Befehl aus:
```bash
sudo apt update && sudo apt install -y sox libsox-fmt-all curl jq wl-clipboard xclip
