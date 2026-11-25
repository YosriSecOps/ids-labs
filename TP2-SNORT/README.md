# TP 2 — SNORT NIDS : Installation, Configuration et Détection d'Intrusions

> **Module :** Intrusion Detection Systems (IDS)  
> **Classe :** ING-5-J-SSIR (2026–2027)  
> **Environnement :** WSL2 Ubuntu 26.04.1 LTS / SNORT 2.9.20 GRE / PCRE 8.45 / DAQ 2.0.7

## Structure du dépôt

```text
TP2-SNORT/
├── README.md                          ← Ce fichier
├── rapport/
│   └── rapport.md                     ← Rapport complet en français (lisible sur GitHub)
├── rapport_TP_SNORT.docx              ← Rapport format Word
├── rapport_TP_SNORT.pdf               ← Rapport format PDF
├── screenshots/                       ← Captures d'écran réelles WSL
│   ├── 01_environment/
│   ├── 02_installation/
│   ├── 03_configuration/
│   ├── 04_icmp/
│   ├── 05_png/
│   ├── 06_gif/
│   └── 07_visa/
├── configs/                           ← Fichiers snort.conf, local.rules et sauvegardes
├── evidence/                          ← Sorties brutes des commandes et tests
└── execution_log.txt                  ← Journal d'exécution complet
```

## Résumé

Ce TP couvre l'installation complète et l'utilisation de **SNORT 2.9.20** en mode NIDS sous WSL2 Ubuntu 26.04 :

- Compilation et installation depuis les sources (`PCRE 8.45`, `libtirpc-dev`, `-std=gnu17 -fcommon` pour GCC 15)
- Configuration de `/etc/snort/snort.conf` avec les **Community Rules** officielles (`4 054` lignes) et validation via `snort -T`
- Détection **ICMP** en temps réel sur `eth0` (`ping 8.8.8.8`)
- Détection de transfert de fichiers **PNG** (`89 50 4E 47 0D 0A 1A 0A`, paquet 109 de `with_png.pcap` rejoué avec `tcpreplay`)
- Détection de transfert de fichiers **GIF** (`GIF87a`/`GIF89a`, paquets 28, 62, 69, 76 de `with_png.pcap`)
- Détection de numéros **Visa en clair** via **PCRE** (paquet 15 de `email_cc2.pcap`)
- Réponses aux questions théoriques (Exercices 21, 32, 33 et 34)

📄 **[Lire le rapport complet →](rapport/rapport.md)**
