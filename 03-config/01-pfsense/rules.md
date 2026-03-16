# Règles Firewall pfSense


## Objectif
Définir une politique de filtrage claire, lisible et sécurisée entre les différentes zones du lab.


Principe appliqué : **deny all par défaut**, autoriser uniquement les flux nécessaires.


---


## Zones réseau
- LAN : postes et serveurs internes
- DMZ : services exposés
- WAN : Internet
- VPN : accès distant et inter-sites


---


## Règles LAN


### LAN → Internet
- HTTP / HTTPS
- DNS
- NTP


### LAN → DMZ
- Flux applicatifs nécessaires uniquement


---


## Règles DMZ


### DMZ → LAN
- ❌ Interdit par défaut


### DMZ → Internet
- Autoriser mises à jour


---


## Règles WAN


### WAN → DMZ
- Ports publiés (80 / 443)


### WAN → LAN
- ❌ Interdit


---


## Règles VPN


### Client-to-Site
- Accès réseau d’administration uniquement


### Site-to-Site
- Réplication AD
- Flux inter-sites nécessaires


---


## Journalisation
- Logging activé sur règles critiques