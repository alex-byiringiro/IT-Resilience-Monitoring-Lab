# Structure Active Directory – OU & Groupes


## Objectif
Déployer une arborescence AD claire, évolutive et orientée entreprise.


---


## Arborescence des OU  
```arduino
lab.lan
│
├── OU=Sites
│   │
│   ├── OU=Site-A
│   │   ├── OU=Users
│   │   ├── OU=Computers
│   │   └── OU=Servers
│   │
│   └── OU=Site-B
│       ├── OU=Users
│       ├── OU=Computers
│       └── OU=Servers
│
├── OU=Groups
│   ├── OU=Security
│   └── OU=Distribution
│
└── OU=Admins
    ├── OU=IT
    └── OU=Service-Accounts
```




## Groupes de sécurité (exemples)
- GRP-IT-Admins
- GRP-Users-SiteA
- GRP-Users-SiteB
- GRP-Servers-Admins




## Bonnes pratiques
- Séparation Users / Computers / Servers
- Groupes basés sur les rôles
- GPO liées au bon niveau OU
- Comptes de service isolés