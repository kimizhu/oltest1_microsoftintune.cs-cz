---
description: na
keywords: na
title: Configure and deploy mobile application management policies in the Microsoft Intune console
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b4fb33a8-a2fa-4353-bd89-5bda48b68e83
---
# Ochrana dat pomoc&#237; z&#225;sad spr&#225;vy mobiln&#237;ch aplikac&#237; v Microsoft Intune
Zásady správy mobilních aplikací v [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] umožňují měnit funkce aplikací, které nasadíte, tak aby byly v souladu se zásadami kompatibility a zabezpečení vaší společnosti. Můžete třeba omezit operace vyjmutí, kopírování a vložení v rámci spravované aplikace nebo aplikaci nakonfigurovat tak, aby všechny webové odkazy otevírala ve spravovaném prohlížeči.

Podpora zásad správy mobilní aplikace:

-   Zařízení se systémem Android 4 nebo novější verzí

-   Zařízení se systémem iOS 7 nebo novější verzí

Na rozdíl od jiných zásad [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] nenasazujte zásadu správy mobilní aplikací přímo. Místo toho přidružíte zásadu k aplikaci, kterou chcete omezit. Při nasazení a instalaci aplikace na zařízení začne platit zadané nastavení.

Pokud chcete u aplikace použít omezení, musí aplikace obsahovat [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] sadu SDK (App Software Development Kit). Tento typ aplikace se dá získat dvěma způsoby:

-   **Použití aplikace se správou zásad** – Má integrovanou sadu App SDK. Pokud chcete tento typ aplikace přidat, zadáte odkaz na aplikaci z App Storu, jako je třeba iTunes Store nebo Google Play. Tento typ aplikace nevyžaduje žádné další zpracování. Podívejte se na seznam [Aplikace Microsoftu, které můžete použít se zásadami správy mobilních aplikací služby Microsoft Intune](../Topic/Microsoft_apps_you_can_use_with_Microsoft_Intune_mobile_application_management_policies.md).

-   **Použít zabalenou aplikaci** – Aplikace, které jsou znovu zabalené, aby používaly sadu App SDK, pomocí nástroje **Microsoft Intune App Wrapping Tool**. Tento nástroj se obvykle používá ke zpracování interně vytvořených podnikových aplikací. Nedá se použít ke zpracování aplikací stažených z App Storu. Viz [Příprava aplikací pro iOS na správu mobilních aplikací nástrojem Microsoft Intune App Wrapping Tool](../Topic/Prepare_iOS_apps_for_mobile_application_management_with_the_Microsoft_Intune_App_Wrapping_Tool.md) a [Příprava aplikací pro Android na správu mobilních aplikací nástrojem Microsoft Intune App Wrapping Tool](../Topic/Prepare_Android_apps_for_mobile_application_management_with_the_Microsoft_Intune_App_Wrapping_Tool.md).

Některé spravované aplikace, například Outlook pro iOS a Android, podporují **víc identit**. To znamená, že [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] v dané aplikaci aplikuje nastavení správy pouze na podnikové účty nebo data.

Například v případě aplikace Outlook:

-   Pokud si uživatel nakonfiguruje podnikový a osobní e-mailový účet, [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] aplikuje nastavení správy jenom na podnikový účet a osobní účet nespravuje.

-   Pokud je zařízení vyřazené nebo odregistrované, odeberou se z něj jenom firemní data Outlooku.

-   Použitý podnikový účet musí být ten samý účet, který byl použitý k registraci zařízení v [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

> [!TIP]
> Pokud službu [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] používáte s nástrojem [!INCLUDE[cmshort](../Token/cmshort_md.md)], projděte si téma [Jak ovládat aplikace pomocí zásad správy mobilních aplikací v Configuration Manageru](https://technet.microsoft.com/library/mt131414.aspx).

## Vytvoření a nasazení aplikace pomocí zásady správy mobilní aplikace

-   **Krok 1:** Získejte odkaz na aplikaci spravovanou zásadou nebo vytvořte zabalenou aplikaci.

-   **Krok 2:** Publikujte aplikaci do cloudového úložiště.

-   **Krok 3:** Vytvořte zásadu správy mobilní aplikace.

-   **Krok 4:**  Nasaďte aplikaci a vyberte k tomu možnost přidružení aplikace pomocí zásad správy mobilní aplikace.

-   **Krok 5:** Monitorujte nasazení aplikace.

## **Krok 1:** Získání odkazu na aplikaci spravovanou zásadou nebo vytvoření zabalené aplikace

-   **Pokud chcete získat odkaz na aplikaci spravovanou zásadou** – V App Storu vyhledejte a poznamenejte si adresu URL aplikace spravované zásadou, kterou chcete nasadit.

    Adresa URL aplikace Microsoft Word pro iPad je třeba **https://itunes.apple.com/us/app/microsoft-word-for-ipad/id586447913?mt=8**

-   **Vytvoření zabalené aplikace** – K vytvoření zabalené aplikace použijte informace v tématu [Příprava aplikací pro iOS na správu mobilních aplikací nástrojem Microsoft Intune App Wrapping Tool](../Topic/Prepare_iOS_apps_for_mobile_application_management_with_the_Microsoft_Intune_App_Wrapping_Tool.md) a [Příprava aplikací pro Android na správu mobilních aplikací nástrojem Microsoft Intune App Wrapping Tool](../Topic/Prepare_Android_apps_for_mobile_application_management_with_the_Microsoft_Intune_App_Wrapping_Tool.md).

    Nástroj vytvoří zpracovanou aplikaci, kterou použijete k publikování aplikace do svého cloudového úložiště.

## **Krok 2:** Publikování aplikace do cloudového úložiště
Když publikujete spravovanou aplikaci, postupy se liší v závislosti na tom, jestli publikujete aplikaci spravovanou zásadou nebo aplikaci zpracovanou pomocí nástroje Microsoft Intune App Wrapping Tool for iOS.

#### Publikování aplikace spravované zásadami

1.  Až budete připravení nahrát aplikaci do úložiště v cloudu, proveďte postup [Publish mobile device software to Microsoft Intune cloud storage](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune_-_deleted.md#BKMK_PublishSoftware).

2.  U aplikací pro iOS vyberte **Spravovaná aplikace pro iOS App z App Storu** v části **Vyberte, jakým způsobem má být tento software zpřístupněn pro zařízení**.

    V případě aplikací pro Android vyberte **Externí odkaz**.

3.  V části **Zadejte adresu URL** zadejte adresu URL aplikace spravované zásadou, kterou jste si předtím poznamenali.

Po dokončení nahrávání se zobrazí **Ano** u **Zásad správy aplikace** na stránce **Vlastnosti softwaru** nahrané aplikace.

Po ověření úspěšného nahrání aplikace pokračujte krokem 3.

#### Publikování aplikace zpracované pomocí nástroje Microsoft Intune App Wrapping Tool

1.  Až budete připravení nahrát aplikaci do úložiště v cloudu, proveďte postup [Publish mobile device software to Microsoft Intune cloud storage](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune_-_deleted.md#BKMK_PublishSoftware).

2.  V části **Vyberte, jakým způsobem má být tento software zpřístupněn pro zařízení** vyberte možnost **Software Installer**.

3.  V části **Typ souboru Software Installer** vyberte **Balíček aplikací pro systém iOS (soubor &#42;.ipa)**.

Po dokončení nahrávání se zobrazí **Ano** u **Zásad správy aplikace** na stránce **Vlastnosti softwaru** nahrané aplikace.

Po ověření úspěšného nahrání aplikace pokračujte krokem 3.

## <a name="bkmk_step3"></a>**Krok 3:** Vytvoření zásady správy mobilní aplikace

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com) klikněte na **Zásady** &gt; **Přehled** &gt; **Přidat zásadu**.

2.  Nakonfigurujte a nasaďte jednu z následujících zásad **Softwaru** v závislosti na typu zařízení, pro které chcete nakonfigurovat aplikace:

    -   **Zásady správy mobilních aplikací (Android 4 a novější)**

    -   **Zásady správy mobilních aplikací (iOS 7 a novější)**

    Můžete použít doporučená nastavení nebo nastavení upravit. Podrobnosti najdete v tématu [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

3.  Podle potřeby nakonfigurujte následující hodnoty. Možnosti se můžou lišit v závislosti na typu zařízení, pro které konfigurujete zásady.

    |Hodnota|Další informace|
    |-----------|-------------------|
    |**Název**|Zadejte název těchto zásad.|
    |**Popis**|V případě potřeby zadejte popis pro tuto zásadu.|
    |**Omezit zobrazování obsahu webu jenom na podnikový spravovaný prohlížeč**|Když je toto nastavení povolené, otevřou se ve spravované prohlížeči jakékoli odkazy v aplikaci. Aby tato možnost fungovala, musíte mít tuto aplikaci nasazenou na zařízeních.|
    |**Zabránit zálohám Androidu** nebo **Zabránit zálohám iTunes a iCloudu**|Zakáže zálohování jakýchkoliv informací z aplikace.|
    |**Povolit aplikaci přenos dat do ostatních aplikací**|Určuje aplikace, do kterých může tato aplikace může odesílat data. Můžete si vybrat, že nepovolíte přenos dat do žádné aplikace, povolíte přenos jenom do dalších spravovaných aplikací, nebo povolíte přenos do všech aplikací.<br /><br />Například když nepovolíte přenos dat, omezíte přenos dat na služby, jako je zasílání zpráv SMS, přiřazování obrázků kontaktům a publikování na Facebooku nebo Twitteru. **Important:** Toto nastavení neřídí použití funkce **Otevřít v** na mobilních zařízeních.<br />Pro zařízení iOS platí, že aby se zabránilo přenosu dokumentu mezi spravovanými a nespravovanými aplikacemi, je nutné nakonfigurovat a nasadit taky zásady zabezpečení mobilního zařízení, které zakazují nastavení **Povolit spravované dokumenty v dalších nespravovaných aplikacích**. **Note:** Pokud vyberete možnost povolit jenom přenos do ostatních spravovaných aplikací, použije se k otevření obsahu příslušného typu prohlížeč Intune PDF a prohlížeč obrázků (pokud je nasazený).|
    |**Povolit aplikaci, aby přijímala data z jiných aplikací**|Určuje aplikace, ze kterých může tato aplikace přijímat data. Můžete se rozhodnout pro následující:<br /><br />-   nepovolovat přenos dat z jakékoli aplikace<br />-   povolit jenom přenos z ostatních spravovaných aplikací<br />-   povolit přenos z jakékoli aplikace|
    |**Zabránit možnosti Uložit jako**|Zakáže použít možnost **Uložit jako** k uložení dat do osobního cloudového úložiště (třeba na osobní OneDrive nebo na Dropbox) v jakékoli aplikaci, která tuto zásadu používá.|
    |**Omezit vyjmutí, kopírování a vkládání v ostatních aplikacích**|Určuje, jak se v aplikaci dají používat operace vyjmutí, kopírování a vložení. Vybírejte z těchto možností:<br /><br />-   **Blokované** – Nepovolujte operace vyjmutí, kopírování a vložení mezi touto a jinými aplikacemi.<br />-   **Aplikace spravované zásadami** – Povolí jenom operace vyjmutí, kopírování a vložení mezi touto a jinými spravovanými aplikacemi.<br />-   **Aplikace spravované zásadami s možností vložení** – Povolí vložení dat vyjmutých nebo zkopírovaných z této aplikace jenom do ostatních spravovaných aplikací. Povolí vložení dat vyjmutých nebo zkopírovaných z jakékoliv aplikace do této aplikace.<br />-   **Libovolná aplikace** – Žádná omezení operací vyjímání, kopírování a vkládání v této aplikaci. **Note:** Aby bylo možné kopírovat a vkládat data mezi spravovanými aplikacemi, musí mít obě aplikace nakonfigurované buď nastavení **Aplikace spravované zásadami**, nebo nastavení **Aplikace spravované zásadami s možností vložení**.|
    |**Požadovat jednoduchý kód PIN pro přístup**|Vyžaduje, aby uživatel zadal číslo kódu PIN, které určí pro použití této aplikace. Uživatel bude požádán o toto nastavení při prvním spuštění aplikace.|
    |**Počet pokusů o zadání před obnovení kódu PIN**|Zadejte počet pokusů o zadání kódu PIN, které může uživatel udělat před resetováním kódu PIN.|
    |**Vyžadovat podnikové přihlašovací údaje pro přístup**|Vyžaduje, aby uživatel zadal své podnikové přihlašovací informace před tím, než může aplikaci používat.|
    |**Vyžadovat kompatibilitu zařízení dodržováním podnikových zásad pro přístup**|Umožňuje použití jenom aplikace, která se má použít, když se na zařízení nepoužil jailbreak nebo root.|
    |**Znovu zkontrolovat požadavky na přístup po (minuty)**|V poli **Časový limit** určete časové období před dalším zkontrolováním požadavků na přístup po spuštění aplikace.|
    |**Offline období odkladu**|Pokud je zařízení offline, určete časové období před opakovaným zkontrolováním požadavků na přístup k aplikaci.|
    |**Zašifrovat data aplikací**|Určuje, že všechna data přidružená k této aplikaci budou zašifrovaná, včetně data uložených externě, například na SD kartách. **Note:** **Šifrování pro iOS**Pro aplikace, které jsou přidružené k zásadám správy mobilní aplikace [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], jsou data zašifrovaná přinejmenším pomocí šifrování na úrovni zařízení poskytované operačním systémem. To zajišťuje zásada kódu PIN, kterou musí nastavit správce IT. Když se vyžaduje kód PIN, budou data zašifrovaná podle nastavení v zásadách správy mobilní aplikace. Jak uvádí dokumentace Apple, [moduly používané v iOS 7 mají certifikaci FIPS 140-2](http://support.apple.com/en-us/HT202739).**Šifrování pro Android**Pro aplikace, které jsou přidružené k zásadám správy mobilní aplikace [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] zajišťuje šifrování Microsoft. Data jsou zašifrovaná synchronně během souborových vstupně-výstupních operací podle nastavení v zásadách správy mobilní aplikace. Spravované aplikace v systému Android používají v režimu CBC šifrování AES-128 využívající kryptografické knihovny platformy. Metoda šifrování nemá certifikaci FIPS 140-2. Obsah v úložišti zařízení bude zašifrovaný vždycky.|
    |**Blokovat snímek obrazovky** (jenom zařízení s Androidem)|Určuje, že jsou při použití této aplikace zablokované možnosti snímku obrazovky zařízení.|

4.  Po dokončení klikněte na **Uložit zásadu**.

Nová zásada se zobrazí v uzlu **Zásady konfigurace** pracovního prostoru **Zásady**.

## **Krok 4:** Přidružení aplikace k zásadě správy mobilní aplikace a nasazení aplikace
Nasaďte aplikaci a na stránce **Správa mobilních aplikací** vyberte zásadu správy mobilní aplikace, kterou chcete k aplikaci přidružit.

Podrobnosti najdete v tématu [Nasazení aplikací do mobilních zařízení v Microsoft Intune](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune_-_deleted.md).

> [!IMPORTANT]
> Pro zařízení, která používají operační systémy starší než iOS 7.1, nebudou při odinstalaci aplikace přidružené zásady odebrané.
> 
> Pokud zrušíte registraci zařízení v [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], z aplikací se neodeberou zásady. Všechny aplikace s použitými zásadami si zachovají nastavení zásady i po odinstalaci a opakované instalaci aplikace.

### Postup v případě, že je aplikace už v zařízeních nasazená
Můžou nastat situace, kdy nasazujete aplikaci a jeden z cílových uživatelů nebo zařízení už má nainstalovanou nespravovanou verzi aplikace, například si uživatel nainstaloval Microsoft Word z obchodu s aplikacemi.

V takovém případě musíte požádat uživatele o ruční odinstalaci nespravované verze, aby se mohla nainstalovat spravovaná verze, kterou konfigurujete.

Pro zařízení se systémem iOS 9 a novějším ale [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] automaticky požádá uživatele o souhlas s převzetím správy stávající aplikace. Pokud souhlasí, stane se aplikace spravovanou aplikací služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] a použijí se taky všechny zásady správy mobilních aplikací přidružené aplikaci.

> [!TIP]
> Když je zařízení v dohledovém režimu, [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] převezme správu stávající aplikace bez předchozího souhlasu uživatele.

## **Krok 5:** Monitorujte nasazení aplikace.
Po vytvoření a nasazení aplikace přidružené k zásadě správy mobilní aplikace použijte následující postupy ke sledování aplikace a vyřešení konfliktů zásad.

#### Zobrazení stavu nasazení

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com) klikněte na **Skupiny** &gt; **Přehled**.

2.  Proveďte jeden z následujících kroků:

    -   Klikněte na **Všichni uživatelé** a potom poklikejte na uživatele, jejichž zařízení chcete prověřit. Na stránce **Vlastnosti uživatele** klikněte na **Zařízení** a poklikejte na zařízení, které chcete prověřit.

    -   Klikněte na **Všechna zařízení** &gt; **Všechna mobilní zařízení**. Na stránce **Vlastnosti skupiny zařízení** klikněte na **Zařízení** a poklikejte na zařízení, které chcete prověřit.

3.  Na stránce **Vlastnosti mobilního zařízení** klikněte na **Zásada** pro zobrazení seznamu zásad správy mobilní aplikace, které jsou na zařízení nasazené.

4.  Vyberte zásady správy mobilní aplikace, jejichž stav chcete zobrazit. Na podrobnosti o zásadě se můžete podívat v dolním podokně a rozbalit její uzel k zobrazení jejího nastavení.

5.  Ve sloupci **Stav** každé ze zásad správy mobilní aplikace se bude zobrazovat hodnota **Vyhovuje**, **Vyhovuje (čekání na schválení)** nebo **Chyba**. Pokud má vybraná zásada jedno nebo víc konfliktních nastavení, zobrazí se v tomto poli hodnota **Chyba**.

6.  Po zjištění konfliktu můžete nastavení konfliktní zásady zkontrolovat, jestli používá stejné nastavení, nebo můžete nasadit jednu zásadu pro aplikaci a uživatele.

### <a name="BKMK_Conf"></a>Způsob řešení konfliktů zásad
Pokud nastal konflikt zásad správy mobilní aplikace při prvním nasazení u uživatele nebo zařízení, konkrétní konfliktní hodnota nastavení se odebere ze zásady nasazené v aplikaci a aplikace bude používat integrovanou konfliktní hodnotu.

Pokud nastal konflikt zásady správy mobilní aplikace při pozdějších nasazeních aplikace nebo uživatele, konkrétní hodnota konfliktního nastavení se nebude aktualizovat na zásady správy mobilní aplikace nasazené do aplikace a aplikace bude používat stávající hodnotu tohoto nastavení.

V případech, kdy zařízení nebo uživatel obdrží dvě konfliktní zásady, platí následující chování:

-   Pokud už byla zásada nasazená na zařízení, stávající nastavení zásad se nepřepíšou.

-   Pokud ještě na zařízení nebyla nasazená žádná zásada a nasadí se dvě konfliktní nastavení, použije se výchozí nastavení zařízení.

## Viz také
[Ochrana dat a zařízení v Microsoft Intune](../Topic/Protect_data_and_devices_with_Microsoft_Intune.md)
[Nasazení a konfigurace aplikací v Microsoft Intune](../Topic/Deploy_and_configure_apps_with_Microsoft_Intune.md)

