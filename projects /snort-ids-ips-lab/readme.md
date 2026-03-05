# 🔐 IDS / IPS Lab – Intrusion Detection and Prevention with Snort

## 🎯 Objectif du projet

L’objectif de ce projet est de mettre en place un système **IDS/IPS (Intrusion Detection and Prevention System)** avec **Snort** afin de surveiller le trafic réseau et détecter des activités malveillantes.

Ce laboratoire permet de comprendre comment les entreprises utilisent les IDS/IPS pour identifier les attaques réseau et protéger leurs infrastructures.

---

# 🧠 Architecture du laboratoire

Le laboratoire est composé de plusieurs machines virtuelles :

* **Kali Linux** : machine d’attaque utilisée pour simuler des attaques
* **Serveur Snort** : système IDS/IPS chargé d’analyser le trafic réseau
* **Machine cible** : serveur ou système surveillé

Le trafic réseau est analysé par Snort afin de détecter des comportements suspects.

---

# ⚙️ Configuration de Snort

Snort a été installé et configuré sur un système Linux.

Des règles personnalisées ont été ajoutées dans le fichier :
```
/etc/snort/rules/local.rules
```

Ces règles permettent de détecter différents types d’activités suspectes sur le réseau.

---

# 🛡️ Règles IDS / IPS implémentées

Plusieurs règles personnalisées ont été créées pour détecter différentes attaques.

### 1️⃣ Détection de Ping ICMP

Détection des scans réseau utilisant ICMP.
```
alert icmp any any -> $HOME_NET any (msg:"ALERTE - Ping ICMP detecte vers le reseau interne";)
```

---

### 2️⃣ Détection de requêtes HTTP

Surveillance des accès HTTP vers le serveur.

```
alert tcp any any -> $HOME_NET 80 (msg:"ALERTE - Requete HTTP detectee sur le serveur";)
```

---

### 3️⃣ Détection de tentatives SSH

Détection des tentatives de connexion SSH.

```
alert tcp any any -> $HOME_NET 22 (msg:"ALERTE - Tentative de connexion SSH detectee";)
```

---

### 4️⃣ Détection de scan de ports

Identification des scans de ports effectués par un attaquant.

```
alert tcp any any -> $HOME_NET any (msg:"ALERTE - Scan de ports detecte - Activite suspecte";)
```

---

### 5️⃣ Détection d’attaque DDoS

Détection de trafic anormal pouvant correspondre à une attaque DDoS.

```
alert tcp any any -> $HOME_NET any (msg:"ALERTE - Attaque DDoS detectee - Trafic anormal";)
```

---

# 🔎 Tests réalisés

Plusieurs attaques ont été simulées depuis Kali Linux afin de tester le système de détection :

* Scan réseau avec **Nmap**
* Ping ICMP
* Tentatives de connexion SSH
* Requêtes HTTP

Snort a détecté ces activités et généré des **alertes en temps réel**.

---

# Captures du projet

### Configuration des règles Snort
<img width="892" height="447" alt="Capture d&#39;écran 2025-08-20 230204" src="https://github.com/user-attachments/assets/e75abf49-237e-4d77-9f95-af702022d7c5" />



### Détection d'attaque

<img width="583" height="444" alt="Capture d&#39;écran 2025-08-17 062326" src="https://github.com/user-attachments/assets/cdd1ad26-05ab-4bfe-b1e2-dc1701f34078" />

<img width="801" height="260" alt="Capture d&#39;écran 2025-08-20 231401" src="https://github.com/user-attachments/assets/e8cd3654-f35c-45d1-8525-73b1eb094a77" />

---

# 🏢 Utilité en entreprise

Les systèmes IDS/IPS sont largement utilisés dans les entreprises pour :

* surveiller le trafic réseau
* détecter les attaques
* analyser les incidents de sécurité
* renforcer la sécurité des infrastructures

Les alertes générées peuvent ensuite être envoyées vers un **SIEM** pour une analyse centralisée.

---

# 🛠️ Technologies utilisées

* Snort
* Linux
* Kali Linux
* Nmap
* IDS / IPS
* Analyse du trafic réseau
