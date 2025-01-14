---
title: 'Impression des déclarations de TVA périodiques [BE]'
description: "La fonction de déclaration de TVA permet d'imprimer les détails des transactions de TVA. Vous devez envoyer trois\_déclarations de TVA aux autorités fiscales belges."
services: project-madeira
documentationcenter: ''
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: null
ms.search.form: '11306,11307,11308'
ms.date: 06/17/2021
ms.author: edupont
---
# <a name="print-periodic-vat-reports-in-the-belgian-version" />Imprimer les déclarations de TVA périodiques dans la version belge
La fonction de déclaration de TVA permet d'imprimer les détails des transactions de TVA. Vous devez envoyer les déclarations de TVA suivantes aux autorités fiscales belges :  

- Déclaration mensuelle/trimestrielle  
- Liste annuelle de TVA (sur papier/disque)  
- TVA - Liste déclaration intracommunautaire (sur papier/disque)  

## <a name="to-print-the-monthlyquarterly-declaration" />Pour imprimer la déclaration mensuelle/trimestrielle

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **Formulaire/Déclaration Intervat**, puis choisissez le lien associé.  
2.  Dans la page **TVA – Formulaire**, renseignez les champs.  

    |Champ|Désignation|  
    |------------------------------------|---------------------------------------|  
    |**N° entreprise incorrect**|Spécifie si vous souhaitez imprimer l'état contenant des numéros d'entreprise incorrects.|  
    |**Liste annuelle de TVA**|Spécifie si vous souhaitez imprimer l'état **Liste annuelle de TVA**.|  
    |**Année**|Entrez l'année de la période pour laquelle vous souhaitez imprimer l'état. Vous devez entrer l'année sous la forme d'un code à quatre chiffres. Par exemple, pour imprimer une déclaration pour 2013, vous devez entrer « 2013 » (au lieu de « 13 »).|  
    |**Montant minimum**|Entrez le solde annuel minimal du client à inclure dans l'état. Si le solde annuel du client est inférieur au montant minimal, le client n'est pas inclus dans la déclaration.|  
    |**Inclure les clients de**|Sélectionnez ce champ pour inclure les clients de tous les pays/régions ou d'un pays/d'une région spécifique dans l'état.|  
    |**Pays/région**|Sélectionnez le pays/la région à inclure dans l'état.|  

3.  Sélectionnez le bouton **Imprimer** pour imprimer l'état, ou le bouton **Aperçu** pour l'afficher à l'écran. Cliquez sur le bouton **Annuler** pour enregistrer les informations sans imprimer l'état.  

## <a name="to-print-the-vat-annual-listing-on-disk" />Pour imprimer la liste annuelle de TVA sur disque

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **Liste annuelle de TVA - Disque**, puis accédez au lien associé.  
2.  Dans la page **Liste annuelle de TVA - Disque**, renseignez les champs comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Année**|Entrez l'année de la déclaration de TVA. Vous devez entrer l'année sous la forme d'un code à quatre chiffres. Par exemple, pour imprimer une déclaration pour 2013, vous devez entrer « 2013 » (au lieu de « 13 »).|  
    |**Minimale**|Entrez le solde annuel minimal du client à inclure dans l'état.<br /><br /> Si le solde annuel du client est inférieur au montant minimal, le client n'est pas inclus dans la déclaration.|  
    |**Déclaration test**|Spécifie si vous souhaitez créer une déclaration test.<br /><br /> Si ce champ est sélectionné, un test d'attribut est écrit dans le fichier qui utilise la valeur 1, indiquant qu'il s'agit d'un fichier test. Si vous souhaitez tester le fichier XML avant de l'envoyer, vous pouvez télécharger ce fichier sur le site Intervat. Le fichier est ensuite validé sans être stocké sur le serveur et vous recevez une notification si le fichier est valide. De plus, le numéro de séquence unique du fichier XML n'est pas augmenté lorsqu'une déclaration de test est créée, ce qui signifie que vous pouvez créer autant de déclarations de test internes que vous le souhaitez.|  
    |**Ajouter un représentant**|Spécifie si vous souhaitez inclure le représentant de la déclaration de TVA.<br /><br /> Un représentant est une personne ou une agence qui a une licence pour créer une déclaration de TVA pour votre société.|  
    |**ID**|Entrez l'ID du représentant chargé de créer la déclaration de TVA.|  
    |**Emplacement**|Entrez le chemin d'accès et le nom du fichier dans lequel vous souhaitez créer la déclaration.|  

3.  Sélectionnez le bouton **Imprimer** pour imprimer l'état, ou le bouton **Aperçu** pour l'afficher à l'écran. Cliquez sur le bouton **Annuler** pour enregistrer les informations sans imprimer l'état.  

## <a name="to-print-the-vat-vies-declaration-report-to-disk" />Pour imprimer l'état TVA - Déclaration intracommunautaire sur disque

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **TVA - Déclaration intracommunautaire sur disque**, puis choisissez le lien associé.  
2.  Entrez les informations nécessaires, puis cliquez sur le bouton **OK** pour lancer le traitement par lots, qui crée un fichier .XML. Pour plus d'informations, voir TVA - Déclaration intracommunautaire sur disque.  
3.  Si vous devez apporter une correction, choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **TVA - Correction déclaration intracommunautaire**, puis choisissez le lien associé.  
4.  Choisissez l'action **Modifier la liste**, puis entrez les informations qui doivent être modifiées. Cliquez sur le bouton **OK**.  

## <a name="see-also" />Voir aussi
 [TVA belge](belgian-vat.md)   
 [Configurer la TVA non déductible](how-to-set-up-non-deductible-vat.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
