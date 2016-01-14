---
description: na
keywords: na
title: Enable mobile device enrollment with the Microsoft Intune Account Portal
search: na
ms.date: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3adf63cd-34b6-4641-aa88-766bb59dd853
robots: noindex,nofollow
---
# Povolen&#237; registrace mobiln&#237;ch zař&#237;zen&#237; na port&#225;lu &#250;čtů Microsoft Intune
Intune umožňuje uživatelům zaregistrovat si vlastní zařízení na **portálu účtu** Microsoft Intune, a podporuje tak strategii BYOD (Bring Your Own Device – přineste si vlastní zařízení). Než začnete s registrací zařízení, musíte Intune nakonfigurovat na správu mobilních zařízení. Jestli jste v organizaci ještě nenastavili správu pro každou platformu zařízení:

-   [Správa iOS](http://technet.microsoft.com/library/dn408185.aspx)

-   [Správa Androidu](http://technet.microsoft.com/library/dn764960.aspx)

-   [Správa Windows](http://technet.microsoft.com/library/dn764959.aspx)

## Povolení registrace mobilních zařízení na portálu účtu Intune

1.  **Přidejte uživatele Intune.** 
    Abyste mohli mobilní zařízení zaregistrovat, musí být jeho vlastník přidaný do portálu účtu Microsoft Intune. Přihlaste se k [portálu účtu Microsoft Intune](http://account.manage.microsoft.com), klikněte na **Přidat uživatele** a vyberte některou možnost:

    -   **Uživatel**: Pokud chcete přidat jednoho uživatele, vyberte **Nový** &gt; **Uživatel** a zadejte **Podrobnosti**, **Přiřazení rolí**, **Nastavit umístění uživatele** a zařaďte uživatele do **skupiny**.

    -   **Hromadné přidání**: Vytvořte soubor .csv (podívejte se na dodané ukázkové soubory) a importujte ho do portálu účtu Intune. Zadejte role, umístění, skupiny a vytvořte účty. Ukázkové i prázdné soubory .csv si můžete stáhnout z portálu účtu Microsoft Intune.

    Můžete taky povolit synchronizaci s Active Directory nebo s Azure Active Directory. Další informace o integraci jiných uživatelů Azure Active Directory do Intune najdete v tématu [Synchronizace adresářů: rozcestník](http://go.microsoft.com/fwlink/?LinkId=511540) nebo na portálu účtu Intune klikněte na **Další způsoby přidávání uživatelů**.

2.  **Vytváření skupin**  (volitelné)
    Skupiny nabízejí flexibilitu při správě zařízení a uživatelů. Můžete je nastavit tak, aby odpovídaly potřebám vaší organizace (třeba podle zeměpisného umístění, oddělení nebo vlastností hardwaru).   Viz [Použití skupin pro správu uživatelů a zařízení s Microsoft Intune](../Topic/Use_groups_to_manage_users_and_devices_with_Microsoft_Intune.md).

3.  **Přidání zásad pro zařízení** (volitelné)
    Zásady jsou skupiny nastavení, které řídí funkce na zařízeních. Většina zásad MDM je specifických pro platformu. Zásady se vytvářejí pomocí šablon, které obsahují doporučená nebo přizpůsobená nastavení. Potom je můžete nasadit do skupin. Viz [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

4.  **Nastavte limit registrovaných zařízení.** (volitelné) 
    Pokud chcete omezit počet mobilních zařízení, která si může uživatel zaregistrovat, přihlaste se ke [konzole pro správu Microsoft Intune](http://manage.microsoft.com), klikněte na **Správce** &gt; **Správa mobilních zařízení** &gt; **Pravidla registrace**. Vyberte maximální počet zařízení, které může uživatel zaregistrovat, a klikněte na **Uložit**.

5.  **Nastavte portál firmy.**
     Firemní portál Intune můžete přizpůsobit potřebám své firmy. V [konzole pro správu Microsoft Intune](http://manage.microsoft.com) klikněte na **Správce** &gt; **Portál firmy**. Co můžete nakonfigurovat:

    -   **název společnosti,**

    -   **Jméno kontaktní osoby oddělení IT**

    -   **Telefonní číslo oddělení IT**

    -   **Další informace**

    -   **Adresa URL prohlášení o zásadách ochrany osobních údajů společnosti**

    -   **adresu URL webu podpory (nezobrazuje se),**

    -   **Název webu**

6.  **Nastavte podmínky a ujednání.** 
    Můžete publikovat podmínky a ujednání, které se uživatelům zobrazí při prvním použití portálu firmy z jakéhokoli zařízení. V [konzole pro správu Microsoft Intune](http://manage.microsoft.com) klikněte na **Portál společnosti** &gt; **Podmínky a ujednání**.

### <a name="BKMK_TermsAndConditions"></a>O podmínkách a ujednáních
Můžete publikovat podmínky a ujednání, které uživatelé uvidí, když na libovolném zařízení poprvé použijí portál firmy. Přitom nezáleží, jestli je zařízení registrované. Jestli uživatelé chtějí mít na portál přístup, musí tyto podmínky přijmout. Pokud podmínky a ujednání podstatně změníte a chcete, aby je uživatelé zobrazili a přijali, označte je jako novou verzi. Při další návštěvě portálu si uživatelé projdou stejný postup.

Podmínky a ujednání platí pro uživatele, nikoli pro zařízení. To znamená, že uživatelé, kteří chtějí firemní portál navštívit, musejí na některém svém zařízení přijmout každou verzi podmínek jenom jednou.

#### Sestavy podmínek a ujednání
Na sestavách **podmínek a ujednání** uvidíte, kteří uživatelé podmínky a ujednání přijali, jakou nejnovější verzi přijali a datum přijetí této verze. Sestavu můžete exportovat, abyste měli archivované datum přijetí předchozí verze uživateli. Viz [Pochopení operací Microsoft Intune pomocí sestav](../Topic/Understand_Microsoft_Intune_operations_by_using_reports.md).

### Registrace mobilních zařízení uživateli
Jakmile nastavíte registraci zařízení, můžete uživatele pozvat, aby si svá zařízení zaregistrovali. K dispozici jsou také [pokyny pro registraci v rámci služby Microsoft Intune](http://go.microsoft.com/fwlink/?LinkID=534864), které můžou uživatelům pomoct s registrací osobních zařízení.  Viz taky [Co říct koncovým uživatelům o používání služby Microsoft Intune](../Topic/What_to_tell_your_end_users_about_using_Microsoft_Intune.md).

Obecné pokyny:

1.  Uživatelé můžou svá mobilní zařízení zaregistrovat a spravovat v aplikaci Portál firmy. Uživatelé můžou také registrovat zařízení pomocí webu Portál společnosti.

    -   **Android** – Uživatelé si nainstalují aplikaci **Portál firmy** od společnosti Microsoft Corporation, která je dostupná na webu [Google Play](http://go.microsoft.com/fwlink/p/?LinkId=386612).

    -   **iOS** – uživatelé si nainstalují aplikaci **Company Portal** od společnosti Microsoft Corporation, která je dostupná v App Storu. Pak můžou uživatelé prohlížet svá **zařízení** a registrovat telefony.

    -   **Windows Phone 8.1** – uživatelé si nainstalují aplikaci **Company Portal** od společnosti Microsoft Corporation, která je dostupná ve Windows Phone Storu. Pokud se distribuovala podepsaná aplikace Portál společnosti, můžou taky uživatelé přejít do **Nastavení** &gt; **Pracovní prostor** &gt; **Přidat účet**, přihlásit se a potom klepnout na **Instalovat firemní aplikaci nebo centrum** a nainstalovat aplikaci Portál společnosti.

    -   **Windows Phone 8.0**  – Uživatelé kliknou na **Nastavení systému** &gt; **Firemní aplikace** a přihlásí se pomocí svého ID uživatele. Aplikace Portál společnosti se nasadí do telefonů uživatelů.

    -   **Windows 8.1 a Windows RT 8.1** – uživatelé si stáhnou aplikaci **Company Portal** z Windows Storu. Pokud se distribuovala podepsaná aplikace Portál společnosti, uživatel může taky přejít na **Nastavení počítače** &gt; **Síť** &gt; **Pracoviště**, přihlásit se, zaškrtnout políčko **Povolit aplikace a služby od správce IT** a pak kliknout na **Připojit**.

    -   **Windows RT** – Klikněte na **Start**, zadejte „konfigurace systému“ a kliknutím na dialogové okno otevřete **Firemní aplikace**.

2.  Firemní portál při otevření vyzve uživatele, aby zadali svá pověření. Jestli jste nevytvořili záznam CNAME veřejné domény, zobrazí se uživatelům Windows a Windows Phone žádost o adresu serveru, kam musí zadat „manage.microsoft.com“. Uživatelé telefonů s Windows Phone 8.1 a iOS si můžou prohlédnout **zaregistrovaná zařízení** a zaregistrovat si svůj telefon.

3.  Když se uživatel poprvé registruje (nebo pokud jste požadovali přijetí nové verze podmínek a ujednání), musí přijmout podmínky a ujednání. Zařízení se zaregistruje bez ohledu na to, jestli podmínky přijme. Pokud je přijmou, můžou pokračovat na portál. Pokud podmínky zamítnou, zobrazí se výzva, aby zamítnutí potvrdili, a pak se zobrazí odkaz na pokyny ke zrušení registrace. Ke zrušení registrace nedojde automaticky. Dokud uživatelé registraci nezruší, můžou zařízení spravovat.

    V tomto bodě se u dosud neregistrovaných zařízení proces liší podle operačního systému zařízení.

    -   U zařízení s Windows a Windows Phone 8.1 firemní portál uživatelům registraci připomene. Ve Windows Phone 8.1 bude odkaz na nastavení registrace. Ve Windows bude odkaz na nápovědu s popisem registrace.

    -   V zařízeních se systémy iOS a Android se uživateli zobrazí průvodce registrací. Uživatelům se zobrazí zpráva od Microsoftu o důsledcích registrace.

> [!CAUTION]
> Uživatelé systému Windows a Windows Phone budou moct najít registrační rozhraní a provést registraci bez zobrazení podmínek a ujednání. Poraďte uživatelům, ať kvůli zviditelnění webu a přijetí podmínek a ujednání začnou ve Windows Storu nebo ve Windows Phone Storu.

**Po zaregistrování zařízení můžete:**

-   [Seznámení se zařízeními s inventářem v Microsoft Intune](../Topic/Understand_your_devices_with_inventory_in_Microsoft_Intune.md)

-   [Povolení přístupu k prostředkům společnosti se službou Microsoft Intune](../Topic/Enable_access_to_company_resources_with_Microsoft_Intune_-_deleted.md)

-   [Nasazení aplikací do mobilních zařízení v Microsoft Intune](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune_-_deleted.md)

-   [Správa nastavení a funkcí v zařízeních pomocí zásad Microsoft Intune](../Topic/Manage_settings_and_features_on_your_devices_with_Microsoft_Intune_policies.md)

-   [Chraňte svá data pomocí vzdáleného vymazání, vzdáleného zámku nebo resetování hesla pomocí Microsoft Intune](../Topic/Help_protect_your_data_with_remote_wipe,_remote_lock,_or_passcode_reset_using_Microsoft_Intune.md)

## Viz také
[Příprava registrace zařízení v Microsoft Intune](../Topic/Get_ready_to_enroll_devices_in_Microsoft_Intune.md)
[Přihlášení firemních zařízení pomocí manažera registrace zařízení v Microsoft Intune](../Topic/Enroll_corporate-owned_devices_with_the_Device_Enrollment_Manager_in_Microsoft_Intune.md)
[Jak koupit Intune](http://technet.microsoft.com/library/dn646949.aspx)

