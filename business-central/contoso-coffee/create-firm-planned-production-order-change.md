---
title: Créer un ordre de fabrication planifié ferme et le modifier
description: Procédure pas à pas pour un gestionnaire de production chez Contoso Coffee qui souhaite créer un ordre de fabrication planifié ferme, puis le modifier.
ms.date: 04/01/2022
ms.topic: article
ms.service: dynamics365-business-central
author: edupont04
ms.author: andreipa
ms.openlocfilehash: 7a057e144ed6825435c62f565eeaaa73974fedf9
ms.sourcegitcommit: 8a12074b170a14d98ab7ffdad77d66aed64e5783
ms.translationtype: HT
ms.contentlocale: fr-BE
ms.lasthandoff: 03/31/2022
ms.locfileid: "8525433"
---
# <a name="walkthrough-create-a-firm-planned-production-order-and-change-it"></a>Procédure pas à pas : Créer un ordre de fabrication planifié ferme et le modifier

Dans cet article, nous vous expliquons comment utiliser les données de démonstration Contoso Coffee pour les ordres de fabrication.  

## <a name="scenario"></a>Scénario

Eduardo, le gestionnaire de production chez Contoso Coffee, doit créer un ordre de fabrication pour 10 unités de l’article **SP-SCM1009, Airpot** dont l’échéance est le 28 avril. Il effectue une planification en arrière et confirme qu’il peut commencer l’ordre le 27 avril.  

Peu de temps après avoir terminé cette tâche, il doit augmenter l’ordre à 50 unités. Lorsqu’il augmente la quantité, la date de début de l’ordre annoncée par la fonctionnalité de planification en arrière est trop tôt. Il planifie donc l’ordre à partir du 23 avril afin de déterminer une date de fin plus réaliste.  

## <a name="steps"></a>Étapes

1. Créez l’ordre de fabrication initial pour 10 unités de l’article **SP-SCM1009, Airpot**.

    1. Sélectionnez ![l’icône Ampoule qui ouvre la fonction Tell Me.](../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") entrez **O.F. planifiés fermes**, puis sélectionnez le lien associé.  

    2. Cliquez sur l’action **Nouveau**, puis renseignez les champs comme indiqué dans le tableau suivant.  

        |Champ  |Valeur  |
        |---------|---------|
        |**Type origine** |Article ;|
        |**N° origine** |SP-SCM1009|
        |**Quantité** |10|
        |**Date d’échéance**|Avril 28  |

    3. Choisissez l’action **Actualiser O.F.**.  

    4. Sur la page **Actualiser O.F.**, acceptez toutes les valeurs par défaut, puis choisissez le bouton **OK** pour démarrer le processus.  

        Dans la configuration actuelle, ce processus utilise la planification en arrière. Dans la nouvelle ligne de l’ordre de fabrication, la date de début est le 26 avril.  

2. Modifiez la quantité de l’ordre de fabrication à 50 unités et planifiez l’ordre.  

    1. Sur le raccourci **Lignes** de la **Nomenclature de production**, sélectionnez la ligne récemment ajoutée, puis, dans le champ **Quantité**, entrez *50*.  

3. Choisissez l’action **Actualiser O.F.**.  

    La date de début est désormais repoussée au 20 avril. Cette date n’est pas acceptable pour Eduardo.

4. Déclenchez une planification en avant de l’ordre de fabrication.

    1. Sur le raccourci **Planifier**, définissez le champ **Date de début** sur *23 avril*.

    La date de début de l’ordre est maintenant le 25 avril et la date de fin est le 2 mai. La date d’échéance de l’ordre est fixée un jour plus tard, le 3 mai. Eduardo sait maintenant que la livraison de l’ordre pour lequel la quantité a été augmentée aura lieu le 3 mai.

> [!NOTE]
> Planifier un ordre en modifiant sa date de début ou de fin ne nécessite pas d’effectuer le traitement par lots **Actualiser O.F.**, car toutes les dates sont recalculées automatiquement.

Le nouvel ordre de fabrication est maintenant mis en place et les exigences d’Eduardo sont satisfaites.  

## <a name="see-also"></a>Voir aussi

[Introduction aux données de démonstration Contoso Coffee](contoso-coffee-intro.md)  