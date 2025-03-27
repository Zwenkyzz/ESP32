🔐 Guardia – Système de Contrôle d'Accès RFID connecté à une API
Ce projet permet de contrôler l'accès à un espace sécurisé grâce à un badge RFID (MFRC522) et un ESP32-C3 (Seeed Studio XIAO).
Les autorisations sont vérifiées via une API FastAPI distante avec gestion des rôles (admin, user).

!RFID + ESP32 + API

---

🧠 Fonctionnalités
🔐 Lecture de badges RFID
☁️ Vérification d'autorisation via une API HTTP
👤 Gestion des rôles : admin, user
➕ Création de nouveaux badges à partir d'un badge admin
🔄 Ajout automatique des badges via interface série

---

🛠 Matériel nécessaire
| Composant               | Référence                        |
|-------------------------|----------------------------------|
| Microcontrôleur         | Seeed Studio XIAO ESP32-C3       |
| Lecteur RFID            | MFRC522                          |
| Cartes ou badges RFID   | 13.56 MHz (type MIFARE)          |
| Câbles Dupont           | M/F                              |
| Accès Internet WiFi     | Obligatoire pour l’ESP32         |

---

🔌 Schéma de câblage (SPI)
| MFRC522     | ESP32-C3 (XIAO) | Pin |
|-------------|------------------|-----|
| SDA (SS)    | GPIO10           | D10 |
| SCK         | GPIO8            | SCK |
| MOSI        | GPIO10           | MOSI |
| MISO        | GPIO9            | MISO |
| RST         | GPIO3            | D1  |
| GND         | GND              | -   |
| VCC (3.3V)  | 3.3V              | -   |

⚠️ Ne pas alimenter en 5V, uniquement 3.3V.

---

🧑‍💻 Installation
Cloner ce repo :```bash
git clone https://github.com/ton-utilisateur/guardia-rfid.git
cd guardia-rfid
