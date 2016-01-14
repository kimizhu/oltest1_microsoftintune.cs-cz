---
description: na
keywords: na
title: Control what admins can see in the Microsoft Intune admin console
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e0783eaa-67dc-410e-9e80-4d3aa72f36d8
---
# Určen&#237; toho, co se spr&#225;vcům zobraz&#237; v konzole pro spr&#225;vu Microsoft Intune
[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] poskytuje možnost filtrovat zobrazení konzoly správu, abyste uživatelům povolili přístup jenom k položkám, ke kterým chcete. Můžete třeba chtít dovolit aktualizace definic malwaru nebo obnovování hesel pro zařízení jenom operátorům konzoly pro správu. To se dá udělat pomocí přednastavených **označení**, která přiřadíte konkrétním uživatelům. Když pak tito uživatelé přejdou do konzoly pro správu, uvidí jenom položky specifické pro své označení.

Tato funkce vám pomůže přiřazovat úlohy správy zaměstnancům při současném zajištění bezpečnosti dat [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

## Přiřazení označení uživateli

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com) klikněte na **Správce** &gt; **Správci služeb**.

2.  Ze seznamu správců služeb vyberte uživatele, u kterého chcete změnit označení, a klikněte na **Spravovat přístup**.

3.  V dialogu **Spravovat přístup** vyberte úroveň přístupu, kterou chcete vybranému uživateli přidělit. Na výběr máte tyto:

    -   **Úplný přístup**

    -   **Přístup jenom pro čtení**

    Kromě toho můžete zvolit jedno z následujících označení, které poskytují vlastní úrovně přístupu konzole pro správu [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]:

    |Označení|Uživatel může:|
    |------------|------------------|
    |**Helpdesk – uzel Skupiny**|<ul><li>Zobrazte seznam uživatelů a zařízení (uživatel nemůže ke změně zobrazení použít filtry. Můžete ale pomocí filtrování skupiny změnit, co uživatel uvidí). Další informace najdete v části [Použití skupin pro správu uživatelů a zařízení s Microsoft Intune](../Topic/Use_groups_to_manage_users_and_devices_with_Microsoft_Intune.md).</li><li>Tisk seznamu uživatelů a zařízení</li><li>Export seznamu uživatelů a zařízení</li><li>Zobrazení vlastností uživatele nebo zařízení</li><li>Provádějte následující vzdálené úlohy:<br /><br /><ul><li>Spustit úplnou kontrolu malwaru</li><li>Spustit rychlou kontrolu malwaru</li><li>Restartovat počítač</li><li>Aktualizovat definice malwaru</li><li>Aktualizovat zásady</li><li>Aktualizovat inventáře</li><li>Vzdáleně uzamknout zařízení</li><li>Resetování hesla</li></ul></li></ul>|

Když nakonfigurovaný uživatel později otevře konzolu pro správu [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], bude mu udělená úroveň přístupu, kterou jste určili.

## Viz také
[Technické reference pro Microsoft Intune](../Topic/Technical_reference_for_Microsoft_Intune.md)

