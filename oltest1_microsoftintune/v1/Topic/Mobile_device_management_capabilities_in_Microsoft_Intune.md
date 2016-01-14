---
description: na
keywords: na
title: Mobile device management capabilities in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f23b3ee7-78da-4e53-9fc2-78e58401bcf9
---
# Možnosti spr&#225;vy mobiln&#237;ch zař&#237;zen&#237; v Microsoft Intune
Intune podporuje správu mobilních zařízení s iOS a Androidem a zařízení Windows Phone. Podporuje také správu počítačů se systémem Windows RT, Windows a Mac OS X jako mobilních zařízení. Uživatelé používají *portál společnosti* k instalaci aplikací, zápisu (registraci) a odebírání zařízení a umožňuje jim obrátit se na IT oddělení nebo technickou podporu. Abyste mohli provést zápis mobilních zařízení, musíte nastavit [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] jako svoji *autoritu mobilního zařízení* a potom nakonfigurovat infrastrukturu tak, aby podporovala platformy, které chcete spravovat. To vyžaduje navázání vztahu důvěryhodnosti se zařízením.

## <a name="BKMK_MobileDeviceReqs"></a>Podporovaná mobilní zařízení
Požadavky pro správu mobilního zařízení a úroveň vaší správy závisí na tom, jestli zařízení budete spravovat přímo nebo použijete Exchange ActiveSync:

-   **Přímá správa**: Různé typy mobilních zařízení mají různé požadavky na přímou správu. Pokud chcete spravovat třeba zařízení s iOS, potřebujete certifikát služby Apple Push Notification a správa aplikací pro zařízení s [!INCLUDE[winblue_winrt_2](../Token/winblue_winrt_2_md.md)] vyžaduje klíče pro zkušební načtení a certifikát pro podpis kódu.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] dokáže spravovat následující zařízení se správou mobilních zařízení:

    -   Apple iOS 7.1 a novější

        > [!NOTE]
        > Zařízení se systémem iOS 6.0, která jsou už zaregistrovaná, zůstanou zaregistrovaná, ale pokud budete chtít zaregistrovat do Intune nová zařízení, musí používat iOS verze 7.1 nebo novější.

    -   Google Android 4.0 nebo novější (zahrnuje Samsung KNOX)

    -   Windows Phone 8.0 nebo novější

    -   Windows RT a Windows 8.1 RT

    -   Počítače s Windows 8.1 a novější (spravované jako mobilní zařízení; viz [Možnosti správy počítačů s Windows v Microsoft Intune](../Topic/Windows_PC_management_capabilities_in_Microsoft_Intune.md))

    -   Mac OS X 10.9 a novější

    Abyste mohli mobilní zařízení spravovat přímo, musíte provést nastavení autority správy mobilních zařízení podle informací v článku [Nastavení autority správy mobilních zařízení na Microsoft Intune](../Topic/Set_mobile_device_management_authority_and_configure_Microsoft_Intune.md).

-   **Exchange ActiveSync**: Abyste mohli spravovat zařízení pomocí Exchange ActiveSync, musíte nainstalovat konektor On-Premises Connector nebo použít integrovaný konektor Service to Service Connector pro připojení k Exchange Serveru.

    Další informace o požadavcích na hardware a software pro instalaci konektoru On-Premises Connector najdete v části [Požadavky na konektor On-Premises Connector](../Topic/Network_infrastructure_requirements_for_Microsoft_Intune.md#BKMK_ExchanceConnectorReqs).

    Další informace o použití konektoru On-Premises Connector nebo konektoru Service to Service Connector se Exchange najdete v tématu [Správa mobilních zařízení pomocí protokolu Exchange ActiveSync a služby Microsoft Intune](../Topic/Mobile_device_management_with_Exchange_ActiveSync_and_Microsoft_Intune.md).

## Funkce správy mobilních zařízení
Intune podporuje správu mobilních zařízení s iOS a Androidem a zařízení Windows Phone. Také podporuje správu počítačů se systémem Windows RT a Windows jako mobilních zařízení.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] umožňuje spravovat zařízení uživatelů (často se používá označení „Přineste si vlastní zařízení“ (BYOD – Bring Your Own Device). Umožňuje také spravovat zařízení v majetku společnosti, včetně situací, kdy dá společnost uživatelům seznam zařízení, ze kterého mohou vybírat (CYOD – Choose Your Own Device).

Můžete zaregistrovat zařízení, aby splňovalo potřeby vaší organizace:

|Typ registrace|Uživatelé s vlastním zařízením|Uživatelé s firemním zařízením|Sdílené zařízení s účtem správce|Sdílené zařízení bez účtu správce|
|------------------|----------------------------------|----------------------------------|------------------------------------|-------------------------------------|
|**Popis**|Osobní zařízení zaregistrované pomocí Microsoft Intune|Zařízení jediného uživatele vlastněné společností|Zařízení vlastněné společností, sdílené mnoha uživateli a spravované účtem správce|Zařízení bez uživatele vlastněné společností a používané mnoha uživateli|
|**Uživatel zařízení**|Vlastník|Přiřazený uživatel|Žádný účet specifický pro uživatele|Bez konkrétního uživatele|
|**Kdo se registruje**|Vlastník|Správce|Správce zařízení|Kdokoliv|
|**Kdo ruší registraci**|Vlastník nebo správce|Správce|Správce|Správce|
|**Kdo resetuje**|Vlastník nebo správce|Správce|Správce|Správce|
Abyste mohli provést zápis mobilních zařízení, musíte nastavit [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] jako svoji *autoritu mobilního zařízení* a potom nakonfigurovat infrastrukturu tak, aby podporovala platformy, které chcete spravovat. To vyžaduje navázání vztahu důvěryhodnosti se zařízením.

Operace správy, inventáře, nasazování aplikací, zřizování a vyřazování z provozu probíhají prostřednictvím konzoly pro správu [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Uživatelé získají přístup k portálu společnosti, odkud můžou instalovat aplikace a registrovat a odebírat zařízení a odkud můžou snadno kontaktovat IT oddělení nebo technickou podporu.

**Funkce pro správu mobilních zařízení (MDM)** se mezi platformami mobilních zařízení liší, ale všechny platformy podporují následující:

-   **Profily certifikátů, e-mailů, VPN a Wi-Fi.** Do mobilních zařízení můžete nasazovat profily certifikátů, ale i e-mailové profily a profily VPN a Wi-Fi. Viz [Povolení přístupu k prostředkům společnosti se službou Microsoft Intune](../Topic/Enable_access_to_company_resources_with_Microsoft_Intune_-_deleted.md).

-   **Správa zařízení iOS vlastněných společností.** Můžete nastavit zařízení pro registraci a pak je distribuovat určitým uživatelům nebo můžete zaregistrovat zařízení, takže je může sdílet víc uživatelů. Viz [Nastavení správy iOS pomocí Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md).

-   **Správa mobilních aplikací.** Pro zvýšení ochrany vaší organizace se dají spravované mobilní aplikace nakonfigurovat tak, aby omezily určité operace, jako třeba kopírování a vkládání. Pomocí spravovaného prohlížeče můžete taky určovat, jaké weby můžou uživatelé navštívit. Viz [Ochrana dat pomocí zásad správy mobilních aplikací v Microsoft Intune](../Topic/Configure_and_deploy_mobile_application_management_policies_in_the_Microsoft_Intune_console.md) a [Správa přístupu k internetu pomocí zásad spravované prohlížeče v Microsoft Intune](../Topic/Manage_Internet_access_using_managed_browser_policies_with_Microsoft_Intune.md).

-   **Podmíněný přístup.** Zásady podmíněného přístupu [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] můžete použít k řízení přístupu k e-mailu místního Microsoft Exchange z mobilních zařízení, a to i v případě, že zařízení nespravuje Intune. Viz [Správa přístupu k e-mail a SharePointu pomocí Microsoft Intune](../Topic/Manage_access_to_email_and_SharePoint_with_Microsoft_Intune.md).

-   **Správa hesel** se pro různé platformy mobilních zařízení liší, ale všechny podporované platformy vám umožňují vyžadovat heslo, omezit počet neúspěšných pokusů o přihlášení, omezit dobu, po které se uzamkne obrazovka zařízení, nastavit dobu platnosti hesla a zabránit používání dříve použitých hesel.

-   **Nastavení aplikací.** Můžete ovládat nastavení prohlížeče a i taková nastavení aplikací, jako to, jestli se můžou na mobilních zařízeních používat obchody s aplikacemi.

-   **Mobilní a hlasové možnosti zařízení.** Můžete povolit nebo zakázat používání fotoaparátu, ovládat nastavení roamingu a povolit nebo zakázat hlasového asistenta iOS a funkce hlasového vytáčení.

-   **Resetování hesel, uzamčení zařízení a selektivní vymazání nebo vyřazení zařízení z provozu.** Můžete resetovat hesla, když uživatelé ztratí přístup ke svým zařízením, uzamknout ztracená nebo odcizená zařízení nebo z takových zařízení dokonce vymazat data.

## Konfigurace a zabezpečení zařízení

|Funkce|Podrobnosti|Další informace|
|----------|---------------|-------------------|
|Zásady konfigurace|Zásady konfigurace mobilního zařízení umožňují spravovat množství nastavení a funkcí na mobilních zařízeních ve vaší organizaci.|[Nastavení zásad konfigurace pro iOS v Microsoft Intune](../Topic/iOS_configuration_policy_settings_in_Microsoft_Intune.md)<br /><br />[Nastavení zásad konfigurace pro Android v Microsoft Intune](../Topic/Android_configuration_policy_settings_in_Microsoft_Intune.md)<br /><br />[Nastavení zásad konfigurace pro Windows v Microsoft Intune](../Topic/Windows_configuration_policy_settings_in_Microsoft_Intune.md)<br /><br />[Nastavení zásad konfigurace pro Windows Phone v Microsoft Intune](../Topic/Windows_Phone_configuration_policy_settings_in_Microsoft_Intune.md)<br /><br />[Nastavení zásad Exchange ActiveSync v Microsoft Intune](../Topic/Exchange_ActiveSync_policy_settings_in_Microsoft_Intune.md)<br /><br />[Nastavení zásad zabezpečení mobilního zařízení v Microsoft Intune](../Topic/Mobile_device_security_policy_settings_in_Microsoft_Intune.md)|
|Vlastní zásady|Vlastní zásady použijte při konfiguraci zásad, které neobsahují nastavení, které vyžadujete. Pro zařízení s iOS můžete importovat nastavení, které jste vyexportovali z nástroje Apple Configurator. Pro další zařízení můžete pomocí nastavení OMA-URI nakonfigurovat nastavení a funkce v zařízení.|[Nastavení vlastních zásad pro iOS v Microsoft Intune](../Topic/iOS_custom_policy_settings_in_Microsoft_Intune.md)<br /><br />[Nastavení vlastních zásad pro Android v Microsoft Intune](../Topic/Android_custom_policy_settings_in_Microsoft_Intune.md)<br /><br />[Nastavení vlastních zásad pro Windows Phone v Microsoft Intune](../Topic/Windows_Phone_custom_policy_settings_in_Microsoft_Intune.md)<br /><br />[Nastavení vlastních zásad pro Windows 10 v Microsoft Intune](../Topic/Windows_10_custom_policy_settings_in_Microsoft_Intune.md)|
|Vzdálené vymazání, Vzdálené uzamčení a Resetování hesla|Pokud dojde ke ztrátě nebo odcizení zařízení, vymažou se citlivá data. Zařízení můžete třeba vzdáleně uzamknout, obnovit do továrního nastavení nebo vymazat jenom firemní data.|[Chraňte svá data pomocí vzdáleného vymazání, vzdáleného zámku nebo resetování hesla pomocí Microsoft Intune](../Topic/Help_protect_your_data_with_remote_wipe,_remote_lock,_or_passcode_reset_using_Microsoft_Intune.md)|
|Celoobrazovkový režim|Umožňuje uzamknout určité funkce mobilních zařízení, třeba snímek obrazovky a vypínač. Umožňuje taky omezit zařízení tak, aby v nich mohla běžet jenom jedna vámi určená aplikace.|[Nastavení zásad konfigurace pro iOS v Microsoft Intune](../Topic/iOS_configuration_policy_settings_in_Microsoft_Intune.md)|

## Správa aplikací

|Funkce|Podrobnosti|Další informace|
|----------|---------------|-------------------|
|Správa a nasazení aplikací|Poskytuje řadu nástrojů, které vám pomůžou spravovat mobilní aplikace v průběhu jejich životního cyklu, včetně nasazení aplikací z instalačních souborů a obchodů s aplikacemi, podrobného sledování stavu aplikací a jejich odebrání.|[Nasazení aplikací do mobilních zařízení v Microsoft Intune](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune_-_deleted.md)|
|Kompatibilní a nekompatibilní aplikace|Umožňuje určit seznam kompatibilních aplikací (které uživatelé můžou nainstalovat) a nekompatibilních aplikací (které uživatelé nesmí nainstalovat).|[Nastavení zásad konfigurace pro iOS v Microsoft Intune](../Topic/iOS_configuration_policy_settings_in_Microsoft_Intune.md)|
|Správa mobilních aplikací|Nakonfigurujte omezení pro aplikace pomocí zásad správy mobilních aplikací. Umožňuje zvýšit zabezpečení firemních dat omezením operací, jako jsou třeba kopírování a vkládání, externí zálohování dat a přenos dat mezi aplikacemi.|[Ochrana dat pomocí zásad správy mobilních aplikací v Microsoft Intune](../Topic/Configure_and_deploy_mobile_application_management_policies_in_the_Microsoft_Intune_console.md)<br /><br />[Příprava aplikací pro iOS na správu mobilních aplikací nástrojem Microsoft Intune App Wrapping Tool](../Topic/Prepare_iOS_apps_for_mobile_application_management_with_the_Microsoft_Intune_App_Wrapping_Tool.md)<br /><br />[Příprava aplikací pro Android na správu mobilních aplikací nástrojem Microsoft Intune App Wrapping Tool](../Topic/Prepare_Android_apps_for_mobile_application_management_with_the_Microsoft_Intune_App_Wrapping_Tool.md)<br /><br />[Aplikace Microsoftu, které můžete použít se zásadami správy mobilních aplikací služby Microsoft Intune](../Topic/Microsoft_apps_you_can_use_with_Microsoft_Intune_mobile_application_management_policies.md)|
|Spravovaný prohlížeč|Po nasazení spravovaného prohlížeče pro uživatele můžete nakonfigurovat zásadu spravovaného prohlížeče pro řízení webů, které můžou uživatelé navštěvovat. Pro spravovaný prohlížeč můžete taky použít zásady správy mobilních aplikací.|[Správa přístupu k internetu pomocí zásad spravované prohlížeče v Microsoft Intune](../Topic/Manage_Internet_access_using_managed_browser_policies_with_Microsoft_Intune.md)|

## Přístup k prostředkům společnosti

|Funkce|Podrobnosti|Další informace|
|----------|---------------|-------------------|
|Profily certifikátů|Vytvořte a nasaďte profily důvěryhodných certifikátů a certifikáty protokolu SCEP (Simple Certificate Enrollment Protocol), které se dají použít k zabezpečení a ověření profilů Wi-Fi, VPN a e-mailu.|[Povolení přístupu k firemním prostředkům pomocí profilů certifikátů v Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md)|
|Profily sítě Wi-Fi|Nasaďte uživatelům nastavení bezdrátové sítě. Nasazením těchto nastavení minimalizujete úsilí koncových uživatelů potřebné k připojení k firemní síti.|[Pomoc uživatelům s připojením k sítím společnosti pomocí Wi-Fi profilů s Microsoft Intune](../Topic/Help_users_connect_to_company_networks_using_Wi-Fi_profiles_with_Microsoft_Intune.md)|
|E-mailové profily|Vytvořte a nasaďte nastavení e-mailu pro zařízení. Díky tomu mají uživatelé na svých osobních zařízeních přístup k podnikovému e-mailu, bez nutnosti něco nastavovat.|[Konfigurace přístupu k podnikovému e-mailu pomocí e-mailových profilů v Microsoft Intune](../Topic/Configure_access_to_corporate_email_using_email_profiles_with_Microsoft_Intune.md)|
|Profily sítě VPN|Nasaďte nastavení sítě VPN pro uživatele a zařízení ve vaší organizaci. Nasazením těchto nastavení zjednodušíte koncovým uživatelům připojování k prostředkům v síti společnosti.|[Pomoc uživatelům připojit s k práci pomocí profilů VPN v Microsoft Intune](../Topic/Help_users_connect_to_their_work_using_VPN_profiles_with_Microsoft_Intune.md)|
|Zásady podmíněného přístupu|Spravujte přístup k e-mailu Microsoft Exchange a službám SharePoint Online ze zařízení, která nespravuje [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].|[Správa přístupu k e-mail a SharePointu pomocí Microsoft Intune](../Topic/Manage_access_to_email_and_SharePoint_with_Microsoft_Intune.md)|

## Inventář a vytváření sestav

|Funkce|Podrobnosti|Další informace|
|----------|---------------|-------------------|
|Inventář a vytváření sestav|Vyhledejte informace o vámi spravovaných zařízeních a softwaru, který používají.<br /><br />Tyto sestavy můžete filtrovat několika způsoby, například podle platformy zařízení nebo kompatibility s firemními standardy.|[Pochopení operací Microsoft Intune pomocí sestav](../Topic/Understand_Microsoft_Intune_operations_by_using_reports.md)|

## Viz také
[Úvod do Microsoft Intune](../Topic/Introduction_to_Microsoft_Intune.md)
[Příprava registrace zařízení v Microsoft Intune](../Topic/Get_ready_to_enroll_devices_in_Microsoft_Intune.md)
[Správa mobilních zařízení a počítačů z cloudu](http://technet.microsoft.com/library/dn715906.aspx)
[Průvodce aspekty návrhu funkce BYOD (Přineste si vlastní zařízení)](http://technet.microsoft.com/library/dn656905.aspx)
[Registrace bezplatné zkušební verze](https://account.manage.microsoft.com/Signup/MainSignUp.aspx?OfferId=A77BE827-FC8B-4EF2-A0F5-7CD6C813AA65&ali=1)
[Jak koupit Intune](http://technet.microsoft.com/library/dn646949.aspx)
[Začít používat Microsoft Intune](../Topic/Start_using_Microsoft_Intune.md)
[Popis služby Microsoft Intune](../Topic/Microsoft_Intune_Service_Description.md)
[Začínáme s bezplatnou 30denní zkušební verzí Microsoft Intune](../Topic/Get_started_with_a_30-day_trial_of_Microsoft_Intune.md)

