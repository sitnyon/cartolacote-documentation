Webservices
===========

Chantiers et perturbations de trafic
------------------------------------

Le webservice des chantiers permet de renvoyer une liste des chantiers et des perturbations trafic lié à celui-ci . C'est un service uniquement dédié aux partenaires Cartolacôte. 

URL
***

``https://map.cartolacote.ch/webservice/chantiers?entite={nom_entite}``


Paramètre 
*********

+---------------+------------------+------------------------+
| Paramètre     | Description      | Valeurs supportées     |
+===============+==================+========================+
| entite        | Le nom technique | ambulances, coppet,    |
| (requis)      | d'une entité     | givrins, gland, mies,  |
|               | Cartolacôte qui  | nyon, perroy, pnr,     |
|               | permet de filter | prangins, region_nyon, |
|               | selon son emprise| sdis_gs, sdis_nd,      |
|               | géographique     | sdis_ts, seic,         |
|               |                  | thermoreso_nyon, trn,  |
|               |                  | vich                   |
+---------------+------------------+------------------------+

Liste des attributs
*******************

* **evenement (obligatoire)** : nom de l'évènement 
* **type_evenement (obligatoire)** : type de chantier (uniquement Chantier)
* **service_pilote (obligatoire)** : nom du service pilote 
* **telephone_contact** : numéro de téléphone du service pilote
* **email_contact** : adresse e-mail du service pilote
* **horaire_travaux** : horaires des travaux (jour, nuit ou les deux)
* **confirme (obligatoire)** : si l'évènement est confirmée ou non
* **perturbations (obligatoire)** : liste des perturbations de trafic

	* **type_perturbation (obligatoire)** : type de la perturbation
	* **periode_public** : période pendant laquelle a lieu la perturbation
	* **date_debut_public** : date de début des travaux
	* **date_fin_public** : date de fin des travaux
	* **periode_secours** : période pendant laquelle a lieu la perturbation (uniquement pour les secours)
	* **date_debut_secours** : Date de début des travaux (uniquement pour les secours)
	* **date_fin_secours** : Date de fin des travaux (uniquement pour les secours)
	* **etat_public** : état de la perturbation (Passé, En cours, Futur) 
	* **etat_secours** : état de la perturbation (Passé, En cours, Futur) (uniquement pour les secours)

* **coordonnee_x (obligatoire)** : coordonnées x du point de l'évènement 
* **coordonnee_y (obligatoire)** : coordonnées y du point de l'évènement 