---
description: na
keywords: na
title: Manage settings and features on your devices with Microsoft Intune policies
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: d27f2739-9791-4aae-a9db-01a4e59ccfe5
---
# Spr&#225;va nastaven&#237; a funkc&#237; v zař&#237;zen&#237;ch pomoc&#237; z&#225;sad Microsoft Intune
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] používá **zásady**, které vám pomohou při konfiguraci celé řady bezpečnostních a funkčních nastavení pro zaregistrovaná mobilní zařízení, včetně:

-   Nastavení hardwaru, například povolení používání fotoaparátu/kamery nebo funkce Bluetooth zařízení

-   Nastavení hesla, včetně jeho délky a kvality

-   Povolené a blokované aplikace umožňují nakonfigurovat aplikace, které splňují (nesplňují) předpisy v rámci vaší organizace, a potom nahlásit zařízení, která nesplňují předpisy (pro zařízení Windows Phone můžete blokovat instalaci nebo používání aplikací).

-   Nastavení celoobrazovkového režimu umožňuje zablokovat určité funkce zařízení, například tímto způsobem můžete povolit, že se bude dát spustit jenom jedna aplikace, nebo třeba zakázat funkci vypínače a ovládacích prvků hlasitosti.

Informace v tomto tématu vám pomohou rozhodnout, jaké zásady byste měli používat ke správě svých zařízení.

> [!TIP]
> Další informace o použití zásady najdete v tématu [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

## <a name="BKMK_WhatPol"></a>Kterou zásadu použít

### Android

|Název zásady|Použijte v případě, že chcete|
|----------------|---------------------------------|
|**Vlastní konfigurace (Android 4 nebo novější, Samsung KNOX Standard 4.0 a novější)**|-   Nasadit nastavení OMA-URI, třeba nastavení Wi-Fi, která se dají použít k ovládání funkcí na zařízeních. To je užitečné, když nastavení, které potřebujete, není k dispozici v zásadách konfigurace.<br /><br />Podrobnosti najdete v tématu [Nastavení vlastních zásad pro Android v Microsoft Intune](../Topic/Android_custom_policy_settings_in_Microsoft_Intune.md).|
|**E-mailový profil (Samsung KNOX Standard 4.0 a novější)**|-   Vytvořit, nasadit a monitorovat nastavení e-mailů Exchange ActiveSync na spravovaných zařízeních. Díky tomu mají uživatelé na svých osobních zařízeních přístup k podnikovému e-mailu, bez nutnosti něco nastavovat.<br /><br />Podrobnosti najdete v tématu [Konfigurace přístupu k podnikovému e-mailu pomocí e-mailových profilů v Microsoft Intune](../Topic/Configure_access_to_corporate_email_using_email_profiles_with_Microsoft_Intune.md).|
|**Obecná konfigurace (Android 4 nebo novější, Samsung KNOX Standard 4.0 a novější)**|-   Nakonfigurovat zabezpečení mobilního zařízení a funkční nastavení<br />-   Zadat aplikace, které jsou (nebo nejsou) v souladu s předpisy, a zobrazit zprávu o jejich používání<br />-   Nakonfigurovat celoobrazovkový režim, ve kterém můžete zařízení zamknout, a povolit fungování jenom některých funkcí, třeba můžete povolit, aby na zařízení běžela jenom jedna aplikace, nebo můžete zakázat tlačítka hlasitosti.<br /><br />Podrobnosti najdete v tématu [Nastavení zásad konfigurace pro Android v Microsoft Intune](../Topic/Android_configuration_policy_settings_in_Microsoft_Intune.md).|
|**Profil certifikátu PKCS #12 (.PFX) (Android 4 a novější)**|-   Použít tento profil k vytvoření a nasazení nastavení PFX pro požadavky certifikátů zařízení.<br /><br />Podrobnosti najdete v tématu [Povolení přístupu k firemním prostředkům pomocí profilů certifikátů v Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md).|
|**Profil certifikátu SCEP (Android 4 a novější)**|-   Nakonfigurujte certifikát protokolu SCEP, který můžete použít společně s certifikátem důvěryhodného mobilního zařízení k ověřování mobilních zařízení a povolení jejich přístupu k síťovým prostředkům, například nakonfigurovaným profily Wi-Fi a VPN.<br /><br />Podrobnosti najdete v tématu [Povolení přístupu k firemním prostředkům pomocí profilů certifikátů v Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md).|
|**Profil důvěryhodného certifikátu (Android 4 a novější)**|-   Nakonfigurujte certifikát důvěryhodného mobilního zařízení, který můžete použít k ověřování mobilních zařízení a povolení jejich přístupu k síťovým prostředkům, například nakonfigurovaným profily Wi-Fi a VPN.<br /><br />Podrobnosti najdete v tématu [Povolení přístupu k firemním prostředkům pomocí profilů certifikátů v Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md).|
|**Profil VPN (Android 4 a novější)**|-   Nakonfigurujte a nasaďte nastavení, která uživatelům umožňují zabezpečený přístup k podnikové síti z jejich mobilních zařízení. Nasazením těchto nastavení minimalizujete úsilí koncových uživatelů potřebné pro připojení k jejich práci.<br /><br />Podrobnosti najdete v tématu [Pomoc uživatelům připojit s k práci pomocí profilů VPN v Microsoft Intune](../Topic/Help_users_connect_to_their_work_using_VPN_profiles_with_Microsoft_Intune.md).|
|**Profil Wi-Fi (Android 4 a novější)**|-   Nakonfigurujte a nasaďte nastavení bezdrátové sítě na uživatele ve vaší organizaci. Nasazením těchto nastavení minimalizujete úsilí koncových uživatelů potřebné k připojení k bezdrátové síti.<br /><br />Podrobnosti najdete v tématu [Pomoc uživatelům s připojením k sítím společnosti pomocí Wi-Fi profilů s Microsoft Intune](../Topic/Help_users_connect_to_company_networks_using_Wi-Fi_profiles_with_Microsoft_Intune.md).|

### iOS

|Název zásady|Použijte v případě, že chcete|
|----------------|---------------------------------|
|**Vlastní konfigurace (iOS 7.1 a novější)**|-   Nasaďte konfigurační profily do zařízení s iOS vytvořených pomocí nástroje Apple Configurator. To je užitečné, když nastavení, které potřebujete, není k dispozici v zásadách konfigurace.<br /><br />Podrobnosti najdete v tématu [Nastavení vlastních zásad pro iOS v Microsoft Intune](../Topic/iOS_custom_policy_settings_in_Microsoft_Intune.md).|
|**E-mailový profil (iOS 7.1 a novější)**|-   Vytvořit, nasadit a monitorovat nastavení e-mailů Exchange ActiveSync na spravovaných zařízeních. Díky tomu mají uživatelé na svých osobních zařízeních přístup k podnikovému e-mailu, bez nutnosti něco nastavovat.<br /><br />Podrobnosti najdete v tématu [Konfigurace přístupu k podnikovému e-mailu pomocí e-mailových profilů v Microsoft Intune](../Topic/Configure_access_to_corporate_email_using_email_profiles_with_Microsoft_Intune.md).|
|**Obecná konfigurace (iOS 7.1 a novější)**|-   Nakonfigurovat zabezpečení mobilního zařízení a funkční nastavení<br />-   Zadat aplikace, které jsou (nebo nejsou) v souladu s předpisy, a zobrazit zprávu o jejich používání<br />-   Nakonfigurovat celoobrazovkový režim, ve kterém můžete zařízení zamknout, a povolit fungování jenom některých funkcí, třeba můžete povolit, aby na zařízení běžela jenom jedna aplikace, nebo můžete zakázat tlačítka hlasitosti.<br /><br />Podrobnosti najdete v tématu [Nastavení zásad konfigurace pro iOS v Microsoft Intune](../Topic/iOS_configuration_policy_settings_in_Microsoft_Intune.md).|
|**Profil certifikátu SCEP (iOS 7.1 a novější)**|-   Nakonfigurujte certifikát protokolu SCEP, který můžete použít společně s certifikátem důvěryhodného mobilního zařízení k ověřování mobilních zařízení a povolení jejich přístupu k síťovým prostředkům, například nakonfigurovaným profily Wi-Fi a VPN.<br /><br />Podrobnosti najdete v tématu [Povolení přístupu k firemním prostředkům pomocí profilů certifikátů v Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md).|
|**Profil důvěryhodného certifikátu (iOS 7.1 a novější)**|-   Nakonfigurujte certifikát důvěryhodného mobilního zařízení, který můžete použít k ověřování mobilních zařízení a povolení jejich přístupu k síťovým prostředkům, například nakonfigurovaným profily Wi-Fi a VPN.<br /><br />Podrobnosti najdete v tématu [Povolení přístupu k firemním prostředkům pomocí profilů certifikátů v Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md).|
|**Profil VPN (iOS 7.1 a novější)**|-   Nakonfigurujte a nasaďte nastavení, která uživatelům umožňují zabezpečený přístup k podnikové síti z jejich mobilních zařízení. Nasazením těchto nastavení minimalizujete úsilí koncových uživatelů potřebné pro připojení k jejich práci.<br /><br />Podrobnosti najdete v tématu [Pomoc uživatelům připojit s k práci pomocí profilů VPN v Microsoft Intune](../Topic/Help_users_connect_to_their_work_using_VPN_profiles_with_Microsoft_Intune.md).|
|**Profil Wi-Fi (iOS 7.1 a novější)**|-   Nakonfigurujte a nasaďte nastavení bezdrátové sítě na uživatele ve vaší organizaci. Nasazením těchto nastavení minimalizujete úsilí koncových uživatelů potřebné k připojení k bezdrátové síti.<br /><br />Podrobnosti najdete v tématu [Pomoc uživatelům s připojením k sítím společnosti pomocí Wi-Fi profilů s Microsoft Intune](../Topic/Help_users_connect_to_company_networks_using_Wi-Fi_profiles_with_Microsoft_Intune.md).|
|**Zásady konfigurace mobilních aplikací (iOS 7.1 a novější)**|-   Použít zásady konfigurace mobilních aplikací k automatickému poskytování zásad, které se můžou požadovat, když uživatel spustí aplikaci pro iOS.<br /><br />Podrobnosti najdete v tématu [Konfigurace aplikací pomocí zásad konfigurace mobilních aplikací v Microsoft Intune](../Topic/Configure_apps_with_mobile_app_configuration_policies_in_Microsoft_Intune.md).|

### Mac OS X

|Název zásady|Použijte v případě, že chcete|
|----------------|---------------------------------|
|**Vlastní konfigurace (Mac OS X 10.9 a novější)**|-   Nasaďte konfigurační profily do počítačů Mac vytvořených pomocí nástroje Apple Configurator. To je užitečné, když nastavení, které potřebujete, není k dispozici v zásadách konfigurace.<br /><br />Podrobnosti najdete v tématu [Nastavení vlastních zásad pro Mac OS X v Microsoft Intune](../Topic/Mac_OS_X_custom_policy_settings_in_Microsoft_Intune.md).|
|**Obecná konfigurace (Mac OS X 10.9 a novější)**|-   Nakonfigurovat zabezpečení mobilního zařízení a funkční nastavení<br />-   Zadat aplikace, které jsou (nebo nejsou) v souladu s předpisy, a zobrazit zprávu o jejich používání<br /><br />Podrobnosti najdete v tématu [Nastavení zásad konfigurace pro Mac OS X v Microsoft Intune](../Topic/Mac_OS_X_configuration_policy_settings_in_Microsoft_Intune.md).|
|**Profil certifikátu SCEP (Mac OS X 10.9 a novější)**|-   Nakonfigurujte certifikát protokolu SCEP, který můžete použít společně s certifikátem důvěryhodného mobilního zařízení k ověřování mobilních zařízení a povolení jejich přístupu k síťovým prostředkům, například nakonfigurovaným profily Wi-Fi a VPN.<br /><br />Podrobnosti najdete v tématu [Povolení přístupu k firemním prostředkům pomocí profilů certifikátů v Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md).|
|**Profil důvěryhodného certifikátu (Mac OS X 10.9 a novější)**|-   Nakonfigurujte certifikát důvěryhodného mobilního zařízení, který můžete použít k ověřování mobilních zařízení a povolení jejich přístupu k síťovým prostředkům, například nakonfigurovaným profily Wi-Fi a VPN.<br /><br />Podrobnosti najdete v tématu [Povolení přístupu k firemním prostředkům pomocí profilů certifikátů v Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md).|
|**Profil sítě VPN (Mac OS X 10.9 a novější)**|-   Nakonfigurujte a nasaďte nastavení, která uživatelům umožňují zabezpečený přístup k podnikové síti z jejich mobilních zařízení. Nasazením těchto nastavení minimalizujete úsilí koncových uživatelů potřebné pro připojení k jejich práci.<br /><br />Podrobnosti najdete v tématu [Pomoc uživatelům připojit s k práci pomocí profilů VPN v Microsoft Intune](../Topic/Help_users_connect_to_their_work_using_VPN_profiles_with_Microsoft_Intune.md).|
|**Profil Wi-Fi (Mac OS X 10.9 a novější)**|-   Nakonfigurujte a nasaďte nastavení bezdrátové sítě na uživatele ve vaší organizaci. Nasazením těchto nastavení minimalizujete úsilí koncových uživatelů potřebné k připojení k bezdrátové síti.<br /><br />Podrobnosti najdete v tématu [Pomoc uživatelům s připojením k sítím společnosti pomocí Wi-Fi profilů s Microsoft Intune](../Topic/Help_users_connect_to_company_networks_using_Wi-Fi_profiles_with_Microsoft_Intune.md).|

### Windows
Platí jenom pro Windows Phone a zaregistrovaná zařízení s Windows.

|Název zásady|Použijte v případě, že chcete|
|----------------|---------------------------------|
|**Vlastní konfigurace (Windows 10 Desktop a Mobile a novější)**|-   Nasadit nastavení OMA URI, která se dají použít k řízení funkcí zařízení. To je užitečné, když nastavení, které potřebujete, není k dispozici v zásadách konfigurace.<br />    Seznam dostupných nastavení najdete v tématu [Vlastní nastavení URI pro zařízení s Windows 10](../Topic/Custom_URI_settings_for_Windows_10_devices.md).<br /><br />Podrobnosti najdete v tématu [Nastavení vlastních zásad pro Windows 10 v Microsoft Intune](../Topic/Windows_10_custom_policy_settings_in_Microsoft_Intune.md).|
|**Vlastní konfigurace (Windows Phone 8.1 a novější)**|-   Nasadit nastavení OMA URI, která se dají použít k řízení funkcí zařízení. To je užitečné, když nastavení, které potřebujete, není k dispozici v zásadách konfigurace.<br /><br />Podrobnosti najdete v tématu [Nastavení vlastních zásad pro Windows Phone v Microsoft Intune](../Topic/Windows_Phone_custom_policy_settings_in_Microsoft_Intune.md).|
|**E-mailový profil (Windows Phone 8 a novější)**<br /><br />**E-mailový profil (Windows 10 Desktop a Mobile a novější)**|-   Vytvořit, nasadit a monitorovat nastavení e-mailů Exchange ActiveSync na spravovaných zařízeních. Díky tomu mají uživatelé na svých osobních zařízeních přístup k podnikovému e-mailu, bez nutnosti něco nastavovat.<br /><br />Podrobnosti najdete v tématu [Konfigurace přístupu k podnikovému e-mailu pomocí e-mailových profilů v Microsoft Intune](../Topic/Configure_access_to_corporate_email_using_email_profiles_with_Microsoft_Intune.md).|
|**Obecná konfigurace (Windows 10 Desktop a Mobile a novější)**|-   Konfigurovat zabezpečení mobilních zařízení a funkční nastavení pro zaregistrovaná zařízení s Windows 10 Desktop a Mobile.<br /><br />Podrobnosti najdete v tématu [Nastavení zásad konfigurace Windows 10 v Microsoft Intune](../Topic/Windows_10_configuration_policy_settings_in_Microsoft_Intune.md).|
|**Obecná konfigurace (Windows 10 Team a novější)**|-   Nakonfigurujte nastavení funkcí a zabezpečení zařízení pro registrovaná zařízení se systémem Windows 10 Team (například zařízení Surface Hub).<br /><br />Podrobnosti najdete v tématu [Nastavení zásad konfigurace pro Windows Team v Microsoft Intune](../Topic/Windows_Team_configuration_policy_settings_in_Microsoft_Intune.md).|
|**Obecná konfigurace (Windows 8.1 a novější)**|-   Konfigurovat zabezpečení mobilních zařízení a funkční nastavení pro zaregistrovaná zařízení s Windows.<br /><br />Podrobnosti najdete v tématu [Nastavení zásad konfigurace pro Windows v Microsoft Intune](../Topic/Windows_configuration_policy_settings_in_Microsoft_Intune.md).|
|**Obecná konfigurace (Windows Phone 8.1 a novější)**|-   Nakonfigurovat zabezpečení mobilního zařízení a funkční nastavení<br />-   Zadat aplikace, které uživatelé můžou nebo nemůžou používat a blokovat instalaci nebo použití nevyhovujících aplikací.<br /><br />Podrobnosti najdete v tématu [Nastavení zásad konfigurace pro Windows Phone v Microsoft Intune](../Topic/Windows_Phone_configuration_policy_settings_in_Microsoft_Intune.md).|
|**Profil certifikátu PKCS #12 (.PFX) (Windows 10 Desktop a Mobile a novější)**|-   Použít tento profil k vytvoření a nasazení nastavení PFX pro požadavky certifikátů zařízení.<br /><br />Podrobnosti najdete v tématu [Povolení přístupu k firemním prostředkům pomocí profilů certifikátů v Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md).|
|**Profil certifikátu SCEP (Windows 8.1 a novější)**<br /><br />**Profil certifikátu SCEP (Windows Phone 8.1 a novější)**|-   Nakonfigurujte certifikát protokolu SCEP, který můžete použít společně s certifikátem důvěryhodného mobilního zařízení k ověřování mobilních zařízení a povolení jejich přístupu k síťovým prostředkům, například nakonfigurovaným profily Wi-Fi a VPN.<br /><br />Podrobnosti najdete v tématu [Povolení přístupu k firemním prostředkům pomocí profilů certifikátů v Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md).|
|**Profil důvěryhodného certifikátu (Windows 8.1 a novější)**<br /><br />**Profil důvěryhodného certifikátu (Windows Phone 8.1 a novější)**|-   Nakonfigurujte certifikát důvěryhodného mobilního zařízení, který můžete použít k ověřování mobilních zařízení a povolení jejich přístupu k síťovým prostředkům, například nakonfigurovaným profily Wi-Fi a VPN.<br /><br />Podrobnosti najdete v tématu [Povolení přístupu k firemním prostředkům pomocí profilů certifikátů v Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md).|
|**Profil VPN (Windows 10 Desktop a Mobile a novější)**<br /><br />**Profil VPN (Windows Phone 8.1 a novější)**<br /><br />**Profil VPN (Windows Phone 8.1 a novější)**|-   Nakonfigurujte a nasaďte nastavení, která uživatelům umožňují zabezpečený přístup k podnikové síti z jejich mobilních zařízení. Nasazením těchto nastavení minimalizujete úsilí koncových uživatelů potřebné pro připojení k jejich práci.<br /><br />Podrobnosti najdete v tématu [Pomoc uživatelům připojit s k práci pomocí profilů VPN v Microsoft Intune](../Topic/Help_users_connect_to_their_work_using_VPN_profiles_with_Microsoft_Intune.md).|
|**Import ve Wi-Fi**|-   Importujte a nasaďte konfigurace Wi-Fi pro Windows, které jste předtím exportovali do souboru.<br /><br />Podrobnosti najdete v tématu [Pomoc uživatelům s připojením k sítím společnosti pomocí Wi-Fi profilů s Microsoft Intune](../Topic/Help_users_connect_to_company_networks_using_Wi-Fi_profiles_with_Microsoft_Intune.md).|

### Software

|Název zásady|Použijte v případě, že chcete|
|----------------|---------------------------------|
|**Zásady spravovaného prohlížeče (Android 4 a novější)**<br /><br />**Zásady spravovaného prohlížeče (iOS 7.1 a novější)**|-   Zadejte weby, ke kterým uživatelé můžou a nemůžou přistupovat pomocí aplikace spravovaného prohlížeče.<br /><br />Podrobnosti najdete v tématu [Správa přístupu k internetu pomocí zásad spravované prohlížeče v Microsoft Intune](../Topic/Manage_Internet_access_using_managed_browser_policies_with_Microsoft_Intune.md).|
|**Zásady správy mobilních aplikací (Android 4 a novější)**<br /><br />**Zásady správy mobilních aplikací (iOS 7.1 a novější)**|-   Upravte funkce nasazovaných aplikací tak, aby byly v souladu s předpisy a zásadami zabezpečení vaší společnosti. Můžete například omezit operace vyjmutí, kopírování a vložení v rámci aplikace s omezeným přístupem, nebo aplikaci nakonfigurovat tak, aby všechny webové odkazy otevírala ve spravovaném prohlížeči.<br /><br />Podrobnosti najdete v tématu [Ochrana dat pomocí zásad správy mobilních aplikací v Microsoft Intune](../Topic/Configure_and_deploy_mobile_application_management_policies_in_the_Microsoft_Intune_console.md).|

### Obecná nastavení mobilních zařízení

|Název zásady|Použijte v případě, že chcete|
|----------------|---------------------------------|
|**Zásady Exchange ActiveSync**|-   Konfigurovat nastavení zabezpečení mobilních zařízení a funkční nastavení pro zařízení, která se spravují přes Exchange ActiveSync<br /><br />Podrobnosti najdete v tématu [Nastavení zásad Exchange ActiveSync v Microsoft Intune](../Topic/Exchange_ActiveSync_policy_settings_in_Microsoft_Intune.md).|
|**Zásady zabezpečení mobilních zařízení**|<ul><li>Konfiguruje nastavení pro mobilní zařízení (všechny platformy), včetně:<br /><br /><ul><li>Zabezpečení</li><li>Šifrování</li><li>Systému</li><li>E-mailu</li><li>Aplikací</li></ul></li></ul> **Important:** [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] teď nabízí oddělené **zásady konfigurace** pro každou platformu zařízení a tyto zásady obsahují nejaktuálnější nastavení, které můžete použít. Můžete pokračovat v používání zásad zabezpečení mobilních zařízení a všechna existující nasazení budou i nadále fungovat, měli byste ale naplánovat, aby se v co nejbližší době provedla migrace na nové zásady konfigurace.<br />Podrobnosti najdete v tématu [Nastavení zásad zabezpečení mobilního zařízení v Microsoft Intune](../Topic/Mobile_device_security_policy_settings_in_Microsoft_Intune.md).|

### Zásady podmíněného přístupu a zásady dodržování předpisů

#### Podmíněný přístup

|Název zásady|Použijte v případě, že chcete|
|----------------|---------------------------------|
|**Zásady Exchange Online**<br /><br />**Zásady místního systému Exchange**|-   Spravovat přístup k e-mailům Microsoft Exchange ze zařízení, která nespravuje [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] nebo která nevyhovují vytvořeným zásadám dodržování předpisů.<br /><br />Podrobnosti najdete v tématu [Správa přístupu k e-mailu s Microsoft Intune](../Topic/Manage_email_access_with_Microsoft_Intune.md).|
|**Zásady SharePointu Online**|-   Spravovat přístup k SharePointu Online ze zařízení, která nespravuje [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] nebo která nevyhovují vytvořeným zásadám dodržování předpisů.<br /><br />Podrobnosti najdete v tématu [Správa přístupu na SharePoint Online přes Microsoft Intune](../Topic/Manage_SharePoint_Online_access_with_Microsoft_Intune.md).|
> [!NOTE]
> Zásady podmíněného přístupu nenasazujte na uživatele a zařízení. Namísto toho můžete nakonfigurovat požadované zásady, které se použijí na všechny cílové skupiny v zásadách.

#### Zásady slučitelnosti

|Název zásady|Použijte v případě, že chcete|
|----------------|---------------------------------|
|**Zásady slučitelnosti**|-   Definovat úroveň souladu s předpisy pro zařízení a vytvářet zprávy o zařízeních, která nejsou v souladu s předpisy. Tyto zásady se společně s podmíněným přístupem používají k vyhodnocení zařízení, u kterých se mají blokovat služby.<br /><br />Podrobnosti najdete v tématu [Správa zásad dodržování předpisů zařízeními pro Microsoft Intune](../Topic/Manage_device_compliance_policies_for_Microsoft_Intune.md).|

### Správa počítače

|Název zásady|Použijte v případě, že chcete|
|----------------|---------------------------------|
|**Nastavení agenta Microsoft Intune**|Konfigurovat klienta [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] v počítačích, včetně nastavení pro:<br /><br />-   Endpoint Protection<br />-   Aktualizace softwaru<br />-   Plán kontrol zásad<br /><br />Tento typ zásad se dá nasadit jenom na skupiny zařízení.<br /><br />Klienti [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] stahují nové a aktualizované zásady podle nastavení **Četnost detekce aktualizací a aplikací**. Výchozí nastavení je 8 hodin. Aktualizaci zásad v počítačích ale můžete kdykoli vynutit.<br /><br />Podrobnosti najdete v tématu [Udržování počítačů s Windows v aktuálním stavu díky softwarovým aktualizacím v Microsoft Intune](../Topic/Keep_Windows_PCs_up_to_date_with_software_updates_in_Microsoft_Intune.md).|
|**Nastavení centra Microsoft Intune**|Konfigurovat podrobnosti, které se zobrazují v centru [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Center na spravovaných počítačích.<br /><br />Tento typ zásad se dá nasadit jenom na skupiny zařízení.<br /><br />Podrobnosti najdete v tématu [Běžné úlohy správy počítačů s Windows pomocí počítačového klienta Microsoft Intune](../Topic/Common_Windows_PC_management_tasks_with_the_Microsoft_Intune_computer_client.md).|
|**Nastavení brány Windows Firewall**|Nakonfiguruje nastavení brány Windows Firewall a výjimky pro běžné síťové komunikace v počítačích, včetně:<br /><br />-   BranchCache<br />-   Vzdálená pomoc<br />-   Sdílení médií<br /><br />Tento typ zásad se dá nasadit jenom na skupiny zařízení.<br /><br />Podrobnosti najdete v tématu [Pomoc se zabezpečením počítačů s Windows pomocí služby Endpoint Protection pro Microsoft Intune](../Topic/Help_secure_Windows_PCs_with_Endpoint_Protection_for_Microsoft_Intune.md).|

## Viz také
[Konfigurace a správa zařízení přes Microsoft Intune](../Topic/Configure_and_manage_devices_with_Microsoft_Intune.md)
[Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

