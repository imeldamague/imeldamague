# 🌐 Network Architecture Project – ALPHANET

## 🎯 Objectif du projet

Ce projet consiste à concevoir et sécuriser l’infrastructure réseau d’une entreprise multi-sites appelée **ALPHANET**.

L’entreprise possède trois sites géographiques :

- Paris (siège social)
- Nantes (agence régionale)
- Lyon (site technique)

L’objectif est de permettre la communication sécurisée entre ces sites tout en appliquant des mécanismes de sécurité réseau utilisés dans les entreprises.

Ce projet a été réalisé avec **Cisco Packet Tracer**.

---

# 🧠 Architecture réseau

L’infrastructure repose sur une architecture **Hub-and-Spoke**.

- Paris agit comme **Hub central**
- Nantes et Lyon sont des **Spokes**

Tous les flux inter-sites passent par le site central de Paris.

Cette architecture permet :

- la centralisation de la sécurité
- une gestion simplifiée des tunnels VPN
- une meilleure évolutivité du réseau

---

# 🌍 Infrastructure multi-sites

Chaque site possède :

- un routeur de bordure (**R-EDGE**) pour la connexion WAN et les tunnels VPN
- un routeur interne (**R-LAN**) pour le routage local
- des switches Layer 3 pour le routage inter-VLAN
- des switches Layer 2 pour les utilisateurs

Cette séparation améliore la sécurité et la performance du réseau. :contentReference[oaicite:0]{index=0}

---

# 🔐 Segmentation réseau avec VLAN

Le réseau est segmenté en plusieurs VLAN afin d'isoler les différents types d'équipements :

- VLAN 10 : Utilisateurs
- VLAN 20 : Serveurs
- VLAN 30 : Imprimantes
- VLAN 40 : NAS
- VLAN 50 : Tests
- VLAN 99 : Administration

La segmentation permet :

- d'isoler les ressources critiques
- de réduire le trafic réseau
- d'appliquer des règles de sécurité spécifiques. :contentReference[oaicite:1]{index=1}

---

# 🛡️ Mise en place des ACL (Access Control Lists)

Plusieurs **ACL de sécurité** ont été configurées pour contrôler les communications entre VLAN.

Exemple :

- les utilisateurs ne peuvent pas accéder directement au NAS
- seuls les serveurs et les administrateurs peuvent accéder aux ressources sensibles

Cette approche applique le principe de **moindre privilège**. :contentReference[oaicite:2]{index=2}

---

# 🔒 Sécurisation des communications inter-sites

La communication entre les sites est sécurisée grâce à des **tunnels VPN IPsec**.

Caractéristiques :

- chiffrement AES
- authentification SHA
- tunnels sécurisés entre Paris-Nantes et Paris-Lyon

Les données échangées entre les sites sont ainsi protégées contre les interceptions. :contentReference[oaicite:3]{index=3}

---

# 📡 Routage réseau

Deux méthodes de routage ont été utilisées :

### OSPF
Utilisé pour le routage interne dans chaque site.

### Routes statiques
Utilisées pour le routage entre les sites.

Cette combinaison permet une gestion simple et efficace du réseau multi-sites.

---

# 🧪 Tests réalisés

Plusieurs tests ont été effectués pour valider l'infrastructure :

- communication entre les sites via VPN
- vérification du routage
- tests d’accès aux ressources
- blocage des accès non autorisés par ACL

Les tests confirment le bon fonctionnement de l’architecture Hub-and-Spoke et des tunnels VPN sécurisés. :contentReference[oaicite:4]{index=4}

---

# 🛠️ Technologies utilisées

- Cisco Packet Tracer
- VLAN
- OSPF
- ACL
- VPN IPsec
- Routage statique
- Architecture Hub-and-Spoke

---

# 📸 Captures du projet

### Topologie réseau

<img width="1030" height="774" alt="Capture d&#39;écran 2026-01-09 022944" src="https://github.com/user-attachments/assets/62b33179-ac26-45df-bbb5-0f1eb099ab09" />


RAPPORT 

[RAPPORT RESAU-AGUEDIA-IMELDA.pdf](https://github.com/user-attachments/files/25781679/RAPPORT.RESAU-AGUEDIA-IMELDA.pdf)




# 🏢 Utilité en entreprise

Cette architecture peut être utilisée par les entreprises possédant plusieurs sites.

Elle permet :

- de sécuriser les communications inter-sites
- de segmenter le réseau
- de protéger les ressources critiques
- de centraliser la sécurité réseau

---

# 👨‍💻 Auteur

**AGUEDIA MAGUE Imelda Raidelle**  
Master 1 Cybersécurité – INGETIS
