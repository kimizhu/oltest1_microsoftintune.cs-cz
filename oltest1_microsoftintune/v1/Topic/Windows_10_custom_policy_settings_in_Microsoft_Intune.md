---
description: na
keywords: na
title: Windows 10 custom policy settings in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5756b025-6fe9-418d-a1c4-cae576d31b79
---
# Nastaven&#237; vlastn&#237;ch z&#225;sad pro Windows 10 v Microsoft Intune
Pomocí **vlastní zásady konfigurace**[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] systémů Windows 10 a Windows 10 Mobile nasaďte nastavení OMA-URI (Open Mobile Alliance Uniform Resource Identifier), které se dá používat k ovládání funkcí na zařízeních s Windows 10 a Windows 10 Mobile. Jsou to standardní nastavení, která k ovládání funkcí zařízení používá spousta výrobců mobilních zařízení.

Díky této vlastnosti můžete nasadit nastavení Windows 10, které nejde konfigurovat se zásadami aplikace [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Informace o nastaveních, která můžete pomocí těchto zásad konfigurovat, najdete v části [Správa nastavení a funkcí v zařízeních pomocí zásad Microsoft Intune](../Topic/Manage_settings_and_features_on_your_devices_with_Microsoft_Intune_policies.md) v tomto tématu.

Seznam nastavení OMA-URI, která se dají konfigurovat na registrovaných zařízeních Windows 10, najdete v tématu [Vlastní nastavení URI pro zařízení s Windows 10](../Topic/Custom_URI_settings_for_Windows_10_devices.md).

## Jak vytvořit vlastní zásadu pro Windows 10

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com) klikněte na **Zásady** &gt; **Přidat zásadu**.

2.  V části **Windows** nakonfigurujte zásadu **Vlastní konfigurace (Windows 10 Desktop a Mobile a novější)**.

    Nápovědu k vytvoření a nasazení zásad najdete v tématu [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

    Vytvořit a nasadit můžete jenom vlastní zásadu. Doporučená nastavení nejsou dostupná.

3.  S konfigurací obecného nastavení zásad vám pomůže následující tabulka:

    |Název nastavení|Další informace|
    |-------------------|-------------------|
    |**Název**|Zadejte jedinečný název vlastní zásady, abyste ji mohli v konzole [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] snadno identifikovat.|
    |**Popis**|Zadejte popis, který zásadu vystihne, a uveďte jakékoli další důležité informace, které vám pomůžou zásadu najít.|

4.  V části **Nastavení OMA-URI** přidejte nastavení kliknutím na **Přidat**. Můžete taky upravit nebo odstranit existující nastavení.

5.  V dialogovém okně **Přidat nebo upravit nastavení OMA-URI** zadejte následující informace:

    |Položka|Další informace|
    |-----------|-------------------|
    |**Název nastavení**|Zadejte jedinečný název nastavení OMA-URI, který vám pomůže ho rozpoznat v seznamu nastavení.|
    |**Popis nastavení**|Zadejte popis, který nastavení přehledně vystihne, a další důležité informace, které vám ho pomůžou najít.|
    |**Datový typ**|Vyberte datový typ, ve kterém toto nastavení OMA-URI určíte. Vybírejte z těchto možností:<br /><br />-   **Řetězec**<br />-   **Řetězec (XML)**<br />-   **Datum a čas**<br />-   **Celé číslo**<br />-   **Číslo s plovoucí desetinnou čárkou**<br />-   **Logická hodnota**|
    |**OMA-URI (rozlišuje velká a malá písmena)**|Zadejte OMA-URI, pro který chcete zadat nastavení.|
    |**Hodnota**|Zadejte hodnotu pro přidružení k OMA-URI, který jste zadali dřív.|

6.  Klikněte na tlačítko **OK** pro uložení nastavení a návrat na stránku **Vytvořit zásadu**.

7.  Pokračujte pro přidání tolika nastavení, kolik potřebujete. Po dokončení klikněte na **Uložit zásadu**.

Nová zásada se zobrazí v uzlu **Zásady konfigurace** pracovního prostoru **Zásady**.

## Nasazení vlastní zásady pro Windows 10

1.  Nasaďte zásadu do jedné nebo víc skupin uživatelů nebo zařízení ve vaší organizaci.

Další informace o tom, jak nasazovat zásady, najdete v tématu [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

Shrnutí stavu a výstrahy na stránce **Přehled** v pracovním prostoru **Zásady** identifikují problémy se zásadami, které vyžadují vaši pozornost. Kromě toho se v pracovním prostoru **Řídicí panel** zobrazí shrnutí stavu.

## Viz také
[Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

