# WakeOps Enterprise

WakeOps ist eine webbasierte Netzwerk-Operations-Oberfläche zum Scannen, Pingen, Geräte-Management (OUI/Vendor, Notizen, SSH-Keys) und zum Ausführen typischer Remote-Aktionen wie WOL/RDP – mit Logging, Report-Export und Lizenz-Freischaltung.

---

## Features

- **Device-Liste** mit IP/Hostname/MAC/Vendor/Status/LastSeen/OS
- **Scan / Auto-Scan** (planbar) + **Status-Check** (planbar)
- **Ping** (inkl. Dauerping) als Popup mit Fortschritt
- **WOL** (Wake-on-LAN) inkl. Broadcast-Fallbacks
- **OUI/Vendor**
  - OUI-Update (progressiv) mit Fortschritt & Fehlerliste
  - OUI-Suche
- **Details-Popup**
  - editierbarer Anzeigename
  - Notizen
  - SSH-Key Upload/Clear
- **Report** (Übersicht + Print)
- **Audit-Log**
  - Aktionen protokolliert
  - optional verschlüsselte Speicherung in DB
- **Lizenzsystem**
  - Maschinen-ID im Setup
  - Lizenz-Popup zum Aktivieren
  - ohne Lizenz: **nur Ping** aktiv, Rest ausgegraut/gesperrt
- **UI**
  - M365-ähnlicher Ribbon-Look
  - Modals blocken Hintergrund zuverlässig
  - Favicon vorhanden

---

## Screenshots

<img width="1920" height="1080" alt="2026-02-16 20_32_12-WakeOps - Malte Speck – Microsoft​ Edge" src="https://github.com/user-attachments/assets/324bc6de-6f48-48bf-8e4f-561a1b42a4b3" />
---

## Requirements

- Linux-Server (empfohlen)
- Apache oder Nginx
- PHP 8.x (mit PDO MySQL/MariaDB)
- MariaDB/MySQL
- Systemtools (je nach Features):
  - `ping` (iputils)
  - optional: `ip` (iproute2) für bessere Routing-Erkennung bei WOL


## Lizenzsystem

Maschinen-ID
Die Maschinen-ID wird im Setup generiert und gespeichert. Sie wird im Lizenz-Dialog angezeigt.

Lizenz aktivieren

In der App: Lizenz → Code einfügen → speichern.

Ohne gültige Lizenz gilt:

nur Ping ist aktiv

alle anderen Buttons/Funktionen sind ausgegraut und serverseitig gesperrt
