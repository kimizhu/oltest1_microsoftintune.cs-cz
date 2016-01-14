---
description: na
keywords: na
title: Set up iOS and Mac management with Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dc451224-1372-4b84-b641-cfa67cb3849b
---
# Nastaven&#237; spr&#225;vy iOS pomoc&#237; Microsoft Intune
Ve službě [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] můžete pro registraci zařízení se systémem iOS povolit funkci Přineste si vlastní zařízení (BYOD), která zajistí přístup k podnikovým e-mailům a aplikacím pro uživatele zařízení iPhone a iPad. Až uživatelé nainstalují aplikaci Portál společnosti služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], můžou se jejich zařízení prostřednictvím konzoly pro správu služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] stát cílem zásad.  Než budete moct spravovat zařízení se systémem iOS, musíte importovat certifikát APNs (Apple Push Notification service) od společnosti Apple. Tento certifikát umožňuje službě Intune spravovat zařízení s iOS a navázat akreditované, šifrované připojení IP se službami autorit pro správu mobilních zařízení.

Jako alternativu k registraci do aplikace Portál společnosti můžete také [registrovat zařízení iOS vlastněná společností](https://technet.microsoft.com/en-US/library/dn408185.aspx#BKMK_CODiOS) .

## Příprava na správu mobilních zařízení se systémem iOS v Microsoft Intune
Následující postup umožňuje službě [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] spravovat zařízení se systémem iOS pomocí portálu společnosti.

#### Nastavení registrace iOS v Intune

1.  **Nastavení Intune** 
    Pokud jste to ještě neudělali, připravte se na správu mobilních zařízení [nastavením autority pro správu mobilních zařízení](https://technet.microsoft.com/library/mt346013.aspx) na **Microsoft Intune**.

2.  **Získání žádosti o podepsání certifikátu** 
    Jako uživatel s oprávněním správce otevřete [konzolu pro správu Microsoft Intune](http://manage.microsoft.com), přejděte na **Správa** &gt; **Správa mobilních zařízení** &gt; **iOS** &gt; **Nahrát na server certifikát služby APN** a klikněte na **Stáhnout žádost certifikátu služby APN**. Uložte soubor žádosti o podepsání certifikátu (.csr) místně. Soubor .csr slouží k vyžádání certifikátu vztahu důvěryhodnosti z portálu Apple Push Certificates Portal.

    ![](../Image/Intune_iOS_enrollment_with_APNS.bmp)

3.  **Získání certifikátu APNs (Apple Push Notification Service)**
    Přejděte na portál [Apple Push Certificates Portal](http://go.microsoft.com/fwlink/?LinkId=269844) a přihlaste se pomocí Apple ID vaší společnosti, abyste mohli vytvořit certifikát služby APN pomocí souboru .csr. Toto Apple ID bude v budoucnu potřeba při obnovení certifikátu APNs. Stáhněte certifikát APNs (.pem) a uložte soubor místně. Tento soubor certifikátu APNs slouží k vytvoření vztahu důvěryhodnosti mezi serverem Apple Push Notification a autoritou pro správu mobilních zařízení služby Intune.

4.  **Přidání certifikátu APNs do služby Intune**
    V [konzole pro správu Microsoft Intune](http://manage.microsoft.com) přejděte na **Správa** &gt; **Správa mobilních zařízení** &gt; **iOS** &gt; **Nahrát na server certifikát služby APN** a klikněte na **Nahrát certifikát služby APN**.**Vyhledejte** soubor certifikátu (.pem), klikněte na **Otevřít** a pak zadejte svoje **Apple ID**. S certifikátem APNs může Intune registrovat a spravovat zařízení se systémem iOS vynucením zásady registrace mobilních zařízení.

5.  **Přidání uživatelů Intune** 
    Abyste mohli mobilní zařízení zaregistrovat, musí být jeho vlastník přidaný do portálu účtu. Přihlaste se k [portálu účtu Microsoft Intune](http://account.manage.microsoft.com), klikněte na **Přidat uživatele** a vyberte některou možnost:

    -   **Uživatel**: Pokud chcete přidat jednoho uživatele, vyberte **Nový** &gt; **Uživatel**, zadejte informace do polí **Podrobnosti**, **Přiřadit role** a **Nastavení umístění uživatele** a potom v poli **Skupina** přiřaďte uživatele do skupiny.

    -   **Hromadné přidání**: Vytvořte soubor .csv (podívejte se na dodané ukázkové soubory) a importujte ho na portál účtů. Zadejte role, umístění, skupiny a vytvořte účty. Ukázkové i prázdné soubory .csv si můžete stáhnout z portálu účtu.

    Můžete taky povolit synchronizaci s Active Directory nebo s Azure Active Directory. Pokud chcete další informace o integraci jiných uživatelů Azure Active Directory do Intune, přečtěte si téma [Synchronizace adresářů: rozcestník](http://go.microsoft.com/fwlink/?LinkId=511540) nebo na portálu účtu klikněte na **Další způsoby přidávání uživatelů**.

6.  **Vytváření skupin**  (volitelné)
    Skupiny nabízejí flexibilitu při správě zařízení a uživatelů. Můžete je nastavit tak, aby odpovídaly potřebám vaší organizace (třeba podle zeměpisného umístění, oddělení nebo vlastností hardwaru).   Viz [Použití skupin pro správu uživatelů a zařízení s Microsoft Intune](../Topic/Use_groups_to_manage_users_and_devices_with_Microsoft_Intune.md).

7.  **Přidání zásad pro zařízení** (volitelné)
    Zásady jsou skupiny nastavení, které řídí funkce na zařízeních. Většina zásad MDM je specifických pro platformu. Zásady se vytvářejí pomocí šablon, které obsahují doporučená nebo přizpůsobená nastavení. Potom je můžete nasadit do skupin. Viz [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

8.  **Nastavte limit registrovaných zařízení.** (volitelné) 
    Pokud chcete omezit počet mobilních zařízení, která si může uživatel zaregistrovat, přihlaste se ke [konzole pro správu Microsoft Intune](http://manage.microsoft.com), klikněte na **Správce** &gt; **Správa mobilních zařízení** &gt; **Pravidla registrace**. Vyberte maximální počet zařízení, které může uživatel zaregistrovat, a klikněte na **Uložit**.

9. **Nastavte portál firmy.**
     Portál společnosti Intune můžete přizpůsobit potřebám své firmy. V [konzole pro správu Microsoft Intune](http://manage.microsoft.com) klikněte na **Správce** &gt; **Portál společnosti**. Co můžete nakonfigurovat:

    -   **název společnosti,**

    -   **Jméno kontaktní osoby oddělení IT**

    -   **Telefonní číslo oddělení IT**

    -   **Další informace**

    -   **Adresa URL prohlášení o zásadách ochrany osobních údajů společnosti**

    -   **adresu URL webu podpory (nezobrazuje se),**

    -   **Název webu**

10. **Nastavení podmínek a ujednání**
     Můžete publikovat podmínky a ujednání, které uživatelé uvidí, když na libovolném zařízení poprvé použijí portál společnosti. Přitom nezáleží, jestli je zařízení registrované. Jestli uživatelé chtějí mít na portál přístup, musí tyto podmínky přijmout. Pokud podmínky a ujednání podstatně změníte a chcete, aby je uživatelé zobrazili a přijali, označte je jako novou verzi. Při další návštěvě portálu si uživatelé projdou stejný postup.

    V [konzole pro správu Microsoft Intune](http://manage.microsoft.com) klikněte na **Portál společnosti** &gt; **Podmínky a ujednání**.

    Určete následující nastavení:

    -   **Bude se od uživatelů vyžadovat, aby před použitím portálu společnosti přijali firemní podmínky a ujednání**

    -   **Název**

    -   **Text podmínek**

    -   **Vysvětlení, co to znamená, když uživatel přijme podmínky**

    Zobrazí se [podrobnosti o podmínkách a ujednáních](https://technet.microsoft.com/library/mt405893.aspx).  To, kteří uživatelé souhlasili s podmínkami a ujednáními, můžete také zjistit pomocí [sestav podmínek a ujednání](https://technet.microsoft.com/library/dn646977.aspx).

11. **Informování uživatelů, jak pomocí portálu společnosti získat přístup k firemním prostředkům** 
    [Co říct koncovým uživatelům o používání služby Microsoft Intune](../Topic/What_to_tell_your_end_users_about_using_Microsoft_Intune.md)

## <a name="BKMK_CODiOS"></a>Správa firemních zařízení (COD) pomocí Microsoft Intune
Jako alternativu k registraci do aplikace Portál společnosti můžete také registrovat zařízení Apple vlastněná společností. Intune podporuje registraci firemních zařízení iOS prostřednictvím programu Apple Device Enrollment Program (DEP) nebo pomocí nástroje [Apple Configurator](http://go.microsoft.com/fwlink/?LinkId=518017) spuštěného na počítači Mac.

Existují tři způsoby registrace firmou zaregistrovaných zařízení iOS:

-   **Program registrace zařízení (DEP)** – Nasadí profil registrace, který zařízení registruje „vzduchem“ a může zahrnovat možnosti pomocníka nastavení zařízení. U zařízení zaregistrovaných v programu DEP uživatelé nemůžou registraci zrušit.

-   **Registrace v průvodci nastavením** – Obnoví tovární nastavení a připraví zařízení k nastavení jeho novým uživatelem. Tento způsob podporuje registraci v programu i použití Apple Configuratoru.

-   **Přímá registrace** – Vytvoří soubor kompatibilní s Apple Configuratorem, který můžete použít při přípravě zařízení. V zaregistrovaném zařízení není obnovené výrobní nastavení. Tento způsob nejde použít k registraci v programu DEP. Tato metoda funguje jenom v případě, že jako přidružení uživatele je nastavené Bez přidružení uživatele.

> [!CAUTION]
> Zařízení zaregistrovaná těmito metodami nepodporují aplikaci Portál společnosti. Proto v nich nejsou dostupné některé funkce služby Intune, třeba [Podmíněný přístup](https://technet.microsoft.com/library/dn818907.aspx) a [Správa mobilních aplikací](https://technet.microsoft.com/library/dn878026.aspx). Pořád ale můžete do těchto zařízení nasadit [zásady](https://technet.microsoft.com/library/mt346005.aspx) služby Intune, [profily přístupu k prostředkům](https://technet.microsoft.com/library/dn997277.aspx) a [požadované aplikace](https://technet.microsoft.com/library/dn646955.aspx) (kromě [zařízení, která vyžadují zásadu MAM](https://technet.microsoft.com/library/dn708489.aspx)). Kvůli zajištění budoucí kompatibility s portálem společnosti byste měli pro svůj profil registrace do programu DEP nakonfigurovat nastavení **Výzva k přidružení uživatele** a nastavit v zařízení Apple ID.

### <a name="BKMK_DEP"></a>Správa Apple DEP pro zařízení s iOS pomocí Microsoft Intune
Aby vaše společnost mohla pomocí programu Apple DEP (Device Enrollment Program) spravovat zařízení s iOS, která sama vlastní, musí se do tohoto programu zapojit a musí prostřednictvím něj získat zařízení. Podrobnosti o tomto procesu najdete na [https://deploy.apple.com](https://deploy.apple.com). K výhodám tohoto programu patří bezobslužné nastavení zařízení, kdy není potřeba připojovat jednotlivá zařízení k počítači pomocí USB.

Abyste mohli v programu DEP registrovat zařízení iOS vlastněná společností, potřebujete od společnosti Apple token DEP. Token umožňuje Intune synchronizovat informace o zařízeních vlastněných společností, která se účastní programu DEP. Token taky umožňuje Intune odesílat společnosti Apple registrační profil a přiřazovat k těmto profilům zařízení.

#### <a name="BKMK_DEPtok"></a>Povolení správy DEP pomocí Intune

1.  **Zahájení správy zařízení se systémem iOS v Microsoft Intune** 
    Před registrací zařízení do programu iOS Device Enrollment Program (DEP) musíte pro službu Intune povolit správu zařízení iOS.

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

### <a name="BKMK_SAE"></a>Registrace Pomocníka s nastavením pro zařízení s iOS v Microsoft Intune
Pomocí Apple Configuratoru můžete v zařízeních s iOS obnovit tovární nastavení a připravit je pro nového uživatele.  Tato metoda vyžaduje, abyste zařízení s iOS připojili pomocí USB k počítači Mac a nastavili firemní prostředí.

##### Povolení registrace Pomocníka s nastavením v Intune

1.  **Vytvořte skupinu mobilních zařízení** (volitelné). 
    Jestli podnik potřebuje ke správě zařízení skupiny mobilních zařízení, vytvořte je.[Použití skupin pro správu uživatelů a zařízení s Microsoft Intune](../Topic/Use_groups_to_manage_users_and_devices_with_Microsoft_Intune.md).

2.  **Vytvořte profil zařízení.**
    Profil registrace zařízení definuje nastavení, která se použijí pro skupinu zařízení. Jestli jste to ještě neudělali, vytvořte profil registrace zařízení pro zařízení iOS zaregistrovaná v Apple Configuratoru. Při registraci v **průvodci nastavením** by měla být zapnutá **výzva k přidružení uživatele**.

    ###### Vytvoření profilu

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
        0000000,PO 1234 111111111,PO 1234
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

### <a name="BKMK_DE"></a>Přímá registrace zařízení s iOS v Microsoft Intune

##### Povolení přímé registrace v Intune

1.  **Vytvořte skupinu mobilních zařízení** (volitelné). 
    Pokud podnik nebo organizace potřebuje ke správě zařízení skupiny mobilních zařízení, vytvořte je.[Použití skupin pro správu uživatelů a zařízení s Microsoft Intune](../Topic/Use_groups_to_manage_users_and_devices_with_Microsoft_Intune.md).

2.  **Vytvořte profil zařízení.**
    Profil registrace zařízení definuje nastavení, která se pro zařízení použijí. Jestli jste to ještě neudělali, vytvořte profil registrace zařízení pro zařízení iOS zaregistrovaná v Apple Configuratoru.

    ###### Vytvoření profilu

    1.  V [konzole pro správu Microsoft Intune](http://manage.microsoft.com) přejděte na **Zásady** &gt; **Registrace podnikového zařízení** a klikněte na **Přidat…**.

    2.  Zadejte podrobnosti profilů zařízení:

        -   **Název** – Název profilu registrace zařízení. (Uživatelé ho nevidí.)

        -   **Popis** – Popis profilu registrace zařízení. (Uživatelé ho nevidí.)

        -   **Přidružení uživatele** – Určuje, jak se budou zařízení registrovat. Pro přímou registraci vyberte **Bez přidružení uživatele**.

        -   **Předběžné přiřazení skupiny zařízení** – Do této skupiny na začátku patří všechna zařízení nasazená s tímto profilem. Po registraci můžete zařízení přiřadit někomu jinému.

    3.  Jestli chcete profil přidat, klikněte na **Uložit profil**.

3.  **Vyberte a exportujte soubor registračního profilu.** 
    V [konzole pro správu Microsoft Intune](http://manage.microsoft.com) přejděte na **Zásady** &gt; **Registrace podnikového zařízení** a vyberte profil zařízení, který nasadíte do zařízení iOS. Na hlavním panelu klikněte na **Exportovat**. Otevře se okno **Metoda konfigurace Apple**.

    V části **Metoda konfigurace Apple** vyberte **Přímá registrace**. Stáhněte a uložte si soubor přímého registračního profilu (.mobileconfig). Pokud chcete definovat profil Intune používaný zařízeními iOS, musíte soubor importovat do Apple Configuratoru. Soubor s registračním profilem platí 2 týdny.

4.  **Importujte soubor profilu a připravte zařízení.** 
    Zkopírujte soubor registračního profilu (.mobileconfig) z Intune do počítače Mac a naimportujte ho do Apple Configuratoru. Pak můžete k portu USB připojit zařízení iOS a zaregistrovat je Apple Configuratorem. Zařízení, která tímto souborem nakonfigurujete, musela dokončit průvodce nastavením. Při použití souboru musí být zařízení připojená k internetu.

## Viz také
[Příprava registrace zařízení v Microsoft Intune](../Topic/Get_ready_to_enroll_devices_in_Microsoft_Intune.md)

