# <center>Programme D-CLIC
# <center> Module : UML/Merise
# <center> JARVIS partie 1



# 1 Analyse de la diagramme des cas utilisation

<img src="./assets/img/Jarvis_usecase.png">


## 1.1 Liste des Acteurs 
* **Primaire** :
	* Proprietaire
	* Co-propriétaire
	* Membre
	* Visiteur

* **Secondaire** :
	* GOOGLE API

## 1.2 Fonctionnalité pour chaque acteur:

* **Visiteur** :
	* S'authentifier

* **Membre** : 
	* S'authentifier
	* Récupérer la liste des pieces
	* Récupération de la liste des objets connecter _(**Obligatoire**)_
	* Modification d'un Objet connecter _(Optionnelle)_
	* Mettre en place un objet connecter dans une pièce _(Optionnelle)_

* **Co-Propriétaire** :
	* S'authentifier
	* Récupérer la liste des pieces
	* Récupération de la liste des objets connecter
	* Modification d'un Objet connecter
	* Mettre en place un objet connecter dans une pièce _(**Obligatoire**)_
	* Ajouter un objet connecter
	* Créé une nouvelle pièce

* **Propriétaire** :
	* S'authentifier
	* Récupérer la liste des pieces
	* Récupération de la liste des objets connecter
	* Modification d'un Objet connecter
	* Mettre en place un objet connecter dans une pièce
	* Modifier le role d'un utilisateur
	* Cree un Domicile
	* Rechercher d'adrese _(**Obligatoire**)_

* **GOOGLE API** : 
	* Fournir l'adresse démander

## 1.3 Les actions obigatoire/optionnelle
Elle sont Marqué dans la section 1.2

# 2 MCD 
<img src="./assets/img/Jarvis_mcd_ok.png">

## 2.1 Liste des Entintés et leurs propriété respéctives
* Ulilisateurs
* Membres
* Co-Proprietaires
* Proprietaires
* Domiciles
* Pieces
* Appareils


<!--
* Membre
* Co-proprietaire
* ProPrietaire
* ObjetConnecter
* Abonnement
* Carte
* Piece
* Domicile
-->
## 2.2 Les associations entre divers Entités
* **Utilisateur** :
	* _Habiter_ au moins dans un **Domicile**
	* _Peut être_ un **Membre** ou **CoProprietaire** ou **Propriétaire** (Exclisive) ou **Autre**

* **Proprietaires**:
	* _Possede_ un **Domiciles**

* **Pieces** :
	* _Contenu_ dans un **Domiciles**

* **Appareil** :
	* _SeTrouve_ dans une **Piece**


<!--
* **Membre** :
	* _Habiter_ dans un **Domicile**
	* _Avoir_ un **ObjetConnecter**
* **Co-Proprietaire** :
	* _Cree_ **Piece** dans un *Domicile*
	* _AjouterObjetConncter_ dans une **Piece**

* **Proprietaire**:
	* _Proprietaire_ (Appartien) d'un **Domicile**
	* _Abonner_ a un **Abonnement**
	* _Possede_(carte de) au moins une **Carte**
-->
## 2.3 MLD

	Utilisateurs (idUtilisateur, nomUtilisateur, prenomUtilisateur, dNaissUtilisateur, emailUtilisateur, telUtilisateur)

	Membres (#idUtilisateur, idMembre)

	CoProprietaires (#idUtilisateur, idCoproprietaire)

	Proprietaires (#idUtilisateur, idProprietaire)

	Domiciles (idDomicile, addresseDomicile, #idUtilisateur)

	Appareils (idAppareil, nomAppareil, typeAppareil, #idPiece)

	Pieces (idPiece, #idDomicile)

	Habiter (#idUtilisateur, #idDomicile)

## 2.4 MPD
<img src="./assets/img/Jarvis_mpd_ok.png">
