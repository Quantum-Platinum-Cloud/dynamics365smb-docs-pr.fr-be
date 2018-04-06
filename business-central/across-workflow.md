---
title: Workflow | Microsoft Docs
description: "Vous pouvez configurer et utiliser des workflows qui connectent des tâches de processus entreprise exécutées par différents utilisateurs. Les tâches du système, telles que la validation automatique, peuvent être incluses comme étapes du workflow, précédées ou suivies des tâches de l'utilisateur. Demander et accorder une approbation pour créer des enregistrements sont des étapes classiques du workflow."
services: project-madeira
documentationcenter: 
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: 
ms.date: 02/20/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 06783cab93ae83111b9646de7c8577fb0669d466
ms.contentlocale: fr-be
ms.lasthandoff: 03/22/2018

---
# <a name="workflow"></a>Flux de travail
Vous pouvez configurer et utiliser des workflows qui connectent des tâches de processus entreprise exécutées par différents utilisateurs. Les tâches du système, telles que la validation automatique, peuvent être incluses comme étapes du workflow, précédées ou suivies des tâches de l'utilisateur. Demander et accorder une approbation pour créer des enregistrements sont des étapes classiques du workflow.  

 Dans la fenêtre **Workflow**, créez un workflow en répertoriant les étapes concernées sur les lignes. Chaque étape comprend un événement de workflow modéré par des conditions d'événement, et une réponse de workflow modérée par des options de réponse. Définissez les étapes de workflow en renseignez les champs des lignes de workflow à partir de listes fixes de valeurs d'événement et de réponse qui sont les scénarios pris en charge par le code d'application.  

 La version générique de [!INCLUDE[d365fin](includes/d365fin_md.md)] inclut plusieurs workflows préconfigurés, représentés par des modèles de workflow que vous pouvez copier pour créer des workflows. Le code des modèles de workflow ajoutés par Microsoft a le préfixe « MS- ». Pour plus d'informations, voir la liste des modèles de workflow dans la fenêtre Modèles flux de travail.  

 Si un scénario d'entreprise requiert un événement ou une réponse de workflow qui n'est pas pris en charge, un partenaire Microsoft doit l'implémenter en personnalisant le code de l'application. Pour plus d'informations, voir [Procédure pas à pas : implémentation de nouveaux événements et réponses de flux de travail](/dynamics-nav/Walkthrough--Implementing-New-Workflow-Events-and-Responses) dans l'Aide destinée aux développeurs et aux professionnels de l'informatique.  

 Le tableau suivant décrit une série de tâches et inclut des liens vers les rubriques qui les décrivent.  

|**Pour**|**Voir**|  
|------------|-------------|  
|Configurer des utilisateurs du workflow, spécifier comment les utilisateurs sont notifiés et créer des workflows. Pour de nouveaux workflows pour des scénarios non pris en charge, implémentez les éléments requis du workflow en personnalisant le code d'application.|[Paramétrage des workflows](across-set-up-workflows.md)|  
|Activer des workflows, agir sur les notifications du workflow, notamment les approbations de demandes et approuver des demandes pour effectuer une étape du workflow. Archiver et supprimer des workflows.|[Utilisation des workflows](across-use-workflows.md)|  

## <a name="see-also"></a>Voir aussi  
[Ventes](sales-manage-sales.md)  
[Achats](purchasing-manage-purchasing.md)  
[Gestion des projets](projects-manage-projects.md)  
[Utilisation de [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
