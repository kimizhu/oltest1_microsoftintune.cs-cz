---
description: na
keywords: na
title: iOS custom policy settings in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 04e60d5a-3da6-4943-b6ff-e6a331bcbcfa
---
# Nastaven&#237; vlastn&#237;ch z&#225;sad pro iOS v Microsoft Intune
Pomocí **vlastní zásady konfigurace iOS**[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] nasaďte nastavení, které jste vytvořili pomocí [nástroje Apple Configurator](https://itunes.apple.com/us/app/apple-configurator/id434433123?mt=12), do zařízení s iOS. Pomocí tohoto nástroje se dá vytvořit spousta nastavení, která řídí provoz těchto zařízení, a exportovat je do konfiguračního profilu. Potom tento konfigurační profil můžete importovat do vlastní zásady iOS na zařízení [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] a nasadit nastavení pro uživatele a zařízení ve vaší organizaci.

Díky této vlastnosti můžete nasadit nastavení iOS, které nejde konfigurovat se zásadami aplikace [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Informace o nastaveních, která můžete pomocí těchto zásad konfigurovat, najdete v části [Nastavení zásad konfigurace pro iOS v Microsoft Intune](../Topic/iOS_configuration_policy_settings_in_Microsoft_Intune.md) v tomto tématu.

## Požadavky
Než začnete, je potřeba nainstalovat Apple Configurator a vytvořit konfigurační soubor s nastaveními, která chcete nasadit pro uživatele nebo zařízení. Apple Configurator si můžete stáhnout z [Mac App Storu](https://itunes.apple.com/us/app/apple-configurator/id434433123?mt=12), kde taky najdete informace o něm.

> [!NOTE]
> [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] nevytváří sestavu dodržování předpisů individuálních nastavení ve vlastních zásadách iOS. Vytvoří se ale sestava celkového dodržování zásad.

## Jak vytvořit vlastní zásady pro iOS

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com) klikněte na **Zásady** &gt; **Přehled** &gt; **Přidat zásadu**.

2.  Nakonfigurujte zásady typu **iOS** &gt; **Vlastní konfigurace**.

    Nápovědu k vytvoření a nasazení zásad najdete v tématu [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

    Můžete vytvořit a nasadit vlastní zásady pro iOS. Doporučená nastavení nejsou dostupná.

3.  S konfigurací nastavení zásad vám pomůže následující tabulka:

    |Název nastavení|Další informace|
    |-------------------|-------------------|
    |**Název**|Zadejte jedinečný název vlastní zásady pro iOS, abyste ji mohli v konzole [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] snadno identifikovat.|
    |**Popis**|Zadejte popis, který bude shrnovat účel vlastní zásady pro iOS, a uveďte jakékoli další důležité informace, které vám pomůžou zásadu najít.|
    |**Vlastní název konfiguračního profilu (zobrazený uživatelům)**|Zadejte název zásady tak, jak se bude zobrazovat na zařízení a v sestavách zásad [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].|
    |**Soubor konfiguračního profilu**|Klikněte na **Importovat** a potom vyhledejte konfigurační profil, který jste vytvořili pomocí nástroje Apple Configurator. **Note:** Nastavení, které exportujete z nástroje Apple Configurator, musí být kompatibilní s verzí iOS na zařízeních, na která nasazujete vlastní zásady pro iOS. Informace o tom, jak se řeší nekompatibilní nastavení, najdete v **referenci na konfigurační profil**  a **referenci na protokol správy mobilního zařízení** na webu pro [vývojáře Apple](https://developer.apple.com/).|
    |**Podrobnosti konfiguračního profilu**|Zobrazí kód XML pro konfigurační profil, který jste importovali.|

4.  Po dokončení klikněte na **Uložit zásadu**.

5.  Nová zásada se zobrazí v uzlu **Zásady konfigurace** pracovního prostoru **Zásady**.

## Nasazení vlastních zásad pro iOS

-   Nasaďte vlastní zásady pro iOS do jedné nebo víc skupin uživatelů nebo zařízení ve vaší organizaci.

Nápovědu k nasazení zásad najdete v tématu [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

Shrnutí stavu a výstrahy na stránce **Přehled** v pracovním prostoru **Zásady** identifikují problémy se zásadami, které vyžadují vaši pozornost. Kromě toho se v pracovním prostoru **Řídicí panel** zobrazí shrnutí stavu.

## Viz také
[Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

