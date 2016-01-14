---
description: na
keywords: na
title: Enroll corporate-owned iOS devices in Microsoft Intune
search: na
ms.date: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2d3ca4ab-f20c-4d56-9413-f8ef19cf0722
robots: noindex,nofollow
---
# Registrace zař&#237;zen&#237; iOS vlastněn&#253;ch společnost&#237; v Microsoft Intune
Intune podporuje registraci firemních zařízení iOS prostřednictvím programu Apple Device Enrollment Program (DEP) nebo pomocí nástroje [Apple Configurator](http://go.microsoft.com/fwlink/?LinkId=518017) spuštěného na počítači Mac.

Existují tři způsoby registrace firmou zaregistrovaných zařízení iOS:

-   **Registrace v průvodci nastavením** – Obnoví tovární nastavení a připraví zařízení k nastavení jeho novým uživatelem. Tento způsob podporuje registraci v programu i použití Apple Configuratoru.

-   **Přímá registrace** – Vytvoří soubor kompatibilní s Apple Configuratorem, který můžete použít při přípravě zařízení. Zaregistrované zařízení nemá obnovené tovární nastavení a nemá přiřazeného uživatele. Tento způsob nejde použít k registraci v programu DEP.

-   **Program registrace zařízení (DEP)** – Nasadí profil registrace, který zařízení registruje „vzduchem“ a může zahrnovat možnosti pomocníka nastavení zařízení. U zařízení zaregistrovaných v programu DEP uživatelé nemůžou registraci zrušit.

## Pokyny průvodce nastavením

1.  **Vytvořte skupinu mobilních zařízení** (volitelné). 
    Jestli podnik potřebuje ke správě zařízení skupiny mobilních zařízení, vytvořte je.[Použití skupin pro správu uživatelů a zařízení s Microsoft Intune](../Topic/Use_groups_to_manage_users_and_devices_with_Microsoft_Intune.md).

2.  **Vytvořte profil zařízení.**
    Profil registrace zařízení definuje nastavení, která se použijí pro skupinu zařízení. Jestli jste to ještě neudělali, vytvořte profil registrace zařízení pro zařízení iOS zaregistrovaná v Apple Configuratoru. Při registraci v **průvodci nastavením** by měla být zapnutá **výzva k přidružení uživatele**.

    ###### Pokyny

    1.  V [konzole pro správu Microsoft Intune](http://manage.microsoft.com) přejděte na **Zásady** &gt; **Zařízení ve vlastnictví firmy** a klikněte na **Přidat**.

    2.  Zadejte podrobnosti profilů zařízení:

        -   **Název** – Název profilu registrace zařízení. (Uživatelé ho nevidí.)

        -   **Popis** – Popis profilu registrace zařízení. (Uživatelé ho nevidí.)

        -   **Přidružení uživatele** – Určuje, jak se budou zařízení registrovat.

            -   **Výzva ke spřažení uživatele** – Při počátečním nastavení je možné zařízení spojit s uživatelem a pak mu umožnit přístup k firemním datům a e-mailu. Tento režim podporuje různé scénáře:

                -   **Osobní zařízení vlastněné společností** – „Vyberte si vlastní zařízení“ (CYOD). Podobá se vlastním soukromým nebo osobním zařízením s tím, že správce má určitá privilegia, třeba právo zařízení vymazat, resetovat, spravovat nebo zrušit jeho registraci. Uživatel zařízení může instalovat aplikace a má i většinu dalších oprávnění k používání zařízení, pokud je neblokují zásady správy.

                -   **Účet správce registrace zařízení** – K registraci zařízení se použije zvláštní účet správce Intune. Zařízení je možné spravovat jako soukromý účet, ale instalovat aplikace, vymazat, resetovat nebo spravovat zařízení nebo zrušit jeho registraci může jenom uživatel, který zná pověřovací údaje správce registrace. Informace o registraci zařízení sdíleného mnoha uživateli prostřednictvím společného účtu najdete v tématu [Přihlášení firemních zařízení pomocí manažera registrace zařízení v Microsoft Intune](../Topic/Enroll_corporate-owned_devices_with_the_Device_Enrollment_Manager_in_Microsoft_Intune.md).

            -   **Bez spřažení uživatele** – Zařízení nemá definovaného uživatele. Toto spřažení použijte u zařízení určených k plnění úkolů, u kterých není potřeba přístup k místním uživatelským datům. Aplikace, které vyžadují spřažení s uživatelem, jsou zakázané nebo nefungují.

        -   **Předběžné přiřazení skupiny zařízení** – Do této skupiny na začátku patří všechna zařízení nasazená s tímto profilem. Po registraci můžete zařízení přiřadit někomu jinému.

    3.  Jestli chcete profil přidat, klikněte na **Uložit profil**.

3.  **Přidejte zařízení iOS, která chcete zaregistrovat v průvodci nastavením**
    V [konzole pro správu Microsoft Intune](http://manage.microsoft.com) přejděte na **Skupiny** &gt; **Všechna zařízení** &gt; **Všechna zařízení ve vlastnictví firmy** &gt; **Všechna zařízení** a klikněte na **Přidat zařízení…**. Zařízení můžete přidat dvěma způsoby:

    -   **Odesláním souboru CSV se sériovými čísly** – Vytvořte seznam oddělený čárkami (.csv), který bude mít dva sloupce a bude bez záhlaví. Soubor může obsahovat maximálně 5 000 zařízení, a nesmí být větší než 5 MB.

        |||
        |-|-|
        |&lt;Sériové č. 1&gt;|&lt;Podrobnosti o zařízení č. 1&gt;|
        |&lt;Sériové č. 2&gt;|&lt;Podrobnosti o zařízení č. 2&gt;|
        V textovém editoru vypadá soubor .csv takhle:

        ```
        0000000,PO 1234
        111111111,PO 1234
        ```

    -   **Ručním přidáním podrobností o zařízeních** – Zadejte sériové číslo a podrobnosti až o pěti zařízeních.

    > [!NOTE]
    > Pokud později musíte zařízení vlastněná firmou ze správy Intune odebrat, musíte odebrat sériové číslo zařízení z Intune ve skupině **Zařízení vlastněná firmou** a deaktivovat tak registraci zařízení.  Pokud Intune provádí postup pro zotavení po havárii v době, kdy se odebírala sériová čísla, je potřeba ověřit, jestli jsou v dané skupině dostupná sériová čísla jenom aktivních zařízení.

    Pak klikněte na **Další**.

4.  **Vyberte zařízení k registraci.**
    Potvrďte zařízení k registraci. Sériová čísla, která jsou zaregistrovaná nebo byla zaregistrovaná jiným způsobem, nejdou importovat. Pokračujte kliknutím na položku **Další**.

5.  **Přiřaďte profil.**
    V seznamu dostupných profilů vyberte profil, který se přiřadí přidávaným zařízením. Zkontrolujte **podrobnosti registračního profilu** a pak klikněte na **Dokončit**. Ručně přidávaným zařízením můžete přiřadit jakýkoli registrační profil, ale zařízením synchronizovaným v programu DEP musíte přiřadit profil s povoleným programem DEP.

6.  **Vyberte profil, který se nasadí na zařízení iOS.**
    V [konzole pro správu Microsoft Intune](http://manage.microsoft.com) přejděte na **Zásady** &gt;**Registrace podnikového zařízení** a vyberte profil, který se u mobilních zařízení nasadí. Na hlavním panelu klikněte na **Exportovat**. Zkopírujte a uložte **URL profilu**. Později URL odešlete do Apple Configuratoru, abyste definovali profil Intune používaný zařízeními iOS. U zařízení DEP jednoduše z tovární image spusťte průvodce nastavením nebo obnovte tovární nastavení zařízení.

7.  **Připravte zařízení Apple Configuratorem.** 
    Zařízení iOS jsou připojená k počítači Mac a zaregistrovaná do správy mobilních zařízení.

    > [!WARNING]
    > V průběhu registrace bude v zařízeních obnovená tovární konfigurace.

    1.  Na počítači Mac otevřete **Apple Configurator**.

    2.  Vyberte **Nastavení** a pak **Registrace zařízení**. Do **URL serveru pro správu mobilních zařízení** zadejte registrační adresu URL z Intune a klikněte na **Uložit**.

    3.  Mobilní zařízení iOS připojte adaptérem USB k počítači Apple.

    4.  Klikněte na **Připravit**. V Apple Configuratoru se zobrazí průběh přípravy.

8.  **Distribuujte zařízení.** 
    Zařízení jsou připravená na registraci ve společnosti. Vypněte zařízení a rozdejte je uživatelům. Po jeho zapnutí se spustí průvodce nastavením, který uživatele vyzve k zadání pracovního nebo školního účtu.

## Pokyny k přímé registraci

1.  **Vytvořte skupinu mobilních zařízení** (volitelné). 
    Pokud podnik nebo organizace potřebuje ke správě zařízení skupiny mobilních zařízení, vytvořte je.[Použití skupin pro správu uživatelů a zařízení s Microsoft Intune](../Topic/Use_groups_to_manage_users_and_devices_with_Microsoft_Intune.md).

2.  **Vytvořte profil zařízení.**
    Profil registrace zařízení definuje nastavení, která se pro zařízení použijí. Jestli jste to ještě neudělali, vytvořte profil registrace zařízení pro zařízení iOS zaregistrovaná v Apple Configuratoru.

    ###### Pokyny

    1.  V [konzole pro správu Microsoft Intune](http://manage.microsoft.com) přejděte na **Zásady** &gt; **Registrace podnikového zařízení** a klikněte na **Přidat…**.

    2.  Zadejte podrobnosti profilů zařízení:

        -   **Název** – Název profilu registrace zařízení. (Uživatelé ho nevidí.)

        -   **Popis** – Popis profilu registrace zařízení. (Uživatelé ho nevidí.)

        -   **Přidružení uživatele** – Určuje, jak se budou zařízení registrovat. U přímé registrace vyberte, že **nechcete zobrazovat výzvu**.

        -   **Předběžné přiřazení skupiny zařízení** – Do této skupiny na začátku patří všechna zařízení nasazená s tímto profilem. Po registraci můžete zařízení přiřadit někomu jinému.

    3.  Jestli chcete profil přidat, klikněte na **Uložit profil**.

3.  **Vyberte a exportujte soubor registračního profilu.** 
    V [konzole pro správu Microsoft Intune](http://manage.microsoft.com) přejděte na **Zásady** &gt; **Registrace podnikového zařízení** a vyberte profil zařízení, který nasadíte do zařízení iOS. Na hlavním panelu klikněte na **Exportovat**. Otevře se okno **Metoda konfigurace Apple**.

    V části **Metoda konfigurace Apple** vyberte **Přímá registrace**. Stáhněte a uložte si soubor přímého registračního profilu (.mobileconfig). Pokud chcete definovat profil Intune používaný zařízeními iOS, musíte soubor importovat do Apple Configuratoru. Soubor s registračním profilem platí 2 týdny.

4.  **Importujte soubor profilu a připravte zařízení.** 
    Zkopírujte soubor registračního profilu (.mobileconfig) z Intune do počítače Mac a naimportujte ho do Apple Configuratoru. Pak můžete k portu USB připojit zařízení iOS a zaregistrovat je Apple Configuratorem. Zařízení, která tímto souborem nakonfigurujete, musela dokončit průvodce nastavením. Při použití souboru musí být zařízení připojená k internetu.

## Zaregistrujte zařízení s iOS vlastněná společností v Microsoft Intune pomocí programu Apple Device Enrollment Program.
Aby mohly společnosti spravovat zařízení s iOS, která samy vlastní, pomocí programu Apple DEP (Device Enrollment Program), musí se do tohoto programu zapojit a musí prostřednictvím něj získat zařízení. Podrobnosti o procesu najdete na adrese: [https://deploy.apple.com](https://deploy.apple.com)

Abyste mohli v programu DEP registrovat zařízení iOS vlastněná společností, potřebujete od společnosti Apple token DEP. Token umožňuje Intune synchronizovat informace o zařízeních vlastněných společností, která se účastní programu DEP. Token taky umožňuje Intune odesílat společnosti Apple registrační profil a přiřazovat k těmto profilům zařízení.

### <a name="BKMK_DEPtok"></a>

1.  **Zahájení správy zařízení se systémem iOS v Microsoft Intune** 
    Před registrací zařízení do programu iOS Device Enrollment Program (DEP) musíte provést kroky uvedené v tématu [Nastavení správy iOS pomocí Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md).

2.  **Získání šifrovacího klíče** 
    Jako uživatel typu správce otevřete [konzolu pro správu Microsoft Intune](http://manage.microsoft.com), přejděte na **Správce** &gt; **Správa mobilních zařízení** &gt; **iOS** &gt; **Program DEP (Device Enrollment Program)** a klikněte na **Stáhnout šifrovací klíč**. Uložte soubor šifrovacího klíče (.pem) místně. Soubor .pem slouží k vyžádání certifikátu vztahu důvěryhodnosti z portálu Apple Device Enrollment Program.

3.  **Získejte token DEP (Device Enrollment Program).** 
    Přejděte na [portál programu Device Enrollment Program](https://deploy.apple.com) (https://deploy.apple.com) a přihlaste se pod firemním Apple ID, abyste vytvořili token DEP. Toto Apple ID musíte v budoucnosti použít k obnovení tokenu DEP.

    1.  Na [portálu programu Device Enrollment Program](https://deploy.apple.com) přejděte na **Device Enrollment Program** &gt; **Spravovat servery** a potom klikněte na **Přidat server MDM**.

    2.  Zadejte **název serveru MDM** a potom klikněte na **Další**. Název serveru slouží pro vaši informaci, abyste dokázali server MDM identifikovat. Není to název nebo adresa URL serveru Microsoft Intune.

    3.  Zobrazí se dialogové okno **Přidat &lt;název_serveru&gt;**. Klikněte na **Zvolit soubor...** a zvolte soubor .pem, který chcete nahrát. Potom klikněte na **Další**.

    4.  V dialogovém okně **Přidat &lt;název_serveru&gt;** se zobrazí odkaz s **vaším tokenem serveru**. Stáhněte si soubor tokenu serveru (.p7m) do počítače a potom klikněte na **Hotovo**.

    Soubor certifikátu (.p7m) se používá k navázání vztahu důvěryhodnosti mezi serverem Intune a serverem programu DEP (Device Enrollment Program) společnosti Apple.

4.  **Přidejte token DEP do Intune.** 
    V [konzole pro správu Microsoft Intune](http://manage.microsoft.com) přejděte na **Správa** &gt; **Správa mobilních zařízení** &gt; **iOS** &gt; **Device Enrollment Program** a klikněte na **Nahrát token DEP**.**Vyhledejte** soubor certifikátu (.p7m), zadejte své **Apple ID** a klikněte na **Nahrát**.

5.  **Přidání zásad registrace podnikových zařízení** 
    V [konzole pro správu Microsoft Intune](http://manage.microsoft.com) přejděte na **Zásady** &gt; **Registrace podnikového zařízení** a potom klikněte na **Přidat**. Zadejte **obecné** podrobnosti, včetně **názvu** a **popisu**, zadejte, jestli zařízení přiřazená k profilu uživatele mají spřažení s uživatelem nebo jestli patří do skupiny, a pak povolte nastavení **Nakonfigurujte nastavení DEP (Device Enrollment Program) pro tuto zásadu**, aby se podporoval program DEP.**Podokna Pomocníka s nastavením** definují nastavení zařízení iOS nakonfigurovaná v průběhu instalace.

6.  **Přiřazení zařízení DEP (Device Enrollment Program) pro správu.** 
    Přejděte na [portál programu Device Enrollment Program](https://deploy.apple.com) (https://deploy.apple.com) a přihlaste se pod firemním Apple ID, abyste vytvořili token DEP. Přejděte na **Program nasazení** &gt; **Device Enrollment Program** &gt; **Spravovat zařízení**. Zadejte, jak budete **volit zařízení** a zadejte podrobné informace o zařízení: **Sériové číslo**, **Číslo objednávky** nebo **Nahrát soubor CSV**. Potom vyberte **Přiřadit k serveru** a vyberte &lt;název_serveru&gt; zadaný pro Microsoft Intune. Potom klikněte na **OK**.

7.  **Distribuování zařízení uživatelům** 
    Zařízení vlastněná vaší společností se teď dají distribuovat uživatelům. Pokud je zařízení s iOS zapnuté, zaregistruje se jeho správa službou Intune.

8.  **Synchronizace zařízení spravovaných programem DEP** 
    Přihlaste se jako uživatel s oprávněními správce a otevřete [konzolu pro správu Microsoft Intune](http://manage.microsoft.com). Přejděte na **Správa** &gt; **Správa mobilních zařízení** &gt; **iOS** &gt; **Device Enrollment Program** a klikněte na **Synchronizovat**. Žádost o synchronizaci se pošle společnosti Apple. Pokud chcete po synchronizaci zobrazit zařízení spravovaná programem DEP, přejděte v [konzole pro správu Microsoft Intune](http://manage.microsoft.com) na **Skupiny** &gt; **Všechna zařízení ve vlastnictví firmy**. V pracovním prostoru **Všechna zařízení ve vlastnictví firmy** mají spravovaná zařízení **stav** Nekontaktované, dokud se zařízení nezapne a nespustí se Pomocník s nastavením pro registraci zařízení.

## Další kroky
**Po zaregistrování zařízení můžete:**

-   [Seznámení se zařízeními s inventářem v Microsoft Intune](../Topic/Understand_your_devices_with_inventory_in_Microsoft_Intune.md)

-   [Povolení přístupu k prostředkům společnosti se službou Microsoft Intune](../Topic/Enable_access_to_company_resources_with_Microsoft_Intune_-_deleted.md)

-   [Nasazení aplikací do mobilních zařízení v Microsoft Intune](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune_-_deleted.md)

-   [Správa nastavení a funkcí v zařízeních pomocí zásad Microsoft Intune](../Topic/Manage_settings_and_features_on_your_devices_with_Microsoft_Intune_policies.md)

-   [Chraňte svá data pomocí vzdáleného vymazání, vzdáleného zámku nebo resetování hesla pomocí Microsoft Intune](../Topic/Help_protect_your_data_with_remote_wipe,_remote_lock,_or_passcode_reset_using_Microsoft_Intune.md)

## Viz také
[Příprava registrace zařízení v Microsoft Intune](../Topic/Get_ready_to_enroll_devices_in_Microsoft_Intune.md)

