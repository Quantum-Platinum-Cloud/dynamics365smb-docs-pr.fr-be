---
title: "Procédure : exporter et importer des flux de travail | Microsoft Docs"
description: "Pour transférer des workflows vers d'autres bases de données [!INCLUDE[d365fin](includes/d365fin_md.md)], par exemple pour gagner du temps lors de la création de workflows, vous pouvez exporter et importer des workflows."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-financials
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 07/01/2017
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: 2c13559bb3dc44cdb61697f5135c5b931e34d2a8
ms.openlocfilehash: 8126d3850103819e885d9d131ca3074f1b7cfda1
ms.contentlocale: fr-be
ms.lasthandoff: 09/22/2017

---
# <a name="how-to-export-and-import-workflows"></a>Procédure : exporter et importer des workflows
Pour transférer des workflows vers d'autres bases de données [!INCLUDE[d365fin](includes/d365fin_md.md)], par exemple pour gagner du temps lors de la création de workflows, vous pouvez exporter et importer des workflows.  

 Un autre moyen rapide de créer des workflows consiste à les créer à partir de modèles de workflow. Pour plus d'informations, reportez\-vous à [Procédure : créer des flux de travail à partir de modèles de flux de travail](across-how-to-create-workflows-from-workflow-templates.md).  

 Dans la fenêtre **Workflow**, créez un workflow en répertoriant les étapes concernées sur les lignes. Chaque étape comprend un événement de workflow modéré par des conditions d'événement, et une réponse de workflow modérée par des options de réponse. Définissez les étapes de workflow en renseignez les champs des lignes de workflow à partir de listes fixes de valeurs d'événement et de réponse qui sont les scénarios pris en charge par le code d'application. Pour plus d'informations, reportez\-vous à [Procédure : créer des flux de travail](across-how-to-create-workflows.md).  

## <a name="to-export-a-workflow"></a>Pour exporter un workflow  
1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Flux de travail**, puis sélectionnez le lien connexe.  
2.  Sélectionnez un flux de travail, puis sélectionnez l'action **Exporter vers un fichier**.  
3.  Dans la fenêtre **Exporter fichier**, cliquez sur le bouton **Enregistrer**.  
4.  Dans la fenêtre **Exporter**, sélectionnez un emplacement de fichier, puis choisissez le bouton **Enregistrer**.  

## <a name="to-import-a-workflow"></a>Pour importer un workflow  
1.  Sélectionnez l'icône ![Page ou état pour la recherche](media/ui-search/search_small.png "Page ou état pour la recherche"), entrez **Flux de travail**, puis sélectionnez le lien connexe.  
2.  Choisissez l'action **Importer à partir d'un fichier**.  
3.  Dans la fenêtre **Importer**, sélectionnez le fichier XML contenant le workflow, puis choisissez le bouton **Ouvrir**.  

> [!CAUTION]  
>  Si le code du workflow existe déjà dans la base de données, les étapes du workflow sont remplacées avec celles du workflow importé.  

## <a name="see-also"></a>Voir aussi  
 [Procédure : créer des workflows](across-how-to-create-workflows.md)   
 [Procédure : créer des workflows à partir de modèles de workflow](across-how-to-create-workflows-from-workflow-templates.md)   
 [Procédure : afficher des instances d'étape de workflow archivées](across-how-to-view-archived-workflow-step-instances.md)   
 [Procédure : supprimer des workflows](across-how-to-delete-workflows.md)   
 [Procédure pas à pas : Configuration et utilisation d'un flux d'approbation achat](walkthrough-setting-up-and-using-a-purchase-approval-workflow.md)   
 [Paramétrage des workflows](across-set-up-workflows.md)   
 [Utilisation des workflows](across-use-workflows.md)   
 [Flux de travail](across-workflow.md)   
