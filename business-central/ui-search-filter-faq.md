---
title: "À propos de la recherche et du filtrage dans Business Central"
description: "Réponses aux questions posées fréquemment sur la recherche et le filtre."
author: mikebcMSFT
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: keyboarding, productivity, how do i, filter pane
ms.date: 10/01/2018
ms.author: mikebc
ms.translationtype: HT
ms.sourcegitcommit: 9dbd92409ba02281f008246194f3ce0c53e4e001
ms.openlocfilehash: b34acf29e142ef1a892f6c3c5a0ce2b6b8f7cb29
ms.contentlocale: fr-be
ms.lasthandoff: 09/28/2018

---

# <a name="about-searching-and-filtering-in-included365finincludesd365finmdmd"></a>À propos de la recherche et du filtrage dans [!INCLUDE[d365fin](includes/d365fin_md.md)]
Cet article répond à des questions courantes que vous pouvez avoir à propos de la recherche et du filtrage.

## <a name="is-there-a-difference-between-searching-and-filtering"></a>Existe-t-il une différence entre la recherche et le filtrage ?
Oui.
- La recherche est simples et large : elle faire correspondre des enregistrements contenant le texte de recherche dans tous les champs visibles de la page, puis ne respecte pas la casse.
- Le filtrage est très flexible et peut être appliqué à des champs spécifiques, notamment ceux qui ne sont pas visibles dans la page : il affiche les enregistrements qui comportent des correspondances exactes et respectant la casse, mais il peut être ajusté avec des symboles, des jetons et des formules de recherche puissants. Pour plus d'informations sur l'utilisation de ces fonctions, voir [Tri, recherche et filtrage dans les listes](ui-enter-criteria-filters.md)

## <a name="is-there-a-keyboard-experience-for-search-and-filter"></a>Existe-t-il une expérience clavier pour la recherche et le filtre ?
La recherche et le filtre ont été fortement optimisés pour les utilisateurs qui préfèrent l'interaction sans souris pour utiliser efficacement leurs données. Il existe un grand choix de touches de raccourci qui peuvent être utilisées dans l'ordre pour travailler à grande vitesse. Pour plus d'informations, reportez-vous à [Raccourcis clavier](keyboard-shortcuts.md#KeyboardFilter).

## <a name="is-the-filter-pane-available-on-all-lists"></a>Le volet Filtre est-il disponible sur toutes les listes ?
Le volet Filtre est disponible sur les écrans où la liste est le principal contenu sur la page, tels que des feuilles de calcul et des pages de liste, y compris les listes accessibles depuis la barre de navigation. Le volet Filtre n'est pas encore disponible pour les listes intégrées, telles que les lignes vente sur les commandes vente, ou pour les listes avec des colonnes dynamiques (souvent appelées pages matricielles). 

## <a name="how-can-i-save-my-filters"></a>Comment enregistrer mes filtres ?
Vos filtres et ajustements des filtres prédéfinis sont enregistrés tout au long de la session (lorsque vous restez connecté), même si vous quittez la page. Il n'est actuellement pas possible de sauvegarder définitivement les filtres.
Contrairement aux filtres, le texte de recherche n'est pas conservé lorsque vous quitté une page.

## <a name="is-this-the-same-as-advanced-filters-and-limit-totals-in-microsoft-dynamics-nav"></a>Est-e pareil qu'avec les filtres avancés et les totaux de limite dans Microsoft Dynamics NAV ?
[!INCLUDE[d365fin](includes/d365fin_md.md)] s'appuie sur ces fonctions populaires et présente une expérience moderne et extrêmement utilisable pour rechercher et analyser vos données. Avec plus de raccourcis clavier et l'introduction de la recherche, [!INCLUDE[d365fin](includes/d365fin_md.md)] surpasse la fonctionnalité fournie dans Dynamics NAV.

## <a name="can-i-search-and-filter-using-the-companion-apps-and-outlook-addin"></a>Puis-je rechercher et filtrer à l'aide des applications complémentaires et Outlook AddIn ?
Sur différents facteurs d'écrans tels que des appareils mobiles ou dans Outlook, vous pouvez rechercher dans les listes mais ne pouvez pas filtrer sur les différents champs dans la plupart des cas.

## <a name="is-the-filter-pane-available-for-filtering-reports"></a>Le volet Filtre est-il disponible pour filtrer les états ?
Non. La boîte de dialogue de filtre d'état, généralement considérée comme la page de demande, utilise actuellement une expérience différente qui fournit certaines, mais pas toutes, les capacités du volet Filtre.

## <a name="will-microsoft-extend-the-filter-pane-experience"></a>Microsoft étendra-il l'expérience du volet Filtre ?
Chez Microsoft, nous écoutons constamment les commentaires de notre communauté diverse d'utilisateurs et prenons les mesures nécessaires pour agir sur les principales propositions de la communauté. Si vous souhaitez étendre le volet Filtre à plus de facteurs d'écrans, plus de types de listes et d'états, ou que vous avez une excellente idée pour l'améliorer, ajoutez une idée ou votez pour les idées existantes à l'adresse [aka.ms/BusinessCentralIdeas](https://aka.ms/businesscentralideas).

## <a name="can-i-do-anything-about-the-searching-for-rows-is-taking-too-long-message"></a>Puis-je faire quelque chose concernant le message « La recherche de lignes prend trop de temps » ?

Il existe une limite de temps concernant une opération de recherche. Premièrement, essayez de modifier les critères de recherche et recherchez à nouveau. Si vous utilisez [!INCLUDE[prodshort](includes/prodshort.md)] local, contactez votre administrateur système, parce qu'un administrateur peut augmenter le délai des recherches.

En tant qu'administrateur local, vous développez le délai des recherches en modifiant le paramètre **Expiration de la recherche** du serveur [!INCLUDE[prodshort](includes/prodshort.md)]. Pour plus d'informations, voir [Configuration de Business Central Server](https://docs.microsoft.com/en-us/dynamics365/business-central/dev-itpro/administration/configure-server-instance?#Database) dans l'Aide destinée aux développeurs et aux professionnels de l'informatique Business Central.

## <a name="see-also"></a>Voir aussi .
[Mise en route](product-get-started.md)  
[Tri, recherche et filtrage dans les listes](ui-enter-criteria-filters.md)
