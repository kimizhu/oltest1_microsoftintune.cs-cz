---
description: na
keywords: na
title: Set mobile device management authority and configure Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 668d6460-9d34-47a7-8a85-bbe1ed89f8e1
---
# Nastaven&#237; autority spr&#225;vy mobiln&#237;ch zař&#237;zen&#237; na Microsoft Intune
Než budou moct uživatelé začít registrovat mobilní zařízení do služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], správce IT musí deklarovat službu [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] jako *autoritu pro správu mobilních zařízení*.*Autorita pro správu mobilních zařízení* definuje jedinou službu správy s oprávněním ke správě skupiny zařízení.  Mezi řešení pro autoritu správy mobilních zařízení patří [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], Configuration Manager s [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]nebo řešení Office 365 MDM.

V tomto návodu předpokládáme, že Intune používáte bez integrace System Center Configuration Managera, takže nastavení by mělo být na Microsoft Intune.

## Autorita pro správu mobilních zařízení (MDM)
**Nastavení autority pro správu mobilních zařízení**

> [!IMPORTANT]
> Pečlivě zvažte, jestli chcete ke správě mobilních zařízení používat jenom službu Intune, System Center Configuration Managera s integrací služby Intune nebo Office 365. Jakmile nastavíte autoritu pro správu mobilních zařízení na jednu z těchto možností, nemůžete to změnit. Pokud si nejste jistí tím, jaké máte možnosti, podívejte se na článek [Způsoby zajištění podnikové mobility](../Topic/Ways_to_do_enterprise_mobility.md).

### <a name="BKMK_Set_MDM_Authority"></a>Nastavení autority pro správu mobilních zařízení

1.  V [konzole pro správu Microsoft Intune](http://manage.microsoft.com) klikněte na **Správce** &gt; **Správa mobilních zařízení**.

2.  V seznamu **Úkoly** klikněte na **Nastavit autoritu pro správu mobilních zařízení**. Otevře se dialogové okno **nastavení autority pro správu mobilních zařízení**.

    ![](../Image/Intune_MDM_Authority.bmp)

3.  Intune požádá o potvrzení, že chcete Intune používat jako autoritu pro správu mobilních zařízení. Jestli chcete ke správě mobilních zařízení používat Microsoft Intune, zaškrtněte políčko a klikněte na **Ano**.

4.  Když se teď služba Intune stala autoritou pro správu mobilních zařízení (MDM), můžete povolit registraci zařízení:

    -   [Povolení správy pro systém iOS](https://technet.microsoft.com/library/dn408185.aspx)

    -   [Povolení správy pro systém Android](https://technet.microsoft.com/library/dn764960.aspx)

    -   [Povolení správy pro systém Windows Phone](https://technet.microsoft.com/library/dn764959.aspx)

    -   [Povolení správy pro systém Windows](https://technet.microsoft.com/library/mt346003.aspx)

## Viz také
[Příprava registrace zařízení v Microsoft Intune](../Topic/Get_ready_to_enroll_devices_in_Microsoft_Intune.md)

