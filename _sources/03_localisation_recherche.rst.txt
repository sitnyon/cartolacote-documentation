Localisation et recherche
=========================

Un outil de recherche plein texte permet de se localiser sur un emplacement ou sur un objet
spécifique, ou encore d’ajouter des données (couches et thèmes).

Les résultats sont affichés au fur et à mesure de la saisie, répartis en différents groupes. Un
clic sur le résultat permet de recentrer la carte sur l’objet ou d’ajouter la donnée en question.

La croix à droite de la zone de saisie permet de désactiver la mise en évidence de l’objet.


.. raw:: html

    <p><video width="600" controls><source src="_static/recherche.mp4" type="video/mp4"></video></p><br>

Il est également possible de changer la couleur du résultat en cliquant sur l'icône goutte.

.. image:: _static/personaliser_couleur_recherche.png
  :width: 1000

Objets paramétrés pour la recherche
-----------------------------------


+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Thème         | Mot-clé         | Format de la recherche | Exemple               | Action                  | Accès      | Etendue géographique      |
+===============+=================+========================+=======================+=========================+============+===========================+
| Aménagement   | PQ              | PQ ou PPA ou PEP +     | PQ 5234 La Poterie    | Zoom sur l'emprise      | Public     | Coppet, Nyon, Mies        |
| du territoire | PPA             | numéro de plan + nom   | ou PPA 5358 L'Asse    | du plan et activation   |            |                           |
|               | PEP             | de plan                | ou PEP 3785 A Rive    | de la couche            |            |                           |
|               |                 |                        |                       | **Plan de zones**       |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Cadastre      | x               | Adresse complète       | Grand-Rue 1 Coppet    | Zoom sur l'adresse et   | Public     | District de Nyon          |
|               |                 |                        |                       | mise en surbrillance    |            |                           |
|               |                 |                        |                       | du point                |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Cadastre      | ECA             | ECA + numéro ECA       | ECA 1007              | Zoom sur l'emplacement  | Public     | District de Nyon          |
|               |                 | + Commune              | Prangins              | du bâtiment             |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Cadastre      | EGID            | EGID + numéro EGID     | EGID 812679           | Zoom sur l'emplacement  | Public     | Nyon                      |
|               |                 |                        |                       | du bâtiment et          |            |                           |
|               |                 |                        |                       | activation de la        |            |                           |
|               |                 |                        |                       | couche **Registre **    |            |                           |
|               |                 |                        |                       | **des bâtiments (RCB)** |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Cadastre      | DDP             | DDP + numéro du DPP    | DDP 4306              | Zoom sur l'emplacement  | Public     | District de Nyon          |
|               |                 | + Commune              | Gland                 | du DDP et activation    |            |                           |
|               |                 |                        |                       | de la couche            |            |                           |
|               |                 |                        |                       | **Droit distinct**      |            |                           |
|               |                 |                        |                       | ** et permanent**       |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Cadastre      | x               | Rue + Commune          | Route de Montelly     | Zoom sur la rue et      | Public     | District de Nyon          |
|               |                 |                        | Perroy                | mise en surbrillance    |            |                           |
|               |                 |                        |                       | du tracé                |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Cadastre      | ESID            | ESID + numéro ESID     | ESID 10100815         | Zoom sur la rue,        | Public     | Nyon                      |
|               |                 |                        |                       | mise en surbrillance    |            |                           |
|               |                 |                        |                       | du tracé et activation  |            |                           |
|               |                 |                        |                       | de la couche **Rues**   |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Cadastre      | parcelle        | parcelle + numéro de   | parcelle 1            | Zoom sur la parcelle et | Public     | District de Nyon          |
|               |                 | parcelle               | Vich                  | mise en surbrillance    |            |                           |
|               |                 |                        |                       | de la parcelle          |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Cadastre      | EGRID           | EGRID + numéro de      | EGRID CH828282834506  | Zoom sur la parcelle,   | Public     | District de Nyon          |
|               |                 | EGRID                  |                       | mise en surbrillance    |            |                           |
|               |                 |                        |                       | de la parcelle et       |            |                           |
|               |                 |                        |                       | activation des couches  |            |                           |
|               |                 |                        |                       | **Domaine public **     |            |                           |
|               |                 |                        |                       | **communal** et         |            |                           |
|               |                 |                        |                       | **Domaine public**      |            |                           |
|               |                 |                        |                       | ** cantonal** si la     |            |                           |
|               |                 |                        |                       | parcelle est sur le DP  |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Cadastre      | PPE             | PPE + numéro de PPE    | PPE 57                | Zoom sur la parcelle et | Public     | Nyon                      |
|               |                 | + Commune              | Nyon                  | mise en surbrillance    |            |                           |
|               |                 |                        |                       | de la PPE               |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Cadastre      | Commune         | Commune + numéro OFS   | Mies 5723             | Zoom sur la commune,    | Public     | District de Nyon          |
|               |                 | ou numéro cantonal     | ou                    | mise en surbrillance    |            |                           |
|               |                 |                        | Mies 245              | de la commune et        |            |                           |
|               |                 |                        |                       | activation de la        |            |                           |
|               |                 |                        |                       | couche **Communes**     |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Cadastre      | NPA             | NPA + numéro NPA       | NPA 1271              | Zoom sur la commune,    | Public     | District de Nyon          |
|               |                 |                        |                       | mise en surbrillance    |            |                           |
|               |                 |                        |                       | de la commune           |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Cadastre      | x               | Coordonnées CH1903+    | 2504662 1138354       | Recentre sur les        | Public     | District de Nyon          |
|               |                 | ou WGS84               | ou                    | coordonnées             |            |                           |
|               |                 |                        | 6.19898 46.38976      |                         |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Cadastre      | PFP             | PFP + numéro du PFP    | PFP 1241 121 0        | Zoom sur le PFP et      | Public     | District de Nyon          |
|               |                 |                        |                       | activation de la couche |            |                           |
|               |                 |                        |                       | **Points fixes**        |            |                           |
|               |                 |                        |                       | ** planimétriques**     |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Cadastre      | PFA             | PFA + numéro du PFA    | PFA 1241G041A         | Zoom sur le PFA et      | Public     | District de Nyon          |
|               |                 |                        |                       | activation de la couche |            |                           |
|               |                 |                        |                       | **Points fixes**        |            |                           |
|               |                 |                        |                       | ** altimétriques**      |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Ecoles et     | AMF             | AMF + nom de l'AMF     | AMF Pierre Martin     | Zoom sur la             | Restreint  | Nyon                      |
| accueil de    |                 |                        |                       | localisation de l'AMF   |            |                           |
| jour          |                 |                        |                       |                         |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Environnement | x               | Nom du cours d'eau     | L'Asse                | Zoom sur le cours d'eau | Public     | Nyon                      |
|               |                 |                        |                       | et activation de la     |            |                           |
|               |                 |                        |                       | couche **Cours d'eau**  |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Espaces verts | Arbre           | Arbre + numéro de      | Arbre 1               | Zoom sur l'arbre        | Public     | Nyon                      |
|               |                 | de l'arbre             |                       | et activation de la     |            |                           |
|               |                 |                        |                       | couche **Arbre sur **   |            |                           |
|               |                 |                        |                       | **domaine public**      |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Mobilité      | Arrêt           | Arrêt + nom de l'arrêt | Arrêt Changins        | Zoom sur l'arrêt ou la  | Public     | District de Nyon          |
|               |                 | bus ou nom de la gare  | ou Arrêt Arzier       | gare et activation      |            |                           |
|               |                 |                        |                       | de la couche            |            |                           |
|               |                 |                        |                       | **Arrêts de bus** ou    |            |                           |
|               |                 |                        |                       | **Gares**               |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Patrimoine    | x               | Nom de la Salle        | Salle de la Bretèche  | Zoom sur la salle       | Public     | Nyon                      |
|               |                 | communale              |                       | communale et activation |            |                           |
|               |                 |                        |                       | de la couche **Salles** |            |                           |
|               |                 |                        |                       | ** communales**         |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Plan de ville | x               | Nom du point d'intérêt | Ranch Zangalisa       | Zoom sur le point       | Public     | District de Nyon          |
|               |                 |                        |                       | d'intérêt et activation |            |                           |
|               |                 |                        |                       | de la couche concernée  |            |                           |
|               |                 |                        |                       | par le point d'intérêt  |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Plan de ville | x               | Nom du lieu            | Capite à moto         | Zoom sur le lieu        | Public     | District de Nyon          |
| (Lieux        |                 | géographique           |                       | géo. et activation      |            |                           |
| géographiques)|                 |                        |                       | de la couche concernée  |            |                           |
|               |                 |                        |                       | par le lieu             |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Police des    | Permis          | Permis + numéro de     | Permis 7225           | Zoom sur l'emprise      | Public     | Nyon                      |
| constructions |                 | permis                 |                       | géographique du permis  |            |                           |
|               |                 |                        |                       | et activation de la     |            |                           |
|               |                 |                        |                       | couche concernée par le |            |                           |
|               |                 |                        |                       | permis                  |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Police des    | CAMAC           | Permis + numéro de     | CAMAC 193955          | Zoom sur l'emprise      | Public     | Nyon                      |
| constructions |                 | permis                 |                       | géographique du permis  |            |                           |
|               |                 |                        |                       | et activation de la     |            |                           |
|               |                 |                        |                       | couche concernée par le |            |                           |
|               |                 |                        |                       | permis                  |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Réseaux       | BH              | BH + numéro de la BH   | BH 3                  | Zoom sur la BH et       | Restreint  | District de Nyon          |
| souterrains   |                 |                        |                       | activation de la couche | et         |                           |
| (eau)         |                 |                        |                       | **Hydrantes**           | Public     |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Réseaux       | Armoire         | Armoire +              | Armoire               | Zoom sur l'amoire de    | Restreint  | Nyon                      |
| souterrains   |                 | nom de l'armoire       | Dortu                 | distribution et         |            |                           |
| (électricité) |                 |                        |                       | activation de la        |            |                           |
|               |                 |                        |                       | couche **Distributeurs**|            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Réseaux       | Station         | Station électrique +   | Station électrique    | Zoom sur la station     | Restreint  | Nyon                      |
| souterrains   | électrique      | nom de la station      | STAND                 | électrique et           |            |                           |
| (électricité) |                 |                        |                       | activation de la        |            |                           |
|               |                 |                        |                       | couche **Stations**     |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Réseaux       | CD              | CD + nom de la CD      | CD 7                  | Zoom sur la CD et       | Restreint  | Nyon                      |
| souterrains   |                 |                        |                       | activation de la couche |            |                           |
| (gaz)         |                 |                        |                       | **Postes de détente**   |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Réseaux       | BAG             | BAG + nom de la BAG    | BAG 601               | Zoom sur la BAG et      | Restreint  | Nyon                      |
| souterrains   |                 |                        |                       | activation de la couche |            |                           |
| (gaz)         |                 |                        |                       | **Balise de**           |            |                           |
|               |                 |                        |                       | ** signalisation**      |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Sécurité      | SDIS            | SDIS + numéro de       | A05043 Parking les    | Zoom sur la détection   | Restreint  | SDIS Nyon Dôle et         |
| (pompiers)    |                 | détections +           | Foulis                | et activation de la     |            | SDIS Gland-Serine         |
|               |                 | localisation           |                       | couche **Détections**   |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Sécurité      | Clé             | Clé + numéro de clé    | Clé 168               | Zoom sur l'emplacement  | Restreint  | SDIS Nyon Dôle et         |
| (pompiers)    |                 | + localisation         |                       | de la clé et activation |            | SDIS Gland-Serine         |
|               |                 |                        |                       | de la couche **Clés**   |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Sécurité      | Station         | Station essence +      | Station essence Signy | Zoom sur la station     | Restreint  | District de Nyon          |
| (urgences)    | essence         | nom de la station      |                       | essence et activation   |            | (partiellement)           |
|               |                 |                        |                       | de la couche            |            |                           |
|               |                 |                        |                       | **Stations, garages**   |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+
| Sécurité      | Garage          | Garage +               | Garage Binggeli       | Zoom sur le garage      | Restreint  | District de Nyon          |
| (urgences)    |                 | nom du garage          | carrosserie           | activation de la couche |            | (partiellement)           |
|               |                 |                        |                       | **Stations, garages**   |            |                           |
+---------------+-----------------+------------------------+-----------------------+-------------------------+------------+---------------------------+


