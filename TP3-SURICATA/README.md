# TP 3 — Suricata IDS/IPS (Partie 1)

> **Module :** Intrusion Detection Systems (IDS)  
> **Classe :** ING-5-J-SSIR (2026–2027)  
> **Environnement :** WSL2 Ubuntu 26.04.1 LTS / Suricata 8.0.3 RELEASE / Emerging Threats Open

## Structure du dépôt

```text
TP3-SURICATA/
├── README.md                          ← Ce fichier
├── rapport/
│   └── rapport.md                     ← Rapport complet en français (lisible sur GitHub)
└── screenshots/
    ├── 01_installation_et_fichiers.png
    ├── 02_configuration_yaml.png
    ├── 03_suricata_update.png
    ├── 04_validation_suricata_T.png
    ├── 05_service_et_logs.png
    └── 06_detection_blacksun.png
```

## Résumé

Ce TP couvre l'installation, la configuration et l'utilisation de **Suricata** en mode **IDS passif** sous WSL2 Ubuntu 26.04 :

- Installation de **Suricata 8.0.3** et vérification de `/etc/suricata/` et `/var/log/suricata/`
- Configuration de `suricata.yaml` (`HOME_NET`, `EXTERNAL_NET`, `af-packet` sur `eth0`, désactivation GRO/LRO via `ethtool`)
- Mise à jour du jeu de règles **Emerging Threats Open** via `suricata-update` (`69 568` lignes, `53 593` règles actives)
- Validation complète avec `suricata -c /etc/suricata/suricata.yaml -T -v`
- Démarrage du service `suricata` et vérification des logs
- Analyse détaillée de la règle **BlackSun** (`sid:2008983`), génération de trafic HTTP via `curl -A "BlackSun"` et capture de l'alerte dans `/var/log/suricata/fast.log`

📄 **[Lire le rapport complet →](rapport/rapport.md)**

