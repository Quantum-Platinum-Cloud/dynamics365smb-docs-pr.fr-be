---
author: edupont04
ms.topic: include
ms.date: 04/01/2021
ms.author: edupont
ms.openlocfilehash: 5c99520c40098f568df543ccda2996639e22dcb8
ms.sourcegitcommit: cdb57f14960f58b1d36a1b373fbf35dfed5fad9e
ms.translationtype: HT
ms.contentlocale: fr-BE
ms.lasthandoff: 02/23/2022
ms.locfileid: "8334753"
---
Le tableau suivant décrit certains des principaux états dans les états de stock et d’entrepôt.

| État | Description | ID | 
|---------|---------|---------|
|[Échéancier des dispo. de stock](https://businesscentral.dynamics.com?report=707)|Si vous souhaitez avoir un aperçu d’articles/de points de stock spécifiques et de leur disponibilité. Cet état affiche des valeurs cumulées telles que les besoins bruts, les réceptions planifiées et prévues, le stock, etc. |707|
|[Évaluation du stock](https://businesscentral.dynamics.com?report=1001)|Affiche l’évaluation du stock des articles sélectionnés dans votre stock. L’état indique également des informations sur la valeur des augmentations et des diminutions de stock au fil du temps.|1 001|
|[Date expiration article : Quantité](https://businesscentral.dynamics.com?report=5809)|Propose une vue d’ensemble des quantités des articles sélectionnés dans le stock dont les dates d’expiration sont incluses dans une période donnée. La liste indique le nombre d’unités de l’article sélectionné qui expirent à une date donnée. Pour chaque article spécifié lors du paramétrage de l’état, le document imprimé indique le nombre d’unités qui expirent au cours de trois périodes de même durée et la quantité d’inventaire totale de l’article sélectionné.<br>Vous pouvez définir ce que l’état doit inclure en configurant des filtres. Si vous ne définissez aucun filtre, l’état inclut tous les enregistrements. Les quantités indiquées dans l’état reflètent seulement les quantités des articles pour lesquels des dates d’expiration ont été définies.|5809|
|[Ancienneté stock : Quantité](https://businesscentral.dynamics.com?report=5807)|Affiche un aperçu de l’ancienneté des articles sélectionnés dans votre stock. La liste indique la valeur ou le nombre d’unités de l’article sélectionné qui ont été ajoutées au stock ou supprimées du stock, ainsi que la date d’ajout ou de retrait. Les articles peuvent être ajoutés au stock ou supprimés de ce même stock après des achats, des ventes, et des ajustements positifs ou négatifs.|5807|
|[Ancienneté stock : Valeur](https://businesscentral.dynamics.com?report=5808)|Affiche un aperçu de l’ancienneté des articles sélectionnés dans votre stock. La liste indique la valeur ou le nombre d’unités de l’article sélectionné qui ont été ajoutées au stock ou supprimées du stock, ainsi que la date d’ajout ou de retrait. Les articles peuvent être ajoutés au stock ou supprimés de ce même stock après des achats, des ventes, et des ajustements positifs ou négatifs.|5808|
|[Liste prix et coûts stocks](https://businesscentral.dynamics.com?report=716)|Affiche la liste d’informations sur les prix des articles sélectionnés ou des points de stock : coût unitaire direct, dernier coût direct, prix unitaire, pourcentage de marge et marge. |716|
|[Liste emplacements entrep.](https://businesscentral.dynamics.com?report=7319)|Affiche une vue d’ensemble des emplacements d’entrepôt, leur configuration et la quantité d’articles dans les emplacements. Cet état peut être utilisé pour tous les emplacements, qui ont « emplacement » comme champ obligatoire. |7319|
|[Statut expédition entrepôt](https://businesscentral.dynamics.com?report=7313)|Affiche un aperçu des documents origine ouverts avec les articles expédiés ou devant être expédiés, par magasin. Cet état peut être utilisé pour tous les magasins, pour lesquels **Envois requis** est activé. **Statut expédition entrepôt** affiche les magasins, les codes d’emplacement, le statut du document, les quantités.|7313|
|[Liste des prélèvements stock](https://businesscentral.dynamics.com?report=813)|Affiche la liste des commandes vente dans lesquelles un article est inclus. Les informations suivantes sont données pour chaque article : ligne commande vente avec le nom du client, code variante, code magasin, code emplacement, date d’expédition, quantité à expédier et unité. La quantité à livrer est totalisée pour chaque article. L’état peut être utilisé lorsque des articles vont être retirés du stock.<br>REMARQUE : cette fonctionnalité n’est pas disponible pour les fonctionnalités d’entrepôt avancées.|813|
|[Emplacement ajustement entrepôt](https://businesscentral.dynamics.com?report=7320)|Cet état spécial est destiné uniquement à un entrepôt avancé et affiche les quantités restantes qui sont encore stockées dans l’emplacement ajustement lui-même. Normalement, cet emplacement spécifique doit être vide. La seule raison pour laquelle cet emplacement sera rempli est suite au processus de comptage physique ou si des quantités d’articles ont été retirées ou ajoutées à l’entrepôt|7320|