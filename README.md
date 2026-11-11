# school-network-infrastructure
# Proiectare și Configurare Rețea Locală (LAN) – CNLB Sebeș

Proiect complet de dimensionare, proiectare și securizare a infrastructurii de rețea campus pentru Colegiul Național „Lucian Blaga” Sebeș, acoperind parterul și etajul 1 al instituției.

## 📌 Obiective și Caracteristici Principale
- **Topologie hibridă stea extinsă** cu cablare structurată pe cupru Cat.6 LSOH (standard TIA/EIA-568B).
- **Segmentare logică prin 7 VLAN-uri** pentru izolarea traficului administrativ de cel didactic și guest.
- **Infrastructură PoE+** pentru alimentarea a 27 de camere IP Hikvision și a punctelor de acces Wi-Fi 6.
- **Securitate și Servicii:** Server DHCP dedicat, rutare inter-VLAN statică și reguli de NAT / Port Forwarding pentru acces securizat de la distanță la NVR-ul central.

## 🏢 Segmentarea Rețelei (VLANs)
| VLAN ID | Destinație | Subrețea | Gateway |
|---|---|---|---|
| VLAN 1 | Management Echipamente Core | `192.168.0.0/24` | `192.168.0.1` |
| VLAN 10 | Administrație & Săli Curs Parter | `192.168.10.0/24` | `192.168.10.1` |
| VLAN 20 | Educațional & Săli Curs Etaj 1 | `192.168.20.0/24` | `192.168.20.1` |
| VLAN 31 | Laborator Informatică 1 (30 PC-uri) | `192.168.31.0/24` | `192.168.31.1` |
| VLAN 32 | Laborator Informatică 2 (30 PC-uri) | `192.168.32.0/24` | `192.168.32.1` |
| VLAN 50 | Supraveghere Video CCTV (NVR + 27 Camere IP) | `192.168.50.0/24` | `192.168.50.1` |
| VLAN 60 | Wi-Fi Campus / Edu-Guest (Client Isolation) | `192.168.60.0/24` | `192.168.60.1` |

## 🛠️ Echipamente și Unelte Utilizate
- **Echipamente de rețea:** Router/Firewall Enterprise TP-Link, Switch PoE+ 48 porturi (MDF Parter), Switch PoE+ 24 porturi (Etaj 1), Access Point-uri Wi-Fi 6.
- **Securitate & Multimedia:** NVR Hikvision 32 Canale AcuSense, Table interactive Smart 75", Camere IP 4MP.
- **Proiectare și diagnostic:** Floorplanner, Command Prompt (ipconfig, ping).
