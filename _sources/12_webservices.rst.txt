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
* **type_evenement (obligatoire)** : type de chantier
* **etat (obligatoire)** : état du chantier (En cours, Futur)
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
	* **heure_debut** : heure de début de la perturbation
	* **heure_fin** : heure de fin de la perturbation
	* **lundi** : la perturbation a lieu le lundi (oui, non)
	* **mardi** : la perturbation a lieu le mardi (oui, non)
	* **mercredi** : la perturbation a lieu le mercredi (oui, non)
	* **jeudi** : la perturbation a lieu le jeudi (oui, non)
	* **vendredi** : la perturbation a lieu le vendredi (oui, non)
	* **samedi** : la perturbation a lieu le samedi (oui, non)
	* **dimanche** : la perturbation a lieu le dimanche (oui, non)

* **coordonnee_x (obligatoire)** : coordonnées x du point de l'évènement 
* **coordonnee_y (obligatoire)** : coordonnées y du point de l'évènement 