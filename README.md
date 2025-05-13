# MediaTekDocuments

## Présentation de l'application d'origine

Voici le [lien du dépôt d'origine](https://github.com/CNED-SLAM/MediaTekDocuments) où sont expliqués le contexte et les fonctionnalités initiales du projet.

Ce dépôt présente uniquement les **fonctionnalités ajoutées** à l’application dans le cadre de son évolution.

---

## Fonctionnalités ajoutées

### Gestion des documents physiques - Livres - DVD - Revues

- L’interface comporte **plusieurs onglets**, qui permettent de **naviguer** dans l'application.
- **Plusieurs zones** sont séparées visuellement :
  - Une **zone de recherche**.
  - Le **catalogue des documents** de l'onglet actuel.
  - Les **informations détaillées** du document sélectionné.
  - Le **catalogue des exemplaires** du document sélectionné uniquement pour les onglets **Livres** et **DVD**
  

![image](https://github.com/user-attachments/assets/58ea0b13-e774-4bc8-bf2e-a3122a2cc8ed)


- L'onglet **Parutions des revues** affiche les exemplaires disponibles de la revue sélectionné.


![image](https://github.com/user-attachments/assets/a6c465b1-2c55-44c8-a5b4-a7aad778e8a0)


- Un onglet **+ Ajouter un document** permet d'ajouter un document de n'importe quel type.
- Les champs à renseigner changent en fonction du type de document sélectionné.

<p align="center">
  <img src="https://github.com/user-attachments/assets/68a63f05-e7d2-4bd9-be41-7af8b854bfbd">
</p>


- Dans ces onglets, plusieurs fonctionnalités sont disponibles :
  **La modification d'un document** en cliquant sur le bouton **Modifier**.
  

![image](https://github.com/user-attachments/assets/a0efbde7-07bc-4b4a-a1eb-0f241bf6273c)


- **La suppression d'un document** en cliquant sur le bouton **X** qui ouvre une fenêtre de confirmation.
  

![image](https://github.com/user-attachments/assets/4363956a-6ec2-45eb-b0ad-a1ae0508ba11)

</br>

> Après chaque **ajout**, **modification** ou **suppresion**, la liste se met à jour automatiquement.

---

### Gestion des commandes et abonnements - Livres - DVD - Revues

- L'onglet **Commandes** regroupe trois sous onglets :
  - **Commandes Livres**.
  - **Commandes DVDs**.
  - **Commandes Revues**.

- Les onglets liés aux **commandes** de livres et de DVDs sont similaire. On y trouve :
  - Une **zone de recherche** pour trouver le document souhaité.
  - Un **tableau** affichant les commandes associées au document sélectionné.
  - Une zone pour **ajouter une commande**.
  - Un **bouton de suppresion** avec confirmation. <br/>
  ⚠️ La suppression est bloquée si la commande a atteint l’étape **Livrée** ou **Réglée** </br>
    
 
![image](https://github.com/user-attachments/assets/40cfc30c-9013-4b3a-98c8-214b6e51df2a)


> Le tableau contient une ***liste déroulante dans la colonne Suivi**, permettant de modifier l'état de la commande.

- L'onglet **Commandes Revues** est dédié à la **gestion des abonnements**.
- Le fonctionnement est similaire aux autres commandes, à la différence que
  - Le **nombre d'exemplaires** est remplacé par une **date de fin d'abonnement**. </br>
  ⚠️ Le **bouton de suppression** est désactivé si un **exemplaire existe dans la période d’abonnement**.


![image](https://github.com/user-attachments/assets/c3a48d62-56d8-48ee-9e5a-069c9e710e8d)


---

### Gestion des exemplaires - Livres - DVD - Revues

- Pour chaque **livre** ou **DVD**, les exemplaires associés sont affichés dans une grille située en bas de l’interface principale.
- Pour les **revues**, les exemplaires sont accessibles dans l’onglet **Parutions des revues**. <br/>

- **Fonctionnalités disponibles :**
  - **Modification de l’état** d’un exemplaire via une **liste déroulante**.
  - **Suppression** d’un exemplaire avec confirmation.

<p align="center">
  <img src="https://github.com/user-attachments/assets/94389222-5de7-483c-b012-2c7babb06b41"/>
</p> <br/>

- Si un abonnement se termine dans moins de 30 jours, une alerte est affichée.

<p align="center">
  <img src="https://github.com/user-attachments/assets/a9fbe2c1-dcef-4667-909b-beaee0a36df0"/>
</p>

---

### Authentification et gestion des droits

- À l’ouverture de l’application, une **fenêtre de connexion** s’affiche et demande un **identifiant** et **un mot de passe**.
- Une fois connecté, l’utilisateur accède à l’interface principale, dont les fonctionnalités varient selon son **service d’appartenance**. <br/>

<p align="center">
  <img src="https://github.com/user-attachments/assets/62ca14df-88b0-4c50-bac7-6899fa23ba0a"/>
</p>

#### Profils utilisateurs gérés :

| Service            | Droits d’accès                                                           |
| ------------------ | ------------------------------------------------------------------------ |
| **Administrateur** | Accès complet à toutes les fonctionnalités                               |
| **Administratif**  | Accès complet à toutes les fonctionnalités                               |
| **Prêts**          | Accès en **lecture seule** (pas d’ajout, modification ou suppression)    |
| **Culture**        | **Accès refusé** — un message d’alerte s’affiche, l’application se ferme |


> Les onglets **Commandes** et **+ Ajouter un document** ne sont disponible que pour **l'administrateur** et **l'administratif** uniquement.

---

### Documentation intégrée

Un lien vers la **documentation technique de l’application** est disponible dans le site :
👉 [Consulter la documentation](https://mediatekformation.alwaysdata.net/mediatekdocuments/documentation/client/html/d75eb659-6335-53f6-af7a-81814a21ab7f.htm)

---

## Installation et utilisation en local

### Prérequis

- .NET Framework ≥ **4.7**.
- Base de données **MySQL** disponible (locale ou distante). <br/>

> Pour installer l'**API PHP** vous pouvez la trouver en cliquant ici : 👉[API REST PHP](https://github.com/Dirtyrat44/rest_mediatekdocuments)
> Toutes les informations sont dans le **README** du dépôt.

---

### Installation avec Git (recommandé)

#### 1. Cloner le dépôt
```bash
git clone https://github.com/votre-utilisateur/MediaTekDocuments.git
cd mediatekformation
```
#### 2. Ouvrir le projet dans Visual Studio
- Ouvrir le fichier **.sln**.
- Vérifier que les dépendances sont bien restaurées.

#### 3. Configurer les identifiants d'accès à l'API
- Modifier le fichier **App.config**
```bash
<appSettings>
  <add key="ApiUri" value="https://votre-api/rest_mediatekdocuments/" />
  <add key="ApiLogin" value="votrelogin" />
  <add key="ApiPassword" value="votremotdepasse" />
</appSettings>
```
#### 4. Compiler et lancer l’application
- **Démarrer** l'application dans Visual Studio et vérifier que l'application fonctionne.

### Installer l'application (optionnel)
- Télécharger et lancer le fichier **.msi** dans **Setup-MediaTekDocuments/Release**.
- Suivre les instructions de l'assistant d'installation.
- Lancer l'application depuis le **Bureau** ou le **Menu Démarrer**.
