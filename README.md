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


Les processus d'acquisition de données, incluant :

1. Les méthodes d'extraction logiques
2. Les protocoles de communication avec les appareils mobiles


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
# Étude de cas : Analyse dynamique d'une acquisition des contacts via Wifi
![pasted_image033](https://github.com/user-attachments/assets/0ea600de-f7a7-4b17-bf58-a7d40bba2a87)
![pasted_image032](https://github.com/user-attachments/assets/3cc9e56d-15da-4f7d-94a8-c4611159f4a3)
![pasted_image031](https://github.com/user-attachments/assets/4d6e59c4-b654-464b-bee8-a7f0547ccd12)
![pasted_image030](https://github.com/user-attachments/assets/c81db25b-f307-4b70-bb03-1a47913c0bdd)

## 1. Analyse du trafic réseau avec Wireshark

L'analyse des captures Wireshark révèle un trafic TCP significatif entre l'application MOBILeditForensicExpress.exe (PID 4732) et l'adresse IP 192.168.1.119. Les communications montrent plusieurs caractéristiques notables :

### Protocoles identifiés
Le trafic est principalement composé de paquets TCP sur le port 10161->50032, avec des séquences régulières d'échanges [PSH, ACK]. Cette configuration indique une transmission active de données en texte clair, sans chiffrement, ce qui représente une vulnérabilité potentielle.

### Structure des échanges
Les trames capturées ont une taille moyenne de 529 octets, avec des séquences répétitives suggérant un transfert structuré de données de contacts. L'absence de chiffrement TLS/SSL permet d'observer directement le contenu des paquets, exposant potentiellement des informations sensibles.

## 2. Analyse des processus avec Process Monitor
![pasted_image040](https://github.com/user-attachments/assets/229d9a7d-7be2-4a76-aec5-8950f37021f2)
![pasted_image039](https://github.com/user-attachments/assets/288bff89-5c0e-4e07-942b-802520877d63)
![pasted_image038](https://github.com/user-attachments/assets/a4604b49-35f6-46ff-8e9b-fb1312880c94)

L'analyse des graphes de processus révèle une architecture d'exécution complexe :

### Processus principal
MOBILeditForensicExpress.exe agit comme processus parent, générant plusieurs sous-processus et créant des fichiers temporaires dans le répertoire :
```
C:\Users\oem\AppData\Local\Temp\MOBILeditForensicExpress\
```

### Fichiers générés
Le logiciel crée plusieurs fichiers avec des extensions spécifiques :
- LinWK.png
- FoukLl.xml
- upDUSN.png
- iBmY.xml

Ces fichiers semblent être utilisés pour stocker temporairement les données extraites pendant l'acquisition.

## 3. Analyse des modifications du registre Windows
![pasted_image035](https://github.com/user-attachments/assets/7d4ad259-eb04-48c7-b266-2e4b613fd2a4)
![pasted_image034](https://github.com/user-attachments/assets/f35ccd00-cd97-4e10-9e33-a7a50456c1b8)
![pasted_image037](https://github.com/user-attachments/assets/171e3279-c96d-4d22-84e8-c45f6e318997)
![pasted_image036](https://github.com/user-attachments/assets/2b1821f3-7637-4418-8fb5-334b834600e3)


L'analyse des différences de registre via Regshot révèle des modifications substantielles :

### Modifications principales
- 28441 clés ont été supprimées
- Impact majeur dans HKLM\DRIVERS\DriverDatabase
- Nombreuses modifications dans les sous-clés DeviceIds

### Chemins affectés
Les modifications concernent principalement les pilotes et périphériques :
```
HKLM\DRIVERS\DriverDatabase\DeviceIds\*
HKLM\SOFTWARE\Microsoft\Windows\CurrentVersion\
```

Cette analyse montre une application qui effectue des opérations privilégiées nécessitant des modifications système importantes pour établir la communication avec le dispositif mobile.


## analyse de traffic

### Empreinte RSA :

35:67:12:BD:69:88:55:BB:13:56:39:68:C8:5B:D9:88
![WhatsApp Image 2025-01-25 at 12 58 14 AM](https://github.com/user-attachments/assets/5fe146c7-9c6d-42d5-9c0c-8b720a7b4f3b)

- **Description** :  
  Il s'agit d'un identifiant unique pour la clé RSA générée par l'ordinateur (ou l'outil de forensic) tentant de se connecter à l'appareil.  
  Cela garantit que l'appareil ne fait confiance qu'aux connexions provenant d'ordinateurs autorisés.

---

#### Invite de Débogage USB :
- **Description** :  
  L'appareil demande s'il faut autoriser le débogage USB à partir de l'ordinateur connecté.  
  L'option **"Toujours autoriser sur cet ordinateur"** permet à l'appareil de mémoriser l'empreinte RSA pour les connexions futures.

---

#### Explication :
1. **Empreinte RSA** :  
   L'empreinte RSA est une mesure de sécurité utilisée pour authentifier l'ordinateur qui tente de se connecter à l'appareil pour le débogage. Elle est générée à partir de la clé publique RSA de l'ordinateur.

2. **Débogage USB** :  
   Lorsque le débogage USB est activé, l'appareil génère une paire de clés RSA. La clé publique est envoyée à l'appareil, et l'empreinte (un hachage de la clé publique) est affichée pour vérification.  
   En acceptant l'empreinte, l'appareil fait confiance à l'ordinateur pour les sessions de débogage futures.
![Screenshot from 2025-01-18 18-23-03](https://github.com/user-attachments/assets/4bb38882-1f61-4ed5-b542-0685a52382df)

---

#### Étapes Suivantes :
1. **Vérifier l'Empreinte RSA** :  
   Assurez-vous que l'empreinte correspond à celle générée par votre outil de forensic ou votre ordinateur.  
   Cette étape est cruciale pour éviter tout accès non autorisé à l'appareil.

2. **Autoriser le Débogage USB** :  
   Si vous faites confiance à l'ordinateur, sélectionnez **"Toujours autoriser sur cet ordinateur"** pour éviter d'être invité à nouveau à l'avenir.

3. **Procéder à l'Analyse Forensic** :  
   Une fois le débogage USB autorisé, votre outil de forensic devrait pouvoir communiquer avec l'appareil et extraire les données.

###  Énumération de l'Appareil

![Screenshot from 2025-01-18 18-24-16](https://github.com/user-attachments/assets/aaec952b-21e6-4d23-9aa9-4031b449cdc3)

after that mobileedit tries to run it's agent in the phone

![Screenshot from 2025-01-18 18-35-13](https://github.com/user-attachments/assets/09a39c1e-49d6-4043-97c7-3f533ed42166)

but the agent is not yet installed so automatically it gets an error

![Screenshot from 2025-01-18 18-35-47](https://github.com/user-attachments/assets/5c7e8af0-736d-401d-99ea-102639db1094)

#### debugging window manager
La commande adb shell dumpsys window fournit un aperçu détaillé de l'état actuel du gestionnaire de fenêtres sur un appareil Android. Elle permet de visualiser des informations sur les fenêtres actives, leur hiérarchie, leur focus, ainsi que les configurations d'affichage et les méthodes d'entrée (comme le clavier). Cet outil est principalement utilisé pour déboguer des problèmes liés à l'affichage, aux transitions d'applications ou au comportement des fenêtres dans des modes multi-fenêtres.

![Screenshot from 2025-01-18 18-43-17](https://github.com/user-attachments/assets/59c4759b-d8ce-4d0e-9b75-211c47ac877d)

#### enumerating processes
 shell ps lists running processes on an Android device, similar to ps on Linux. It shows process IDs (PID), user, and command.
![Screenshot from 2025-01-18 18-44-58](https://github.com/user-attachments/assets/76399ebf-09ff-4bc6-a608-0ea858314271)

#### more enumeration
The adb shell dumpsys iphonesubinfo command on Android retrieves subscriber-related information, such as the device's phone number, SIM serial number, and other telephony details. Despite the name, it has no connection to Apple's iPhone—it is entirely an Android-specific command.
![Screenshot from 2025-01-18 18-57-10](https://github.com/user-attachments/assets/b24bb153-d57b-4262-8417-cb63a66f3d20)


The command provides details like:

    DeviceId: The IMEI of the device.
    SubscriberId: The IMSI associated with the SIM.
    Line1Number: The phone number (if available).![Screenshot from 2025-02-02 14-46-31](https://github.com/user-attachments/assets/3b643c04-5dc5-4af7-91b8-c20c55f6fec3)

    SimSerialNumber: The serial number of the SIM card.

but in our case it won't work, since the command is deprecated since Android update (5.0 - Lollilop), so mobile edit tries another command:

![Screenshot from 2025-02-02 14-46-31](https://github.com/user-attachments/assets/ebe3b6a9-d953-4ac2-b97b-d7eb08c50a07)


#### system propreties

The getprop command in Android is used to retrieve system properties, which are key-value pairs that store various configuration settings and information about the device. These properties can include details about the hardware, software, network, and other system-level configurations.

![Screenshot from 2025-01-18 19-02-44](https://github.com/user-attachments/assets/24ff9f89-99cb-41b1-b4ad-729bc0d8c47d)

The Android Secure ID (android_id) is a unique 64-bit identifier assigned to each Android device. It is specific to the device and the user account, meaning it can change if the device is factory reset or the user account is removed. The android_id is often used by apps and services to uniquely identify a device without requiring sensitive permissions like accessing the IMEI.

![Screenshot from 2025-02-02 17-56-41](https://github.com/user-attachments/assets/b2dbdb83-f6a6-4413-b6bf-b77105fb7973)

#### user properties

The id command in Linux and Android (via ADB shell) displays the user ID (UID), group ID (GID), and supplementary group IDs of the current user.

![Screenshot from 2025-01-18 19-05-09](https://github.com/user-attachments/assets/9c8c0dc9-610c-4e33-87d7-6e0005cf849a)

results

![Screenshot from 2025-01-18 19-05-24](https://github.com/user-attachments/assets/9a68f1c6-a22e-4a09-97f5-fe0c640cd9c3)

it also checks if the user is root

![Screenshot from 2025-01-18 19-08-20](https://github.com/user-attachments/assets/5f221df4-170a-4345-aa32-6a81f948945b)

#### services enumeration

The adb shell service list command shows all system services running on an Android device. These services manage core functionalities like telephony, WiFi, package management, and more.

![Screenshot from 2025-01-18 19-08-55](https://github.com/user-attachments/assets/d861f261-5f97-4f2c-b100-2a85264fa608)


#### installing the agent

after the enumeration mobileedit trys to restart the agent 

![Screenshot from 2025-01-18 19-44-47](https://github.com/user-attachments/assets/28f72c23-b02d-4405-999f-f76c8dc3882e)






