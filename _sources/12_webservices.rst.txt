Webservices
===========

Adresse
-------

Le webservice des adresses permet de renvoyer un adresse selon un identifiant. C'est un service uniquement dédié aux partenaires Cartolacôte.

URL
***

``https://map.cartolacote.ch/webservice/adresse?fid={identifiant}``

Paramètre
*********

+---------------+------------------+------------------------+
| Paramètre     | Description      | Valeurs supportées     |
+===============+==================+========================+
| fid           | L'identifiant de | Numéro à 6 chiffres    |
| (requis)      | l'adresse        | Ex : 120176            |
+---------------+------------------+------------------------+

Liste des attributs
*******************

* **adresse** : adresse complète
* **coordinates** : coordonnées XY de l'adresse


Adresses
--------

Le webservice des adresses permet de renvoyer la liste des adresses sur l'ensemble du district de Nyon. C'est un service uniquement dédié aux partenaires Cartolacôte.

URL
***

``https://map.cartolacote.ch/webservice/adresses``

Liste des attributs
*******************

* **id** : identifiant
* **numero** : numéro de l'entrée de bâtiment
* **adresse** : adresse complète
* **adresse_court** : adresse simplifiée
* **adresse_index** : adresse au format index (ex : Petite Prairie, allée de la 10)
* **rue** : rue complète
* **rue_court** : rue simplifiée
* **rue_index** : rue au format index (ex : Petite Prairie, allée de la)
* **commune** : nom de la commune
* **coordinates** : coordonnées XY de l'adresse (Point)


Chantiers et perturbations de trafic
------------------------------------

Le webservice des chantiers permet de renvoyer une liste des chantiers et des perturbations trafic lié à celui-ci. C'est un service uniquement dédié aux partenaires Cartolacôte.

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


Catalogue
---------

Le webservice Catalogue permet de renvoyer la liste des couches selon le type d'interface.

URL
***

``https://map.cartolacote.ch/layer_interface?interface={nom_interface}``

Paramètre
*********

+---------------+------------------+------------------------+
| Paramètre     | Description      | Valeurs supportées     |
+===============+==================+========================+
| interface     | Le nom technique | api, desktop, mobile   |
| (requis)      | d'une interface  | iframe                 |
+---------------+------------------+------------------------+


Documents
---------

Le webservice Documents permet de renvoyer un carrousel d'images ou de fichiers.

URL
***

``https://map.cartolacote.ch/docs/{type_document}/{identifiant}``

Paramètre
*********

+---------------+------------------+------------------------+
| Paramètre     | Description      | Valeurs supportées     |
+===============+==================+========================+
| type_document | Le type de       | image ou file          |
| (requis)      | de document que  |                        |
|               | doit renvoyer le |                        |
|               | webservice       |                        |
+---------------+------------------+------------------------+
| identifiant   | L'identifiant du | Ex : ASS253REGARD_R53  |
| (requis)      | ou des documents |                        |
+---------------+------------------+------------------------+

Enquêtes publiques
------------------

Le webservice des enquêtes publiques permet de renvoyer la liste des avis d'enquêtes en cours sur la commune de Nyon. C'est un service uniquement dédié aux partenaires Cartolacôte.

URL
***

``https://map.cartolacote.ch/webservice/enquetes``

Liste des attributs
*******************

* **enquete_num** : numéro d'enquête
* **enquete_type** : type d'enquête
* **camac_num** : numéro CAMAC
* **descriptif_projet** : descriptif du projet
* **lien_dossier_enquête** : url pour télécharger le dossier de l'enquête
* **dates_parution** : date de parution de l'enquête
* **proprietaire_nom** : nom du propriétaire
* **architecte** : nom de l'architecte
* **adresse** : adresse complète concernée par l'enquête
* **no_parcelle** : numéro de la parcelle concernée par l'enquête
* **no_eca** : numéro ECA du bâtiment
* **adoption_commune_date** : date d'adoption par la communne
* **adoption_canton_departement** : date d'adoption par le département du canton
* **adoption_canton_date** : date d'adoption par le canton
* **coordinates** : coordonnées XY de l'adresse (Point)

Métadonnées
-----------

Le webservice Métadonnes permet de renvoyer la liste des copyrights pour les fonds de plan utilisés par Cartolacôte.

URL
***

``https://map.cartolacote.ch/background_metadata``

Liste des attributs
*******************

* **date_import** : date de l'import des données
* **name** : nom du copyright
* **url** : lien vers les conditions d'utilisation


Nature en ville
---------------

Le webservice nature en ville permet de renvoyer la liste des balades nature en ville sur la commune de Nyon. C'est un service uniquement dédié aux partenaires Cartolacôte.

URL
***

``https://map.cartolacote.ch/webservice/nature_ville``

Liste des attributs
*******************

* **id** : identifiant
* **nom** : intitulé de la balade
* **document** : lien vers la fiche de la balade
* **distance_km** : distance de la balade en km
* **denivele_info** : information sur le dénivelé
* **suggestion_depart** : suggestion du départ
* **commodites** : information sur les commodités
* **rgb** : couleur du tracé
* **coordinates** : coordonnées XY de l'emprise (Polygone)


Rues
----

Le webservice des rues permet de renvoyer la liste des adresses sur l'ensemble du district de Nyon. C'est un service uniquement dédié aux partenaires Cartolacôte.

URL
***

``https://map.cartolacote.ch/webservice/rue``

Liste des attributs
*******************

* **id** : identifiant
* **rue** : rue complète
* **rue_court** : rue simplifiée
* **rue_index** : rue au format index (ex : Petite Prairie, allée de la)
* **commune** : nom de la commune