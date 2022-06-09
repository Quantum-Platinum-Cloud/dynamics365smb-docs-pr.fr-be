---
title: Synchroniser les clients
description: Importer les clients de ou les exporter dans Shopify
ms.date: 05/11/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.reviewer: solsen
ms.openlocfilehash: 92ac46e9f7e69204b4c7edee4aa430a8786b6c0b
ms.sourcegitcommit: f071aef3660cc3202006e00f2f790faff849a240
ms.translationtype: HT
ms.contentlocale: fr-BE
ms.lasthandoff: 05/18/2022
ms.locfileid: "8768212"
---
# <a name="synchronize-customers"></a>Synchroniser les clients

Lorsqu’une commande est importée à partir de Shopify, les informations sur le client sont essentielles pour le traitement ultérieur du document dans [!INCLUDE[prod_short](../includes/prod_short.md)]. Il existe deux options principales et leurs combinaisons :

* Utiliser le client spécial pour toutes les commandes.
* Importer les informations client réelles à partir de Shopify. Cette option est également disponible lorsque vous exportez un client dans Shopify à partir de [!INCLUDE[prod_short](../includes/prod_short.md)] en premier.

## <a name="how-connector-chooses-which-customer-to-use"></a>Comment le connecteur choisit le client à utiliser

La fonction *Importer la commande à partir de Shopify* tente de sélectionner le client dans l’ordre suivant :

1. Si le **N° client par défaut** est défini dans **Modèle client Shopify** pour le pays correspondant, **N° client par défaut** est utilisé quels que soient les paramètres dans **Importation client à partir de Shopify** et **Type de mappage client**.
2. Si les champs **Importation client à partir de Shopify** et **N° client par défaut** sont définis, **N° client par défaut** est utilisé.

Les étapes suivantes dépendent du champ **Type de mappage client**.

* **Toujours prendre le client par défaut**, puis utilisez le client défini dans le champ **N° client par défaut** dans la fenêtre **Fiche magasin Shopify**.
* **Par e-mail/téléphone**, le connecteur tente d’abord de trouver le client existant par ID, puis par e-mail, puis par téléphone. Si le client est introuvable, le connecteur crée un client.
* **Par informations de facturation**, le connecteur tente d’abord de trouver le client existant par ID, puis par adresse facturation. Si le client est introuvable, le connecteur crée un client.

> [!NOTE]  
> Le connecteur utilise les informations de l’adresse facturation et crée le client facturé dans [!INCLUDE[prod_short](../includes/prod_short.md)]. Le donneur d’ordre est égal au client facturé.

## <a name="important-settings-when-importing-customers-from-shopify"></a>Paramètres importants lors de l’importation de clients à partir de Shopify

Que vous importiez des clients à partir de Shopify en bloc ou lors de l’importation de commandes, les paramètres suivants permettent de gérer le processus :

|Champ|Désignation|
|------|-----------|
|**Importation client à partir de Shopify**|Sélectionnez **Tous les clients** si vous prévoyez d’importer des clients à partir de Shopify en bloc, soit manuellement en utilisant l’action **Synchroniser les clients**, soit via la file d’attente des tâches pour les mises à jour récurrentes. Quelle que soit la sélection, les informations client sont toujours importées avec la commande. Cependant, l’utilisation de ces informations dépend du champ **Modèles client Shopify** et des paramètres du champ **Type de mappage client**.|
|**Type de mappage client**|Définissez comment le connecteur effectue le mappage.<br>- **Par e-mail/téléphone**, pour que le connecteur mappe le client Shopify importé avec le client existant dans [!INCLUDE[prod_short](../includes/prod_short.md)] en utilisant l’e-mail et le téléphone.</br>- **Par informations de facturation**, pour que le connecteur mappe le client Shopify importé avec le client existant dans [!INCLUDE[prod_short](../includes/prod_short.md)] en utilisant les informations d’adresse de la partie qui réceptionne la facture.</br>Sélectionnez **Toujours prendre le client par défaut** pour que le système utilise un client du champ **N° client par défaut** . |
|**Shopify peut mettre à jour les clients**| Sélectionnez pour que le connecteur mette à jour les clients trouvés si les options **Par e-mail/téléphone** ou **Par informations de facturation** sont sélectionnées dans le champ **Type de mappage client**.|
|**Créer automatiquement des clients inconnus**| Sélectionnez pour que le connecteur crée les clients manquants si les options **Par e-mail/téléphone** ou **Par informations de facturation** sont sélectionnées dans le champ **Type de mappage client**. Un client est créé en utilisant les données importées et **Code modèle client** défini dans les pages **Fiche magasin Shopify** ou **Modèle client Shopify**. Remarquez que le client Shopify doit avoir au moins une adresse. Si cette option n’est pas activée, vous devez créer un client manuellement et le lier au client Shopify. Vous pouvez toujours lancer la création manuelle d’un client à partir de la page **Commande Shopify**.|
|**Code modèle client**|Utilisé avec **Créer automatiquement des clients inconnus**.<br> Choisissez le modèle par défaut à utiliser pour les clients créés automatiquement. Vous pouvez définir des modèles par pays/région dans la fenêtre **Modèles client Shopify**, ce qui est utile pour calculer correctement les taxes. Pour plus d’informations, voir [Remarques sur les taxes](synchronize-orders.md#tax-remarks).|

### <a name="customer-template-per-country"></a>Modèle client par pays

Certains paramètres peuvent être définis au niveau du pays/de la région ou au niveau de l’état/de la province. Les paramètres peuvent être configurés dans [Expédition et livraison](https://www.shopify.com/admin/settings/shipping) sur Shopify.

**Modèle client Shopify** permet de faire ce qui suit pour chaque pays :

1. Indiquer le **N° client par défaut**, qui a priorité sur la sélection présente dans les champs **Importation client à partir de Shopify** et **Type de mappage client**. Il est utilisé dans la commande vente importée.
2. Définir le **Code modèle client**, qui est utilisé pour créer des clients manquants, si l’option **Créer automatiquement des clients inconnus** est activée. Si **Code modèle client** est vide, la fonction utilise le **Code modèle client** défini dans la page **Fiche magasin Shopify**.
3. Dans certains cas, **Code modèle client** par pays ne suffit pas pour assurer le calcul correct des taxes. Par exemple, pour les pays avec taxe de vente.

> [!NOTE]  
> Les codes pays sont les codes pays ISO 3166-1 alpha-2. Pour plus d’informations, voir [Code pays](https://help.shopify.com/en/api/custom-storefronts/storefront-api/reference/enum/countrycode).

## <a name="export-customers-to-shopify"></a>Exporter les clients dans Shopify

Les clients existants peuvent être exportés dans Shopify en bloc. Par conséquence, un client et une adresse par défaut sont créés. Les paramètres suivants permettent de gérer le processus :

|Champ|Désignation|
|------|-----------|
|**Exporter les clients dans Shopify**|Sélectionnez si vous prévoyez d’exporter tous les clients avec une adresse e-mail valide à partir de [!INCLUDE[prod_short](../includes/prod_short.md)] dans Shopify en bloc, soit manuellement en utilisant l’action **Synchroniser les clients**, soit via la file d’attente des tâches pour les mises à jour récurrentes.|
|**Peut mettre à jour les clients Shopify**|Utilisé avec **Exporter le client dans Shopify**. Activez-le pour générer des mises à jour ultérieurement à partir de [!INCLUDE[prod_short](../includes/prod_short.md)] pour les clients qui existent déjà dans Shopify.|

> [!NOTE]  
> Dès que vous avez créé des clients dans Shopify, vous souhaitez peut-être leur envoyer des invitations directes. Cela les encouragera à activer leur compte.

### <a name="populate-customer-information-in-shopify"></a>Remplir les informations client dans Shopify

Un client dans Shopify a un prénom, un nom de famille, une adresse e-mail et/ou un numéro de téléphone. Vous pouvez renseigner le prénom et le nom en fonction des données présentes dans la fiche client dans [!INCLUDE[prod_short](../includes/prod_short.md)].

|Priorité|Champ de la fiche client|Désignation|
|------|------|-----------|
|0|**Nom du contact**|Priorité la plus élevée, si le champ **Nom du contact** est rempli et si le champ **Source du contact** dans la page **Fiche magasin Shopify** contient les options *Prénom et nom* ou *Nom et prénom*, ce qui définit comment diviser les valeurs.|
|2|**Nom 2**|Si le champ **Nom 2** est rempli et si le champ **Source nom 2** dans la page **Fiche magasin Shopify** contient les options *Prénom et nom* ou *Nom et prénom*, ce qui définit comment diviser les valeurs.|
|3|**Nom**|Priorité la moins élevée, si le champ **Nom** est rempli et si le champ **Origine nom** dans la page **Fiche magasin Shopify** contient les options *Prénom et nom* ou *Nom et prénom*, ce qui définit comment diviser les valeurs.|

Un client dans Shopify a également une adresse par défaut qui, en plus du prénom, du nom, de l’e-mail et/ou du téléphone, peut contenir la société et l’adresse. Vous pouvez remplir le champ **Société** en fonction des données présentes dans la fiche client dans [!INCLUDE[prod_short](../includes/prod_short.md)].

|Priorité|Champ de la fiche client|Désignation|
|------|------|-----------|
|0|**Nom**|Priorité la plus élevée, si le champ **Origine nom** dans la page **Fiche magasin Shopify** contient *Nom de la société*.|
|2|**Nom 2**|Priorité la moins élevée, si le champ **Source nom 2** dans la page **Fiche magasin Shopify** contient *Nom de la société*.|

Pour les adresses où le pays/la province est utilisé(e), sélectionnez *Code* ou *Nom* dans le champ **Source pays** dans la page **Fiche magasin Shopify** pour préciser le type de données à stocker dans [!INCLUDE[prod_short](../includes/prod_short.md)] dans le champ **Pays**.

## <a name="sync-customers"></a>Synchroniser les clients

1. Accédez à l’icône de recherche ![Ampoule qui ouvre la fonction de recherche.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , saisissez **Magasin Shopify**, puis choisissez le lien associé.
2. Sélectionnez le magasin pour lequel vous voulez synchroniser les clients pour ouvrir la page **Fiche magasin Shopify**.
3. Sélectionnez l’action **Synchroniser les clients**.

Sinon, vous pouvez utiliser l’action **Lancer la synchronisation des clients** dans la fenêtre **Clients Shopify** ou rechercher le traitement par lots **Synchroniser les clients**.

## <a name="see-also"></a>Voir aussi

[Mise en route du connecteur pour Shopify](get-started.md)  