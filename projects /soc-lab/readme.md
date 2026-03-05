

# 🛡️ SOC Lab – Détection d'Incidents avec IDS et SIEM

## 🎯 Objectif

Mettre en place un laboratoire SOC permettant de détecter des activités suspectes sur un réseau grâce à un système de détection d'intrusion (IDS) et un SIEM pour la centralisation et l'analyse des logs de sécurité.

---

## 🏢 Utilité en entreprise

Dans une entreprise, un SOC (Security Operations Center) surveille les systèmes d'information afin de détecter et analyser les menaces de sécurité.

Le SIEM permet de centraliser les logs provenant de plusieurs équipements et applications afin d'identifier des comportements suspects et faciliter la réponse aux incidents.

---

## 🛠️ Technologies utilisées

- Linux
- IDS (Snort / Suricata)
- SIEM
- Analyse des logs
- Environnement réseau de laboratoire

---

## 🧠 Architecture du laboratoire

Dans ce laboratoire :

- un **IDS surveille le trafic réseau**
- lorsqu'une activité suspecte est détectée, **une alerte est générée**
- ces alertes sont **envoyées vers le SIEM**
- le **SIEM centralise et analyse les événements de sécurité**

Le SIEM peut également récupérer les logs provenant de plusieurs sources :

- IDS / IPS  
- serveurs Linux / Windows  
- équipements réseau (routeurs, firewalls)  
- applications et services  

Cette centralisation permet aux analystes SOC d'avoir une **vision globale de la sécurité du système d'information**.

---

## ⚙️ Étapes du projet

1. Mise en place d'un environnement réseau de laboratoire
2. Installation et configuration de l'IDS
3. Génération de trafic réseau suspect
4. Détection des alertes par l'IDS
5. Transmission des alertes vers le SIEM
6. Centralisation et analyse des logs dans le SIEM

---

Ma realisation 

<img width="500" height="500" alt="Capture d&#39;écran 2025-08-21 113711" src="https://github.com/user-attachments/assets/1fb49abe-e19a-440f-853d-03978128e700" />

<img width="500" height="500" alt="Capture d&#39;écran 2025-08-21 114021" src="https://github.com/user-attachments/assets/2bb8db6f-084f-4dc2-baf0-e26161d2d909" />

<img width="500" height="500" alt="Capture d&#39;écran 2025-08-22 200922" src="https://github.com/user-attachments/assets/473fbda8-8b4f-43be-9c7b-7c22bd3e107d" />


## 📸 Captures du projet

### Interface du SIEM Splunk

Cette capture montre l'interface principale de **Splunk Enterprise**, utilisé comme SIEM dans ce laboratoire.

Le SIEM permet de :

- collecter les logs provenant de différentes sources
- centraliser les événements de sécurité
- analyser les alertes générées par les systèmes de sécurité

Dans ce laboratoire, le SIEM récupère les logs provenant notamment de l'IDS **Snort** afin d'analyser les événements de sécurité.

---

### Tableau de surveillance des alertes

Dans cette capture, on observe un **dashboard de supervision des alertes Snort dans Splunk**.

Ce tableau affiche en temps réel plusieurs informations importantes :

- la **date et l'heure de l'événement**
- l'**adresse IP source**
- l'**adresse IP de destination**
- le **protocole utilisé**
- le **message d'alerte généré**
- le **niveau de priorité de l'alerte**

Dans mon laboratoire, j'ai créé **plusieurs règles de détection dans l'IDS Snort** afin de détecter différents types d'activités suspectes.

Par exemple :

- détection de **scan réseau**
- détection de **tentatives de connexion SSH**
- détection de **trafic ICMP suspect**
- simulation d'une **attaque DDoS**

Lorsque ces règles sont déclenchées, l'IDS génère une alerte qui est ensuite **envoyée au SIEM Splunk pour analyse et visualisation dans le dashboard**.

---

### État du système de surveillance

Cette capture montre l'état du système de surveillance.

Deux états peuvent apparaître dans le dashboard :

- **NORMAL – Rien à signaler** : aucun événement critique détecté
- **CRITIQUE** : une activité suspecte ou une attaque a été détectée

Cela permet aux analystes SOC d'identifier rapidement les incidents de sécurité et de lancer les actions de réponse appropriées.

<img width="500" height="500" alt="Capture d&#39;écran 2025-08-25 204519" src="https://github.com/user-attachments/assets/cb132ae0-f1f9-4feb-8c80-dc584558f5b5" />


<img width="500" height="500" alt="Capture d&#39;écran 2025-08-26 150341" src="https://github.com/user-attachments/assets/b3fadc7f-4cf0-46cb-9514-c7151e0e38e7" />


### Analyse des protocoles et des alertes détectées

Cette section du dashboard présente une visualisation des **protocoles réseau impliqués dans les alertes de sécurité** ainsi que les **types d’attaques les plus fréquentes** détectées dans l’environnement de laboratoire.

Le premier graphique montre la **répartition des protocoles utilisés lors des activités suspectes**, notamment :
- **TCP** : protocole le plus utilisé dans les attaques détectées (ex : scans de ports ou tentatives de connexion).
- **ICMP** : utilisé dans certains tests de connectivité ou tentatives de reconnaissance réseau.
- **UDP** : utilisé dans certains scénarios d’attaque ou de trafic anormal.

Le second graphique présente le **Top des alertes générées par l’IDS Snort**, notamment :
- **Scan de ports détecté – activité suspecte**
- **Tentative de connexion SSH détectée**
- **Ping ICMP vers le réseau interne**
- **Trafic anormal pouvant indiquer une attaque DDoS**
- **BAD-TRAFFIC (trafic suspect entre la même source et destination)**

Ces visualisations permettent aux analystes SOC d’identifier rapidement les **types d’attaques les plus fréquents et les protocoles réseau les plus utilisés par les activités malveillantes**, facilitant ainsi l’analyse et la réponse aux incidents.


<img width="1305" height="538" alt="Capture d&#39;écran 2025-08-31 130919" src="https://github.com/user-attachments/assets/42d3734d-7d63-4509-8d25-b49d6f6c00eb" />

