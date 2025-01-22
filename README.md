# MOBILedit Forensic Express Pro

**MOBILedit Forensic Express Pro** est un logiciel d'analyse avancé conçu pour l'extraction, l'analyse et la gestion des données provenant de téléphones mobiles et d'autres appareils connectés. Il est principalement utilisé par les experts en cybersécurité, les enquêteurs judiciaires, les forces de l'ordre et les analystes en criminalistique numérique pour recueillir des preuves numériques dans le cadre d'enquêtes.

## 1 Caractéristiques principales

### 1.1 **Extraction de données**
- Récupère des données comme les appels, messages, contacts, fichiers multimédias, applications (WhatsApp, Messenger, etc.) et historique de navigation.
- Compatible avec une grande variété d'appareils et de systèmes d'exploitation, y compris Android et iOS.

### 1.2 **Analyse avancée**
- Recherche et analyse des données supprimées.
- Génération de rapports détaillés pour être utilisés comme preuves dans des enquêtes.
- Comparaison des données entre plusieurs appareils.

### 1.3 **Décryptage et contournement de sécurité**
- Capacité à contourner les mots de passe, les verrouillages d'écran et d'autres mécanismes de sécurité.
- Extraction de données à partir d'appareils chiffrés ou protégés.

### 1.4 **Support multi-connexions**
- Compatible avec des connexions via USB, Wi-Fi, Bluetooth, ou encore via des sauvegardes iCloud.

### 1.5 **Utilisation médico-légale**
- Certifié pour fournir des données fiables et admissibles dans des contextes légaux.
- Assure une traçabilité et un traitement sécurisé des données.

### 1.6 **Interface intuitive**
- Offre une interface utilisateur simple, permettant aux utilisateurs de naviguer facilement entre les fonctionnalités (par exemple, "Phone data preview" ou "Hack phone").

## Domaines d'utilisation
- **Enquête criminelle** : Analyse des appareils suspects pour trouver des preuves.
- **Cybersécurité** : Étude des appareils infectés ou compromis pour identifier les attaques.
- **Récupération de données** : Aide à la récupération de données personnelles ou perdues.
- **Audit légal** : Évaluation des appareils pour identifier des infractions ou des comportements suspects.

# Introduction à l'Analyse Statique et Dynamique de MOBILedit Forensic Express Pro
## Contexte et Enjeux
Dans le domaine de la forensique numérique mobile, les outils d'extraction et d'analyse de données jouent un rôle crucial dans les investigations numériques. MOBILedit Forensic Express Pro s'est imposé comme l'un des acteurs majeurs de ce secteur, offrant des capacités avancées d'acquisition et d'analyse de données provenant d'appareils mobiles. Dans un contexte où la sécurité et la fiabilité des preuves numériques sont primordiales, la compréhension approfondie du fonctionnement de tels outils devient essentielle.
La complexité croissante des systèmes mobiles et la diversité des données qu'ils contiennent nécessitent des outils forensiques sophistiqués. MOBILedit Forensic Express Pro répond à ces besoins en proposant une suite complète de fonctionnalités d'extraction et d'analyse. Cependant, cette complexité soulève des questions importantes concernant la fiabilité, la sécurité et l'intégrité des processus d'acquisition de données.
## Présentation de l'Étude
Cette étude technique approfondie de MOBILedit Forensic Express Pro s'inscrit dans une démarche d'évaluation rigoureuse des outils forensiques. Notre analyse vise à décortiquer les mécanismes internes de l'application pour comprendre non seulement ses capacités déclarées, mais aussi ses limites potentielles et ses implications en matière de sécurité.
## Portée de l'Analyse
Notre investigation se concentre sur plusieurs aspects critiques :
L'architecture logicielle de l'application, notamment :

1. Les composants principaux et leurs interactions
2. Les mécanismes de traitement des données
3. Les protocoles de communication utilisés
4. Les mesures de sécurité implémentées
5. Les dépendances externes et leurs implications

Les processus d'acquisition de données, incluant :

1. Les méthodes d'extraction logiques
2. Les protocoles de communication avec les appareils mobiles
3. Les mécanismes de validation et d'intégrité des données
4. Les formats de stockage et d'export des données extraites

## Méthodologie d'Analyse
Pour atteindre nos objectifs, nous avons adopté une approche bidirectionnelle combinant **analyse statique et dynamique**. Cette méthodologie holistique permet d'obtenir une compréhension complète du logiciel sous tous ses aspects.



# 2. Analyse Dynamique de MOBILedit Forensic Express Pro

## 2.1 Introduction

L'analyse dynamique représente une méthodologie sophistiquée permettant de comprendre le comportement des logiciels en examinant leurs caractéristiques d'exécution. Appliquée à MOBILedit Forensic Express Pro, cette approche révèle des informations cruciales sur la façon dont l'outil forensique interagit avec les appareils mobiles, gère l'extraction des données et communique avec le système hôte. Ce guide complet explore les subtilités de la conduite d'une analyse dynamique en utilisant trois outils puissants : **Procmon**, **Wireshark** (avec **USBPcap**), **Regshot**, et **Procdot**.

##  2.2 Préparation de l'Analyse Dynamique

### 2.2.1 Configuration de l'Environnement

Un environnement d'analyse correctement configuré est essentiel pour obtenir des résultats précis et fiables. Les composants suivants doivent être soigneusement préparés :

#### 2.2.2 Configuration de la Machine Virtuelle


L'utilisation d'une machine virtuelle offre plusieurs avantages :
- Isolation du système hôte pour éviter la contamination croisée
- Possibilité de créer des instantanés avant et après l'analyse
- Capacités de réinitialisation facile si le système devient instable
- Accès réseau contrôlé pour la surveillance des communications

Spécifications recommandées pour la VM :
- Minimum 4 Go de RAM allouée
![image](https://github.com/user-attachments/assets/3939cbe7-d372-44d9-91e2-5e84e302a9cb)

- Au moins 50 Go d'espace de stockage
- Capacité de transmission USB activée
- Adaptateur réseau en mode pont
  ![image](https://github.com/user-attachments/assets/359f5bb2-d6cc-4e97-b98a-85a852d435ed)


#### 2.2.3 Exigences d'Installation des Outils

Chaque outil d'analyse nécessite une configuration spécifique :

**Configuration de Procmon :**
![image](https://github.com/user-attachments/assets/e0fd56e8-5605-4c4b-a04d-602e2388b0d5)

- Dernière version de la Suite Sysinternals
- Privilèges administrateur activés
- Chemins des symboles appropriés configurés
- Journalisation au démarrage activée pour une analyse complète

**Configuration de Wireshark & USBPcap :**
![image](https://github.com/user-attachments/assets/7a508290-3a12-44d3-8710-70f97eea94e6)

- Dernière version stable de Wireshark
- Pilote USBPcap correctement installé
- Privilèges de capture appropriés configurés
- Analyseurs de protocoles pertinents activés

**Prérequis pour Procdot :**


![image](https://github.com/user-attachments/assets/ffdd19f1-4827-4548-9ef8-98e9ed97661e)

- Dernière version installée
- Dépendances GraphViz configurées
- Ressources système suffisantes allouées
- Framework .NET compatible installé
  
**Configuration de Regshot :**


![image](https://github.com/user-attachments/assets/3e259565-bbfd-44d9-834b-9f9d2eb7aa97)

- Version stable 1.9.0 ou supérieure installée
- Exécution en tant qu'administrateur activée
- Mode de comparaison détaillée activé
- Répertoires d'exclusion configurés (temp, cache)
- Paramètres de capture de registre optimisés
- Dossier de sortie des rapports défini
  
### 2.2.4 Préparation des Appareils de Test

Le choix et la préparation des appareils de test impactent significativement la qualité de l'analyse :

**Exigences pour les Appareils Mobiles :**
- État de réinitialisation d'usine recommandé
- Données de test connues installées
- Options développeur activées
- Débogage USB activé
- Installation correcte des pilotes vérifiée

## 2.2.4 Analyse Avancée avec Procmon

### Capacités Approfondies de Procmon

Les capacités de surveillance de Procmon s'étendent au-delà des appels système de base :

**Surveillance du Système de Fichiers :**
- Opérations de Création, Lecture, Écriture, Suppression
- Modifications des attributs de fichiers
- Énumération des répertoires
- Transactions du système de fichiers
- Accès aux flux de données alternatifs

**Analyse du Registre :**
- Création et suppression de clés
- Modifications des valeurs
- Énumération des clés
- Transactions du registre
- Modifications des descripteurs de sécurité

**Suivi de l'Activité des Processus :**
- Création et terminaison des threads
- Chargement des modules
- Relations entre processus
- Opérations sur les handles
- Changements de contexte de sécurité

###  Méthodologie Avancée pour Procmon

Le processus d'analyse peut être optimisé grâce à une préparation minutieuse :

**Configuration Pré-Capture :**
1. Configurer les tailles de buffer appropriées
2. Mettre en place des règles de filtrage avancées
3. Activer les traces de pile
4. Configurer les chemins des symboles
5. Préparer les emplacements de journalisation

**Techniques de Filtrage Avancées :**
La création de filtres sophistiqués aide à se concentrer sur les données pertinentes :
```plaintext
Process Name contains MOBILedit
```
![pasted_image002](https://github.com/user-attachments/assets/65d4143d-5b3f-47ed-b61d-2b888fa103ca)

### 2.3 Analyse des Résultats

L'interprétation des données capturées nécessite une approche systématique :

**Identification des Modèles :**
- Séquences d'opérations répétées
- Accès aux ressources système
- Comportements anormaux ou inattendus
- Interactions avec d'autres processus

**Points d'Intérêt Particuliers :**
- Création de fichiers temporaires
- Modifications du registre persistantes
- Communications réseau
- Chargement de DLL externes

## 2.2.5 Analyse Approfondie avec Wireshark et USBPcap

###  Compréhension du Trafic USB

L'analyse du trafic USB révèle des informations cruciales sur la communication entre MOBILedit et l'appareil mobile :

**Types de Transferts USB :**
- Transferts de contrôle pour la configuration
- Transferts en masse pour les données
- Transferts d'interruption pour les événements
- Transferts isochrones pour les flux continus

**Protocoles de Communication :**
- MTP (Media Transfer Protocol)
- PTP (Picture Transfer Protocol)
- Protocoles propriétaires
- Communications de débogage

###  Méthodologie d'Analyse USB

Une approche structurée de l'analyse du trafic USB comprend :


![pasted_image009](https://github.com/user-attachments/assets/dcc3b958-38d5-42be-a8a8-9df0e77ca095)

**Phase de Capture :**
1. Identification des interfaces USB pertinentes
2. Configuration des filtres de capture
3. Synchronisation avec les actions de MOBILedit
4. Documentation des événements observés

**Analyse des Données :**
- Décodage des paquets USB
- Reconstruction des flux de données
- Identification des commandes et réponses
- Analyse des protocoles de haut niveau

## 2.2.6 Visualisation Avancée avec Procdot

### Exploitation Optimale de Procdot

Procdot offre des capacités puissantes de visualisation :

**Fonctionnalités Clés :**
- Représentation graphique des relations entre processus
- Visualisation temporelle des événements
- Cartographie des accès aux ressources
- Identification des dépendances

**Techniques d'Analyse :**
- Filtrage des événements non pertinents
- Regroupement logique des activités
- Identification des modèles comportementaux
- Documentation des flux de travail
Je vais ajouter une section complète sur Regshot après la partie Procmon et avant Wireshark, en gardant la même structure et le même niveau de détail :



## 2.2.7 Analyse Comparative avec Regshot

### Capacités et Fonctionnalités de Regshot

L'utilisation de Regshot permet une analyse comparative approfondie des changements système :

**Capture d'État Système :**
- Enregistrement complet de l'état du registre Windows
- Inventaire détaillé des fichiers et répertoires
- Documentation des permissions et attributs
- Suivi des modifications de taille et dates des fichiers
- Capture des variables d'environnement système

**Types de Modifications Tracées :**
- Ajouts et suppressions dans le registre
- Modifications des valeurs de registre existantes
- Création et suppression de fichiers
- Modifications de structure des répertoires
- Changements dans les droits d'accès

### Méthodologie d'Utilisation de Regshot

Une approche méthodique garantit des résultats précis et exploitables :

**Processus de Capture :**
1. Premier instantané avant l'installation ou l'exécution
2. Actions spécifiques sur le logiciel cible
3. Deuxième instantané après les modifications
4. Génération du rapport comparatif détaillé

**Configuration Optimale :**
- Définition des répertoires à surveiller
- Exclusion des dossiers temporaires
- Paramétrage de la profondeur d'analyse
- Sélection du format de rapport approprié
- Configuration des filtres de comparaison

### Analyse des Résultats Regshot

L'interprétation des rapports Regshot nécessite une analyse structurée :

**Catégorisation des Changements :**
- Modifications critiques du système
- Changements temporaires
- Installations de composants
- Modifications de configuration
- Traces résiduelles

**Points d'Attention Particuliers :**
- Modifications persistantes du registre
- Installation de nouveaux services
- Création de clés de démarrage automatique
- Modifications des paramètres système
- Installation de pilotes ou DLL


# Étude de cas : Analyse dynamique d'une acquisition des contacts via USB

## 1. Analyse du trafic USB avec Wireshark
![pasted_image025](https://github.com/user-attachments/assets/c14470f2-96ad-48f0-8d68-4fce3f0d2cb9)
![pasted_image024](https://github.com/user-attachments/assets/4eea7fbb-354c-45f6-ac0c-c439fc01882f)

### Observations générales
L’analyse des captures Wireshark met en évidence un trafic intensif entre l’ordinateur hôte et le périphérique mobile, majoritairement basé sur le protocole **USB Bulk Transfer**. Ce protocole est couramment utilisé pour transférer de grandes quantités de données de manière fiable, mais il ne garantit pas de chiffrement intrinsèque des données. 

Les multiples entrées « URB_BULK in » et « URB_BULK out » montrent une communication bidirectionnelle soutenue, ce qui est typique des opérations d’extraction ou de synchronisation des données. Chaque paquet présente une taille constante de **539 bytes**, suggérant un formatage standardisé des blocs de données échangés.

### Découverte critique : Absence de chiffrement
Un point d’inquiétude majeur réside dans le fait que les données semblent être transmises en clair. En analysant les paquets, on peut identifier des chaînes de texte lisibles telles que :
- **"android"** : une référence aux fichiers système Android ou aux données utilisateur.
- **"cursor"** : suggérant une extraction liée à des bases de données SQLite, souvent utilisées par les applications mobiles.
- **"telegram"** : une référence explicite à l’application de messagerie, indiquant que des informations sensibles peuvent être récupérées.

Cette absence de chiffrement expose les données à des risques importants, en particulier si le trafic est intercepté par un tiers malveillant disposant d’un accès physique ou réseau au bus USB.

### Analyse temporelle et comportemental
Les timestamps rapprochés des transmissions (par exemple : **83.714986, 83.713439**) confirment une extraction séquentielle automatisée. Cela indique que l’outil effectue une analyse systématique des composants du téléphone. Ces séquences répétitives peuvent également fournir des indices sur l'ordre des opérations effectuées par le logiciel (extraction des contacts, des messages, des journaux d’appels, etc.).

### Recommandations de sécurité
- **Implémentation du chiffrement des données en transit** : Le trafic USB devrait être encapsulé dans des protocoles sécurisés comme TLS.
- **Mécanismes de journalisation** : Les appareils mobiles et les outils de forensics devraient fournir des logs explicites pour retracer les activités.

---

## 2. Analyse des processus avec ProcMon
![pasted_image027](https://github.com/user-attachments/assets/ff2c39fa-083c-41cd-b828-ab06f537f1ba)
![pasted_image026](https://github.com/user-attachments/assets/04b8240a-7e8a-4d00-b3c4-2e021931975f)

### Structure et architecture du logiciel
L’utilisation de **Process Monitor** a permis de cartographier l’architecture d’extraction du logiciel **MOBILedit Forensic Express**. Il apparaît clairement que l’application utilise une **structure hiérarchique et modulaire** :
1. Le processus principal, **MOBILedit Forensic Express.exe** (PID: 2604), agit comme **coordinateur**.
2. Il engendre plusieurs sous-processus spécifiques, chacun étant dédié à un domaine de données précis :
   - **Comptes utilisateurs** : Analyse des comptes présents sur l’appareil (par exemple, Google, Facebook).
   - **Contacts** : Extraction détaillée des informations personnelles de la base de données des contacts.
   - **Paramètres de sécurité** : Récupération de paramètres critiques tels que les mots de passe Wi-Fi, les paramètres VPN ou les préférences utilisateur.
   - **Carte SIM** : Lecture des données IMSI/IMEI ou des répertoires de contacts de la carte SIM.
   - **Journaux d'appels** : Analyse historique des appels entrants, sortants et manqués.

### Détection de comportements potentiellement abusifs
- **Accès aux fichiers sensibles** : Les sous-processus montrent des requêtes répétées vers des fichiers critiques du système Android, souvent localisés dans des répertoires protégés comme **/data/data/[package_name]**. Ces accès nécessitent des permissions root ou administrateur.
- **Récupération exhaustive** : L’outil semble collecter des données bien au-delà des simples métadonnées, incluant parfois des caches ou des données non visibles à l'utilisateur final.

### Suggestions d’améliorations
- Limiter l’accès aux sous-processus uniquement aux données strictement nécessaires.
- Ajouter une séparation claire entre les composants de collecte et les composants d’analyse pour réduire les risques en cas de compromission.

---

## 3. Analyse des modifications du Registre avec Regshot
![pasted_image029](https://github.com/user-attachments/assets/f9918fac-c904-4e8d-b4b0-d20e3ce2329b)
![pasted_image028](https://github.com/user-attachments/assets/f4e4da90-4a88-4417-8a47-672e031aa511)

### Création de clés et modifications détectées
L’utilisation de **Regshot** a révélé plusieurs modifications importantes dans le registre Windows après l’exécution du logiciel, indiquant un impact significatif sur l’environnement système. Voici quelques exemples notables :

1. **Création de clés** :
   - **HKLM\SOFTWARE\Microsoft\Windows\Windows Error Reporting\TermReason** : Probablement utilisé pour capturer et analyser les crashs de l’application.
   - **HKU\S-1-5-21-...\Keyboard Layout** : Des modifications dans cette clé pourraient suggérer une tentative de gestion des entrées clavier, ce qui est une pratique risquée.

2. **Modifications de valeurs existantes** :
   - **ShowToast** : Cette valeur est généralement associée aux notifications utilisateur. Cela pourrait indiquer que l'application génère des alertes en arrière-plan.
   - **Session Explorer** : Des modifications ici pourraient influencer la manière dont les sessions utilisateur sont gérées par l’OS.

3. **Entrées temporaires** :
   - Création de fichiers journaux et de sessions temporaires pour coordonner les opérations d’extraction.

### Implications et risques
Ces modifications, bien qu’essentielles pour le fonctionnement du logiciel, posent des problèmes de sécurité :
- Les modifications non réversibles pourraient affecter l’intégrité du système hôte.
- Les clés liées aux sessions Explorer peuvent potentiellement être exploitées par des attaquants pour accéder aux informations sensibles.

### Recommandations
- Mettre en œuvre une solution de restauration automatique du registre après l’exécution de l’outil.
- Documenter et alerter l’utilisateur sur chaque modification apportée.

---



