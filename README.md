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

<img width="1912" height="902" alt="2026-02-22 11_17_24-HP-GEN8-SRV-Boreas tlp - root@172 2 8 14_2804 - Bitvise xterm - root@hp-gen8-srv" src="https://github.com/user-attachments/assets/588e667b-6f1f-423d-adf4-5736e1fe3704" />
<img width="1909" height="904" alt="2026-02-22 11_30_51-Clipboard" src="https://github.com/user-attachments/assets/e52fdba5-a66c-4f3b-871f-edf398636c45" />
<img width="1920" height="1080" alt="2026-02-22 11_17_59-WakeOps und 1 weitere Seite - Malte Speck – Microsoft​ Edge" src="https://github.com/user-attachments/assets/c448aece-b2e5-4624-96f9-16fe601856ad" />
<img width="1920" height="1080" alt="2026-02-22 11_19_10-WakeOps und 1 weitere Seite - Malte Speck – Microsoft​ Edge" src="https://github.com/user-attachments/assets/7d5bec6d-75dc-44a9-8d8a-eb74ebc4ed97" />
<img width="1920" height="1080" alt="2026-02-22 11_19_29-WakeOps Report und 2 weitere Seiten - Malte Speck – Microsoft​ Edge" src="https://github.com/user-attachments/assets/63b67afe-69f1-43c8-9a1b-cd3d164ed5a4" />
<img width="1920" height="1080" alt="2026-02-22 11_26_54-Clipboard" src="https://github.com/user-attachments/assets/64ef58be-5bcb-461e-95ba-c4c770cc64f3" />
<img width="1920" height="1080" alt="2026-02-22 11_26_12-Clipboard" src="https://github.com/user-attachments/assets/caf2d549-fb67-45b0-be93-79a23b5f7c4e" />

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
