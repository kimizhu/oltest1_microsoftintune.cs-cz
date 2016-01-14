---
description: na
keywords: na
title: Frequently asked questions for Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a8126cca-9ec4-454b-a20b-dc1bb6797327
---
# Nejčastějš&#237; dotazy k Microsoft Intune
Toto téma obsahuje odpovědi na nejčastější dotazy týkající se služby Microsoft Intune. Pokud máte návrhy na další otázky, na které byste si rádi přečetli odpovědi, [dejte nám vědět](https://microsoftintune.uservoice.com/).

## Obsah tohoto článku
Tyto nejčastější dotazy jsou rozdělené do následujících kategorií:

-   [Obecné](#BKMK_General)

-   [Účty](#BKMK_Accounts)

-   [Registrace](#BKMK_Enrollment)

-   [Správa mobilních zařízení](#BKMK_MDM)

-   [Nasazení aplikací](#BKMK_App_Deploy)

-   [Zabezpečení](#BKMK_Security)

-   [Portál společnosti](#BKMK_Company_Portal)

-   [Microsoft Intune s Configuration Managerem](#BKMK_hybrid)

### <a name="BKMK_General"></a>Obecné

-   **Jak poznám, kdy se služba Microsoft Intune aktualizovala?**

    Přihlaste se k svému účtu na adrese manage.microsoft.com. V části Přehled správy vyberte Zobrazit stav služby. Zobrazí se umístění vašeho tenanta a plán údržby. Podrobnosti o aktualizacích služby najdete v článku [Co je nového ve Microsoft Intune](../Topic/What_s_new_in_Microsoft_Intune.md).

-   **Pokud uživatel přejmenuje zařízení v aplikaci Portál společnosti, změní se tento název taky v Intune nebo v Configuration Manageru?**

    Ne, tato změna názvu jenom usnadňuje práci uživatele v aplikaci.

-   **Zahrnuje Intune funkce vzdálené pomoci pro mobilní zařízení?**

    Ne. Mohly by se vám hodit aplikace nezávislých dodavatelů, jako jsou [Lumia Beamer](https://www.lumiabeamer.com/), [Bomgar](http://www.bomgar.com/) nebo [TeamViewer](https://www.teamviewer.com/).

### <a name="BKMK_Accounts"></a>Účty

-   **Pokud si pořídím zkušební verzi Intune a vytvořím pro ni nového tenanta, můžu pro stejného tenanta přidat taky zkušební verzi O365?**

    Ano. Stačí jenom, když se přihlásíte pomocí účtu globálního správce ze svého tenanta/předplatného Intune, například *globaladmin@&lt;společnost&gt;.onmicrosoft.com*.

-   **Když ve zkušebním předplatném Intune přiřadím autoritu MDM, znesnadní mi to přechod na službu jiné společnosti, pokud by se mi Intune nelíbilo?**

    Věříme tomu, že se rozhodnete u Intune zůstat, ale volba autority MDM když tak nijak nebrání tomu, abyste přešli na jinou službu. Při této volbě jde jenom o to, jestli si zvolíte Intune nebo Intune se System Center Configuration Managerem nebo MDM v O365.

-   **Můžeme pro účet Intune použít náš stávající název domény v Office 365?**

    Ano. Je k tomu jenom potřeba, abyste se při vytváření zkušební verze Intune nebo aktivaci licencí přihlásili přes ID vaší organizace, které je přidružené k existujícímu tenantu O365 a ověřené doméně. Intune pak bude používat stejnou doménu, uživatele a další věci jako ve vašem účtu O365. Upozorňujeme ale, že jednotliví uživatelé O365 se musí aktivovat jako uživatelé Intune pomocí licence na Intune. Toto musí udělat globální správce, který spravuje tenanta.

### <a name="BKMK_Enrollment"></a>Registrace

-   **Kde můžou naši uživatelé zjistit, jak si můžou zaregistrovat svoje zařízení?**

    Můžete použít nebo si přizpůsobit informace z [pokynů k registraci pro Microsoft Intune](http://www.microsoft.com/en-us/download/46398).

-   **Jak můžu vyřešit potíže s registrací zařízení?**

    Způsoby řešení běžných problémů s registrací jsou popsané v článku [Řešení potíží s registrací do služby Intune](../Topic/Troubleshoot_device_enrollment_in_Intune.md).

-   **Jak můžu shromáždit protokoly registrace, když má nějaký uživatel problém s registrací?**

    Postupujte podle [těchto pokynů](http://www.microsoft.com/en-us/download/46391).

### <a name="BKMK_MDM"></a>Správa mobilních zařízení

-   **Obecná správa mobilních zařízení**

    -   **Dokáže Intune zjistit, jestli má zařízení jailbreak?**

        Ano, u některých operačních systémů. Informace o správě zařízení s jailbreakem najdete v článku [Správa zásad dodržování předpisů zařízeními pro Microsoft Intune](../Topic/Manage_device_compliance_policies_for_Microsoft_Intune.md).

    -   **Můžu selektivně vymazat podniková data ze zařízení?**

        Ano. Informace o selektivním vymazání najdete v článku [Chraňte svá data pomocí vzdáleného vymazání, vzdáleného zámku nebo resetování hesla pomocí Microsoft Intune](../Topic/Help_protect_your_data_with_remote_wipe,_remote_lock,_or_passcode_reset_using_Microsoft_Intune.md).

    -   **Existuje způsob, jak prostřednictvím Intune blokovat určité weby v prohlížeči mobilního zařízení?**

        V nativním prohlížeči neexistuje na žádné platformě. Můžete ale povolit nebo blokovat adresy URL, pokud jste nasadili webový prohlížeč spravovaný službou [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] v zařízeních s iOS a Androidem. Další informace najdete v článku [Správa přístupu k internetu pomocí zásad spravované prohlížeče v Microsoft Intune](../Topic/Manage_Internet_access_using_managed_browser_policies_with_Microsoft_Intune.md).

    -   **Můžeme uživateli znemožnit odinstalaci aplikace?**

        Obecně ne. Na zařízeních iOS, která máte pod dohledem, ale můžete uživatelům bránit v odinstalaci aplikací distribuovaných přes Apple Configurator. Informace o používání dohledového režimu v Microsoft Intune najdete v článku [Manage access to apps using Microsoft Intune configuration policies - deleted](../Topic/Manage_access_to_apps_using_Microsoft_Intune_configuration_policies_-_deleted.md).

    -   **Existuje způsob, jak spravovat využití mobilní dat?**

        Ne přímo, ale můžete zajistit, aby Wi-Fi bylo upřednostňovanou metodou pro připojení, když do zařízení zavedete profily Wi-Fi podle popisu v článku [Pomoc uživatelům s připojením k sítím společnosti pomocí Wi-Fi profilů s Microsoft Intune](../Topic/Help_users_connect_to_company_networks_using_Wi-Fi_profiles_with_Microsoft_Intune.md). Některé platformy (třeba iOS a Android KNOX) taky umožňují určit nastavení pro hlasový a datový roaming.

    -   **Existuje způsob, jak uživateli zabránit v zrušení registrace zařízení? Co když jde o zařízení, které vlastní naše společnost?**

        Obecně to možné není. Pomocí vlastních nastavení systému Windows Phone to ale můžete vynutit ve Windows Phone 8.1. Zabránit uživateli v zrušení registrace zařízení je taky možné u zařízení iOS, která jsou pod dohledem a zaregistrovaná v programu Apple DEP (Device Enrollment Program).

    -   **Můžeme si přepnout zvolenou autoritu MDM?**

        V některých situacích ano. Pokud to chcete udělat, kontaktujte podporu podle pokynů v článku [Jak získat podporu pro Microsoft Intune](../Topic/How_to_get_support_for_Microsoft_Intune.md). Následující tabulka popisuje, jaké změny jsou možné. Po změnách autority MDM se musí znovu registrovat zařízení.

        |||||
        |-|-|-|-|
        ||**Na:** Intune|**Na:** O365|**Na:** Configuration Manager s Intune|
        |**Z:** Intune||Ano&#42;|Ano|
        |**Z:** O365|Ano&#42;||Ano|
        |**Z:** Configuration Manager s Intune|Ano|Ano||
        &#42; Autority MDM v O365 a Intune můžou existovat společně, takže nebudete muset znovu registrovat mobilní zařízení.

-   **Windows**

    -   **Můžu si zkušebně načíst aplikaci z Windows Storu?**

        Veřejně dostupné aplikace se nedají zkušebně načíst. Můžete si sice stáhnout soubor XAP, ale nemůžete ho nahrát do Intune, protože jde o veřejný soubor XAP, který je šifrovaný a podepsaný pomocí certifikátu vývojáře pro podepisování kódu. Zkušebně načíst si můžete jenom aplikace, které jste sami vyvinuli a podepsali vlastním certifikátem pro podepisování kódu.

    -   **Je u aplikací z Windows Phone Storu distribuovaných přes Portál společnosti nutné, aby měl koncový uživatel účet Microsoft?**

        Ano, bez účtu Microsoft nebude moct koncový uživatel aplikace získat. Výjimkou jsou zkušebně načtené, privátní obchodní aplikace, které jde do zařízení nasadit bez účtu Microsoft.

    -   **Vyžaduje se účet Microsoft v zařízení s Windows Phone 8.1, aby se mohlo spravovat přes Intune?**

        Ne. Je ale potřebný k instalaci většiny aplikací z veřejného obchodu.

-   **Android**

    -   **Jak dlouho trvá šifrování zařízení s Androidem?**

        To závisí hlavně na rychlosti procesoru a celkovém objemu paměti a množství využité paměti v zařízení a není to funkcí Intune.

-   **iOS**

    -   **Pokud se při nasazování aplikací pro iOS přes Intune načte soubor IPA a soubor manifestu aplikace, musí se pro zařízení zadat Apple ID, aby se mohlo pokračovat v instalaci?**

        Ne. Pokud bity poskytuje Intune (soubor IPA je načtený do Intune), aplikace se zkušebně načítají a nevyžadují Apple ID.

    -   **Existuje způsob, jak povolit instalaci aplikací do iOS bez povolení přístupu k Apple Storu?**

        Ne, ale můžete povolit App Store a pomocí povolených a blokovaných aplikací v iOS dohlížet na to, co uživatelé dělají. Zkušebně načtené obchodní aplikace nevyžadují přístup k Apple App Storu.

    -   **Je u aplikací z Apple Storu distribuovaných přes Portál společnosti nutné, aby měl koncový uživatel účet iTunes?**

        Ano, bez účtu iTunes nebude moct koncový uživatel aplikace získat.

    -   **Můžeme App Store zablokovat?**

        Ano, můžete, ale zablokují se tím všechny instalace a aktualizace aplikací z App Storu, ne jenom instalace a aktualizace iniciované koncovým uživatelem. To znamená, že by ani nešlo nainstalovat žádné aplikace z veřejného App Storu, které byste chtěli nasadit z Intune.

### <a name="BKMK_App_Deploy"></a>Nasazení aplikací

-   **Jak můžu přidat doporučenou aplikaci?**

    V Intune se používá označení „vybrané aplikace“ a píše se o nich v článku [Nasazení aplikací do mobilních zařízení v Microsoft Intune](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune_-_deleted.md).

-   **Můžu získat dodatečné cloudové úložiště pro aplikace, které chci nasadit?**

    Ano. Můžete si o tom přečíst v článku [Začínáme s nasazováním aplikací v Microsoft Intune](../Topic/Plan_for_app_deployment_in_Microsoft_Intune.md) v sekci *Požadavky na cloudové úložiště*.

### <a name="BKMK_Security"></a>Zabezpečení

-   **Může Intune vynucovat použití BitLockeru?**

    Agent OMA-DM ve Windows 8.1/RT umožňuje přečíst (zjistit) stav šifrování. Nejde ho ale nastavit. To platí nejen pro Microsoft Intune, ale i jiné služby pro správu mobilních zařízení.

-   **Pokud tablet s Windows 8 šifruji pomocí BitLockeru, můžu vynutit úplné vymazání zařízení v případě, že se uživateli několikrát po sobě nepodaří přihlásit se?**

    V zařízeních s Windows 8.1/RT není žádná možnost pro úplné vymazání v žádné službě pro správu mobilních zařízení včetně Intune. Intune pro tato zařízení poskytuje selektivní vymazání. Další informace o vymazání / selektivním vymazání v Intune najdete v článku [Chraňte svá data pomocí vzdáleného vymazání, vzdáleného zámku nebo resetování hesla pomocí Microsoft Intune](../Topic/Help_protect_your_data_with_remote_wipe,_remote_lock,_or_passcode_reset_using_Microsoft_Intune.md).

### <a name="BKMK_Company_Portal"></a>Portál společnosti

-   **Je možné přizpůsobení Portálu společnosti?**

    Ano. V konzole pro správu Intune najdete tato nastavení v sekci **Správce &gt; Portál společnosti**.

### <a name="BKMK_hybrid"></a>Microsoft Intune s Configuration Managerem

-   **Když se používá Configuration Manager s Intune, kde se spravují zařízení?**

    Spravujte všechny vaše zařízení z konzoly Configuration Manageru, i přes to, že zařízení s instalovaným agentem Intune se zobrazí v konzole Intune. Mobilní zařízení se v konzole Intune nezobrazí.

-   **Jde na zařízeních provést selektivní vymazání?**

    Pokud společně s Intune používáte System Center 2012 R2 Configuration Manager nebo novější, můžete provést selektivní vymazání, kterým se odeberou firemní data. Další informace naleznete v části [Chraňte svá data pomocí vzdáleného vymazání, vzdáleného zámku nebo resetování hesla pomocí Microsoft Intune](../Topic/Help_protect_your_data_with_remote_wipe,_remote_lock,_or_passcode_reset_using_Microsoft_Intune.md).

-   **Pokud používám Configuration Managera společně s Intune, můžu dál používat portál pro správu Intune?**

    Ano, ale z tohoto portálu bude možné spravovat jenom počítače s nainstalovaným agentem Intune. Na portálu jsou taky některé další užitečné informace týkající se výstrah o službě, stavu služby atd., ale žádné nastavení správy zařízení z něj nebude platit pro registrovaná zařízení.

## Viz také
[Technické reference pro Microsoft Intune](../Topic/Technical_reference_for_Microsoft_Intune.md)

