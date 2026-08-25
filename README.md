# 🤖 Robot Autonome Raspberry Pi

> Robot mobile avec pilotage manuel et autonome, détection d'obstacles, streaming vidéo et ordonnancement de tâches temps réel.

![Raspberry Pi](https://img.shields.io/badge/Raspberry%20Pi%204-A22846?style=flat-square&logo=Raspberry%20Pi&logoColor=white)
![C](https://img.shields.io/badge/C-00599C?style=flat-square&logo=c&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)

---

## 🎯 Objectif

Construire un **robot mobile intelligent** sur Raspberry Pi capable de :
- 🕹️ **Pilotage manuel** (télécommande)
- 🤖 **Pilotage autonome** avec **détection d'obstacles**
- 🎥 **Streaming vidéo** en direct
- ⏱️ **Ordonnancement de tâches temps réel**

## 🔧 Matériel utilisé

| Composant | Rôle |
|---|---|
| **Raspberry Pi 4** | Cerveau du robot |
| **Moteurs DC** | Propulsion |
| **Pont en H** | Contrôle direction/ vitesse des moteurs |
| **Capteur ultrasonique HC-SR04** | Détection d'obstacles |
| **Servomoteur** | Orientation / rotation |
| **Caméra** | Vision et streaming vidéo |

## 🛠️ Logiciel & techniques

- **Langages** : C, Python
- **Linux** : gestion système, pilotes, services
- **pigpio** : contrôle des GPIO
- **OpenCV** : traitement d'image et vision
- **Ordonnancement de tâches temps réel** : tâches périodiques/apériodiques, préemption, **RM (Rate Monotonic)**, **EDF**, files de priorité
- **Architecture serveur** : WebSocket pour le contrôle et le streaming

## ✨ Fonctionnalités

- 🔄 Modes manuel / autonome commutables
- 🚧 Évitement d'obstacles par capteur ultrasonique
- 📹 Streaming vidéo temps réel
- ⏰ Ordonnancement temps réel des tâches (capteurs, moteurs, réseau, vision)

## 📁 Structure du projet

```
├── src/
│   ├── motor/          # Contrôle moteurs (pont en H, PWM)
│   ├── sensors/        # Capteur ultrasonique HC-SR04
│   ├── vision/         # Caméra, OpenCV
│   ├── scheduler/      # Ordonnancement temps réel (RM, EDF)
│   └── server/         # Serveur WebSocket, streaming
├── docs/               # Schémas de câblage, documentation
└── README.md
```

## 🚀 Installation

```bash
git clone https://github.com/alphonse32/raspberry-pi-robot.git
cd raspberry-pi-robot
# Activer pigpio
sudo systemctl enable pigpiod
# Compiler les modules C
make
# Lancer le serveur principal
python3 src/server/main.py
```

## 📸 Démos & captures

*(Ajoutez ici : photos du robot, schéma de câblage, extrait vidéo du streaming, démo de détection d'obstacles)*

---

## 🆕 Projet complémentaire : Robot suiveur de ligne (Deep Learning)

Robot capable de **suivre une trajectoire/ligne au sol** à l'aide d'une **caméra et du Deep Learning** (vision par ordinateur + réseau de neurones).

---

## 📬 Contact

**Alphonse Sanou** — [LinkedIn](https://www.linkedin.com/in/alphonse-sanou) · [GitHub](https://github.com/alphonse32)
