---
title: Création et configuration d’un compte Shopify
description: Découvrez comment obtenir un compte Shopify afin de pouvoir démontrer le workflow d’intégration Shopify et Business Central.
ms.date: 06/21/2022
ms.topic: article
ms.service: dynamics365-business-central
ms.reviewer: solsen
author: AndreiPanko
ms.author: andreipa
ms.openlocfilehash: b4449b573307582595ee9949dcb53d5d553ce0f2
ms.sourcegitcommit: bb6ecb20cbd82fdb5235e3cb426fc73c29c0a7ae
ms.translationtype: HT
ms.contentlocale: fr-BE
ms.lasthandoff: 11/23/2022
ms.locfileid: "9803074"
---
# <a name="create-and-set-up-a-shopify-account"></a>Création et configuration d’un compte Shopify

Si vous envisagez d’utiliser Shopify comme solution d’e-commerce et avez besoin d’un compte Shopify pour valider le workflow intégré, vous disposez des options suivantes :

- Obtenir une version d’essai. C’est le point de départ typique pour les utilisateurs finaux.  
- Créer des magasins de développement. Cette approche est destinée aux partenaires qui font des démonstrations récurrentes, des formations et fournissent une assistance.

## <a name="trial-end-user"></a>Essai (utilisateur final)

Accédez au [site web Shopify](https://www.shopify.com) et utilisez votre compte de messagerie pour le compte administrateur afin de vous inscrire pour un essai gratuit. Pour plus d’informations sur la création et la personnalisation de votre boutique en ligne, voir le [Centre d’aide de Shopify](https://help.shopify.com/).

Dans **Administration de Shopify** de la boutique créée, appliquez les **Paramètres** suivants :

- Désactivez **Archiver automatiquement la commande** dans la section **Traitement des commandes** des paramètres [**Validation**](https://www.shopify.com/admin/settings/checkout) dans l’**administration Shopify**.
- Envisagez d’activer *Afficher le lien de connexion dans la vitrine et le paiement* dans la section **Paramètres du compte client** des paramètres de paiement.
- Envisagez de sélectionner l’option *Nom de l’entreprise – Facultatif* dans la section **Informations client** des paramètres de paiement.
- Activez l’option **Afficher les options de pourboire au moment du paiement** dans la section **Pourboire** des paramètres de paiement, si vous prévoyez de démontrer pourboire.
- Activez les paiements tests. Deux options s’offrent à vous. Commencez par accéder aux paramètres [**Paiements**](https://www.shopify.com/admin/settings/payments) :  
  1. *(pour les tests) Bogus Gateway*. Pour plus d’informations, voir [Activer Bogus Gateway pour les tests](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify payments* en mode Test. Pour plus d’informations, voir [Test Shopify Payments](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

- Sélectionnez un plan dans les paramètres [**Plan**](https://www.shopify.com/admin/settings/plan) pour pouvoir tester le processus de paiement.

> [!Important]  
> Pour éviter les paiements, n’oubliez pas d’annuler votre essai Shopify.

## <a name="development-store"></a>Magasin de développement

Commencez par rejoindre le [programme Fournisseur Shopify](https://help.shopify.com/partners/about). Ensuite, utilisez le **tableau de bord des partenaires** pour créer la boutique de développement. Pour plus d’informations, consultez [Création des boutiques de développement](https://help.shopify.com/partners/dashboard/managing-stores/development-stores).

Après la création de la boutique dans **Administration de Shopify** de la boutique créée, appliquez les **Paramètres** suivants :

- Désactivez **Archiver automatiquement la commande** dans la section **Traitement des commandes** des paramètres [**Validation**](https://www.shopify.com/admin/settings/checkout) dans l’**administration Shopify**.
- Envisagez d’activer *Afficher le lien de connexion dans la vitrine et le paiement* dans la section **Paramètres du compte client** des paramètres de paiement.
- Envisagez de sélectionner l’option *Nom de l’entreprise – Facultatif* dans la section **Informations client** des paramètres de paiement.
- Si vous prévoyez de démontrer pourboire, activez l’option **Afficher les options de pourboire au moment du paiement** dans la section **Pourboire** des paramètres de paiement.
- Activez les paiements tests. Deux options s’offrent à vous. Commencez par accéder aux paramètres [**Paiements**](https://www.shopify.com/admin/settings/payments) :  
  1. *(pour les tests) Bogus Gateway*. Pour plus d’informations, voir [Activer Bogus Gateway pour les tests](https://help.shopify.com/en/manual/checkout-settings/test-orders#place-a-test-order-by-simulating-a-transaction).
  2. *Shopify payments* en mode Test. En savoir plus sur la [Test de Shopify Payments](https://help.shopify.com/en/manual/payments/shopify-payments/testing-shopify-payments).

## <a name="see-also"></a>Voir aussi

[Mise en route avec le connecteur Shopify](get-started.md)  
[Procédure pas à pas : configurer et utiliser le connecteur Shopify](walkthrough-setting-up-and-using-shopify.md)