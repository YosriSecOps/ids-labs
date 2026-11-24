# TP 1 — OSSEC HIDS : Installation et Configuration

> **Module :** Intrusion Detection Systems (IDS)  
> **Environnement :** WSL2 Ubuntu / Apache 2.4 / PHP 8.5 / OSSEC HIDS v3.1.0

## Structure du dépôt

```
TP1-OSSEC/
├── README.md                          ← Ce fichier
├── rapport/
│   └── rapport.md                     ← Rapport complet en français
└── screenshots/
    ├── 01_installation_dependances.png
    ├── 02_telechargement_ossec.png
    ├── 03_installation_ossec.png
    ├── 04_demarrage_ossec.png
    ├── 05_interface_web_ossec.png
    ├── 06_configuration_apache.png
    ├── 07_alertes_ossec.png
    └── 08_dashboard_ossec_wui.png
```

## Résumé

Ce TP couvre l'installation complète d'**OSSEC HIDS v3.1.0** en mode local sur Ubuntu, incluant :

- Installation et compilation depuis les sources (avec correction de compatibilité GCC 15)
- Démarrage et vérification des 6 démons OSSEC
- Déploiement de l'interface web **ossec-wui** avec Apache 2 (avec corrections PHP 8.5)
- Configuration d'un VirtualHost Apache pour `http://ossec.example.com`
- Vérification des alertes en temps réel

📄 **[Lire le rapport complet →](rapport/rapport.md)**
