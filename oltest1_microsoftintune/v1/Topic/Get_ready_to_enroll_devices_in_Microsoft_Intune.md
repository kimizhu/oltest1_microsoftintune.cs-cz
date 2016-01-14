---
description: na
keywords: na
title: Get ready to enroll devices in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 44fd4af0-f9b0-493a-b590-7825139d9d40
---
# Př&#237;prava registrace zař&#237;zen&#237; v Microsoft Intune
![](../Image/Nav_Icons/WIT_Tile_W_Overview.png)![](../Image/Nav_Icons/WIT_Tile_W_GetStarted.png)![](../Image/Nav_Icons/WIT_Tile_W_EnrollDevicesHighlight.png)![](../Image/Nav_Icons/WIT_Tile_W_ManageDevices.png)![](../Image/Nav_Icons/WIT_Tile_W_ManageApps.png)![](../Image/Nav_Icons/WIT_Tile_W_ProtectResources.png)![](../Image/Nav_Icons/WIT_Tile_W_RetireData.png)![](../Image/Nav_Icons/WIT_Tile_W_TechnicalReference.png)![](../Image/Nav_Icons/WIT_Tile_W_Troubleshooting.png)
![](../Image/Nav_Icons/WIT_Banner_EnrollDevices.png)

Aby mohli zaměstnanci využívat prostředky společnosti na mobilních zařízeních (včetně zařízení s Androidem a s iOS a zařízení Windows Phone), musíte povolit registraci zařízení, což je proces, kterým se zařízení eviduje, aby ho bylo možné spravovat. K tomu je nutné nejdřív nastavit [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] jako autoritu mobilního zařízení a povolit registraci pro operační systém zařízení. Počítače s Windows 8.1 a Windows 10 můžete taky spravovat jako mobilní zařízení nebo je můžete spravovat přes [klientský software Intune](http://technet.microsoft.com/library/dn646959.aspx).

## Povolení registrace mobilních zařízení
Aby bylo možné povolit registraci Správy mobilních zařízení (MDM), musíte nastavit *autoritu pro správu mobilních zařízení* (MDM). Autorita MDM definuje službu správy s oprávněními ke správě skupiny zařízení.  Příklady možných autorit MDM: [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], Configuration Manager s [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] nebo MDM řešení Office 365.  Office 365 a Intune jde používat současně ke správě mobilních zařízení. Pokud je System Center Configuration Manager nastaven jako autorita správy, ke správě mobilních zařízení nejde použít žádnou jinou službu. Začněte tím, že si [jako autoritu MDM nastavíte Intune](https://technet.microsoft.com/library/mt346013.aspx).

Pak musíte povolit registraci pro operační systémy, které chce vaše organizace podporovat. Aby bylo možné povolit správu, vyžadují některé operační systémy na mobilních zařízeních (například Windows a iOS) důvěryhodný vztah mezi zařízeními a [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

-   [Nastavení správy systému Android pomocí Microsoft Intune](../Topic/Set_up_Android_management_with_Microsoft_Intune.md)

-   [Nastavení správy iOS pomocí Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md) - Včetně [zařízení s iOS vlastněných společností](https://technet.microsoft.com/library/dn408185.aspx#BKMK_DEP)

-   [Nastavení správy pro zařízení Windows Phone v Microsoft Intune](../Topic/Set_up_Windows_Phone_management_with_Microsoft_Intune.md)

-   [Nastavení správy pro zařízení Windows v Microsoft Intune](../Topic/Set_up_Windows_device_management_with_Microsoft_Intune.md)

## Správa víc zařízení přes účet správce registrace zařízení
Organizace můžou pomocí Intune spravovat velké počty mobilních zařízení s jediným uživatelským účtem. Účet *manažera registrace zařízení* je speciální účet Intune s oprávněním přihlásit víc než pět zařízení. Viz [Přihlášení firemních zařízení pomocí manažera registrace zařízení v Microsoft Intune](../Topic/Enroll_corporate-owned_devices_with_the_Device_Enrollment_Manager_in_Microsoft_Intune.md).

## MDM s Intune a Exchange ActiveSync
Aby mohla služba [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] přímo spravovat mobilní zařízení, musí uživatelé tato zařízení v [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] zaregistrovat. U mobilních zařízení, která uživatelé nezaregistrovali, můžete povolit správu pomocí protokolu Exchange ActiveSync s použitím konektoru Exchange. Zařízení Exchange se dají spravovat na místních serverech i prostřednictvím hostovaného Exchange v Microsoft Office 365 v cloudu. Konektor Exchange slouží jako propojení s nasazením Exchange a umožňuje vám spravovat mobilní zařízení prostřednictvím konzoly [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Viz téma [Správa mobilních zařízení pomocí protokolu Exchange ActiveSync a služby Microsoft Intune](../Topic/Mobile_device_management_with_Exchange_ActiveSync_and_Microsoft_Intune.md)

## Viz také
[Dokumentace pro Microsoft Intune](../Topic/Documentation_for_Microsoft_Intune.md)

