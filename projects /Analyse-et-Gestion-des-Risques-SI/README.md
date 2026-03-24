# 📋 Analyse et Gestion des Risques SI – SO-EMBALLAGE

## 🎯 Objectif du projet

Ce projet applique deux méthodes de référence en cybersécurité française — **MEHARI** et **EBIOS Risk Manager** —
à un cas réel d'entreprise : SO-EMBALLAGE, société de distribution B2B (33,8M€ de CA, 185 salariés, région parisienne).

L'objectif est d'identifier, évaluer et traiter les risques pesant sur le système d'information de l'entreprise,
en produisant un plan d'action concret et chiffré.

---

## 🧠 Méthode MEHARI

MEHARI (MEthode Harmonisée d'Analyse des RIsques) est développée par le CLUSIF et conforme à l'ISO/IEC 27005.

Ce projet comprend :

- Cartographie des actifs essentiels (SAP ERP, serveur Linux, données clients, application métier)
- Audit de maturité sécurité sur 9 domaines — score global : **1,2/4 (niveau Initial)**
- Identification de **20 scénarios de risques** cotés potentialité/impact (échelle 1-4)
- 4 risques **CRITIQUES** identifiés dont ransomware (4/4) et panne serveur SPOF (3/4)
- Évaluation des impacts financiers, opérationnels, juridiques et réputationnels

---

## 🔍 Méthode EBIOS Risk Manager

EBIOS RM est la méthode de référence de l'**ANSSI** pour la gestion des risques numériques.

Ce projet suit les **5 ateliers complets** :

- **Atelier 1** — Cadrage et socle de sécurité : périmètre, valeurs métier, biens supports
- **Atelier 2** — Sources de risques : 5 sources identifiées (cybercriminels, concurrents, employés malveillants, prestataires compromis)
- **Atelier 3** — Scénarios stratégiques : ransomware via phishing (CRITIQUE), vol de données web (CRITIQUE), espionnage supply chain (MAJEUR)
- **Atelier 4** — Scénario opérationnel détaillé en **10 phases techniques** : spear-phishing → Cobalt Strike → PrintNightmare (CVE-2021-34527) → Pass-the-Hash → mouvement latéral → LockBit 3.0
- **Atelier 5** — Plan de traitement : mesures techniques, organisationnelles et humaines avec analyse coûts/bénéfices

---

## 📊 Résultats clés

| Indicateur | Valeur |
|---|---|
| Maturité sécurité globale | 1,2/4 (Initial) |
| Scénarios de risques identifiés | 20 |
| Risques critiques | 4 |
| Exposition financière cumulée | > 3 000 000 EUR |
| Investissement plan d'action (2 ans) | 385 000 EUR |
| ROI estimé | 7:1 sur 2 ans |

---

## 🛡️ Plan d'action recommandé

- **Phase 1 (0-3 mois)** — PRA/PCA, EDR, sensibilisation, RSSI
- **Phase 2 (3-9 mois)** — Segmentation réseau VLAN, MFA, patch management, WAF
- **Phase 3 (9-18 mois)** — Conformité RGPD, SIEM, PSSI, exercices de crise

---

## 📄 Rapport complet

Le rapport détaillé est disponible ici :
**GROUPE_8_Analyse_Risques_SO_EMBALLAGE.pdf**
[GROUPE 8 Analyse Risques SO EMBALLAGE (1).pdf](https://github.com/user-attachments/files/26216472/GROUPE.8.Analyse.Risques.SO.EMBALLAGE.1.pdf)

---

## 🛠️ Frameworks & Méthodes utilisés

- MEHARI (CLUSIF)
- EBIOS Risk Manager (ANSSI)
- ISO/IEC 27001 & 27005
- RGPD / GDPR
- MITRE ATT&CK Framework
- NIST Cybersecurity Framework

---

>  Projet réalisé dans le cadre du Master 1 – Atelier Cyber & E-réputation | Ingetis Paris | Février 2026
