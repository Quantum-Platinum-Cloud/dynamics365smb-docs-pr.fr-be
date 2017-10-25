---
title: Workflow | Microsoft Docs
description: "Vous pouvez configurer et utiliser des workflows qui connectent des tâches de processus entreprise exécutées par différents utilisateurs. Les tâches du système, telles que la validation automatique, peuvent être incluses comme étapes du workflow, précédées ou suivies des tâches de l'utilisateur. Demander et accorder une approbation pour créer des enregistrements sont des étapes classiques du workflow."
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
ms.openlocfilehash: f65c0e577e839928809f7afda3dbdb4c9b7702c8
ms.contentlocale: fr-be
ms.lasthandoff: 09/22/2017

---
# <a name="workflow"></a>Flux de travail
Vous pouvez configurer et utiliser des workflows qui connectent des tâches de processus entreprise exécutées par différents utilisateurs. Les tâches du système, telles que la validation automatique, peuvent être incluses comme étapes du workflow, précédées ou suivies des tâches de l'utilisateur. Demander et accorder une approbation pour créer des enregistrements sont des étapes classiques du workflow.  

 Dans la fenêtre **Workflow**, créez un workflow en répertoriant les étapes concernées sur les lignes. Chaque étape comprend un événement de workflow modéré par des conditions d'événement, et une réponse de workflow modérée par des options de réponse. Définissez les étapes de workflow en renseignez les champs des lignes de workflow à partir de listes fixes de valeurs d'événement et de réponse qui sont les scénarios pris en charge par le code d'application.  

 La version générique de [!INCLUDE[d365fin](includes/d365fin_md.md)] inclut plusieurs workflows préconfigurés, représentés par des modèles de workflow que vous pouvez copier pour créer des workflows. Le code des modèles de workflow ajoutés par Microsoft a le préfixe « MS- ». Pour plus d'informations, voir la liste des modèles de workflow dans la fenêtre Modèles flux de travail.  

 Si un scénario d'entreprise requiert un événement ou une réponse de workflow qui n'est pas pris en charge, un partenaire Microsoft doit l'implémenter en personnalisant le code de l'application. Pour plus d'informations, voir [Procédure pas à pas : implémentation de nouveaux événements et réponses de flux de travail](https://msdn.microsoft.com/en-us/library/mt574349.aspx) sur MSDN.  

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
