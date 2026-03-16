
# `IT Resilience & Monitoring Lab`
**Simulation complète d’un environnement IT multi-site**, proche des standards entreprise, déployée sur VMware et documentée étape par étape.

Ce projet a pour objectif de démontrer des compétences réelles en **administration systèmes et réseaux**, avec une forte orientation **sécurité, structuration Active Directory et bonnes pratiques professionnelles**.



## Objectifs du projet

* Concevoir un **réseau multi-site** sécurisé avec pfSense
* Mettre en place une **segmentation LAN / DMZ**
* Déployer un **Active Directory multi-sites** (2 DC)
* Structurer les **OU et groupes AD**
* Appliquer des **GPO de sécurité et d’usage**
* Mettre en œuvre des **VPN client-to-site et site-to-site**
* Superviser les équipements critiques avec **Zabbix**
* Documenter l’ensemble pour une **reproductibilité totale**



## Architecture globale

### Sites

* **Site A**

  * pfSense A
  * DC1 (AD DS / DNS / DHCP)
  * Serveur Zabbix
  * Postes clients Windows 11

* **Site B**

  * pfSense B
  * DC2 (AD DS / DNS)
  * Postes clients Windows 11

### Interconnexion

* VPN **Site-to-Site** entre Site A et Site B
* VPN **Client-to-Site** pour accès administrateur distant


## Choix techniques clés

* **Hyperviseur** : VMware (2 PC physiques)
* **Firewall** : pfSense
* **Annuaire** : Active Directory (Windows Server 2022)
* **Clients** : Windows 11
* **Supervision** : Zabbix (monitoring)



## Sécurité & bonnes pratiques

* Politique firewall **deny all** par défaut
* Segmentation réseau claire (LAN / DMZ)
* Comptes administrateurs isolés
* Groupes AD structurés
* GPO liées au bon niveau d’OU
* Journalisation des flux critiques


##  Périmètre figé du projet

### Environnement

* **Hyperviseur** : VMware (2 PC distincts)
* **OS client** : Windows 11
* **Architecture** : 2 sites (Site A et Site B)

### Réseau & Sécurité (pfSense)

* **Zones** : LAN / DMZ
* **Segmentation** : VLANs par zone et par usage
* **VPN** :

  * Client-to-Site (accès administrateur distant)
  * Site-to-Site (interconnexion Site A ↔ Site B)
* **Multi-WAN** : Non (choix volontaire pour clarté)

### Active Directory

* **Domaine** : `lab.lan`
* **Contrôleurs de domaine** :

  * DC1 : Site A (principal)
  * DC2 : Site B (secondaire / réplication)
* **Services** : AD DS, DNS, DHCP
* **GPO implémentées** :

  * Politique de mot de passe
  * Verrouillage de session
  * Mappage de lecteurs réseau

### Supervision

* **Zabbix** : monitoring uniquement
* **Équipements supervisés** :

  * pfSense
  * Contrôleurs de domaine



## Structure du projet

```arduino
IT Resilience & Monitoring Lab/
│
├── 01-diagrams/
│   ├── global-topology.png
│   ├── site-a.png
│   └── site-b.png
│
├── docs/
│   ├── 01-environnement.md
│   ├── 02-pfsense.md
│   ├── 03-active-directory.md
│   ├── 04-gpo.md
│   ├── 05-zabbix.md
│   └── 06-tests.md
│
├── configs/
│   ├── pfsense/
│   │   ├── rules.md
│   └── ad/
│       ├── ou-structure.md
│
└── screenshots/
│   ├── pfsense/
│   ├── ad/
│   ├── zabbix/
└── README.md
```

## Documentation

Chaque partie du lab est documentée de manière progressive :

- `docs/` : documentation technique détaillée
- `configs/` : règles firewall et structure AD de référence
- `screenshots/` : preuves visuelles ciblées



## Scénarios démontrés

- Communication inter-sites sécurisée
- Réplication Active Directory via VPN
- Application des GPO sur postes clients
- Accès VPN administrateur
- Supervision des équipements critiques


## 🎓 Objectif pédagogique & recrutement

Ce projet met en avant :

- Une **vision globale d’un SI**
- La capacité à **concevoir, sécuriser et exploiter** une infrastructure
- Une approche **structurée et documentée**
- Des compétences directement **présentables en entretien technique**

👉 Projet conçu pour être partagé sur **GitHub**, **LinkedIn** et utilisé comme support en entretien.


## Project Status
🚧 Work in Progress

This homelab project is being developed progressively.   
New components and documentation are added regularly.

## 👤 Auteur

**Alex** – Technicien Systèmes et Réseaux | Support IT & Infrastructure 


Ce projet s’inscrit dans mon **Home Lab personnel**, où je conçois et teste des infrastructures IT afin d’approfondir mes compétences en supportr IT, en administration systèmes, réseaux et sécurité.

🔗 LinkedIn : https://linkedin.com/in/alex-byiringiro   
💻 GitHub : https://github.com/alex-byiringiro


