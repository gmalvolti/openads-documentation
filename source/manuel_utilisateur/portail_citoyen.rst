.. _portail_citoyen:

###############
Portail citoyen
###############

Lors de l’enregistrement d'un nouveau dossier au guichet unique, il de principe que le citoyen reçoit un récépissé. En principe celui-ci l'informe des modalités, délais correspondant à son dossier. Il est possible également de l'informer, lorsque l'accès au portail citoyen est activé, des modalités de connexion (adresse web et clé d'accès) au portail citoyen.
Il pourra alors se rendre à l'adresse indiquée sur le récépissé et accéder à la synthèse de son dossier d'autorisation.
Cet exploit est possible grâce à la variable de substitution :ref:`acces_citoyen <portail_citoyen_configuration>` utilisable dans les courriers et modifiable depuis les :ref:`paramètres <parametrage_parametre>`.

Il est également possible, lorsque l'accès au portail citoyen est activé, de :ref:`générer <instruction_portlet_generate_citizen_access_key>` ou de :ref:`régénérer <instruction_portlet_regenerate_citizen_access_key>` une clé de connexion depuis le dossier d'instruction.

.. _portail_citoyen_configuration:

Configuration du portail citoyen
################################

Liste des points de configuration :

* **option_portail_acces_citoyen** : permet d'activer ou de désactiver l'accès au portail citoyen. La valeur à saisir pour l'activer est "**true**" et celle pour la désactiver est "**false**". Par défaut, la valeur est "false".

* **acces_citoyen** : depuis les éditions, afin de renseigner les pétitionnaires sur la possibilité d'accéder à un portail citoyen, il est conseillé d'utiliser cette variable de remplacement intelligente. Elle ne sera pas interprétée si l'option est désactivée. Par défaut sa valeur est "Vous pouvez consulter directement votre dossier par internet à l'adresse **&acces_citoyen_adresse** et en saisissant votre numéro de dossier ainsi que la clé d'accès **[cle_acces_citoyen]**."

* **acces_citoyen_adresse** : définit le lien vers le portail citoyen. Par exemple "citoyen.openmairie.org/openads/". Le portail citoyen est capable d'être intégré sur un site internet.

* **[cle_acces_citoyen]** : ce champ de fusion, utilisé par défaut dans **acces_citoyen**, est disponible sur toutes les éditions d'instruction. Il permet d'afficher la clé de connexion propre à chaque dossier qui se compose de quatre groupes de quatre chiffres séparés par des tirets. Par exemple "0000-1111-2222-3333".

.. _portail_citoyen_page_acces:

Le formulaire d'accès au suivi de dossier
#########################################

Depuis le formulaire d'accès du portail citoyen.

.. image:: portail_citoyen_formulaire_acces.png

Les informations à saisir sont :

* **Numéro de dossier** : Le numéro de dossier d'autorisation ou de dossier d'instruction,
  qui apparaît sur tous les documents: récépissés, arrêtés etc.

* **Clé d'accès** : La clé d'accès au portail citoyen qui est par défaut présente sur tous
  les récépissés, sur la lettre type "information d'accès citoyen", ou encore sur la fiche
  détaillée du dossier d'instruction, dans le champ pétitionnaire.


.. _portail_citoyen_regenerate_citizen_access_key_auto:

Régénérer automatiquement la clé d'accès au portail citoyen
===========================================================

Il est possible de paramétrer la régénération automatique de la clé d'accès au portail citoyen, depuis le paramétrage d'un type de demande. (voir :ref:`parametrage_dossiers_demande_type`).
Dans ce cas, l'ajout d'une demande de ce type pour un dossier donné génère une nouvelle clé d'accès qui écrase l'ancienne, ce qui la rend inutilisable.

.. _portail_citoyen_fiche:

La fiche "Suivi de mon dossier"
###############################

La visualisation contient deux blocs d'informations :

.. image:: portail_citoyen_suivi_dossier.png

- **En cours de validité** : informations des dossiers d'instructions soumis à un arrété.

    * En noir : les informations importantes en cours de validité
    * En vert : la liste des lots et leurs petitionnaire principal en cours de validité
    * En rouge : la liste des décisions en cours de validité

- **En cours d'instruction** : données du dossier d'instruction en cours d'instruction.

    * En noir : les informations importantes en cours d'instruction
    * En vert : la liste des lots et leur pétitionnaire principal en cours d'instruction
