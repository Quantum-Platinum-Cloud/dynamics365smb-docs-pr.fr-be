---
title: 'Lettrer les relevés CODA [BE]'
description: 'Une fois qu''un relevé CODA a été importé, les lignes relevé sont accessibles à partir de la page Fiche compte bancaire.'
author: SorenGP
ms.topic: conceptual
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.form: 2000040
ms.date: 06/25/2021
ms.author: edupont
---
# <a name="apply-coda-statements-in-the-belgian-version" />Lettrer des relevés bancaires CODA dans la version belge

Une fois qu'un relevé CODA a été importé, les lignes relevé sont accessibles à partir de la page **Fiche compte bancaire**. Le statut de lettrage sur chaque ligne est vide, car les montants du relevé n'ont pas été lettrés aux écritures comptables ouvertes.  

Les montants du relevé peuvent être lettrés aux écritures comptables ouvertes comme suit :  

-   En lettrant manuellement les lignes relevé CODA.  
-   En lettrant automatiquement les montants du relevé CODA aux écritures comptables et aux comptes appropriés. Le traitement automatique des lignes relevé CODA est recommandé.  

## <a name="to-manually-apply-the-coda-statement-lines" />Pour lettrer manuellement les lignes relevé CODA

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **Comptes bancaires**, puis choisissez le lien associé.  
2.  Sélectionnez le compte bancaire, puis choisissez l'action **Relevés CODA**.  
3.  Sélectionnez le relevé CODA, puis choisissez l'action **Modifier**.  
4.  Pour chaque ligne relevé, renseignez les champs comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**N° compte**|Entrez le numéro du compte général, de la banque, du client, du fournisseur ou de l'immobilisation, auquel la ligne relevé du compte bancaire est associée.|  
    |**Description**|[!INCLUDE[prod_short](../../includes/prod_short.md)] récupère automatiquement la description à partir du fichier CODA importé, mais vous pouvez modifier le contenu de ce champ.|  

5.  Choisissez le bouton **OK**.  

## <a name="to-automatically-apply-the-coda-statement-lines" />Pour lettrer automatiquement les lignes relevé CODA

1.  Choisissez l'icône ![Ampoule qui ouvre la fonction Tell Me.](../../media/ui-search/search_small.png "Dites-moi ce que vous voulez faire") , entrez **Comptes bancaires**, puis choisissez le lien associé.  
2.  Sélectionnez le compte bancaire, puis choisissez l'action **Relevés CODA**.  
3.  Sélectionnez le relevé CODA, puis choisissez l'action **Modifier**.  
4.  Choisissez l'action **Traiter les lignes relevé CODA**.  
5.  Renseignez les champs comme indiqué dans le tableau suivant.  

    |Champ|Désignation|  
    |---------------------------------|---------------------------------------|  
    |**Comptabilisation par défaut**|Sélectionnez ce champ si vous souhaitez que le traitement par lots valide les montants du relevé qui ne peuvent pas être associés aux écritures comptables existantes.|  
    |**Imprimer liste**|Sélectionnez ce champ pour imprimer la liste des montants du relevé qui ne peuvent pas être associés automatiquement.|  

6.  Choisissez le bouton **OK**.  

    Lorsque vous démarrez le traitement par lots, les montants du relevé sont lettrés aux écritures comptables existantes en fonction des codes transaction. Pour plus d'informations, voir [Paramétrer les comptes bancaires pour CODA](how-to-set-up-bank-accounts-for-coda.md).

## <a name="see-also" />Voir aussi
 [Relevés bancaires CODA](coda-bank-statements.md)   
 [Paramétrer les comptes bancaires pour CODA](how-to-set-up-bank-accounts-for-coda.md)   
 [Paramétrer les codes transaction IBLC-BLWI](how-to-set-up-iblc-blwi-transaction-codes.md)   
 [Importer les relevés CODA](how-to-import-coda-statements.md)   
 [Créer des journaux financiers](how-to-create-financial-journals.md)   
 [Transférer et publier automatiquement des relevés CODA](how-to-automatically-transfer-and-post-coda-statements.md)   
 [Transférer et publier manuellement des relevés CODA](how-to-manually-transfer-and-post-coda-statements.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
