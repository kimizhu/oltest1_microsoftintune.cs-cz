---
description: na
keywords: na
title: Help with iOS enrollment errors
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c91075e8-e184-49a9-bedf-4a213872613f
robots: noindex,nofollow
---
# N&#225;pověda k chyb&#225;m registrace zař&#237;zen&#237; se syst&#233;mem iOS
Toto téma vám pomůže vyřešit chyby registrace zařízení se systémem iOS.

## Chyby registrace zařízení se systémem iOS
V následující tabulce jsou uvedené chyby, které se můžou objevit při registraci zařízení se systémem iOS. U každé chyby jsou uvedené možné příčiny a podrobnosti řešení.

|Chybová zpráva|Možná příčina|Řešení pomocí [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]|Řešení pomocí System Center 2012 R2 Configuration Manageru|
|------------------|-----------------|-----------------------------------------------------------------------|--------------------------------------------------------------|
|DeviceCapReached|Tato zpráva znamená, že uživatel už má zaregistrovaných příliš mnoho mobilních zařízení.|Než bude moct uživatel zapsat další mobilní zařízení, musí z portálu společnosti odebrat jedno z aktuálně zaregistrovaných mobilních zařízení.|Než bude moct uživatel zapsat další mobilní zařízení, musí z portálu společnosti odebrat jedno z aktuálně zaregistrovaných mobilních zařízení.|
|APNSCertificateNotValid|APNs (Apple Push Notification Service) představuje kanál umožňující registraci zařízení se systémem iOS. Pokud jste neprovedli kroky k získání certifikátu APNs nebo vypršela platnost certifikátu APNs, pak budou pokusy o registraci neúspěšné a zobrazí se tato zpráva.|Projděte si část Vnější závislosti pro registraci zařízení se systémem iOS v dokumentu [Nastavení správy iOS pomocí Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md).|Projděte si část Vnější závislosti pro registraci zařízení se systémem iOS v dokumentu [Nastavení správy iOS pomocí Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md).|
|AccountNotOnboarded|APNs (Apple Push Notification Service) představuje kanál umožňující registraci zařízení se systémem iOS. Pokud jste neprovedli kroky k získání certifikátu APNs, pokusy o registraci budou neúspěšné a zobrazí se tato zpráva.|Projděte si část Vnější závislosti pro registraci zařízení se systémem iOS v dokumentu [Nastavení správy iOS pomocí Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md).|Projděte si část Vnější závislosti pro registraci zařízení se systémem iOS v dokumentu [Nastavení správy iOS pomocí Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md).|
|DeviceTypeNotSupported|Tato zpráva se může zobrazit, pokud se pokusíte o registraci na zařízení s jiným systémem než iOS.|Zkontrolujte, že na zařízení běží systém iOS verze 5.0 nebo novější.|Zkontrolujte, že na zařízení běží systém iOS verze 5.0 nebo novější.|
|UserLicenseTypeInvalid|Než si budou moct uživatelé zaregistrovat zařízení, musí být členy příslušné skupiny uživatelů. Tato zpráva znamená, že uživatel má špatný typ licence pro určenou autoritu pro správu mobilních zařízení. Pokud je třeba vaší určenou autoritou pro správu mobilních zařízení služba [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] a uživatel používá licenci System Center 2012 R2 Configuration Manageru, zobrazí se tato chyba.|Projděte si část Zřízení uživatelů pro registraci zařízení v dokumentu [Nastavení správy iOS pomocí Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md).|Projděte si část Zřízení uživatelů pro registraci zařízení v dokumentu [Nastavení správy iOS pomocí Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md).|
|MdmAuthorityNotDefined|Tato zpráva znamená, že autorita pro správu mobilních zařízení není určená ve službě [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)].|Projděte si část Nastavení autority pro správu mobilních zařízení pro Microsoft Intune v dokumentu [Nastavení správy iOS pomocí Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md).|Projděte si část Nastavení autority pro správu mobilních zařízení pro Microsoft Intune v dokumentu [Nastavení správy iOS pomocí Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md).|
