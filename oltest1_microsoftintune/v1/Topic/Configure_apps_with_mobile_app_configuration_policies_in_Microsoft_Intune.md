---
description: na
keywords: na
title: Configure apps with mobile app configuration policies in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fc6b645a-e837-4b2a-a10f-144065cbd8dd
---
# Konfigurace aplikac&#237; pomoc&#237; z&#225;sad konfigurace mobiln&#237;ch aplikac&#237; v Microsoft Intune
Zásady konfigurace mobilních aplikací ve službě [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] slouží k poskytování nastavení, která se můžou požadovat, když uživatel spustí aplikaci. Aplikace může například vyžadovat, aby uživatel zadal:

-   Vlastní číslo portu při spuštění

-   Nastavení jazyka

-   Nastavení zabezpečení

-   Nastavení brandingu, jako je logo společnosti

Když tato nastavení zadá uživatel špatně, můžete to zvýšit zatížení vašeho helpdesku a také zpomalit přijímání nových aplikací.

Zásady konfigurace mobilních aplikací pomůžou tyto problémy eliminovat tím, že vám dovolí pomocí zásady nasadit tato nastavení pro uživatele dřív, než aplikaci spustí. Nastavení jsou pak zadaná automaticky a uživatel nemusí provádět žádnou akci.

Tyto zásady nenasazujte přímo na uživatele a zařízení. Místo toho přidružíte zásadu k aplikaci, a pak nasadíte aplikaci. Nastavení zásad se použije vždy, když je aplikace zkontroluje (obvykle při prvním spuštění).

> [!TIP]
> Tento typ zásad je nyní k dispozici pouze pro zařízení se systémem iOS 7.1 a novějším a podporuje následující typy instalací aplikací:
> 
> -   **Spravované aplikace pro iOS z obchodu s aplikacemi**
> -   **Balíček aplikace pro iOS**
> 
> Další informace o typech instalací aplikací najdete v tématu [Začínáme s nasazováním aplikací v Microsoft Intune](../Topic/Plan_for_app_deployment_in_Microsoft_Intune.md).

## Konfigurace zásady konfigurace mobilních aplikací

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com) klikněte na **Zásady** &gt; **Přehled** &gt; **Přidat zásadu**.

2.  V seznamu zásad rozbalte **iOS**, klikněte na **Konfigurace mobilních aplikací** a pak klikněte na **Vytvořit zásadu**.

    > [!TIP]
    > Můžete konfigurovat jenom vlastní nastavení pro tento typ zásad. Doporučená nastavení nejsou dostupná.

3.  V části **Obecné** stránky **Vytvořit zásadu** zadejte název a nepovinný popis zásady konfigurace mobilních aplikací.

4.  V části **Zásada konfigurace mobilních aplikací** stránky zadejte nebo vložte do pole seznam vlastností XML obsahující požadovaná konfigurační nastavení aplikace.

    > [!TIP]
    > Další informace o seznamech vlastností XML najdete v tématu [Vysvětlení seznamů vlastností XML](https://developer.apple.com/library/ios/documentation/Cocoa/Conceptual/PropertyLists/UnderstandXMLPlist/UnderstandXMLPlist.html) v knihovně iOS Developer Library.
    > 
    > Formát seznamu vlastností XML se bude lišit v závislosti na aplikaci, kterou konfigurujete. Podrobnosti o přesném formátu, který se má použít, získáte od dodavatele aplikace.
    > 
    > [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] podporuje v seznamu vlastností následující typy dat:
    > 
    > -   &lt;integer&gt;
    > -   &lt;real&gt;
    > -   &lt;string&gt;
    > -   &lt;array&gt;
    > -   &lt;dict&gt;
    > -   &lt;true /&gt; nebo &lt;false /&gt;
    > 
    > Další informace o typech dat najdete v tématu [Informace o seznamech vlastností](https://developer.apple.com/library/ios/documentation/Cocoa/Conceptual/PropertyLists/AboutPropertyLists/AboutPropertyLists.html) v knihovně iOS Developer Library.

5.  Klikněte na **Ověřit**, abyste zkontrolovali, že zadaný kód XML má platný formát seznamu vlastností.

    > [!IMPORTANT]
    > Když kliknete na **Ověřit**, [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] zkontroluje, že zadaný kód XML má platný formát. Nekontroluje, že seznam vlastností XML bude fungovat s aplikací, ke které je přidružen.

6.  Po dokončení klikněte na **Uložit zásadu**.

Nová zásada se zobrazí v uzlu **Zásady konfigurace**.

## Přidružení zásady konfigurace mobilních aplikací k aplikaci
Po vytvoření musíte zásadu konfigurace mobilních aplikací přiřadit k aplikaci iOS, na kterou se mají nastavení v zásadě konfigurace vztahovat.

Abyste to provedli, postupujte podle kroků k vytvoření nasazení aplikace v tématu [Nasazení aplikací do mobilních zařízení v Microsoft Intune](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune_-_deleted.md). Když dojdete v průvodci na stránku **Konfigurace mobilních aplikací**, vyberte z rozevíracího seznamu **Zásada konfigurace aplikací** zásadu, kterou chcete přidružit k aplikaci.

Potom pokračujte v nasazení a monitorování nasazení aplikace obvyklým způsobem.

Při spuštění aplikace nasazené do zařízení se aplikace spustí s nastavením, které jste nakonfigurovali v zásadě konfigurace mobilních aplikací.

> [!TIP]
> V případě konfliktu jedné nebo více zásad konfigurace mobilních aplikací se nevynutí ani jedna zásada a konflikt se ohlásí v **Řídicím panelu** konzoly pro správu služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

## Viz také
[Nasazení a konfigurace aplikací v Microsoft Intune](../Topic/Deploy_and_configure_apps_with_Microsoft_Intune.md)
[Nasazení aplikací do mobilních zařízení v Microsoft Intune](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune_-_deleted.md)

