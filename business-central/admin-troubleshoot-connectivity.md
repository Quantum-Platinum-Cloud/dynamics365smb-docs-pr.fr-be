---
title: Résoudre les problèmes de connectivité
description: Décrit comment utiliser la page Résolution des problèmes de connectivité pour identifier et résoudre les problèmes de connexion à Business Central Online.
author: jswymer
ms.service: dynamics365-business-central
ms.topic: get-started-article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: connectivity, troubleshooting, connection problems
ms.date: 06/17/2021
ms.author: jswymer
ROBOTS: NOINDEX
ms.openlocfilehash: db7b9e602817d7dddcf6bce1b35ede078bd70aa0
ms.sourcegitcommit: a7cb0be8eae6ece95f5259d7de7a48b385c9cfeb
ms.translationtype: HT
ms.contentlocale: fr-BE
ms.lasthandoff: 07/08/2021
ms.locfileid: "6443194"
---
# <a name="troubleshoot-connectivity-for-business-central"></a>Résoudre les problèmes de connectivité pour Business Central

> **S’APPLIQUE À :** [!INCLUDE[prod_short](includes/prod_short.md)] en ligne
>
> Cette fonctionnalité est disponible actuellement en mode Aperçu. La fonctionnalité et la documentation peuvent changer dans les versions ultérieures. Si vous souhaitez contribuer à la documentation sur la base de vos propres découvertes, veuillez sélectionner ![Modifier l’article dans GitHub.](media/github-edit-pencil.png) **Modifier**, et proposez des modifications. Ensuite, jetons-y un œil !

[!INCLUDE[prod_short](includes/prod_short.md)] en ligne comprend la page **Résoudre les problèmes de connectivité** que vous pouvez utiliser pour identifier les problèmes de connexion au service en ligne. Plusieurs éléments affectent la connectivité à Business Central, comme les paramètres de pare-feu de votre réseau ou la configuration du service de nom de domaine. La page vous permet d’exécuter une liste de vérifications qui diagnostiqueront les problèmes de connectivité courants de Business Central. Vous pouvez utiliser les informations pour essayer de résoudre les problèmes vous-même ou les transmettre à votre représentant de l’assistance technique.

> [!NOTE]
> La page **Résoudre les problèmes de connectivité** ne teste pas les performances ou la fiabilité du réseau, comme la vitesse de votre connexion. Il vérifie uniquement la connectivité aux différentes ressources.

## <a name="start-the-connectivity-check"></a>Lancer le contrôle de connectivité 

1. Sélectionnez [ce lien](https://businesscentral.dynamics.com/connectivity) ou ouvrez votre navigateur Internet et saisissez l’URL suivante dans l’adresse :

    ```http
    https://businesscentral.dynamics.com/connectivity
    ```

2. Sur la page **Résoudre les problèmes de connectivité**, choisissez **Démarrer la vérification**.

    Une série de vérifications est exécutée et le résultat de chaque vérification est affiché :

    - ![La vérification de la connectivité a réussi.](media/connectivity-check.png) Indique que le contrôle a réussi.
    - ![Échec de la vérification de la connectivité.](media/connectivity-failed.png) indique que le contrôle a échoué. Consultez le message sous la coche pour plus de détails.
    - ![Le contrôle de connectivité n’a pas été exécuté.](media/connectivity-blocked.png) Indique que la vérification n’a pas été exécutée, généralement en raison d’un échec d’une vérification précédente. Consultez le message sous la coche pour plus de détails.

3. Pour relancer la vérification, choisissez **Redémarrer la vérification**.

Les sections suivantes expliquent les vérifications exécutées et fournissent quelques conseils pour résoudre les problèmes.

## <a name="basic-internet-connectivity"></a>Connectivité Internet principale

Vérifie que vous avez une connexion à Internet en vérifiant que vous pouvez accéder à un domaine public connu, comme www.bing.com.

|Problème|Choses à essayer|
|-------|-------------|
|Votre navigateur ne prend pas en charge cette vérification|Ouvrez la page dans un navigateur pris en charge et réessayez. Pour consulter la liste des navigateurs pris en charge, consultez [Configuration minimale requise pour l’utilisation de Business Central - Navigateurs](product-requirements.md#browsers).|
|Échec de la commande ping du serveur à l’URL suivante : {url}|Vérifiez les paramètres de pare-feu.|

## <a name="cdn-content-delivery-network-resources-loading"></a>Chargement des ressources CDN (réseau de diffusion de contenu)

[!INCLUDE[prod_short](includes/prod_short.md)] utilise Azure Content Delivery Network (CDN) pour fournir les ressources nécessaires à l’exécution du client Web Business Central. Cette vérification vérifie que les ressources requises sont disponibles et accessibles en attribuant une commande ping à l’instance Business Central dans le CDN.

|Problème|Choses à essayer|
|-------|-------------|
|Votre navigateur ne prend pas en charge cette vérification|Voir la vérification **Connectivité Internet principale**.|
|Échec de la commande ping du serveur à l’URL suivante : {url}|Vérifiez les paramètres de pare-feu.|

## <a name="user-authentication"></a>Authentification de l’utilisateur

Vérifie que l’utilisateur actuel s’est connecté avec un compte Business Central valide.

|Problème|Choses à essayer|
|-------|-------------|
|Aucun utilisateur n’est actuellement authentifié|Connectez-vous à Business Central avec un nom d’utilisateur et un mot de passe valides.|

## <a name="business-central-environments-discovery"></a>Découverte des environnements Business Central

Recherche les environnements Business Central disponibles pour un utilisateur authentifié, puis vérifie si l’utilisateur peut être authentifié dans l’environnement.
<!-- example: Your user name or password is incorrect, or you do not have a valid account.. Request duration: 332 milliseconds)-->

|Problème|Choses à essayer|
|-------|-------------|
|Aucun utilisateur authentifié pour effectuer cette vérification|Voir la vérification **Authentification utilisateur**.|
|Échec de la récupération des environnements disponibles pour votre compte.|Consultez la liste des environnements disponibles dans le centre d’administration de Business Central.|
|Votre nom d’utilisateur ou mot de passe n’est pas correct, ou vous n’avez pas de compte valide.| Vérifiez que vous vous êtes connecté en utilisant le nom d’utilisateur et le mot de passe corrects.|

## <a name="application-service-connectivity"></a>Connectivité des services d’application

Vérifie que l’utilisateur authentifié peut se connecter à un environnement découvert, en commençant généralement par l’environnement de production.

|Problème|Choses à essayer|
|-------|-------------|
|Aucun utilisateur authentifié pour effectuer cette vérification|Voir la **Vérification de l’authentification utilisateur**.|
|Échec de la récupération des environnements disponibles pour votre compte.|Voir **Découverte des environnements Business Central**.|
|Aucune adresse de regroupement pour laquelle effectuer cette vérification|Consultez la liste des environnements disponibles dans le centre d’administration de Business Central.|
|Le point de terminaison de la version n’existe pas|Consultez la liste des environnements disponibles dans le centre d’administration de Business Central.|

## <a name="see-also"></a>Voir aussi

[Ressources pour l’Aide et le support](product-help-and-support.md)  
[Aperçu des tâches permettant de paramétrer Business Central](setup.md)  
[Foire aux questions sur l’utilisation de Business Central](across-faq.yml)  
[Utilisation de [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  
[Centre d’administration Business Central](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center)

[!INCLUDE[footer-include](includes/footer-banner.md)]