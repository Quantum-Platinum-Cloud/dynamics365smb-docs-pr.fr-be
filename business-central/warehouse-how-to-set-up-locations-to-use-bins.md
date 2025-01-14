---
title: Comment configurer des magasins de sorte qu’ils utilisent des emplacements
description: Les emplacements représentent la structure d’entrepôt de base et sont utilisés pour faire des propositions relatives à l’emplacement des articles.
author: brentholtorf
ms.author: bholtorf
ms.reviewer: andreipa
ms.topic: how-to
ms.date: 03/28/2023
ms.custom: bap-template
---

# <a name="set-up-locations-to-use-bins" />Configurer des magasins de sorte qu’ils utilisent des emplacements

Les emplacements représentent la structure de base de l’entrepôt et peuvent suggérer où placer les articles. Lorsque vous avez créé vos emplacements, vous pouvez définir leur contenu ou ils sont utilisés en tant qu’emplacements dynamiques sans contenu spécifié.

Pour utiliser la fonctionnalité d’emplacement liée au magasin, activez le bouton à bascule **Emplacement obligatoire** sur la page fiche **Magasin**. Après avoir activé le bouton à bascule, le **Code emplacement** et le **Code zone** sont disponibles sur les documents suivants :

* En-tête réception entrepôt
* Lignes réception entrepôt
* Lignes rangement entrepôt
* En-tête expédition entrepôt
* Lignes expédition entrepôt
* Lignes rangement entrepôt

Ensuite, vous définissez la circulation des articles dans le magasin en spécifiant les codes emplacement dans les champs de configuration qui représentent les différents flux.  

> [!NOTE]  
> Avant de pouvoir spécifier les codes emplacement sur un magasin, vous devez les créer. Pour plus d’informations, voir [Créer emplacements](warehouse-how-to-create-individual-bins.md).  

## <a name="to-set-up-a-location-to-use-bins" />Pour configurer un magasin de sorte qu’il utilise des emplacements

1. Sélectionnez l’icône ![Ampoule qui ouvre la fenêtre de recherche.](media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **Emplacements**, puis choisissez le lien associé.  
2. Sélectionnez le magasin dans lequel vous souhaitez utiliser des emplacements.  
3. Choisissez l’action **Modifier**.  
4. Sur le raccourci **Entrepôt**, cochez la case **Emplacement obligatoire**.  
5. Si vous n’avez pas recours à un prélèvement et à un rangement suggérés dans le magasin, renseignez le champ **Sélection emplacement par déf** en y indiquant la méthode d’attribution d’un emplacement par défaut à un article que [!INCLUDE [prod_short](includes/prod_short.md)] doit utiliser.  
6. Ouvrez la fiche de l’emplacement pour lequel vous souhaitez configurer des emplacements.
7. Sur le raccourci **Emplacements**, sélectionnez les emplacements que vous voulez utiliser par défaut pour les réceptions, les expéditions, les enlogements et les désenlogements, ainsi que pour les emplacements atelier ouverts.  

    Les codes emplacement que vous indiquez ici s’affichent automatiquement dans les en-têtes et sur les lignes de différents documents entrepôt. Les emplacements par défaut définissent tous les placements de début ou de fin des articles dans l’entrepôt.  
8. En cas d’utilisation d’un prélèvement et d’un rangement suggérés, sélectionnez un emplacement pour les ajustements entrepôt. Le code emplacement du champ **Code emplacement ajustement** définit l’emplacement virtuel dans lequel le programme enregistre les différences de stock lorsque vous enregistrez :

    * Lorsque vous observez des différences enregistrées dans la feuille article de l’entrepôt
    * Différences que le programme calcule lorsque vous enregistrez un inventaire entrepôt  
9. En option : Sur le raccourci **Stratégies d’entrepôt**, renseignez les champs. Les champs les plus importants sont les suivants : **Politique capacité empl**, **Autoriser déconditionnement** et **Code modèle rangement**.  
10. Sur les champs **Entrepôt**, renseignez les champs **Délai désenlogement**, **Délai enlogement** et **Code calendrier principal**. Pour en savoir plus, rendez-vous sur [Configurer les calendriers de base](across-how-to-assign-base-calendars.md).

## <a name="fill-in-the-consumption-bin" />Renseigner l’emplacement consommation

Ce graphique indique comment le champ **Code emplacement** sur les lignes composant O.F. est renseigné en fonction de la configuration de votre emplacement.

:::image type="content" source="media/binflow.png" alt-text="Champ de code d’emplacement sur les lignes de composant d’ordre de fabrication.":::

## <a name="see-related-microsoft-trainingtrainingmodulesconfigure-bins-location" />Voir la [formation Microsoft](/training/modules/configure-bins-location/) associée

## <a name="see-also" />Voir aussi

[Vue d’ensemble de la gestion des entrepôts](design-details-warehouse-management.md)
[Stock](inventory-manage-inventory.md)  
[Configuration de la gestion des entrepôts](warehouse-setup-warehouse.md)  
[Gestion des assemblages](assembly-assemble-items.md)  
[Utiliser [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
