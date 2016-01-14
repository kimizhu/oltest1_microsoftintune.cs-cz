---
description: na
keywords: na
title: Mac OS X custom policy settings in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 70459e56-17d8-4d3f-803d-22feefa7a5b6
---
# Nastaven&#237; vlastn&#237;ch z&#225;sad pro Mac OS X v Microsoft Intune
Pomocí **vlastní zásady konfigurace Mac OS X**[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] nasaďte nastavení, které jste vytvořili pomocí [nástroje Apple Configurator](https://itunes.apple.com/us/app/apple-configurator/id434433123?mt=12), do zařízení s Mac OS X. Pomocí tohoto nástroje se dá vytvořit spousta nastavení, která řídí provoz těchto zařízení, a exportovat je do konfiguračního profilu. Potom tento konfigurační profil můžete importovat do vlastní zásady Mac OS X na zařízení [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] a nasadit nastavení pro uživatele a zařízení ve svojí organizaci.

Díky této vlastnosti můžete nasadit nastavení Mac OS X, která nejdou konfigurovat obecnými zásadami konfigurace Mac OS X aplikace [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Informace o nastaveních, která můžete pomocí těchto zásad konfigurovat, najdete v tématu [Nastavení zásad konfigurace pro Mac OS X v Microsoft Intune](../Topic/Mac_OS_X_configuration_policy_settings_in_Microsoft_Intune.md).

## Požadavky
Než začnete, je potřeba nainstalovat Apple Configurator a vytvořit konfigurační soubor s nastaveními, která chcete nasadit pro uživatele nebo zařízení. Apple Configurator si můžete stáhnout z [Mac App Storu](https://itunes.apple.com/us/app/apple-configurator/id434433123?mt=12), kde taky najdete informace o něm.

> [!NOTE]
> [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] nevytváří sestavu dodržování předpisů individuálních nastavení ve vlastních zásadách pro Mac OS X. Vytvoří se ale sestava celkového dodržování zásad.

## Jak vytvořit vlastní zásady pro Mac OS X

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com) klikněte na **Zásady** &gt; **Přehled** &gt; **Přidat zásadu**.

2.  Nakonfigurujte zásady typu **Mac OS X** &gt; **Vlastní konfigurace**.

    Nápovědu k vytvoření a nasazení zásad najdete v tématu [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

    Můžete vytvořit a nasadit vlastní zásady pro Mac OS X. Doporučená nastavení nejsou dostupná.

3.  S konfigurací nastavení zásad vám pomůže následující tabulka:

    |Název nastavení|Další informace|
    |-------------------|-------------------|
    |**Název**|Zadejte jedinečný název vlastní zásady pro Mac OS X, abyste ji mohli v konzole [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] snadno identifikovat.|
    |**Popis**|Zadejte popis, který bude shrnovat účel vlastní zásady pro Mac OS X, a uveďte jakékoli další důležité informace, které vám pomůžou zásadu najít.|
    |**Vlastní název konfiguračního profilu (zobrazený uživatelům)**|Zadejte název zásady tak, jak se bude zobrazovat na zařízení a v sestavách zásad [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].|
    |**Soubor konfiguračního profilu**|Klikněte na **Importovat** a potom vyhledejte konfigurační profil, který jste vytvořili pomocí nástroje Apple Configurator. **Tip:** Informace o vytváření konfiguračního profilu najdete v části [Vytvoření souboru konfiguračního profilu](#BKMK_Prof) v tomto tématu nápovědy.|
    |**Podrobnosti konfiguračního profilu**|Zobrazí kód XML pro konfigurační profil, který jste importovali.|

4.  Po dokončení klikněte na **Uložit zásadu**.

5.  Nová zásada se zobrazí v uzlu **Zásady konfigurace** pracovního prostoru **Zásady**.

## <a name="BKMK_Prof"></a>Vytvoření souboru konfiguračního profilu
Soubor konfiguračního profilu používaný vlastními zásadami můžete vytvořit dvěma způsoby:

-   Exportujte soubor (s příponou **.mobileconfig**) z nástroje Apple Configurator.

-   Vytvořte soubor sami pomocí příslušného schématu z dokumentu [Apple Configuration Profile Key Reference](https://developer.apple.com/library/ios/featuredarticles/iPhoneConfigurationProfileRef/Introduction/Introduction.html).

## Nasazení vlastních zásad pro Mac OS X

-   Nasaďte vlastní zásady pro Mac OS X do jedné nebo víc skupin uživatelů nebo zařízení ve vaší organizaci.

Nápovědu k nasazení zásad najdete v tématu [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

Shrnutí stavu a výstrahy na stránce **Přehled** v pracovním prostoru **Zásady** identifikují problémy se zásadami, které vyžadují vaši pozornost. Kromě toho se v pracovním prostoru **Řídicí panel** zobrazí shrnutí stavu.

> [!IMPORTANT]
> Když je zařízení s Mac OS X v režimu spánku, zásady a profily nejdou doručovat ani inventarizovat. Konzola [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] tak může dočasně zobrazovat stav **Nastavení zásad obsahující chybu**, dokud se zařízení nevzbudí z režimu spánku.

## Viz také
[Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

