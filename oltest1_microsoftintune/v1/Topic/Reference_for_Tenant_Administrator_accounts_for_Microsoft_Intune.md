---
description: na
keywords: na
title: Reference for Tenant Administrator accounts for Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e4eff7b9-4dcd-4959-b1d6-97dc4640dbe2
---
# Referenčn&#237; informace t&#253;kaj&#237;c&#237; se &#250;čtů spr&#225;vců klientů pro Microsoft Intune
Každý správce klienta má přiřazenou jednu z následujících rolí:

|Role|Podrobnosti|
|--------|---------------|
|**Správce fakturace**|Může dělat nákupy, spravovat předplatná, spravovat lístky žádostí o podporu a sledovat stav služeb.|
|**Globální správce**|Má přístup ke všem funkcím pro správu. Prvním globálním správcem ve vašem klientovi se ve výchozím nastavení automaticky stane osoba, která se jménem vaší organizace zaregistruje při nákupu cloudové služby Microsoftu.<br /><br />-   Další role správců můžou přiřazovat jenom globální správci.<br />-   Organizace může mít víc globálních správců.|
|**Správce hesel**|Může resetovat hesla, spravovat žádosti o služby a sledovat stav služeb. Správci hesel můžou resetovat hesla jenom uživatelům a jiným správcům hesel.|
|**Správce služeb**|Může spravovat žádosti o služby a sledovat stav služeb.|
|**Správce správy uživatelů**|Může resetovat hesla, sledovat stav služeb a spravovat uživatelské účty, skupiny uživatelů a žádosti o služby.|
Ke každé roli správce jsou přidružená tato oprávnění:

|Oprávnění|Správce fakturace|Globální správce|Správce hesel|Správce služeb|Správce správy uživatelů|
|-------------|---------------------|--------------------|-----------------|------------------|----------------------------|
|Zobrazovat informace o organizaci a uživatelích|Ano|Ano|Ano|Ano|Ano|
|Spravovat lístky žádostí o podporu|Ano|Ano|Ano|Ano|Ano|
|Resetovat uživatelská hesla|Ne|Ano|Ano|Ne|Ano, ale s omezením. Tento správce nemůže resetovat hesla správců fakturace, globálních správců a správců služeb.|
|Dělat operace spojené s fakturací a nákupem|Ano|Ano|Ne|Ne|Ne|
|Vytvářet a spravovat zobrazení uživatelů|Ne|Ano|Ne|Ne|Ano|
|Vytvářet, upravovat a odstraňovat uživatele a skupiny a spravovat uživatelské licence|Ne|Ano|Ne|Ne|Ano, ale s omezením. Tento správce nemůže odstraňovat globální správce ani vytvářet jiné správce.|
|Spravovat domény|Ne|Ano|Ne|Ne|Ne|
|Spravovat informace o organizaci|Ne|Ano|Ne|Ne|Ne|
|Delegovat role správců jiným uživatelům|Ne|Ano|Ne|Ne|Ne|
|Používat synchronizaci adresářů|Ne|Ano|Ne|Ne|Ne|
Jestli se chcete o účtech správců ve službě [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] dozvědět něco víc, přečtěte si o [různých účtech a oprávněních správců pro jednotlivé úlohy](http://technet.microsoft.com/library/dn646966.aspx). Nápovědu ke správě uživatelů s právy pro správu najdete v části [Task 5: Assign administrative users](../Topic/Get_started_with_a_paid_subscription_to_Microsoft_Intune.md#BKMK_AssignAdmins) tématu [Začněte s placeným předplatným Microsoft Intune](../Topic/Get_started_with_a_paid_subscription_to_Microsoft_Intune.md).

