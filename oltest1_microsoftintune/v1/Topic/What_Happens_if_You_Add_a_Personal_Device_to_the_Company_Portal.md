---
description: na
keywords: na
title: What Happens if You Add a Personal Device to the Company Portal
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 5703d18a-8b5b-4f47-a393-c2cc6cf7a614
---
# Co se stane, když přid&#225;te osobn&#237; zař&#237;zen&#237; na port&#225;l společnosti
Přidáte-li zařízení na portál společnosti, budete moci snadno najít aplikace společnosti určené k instalaci, zobrazit další zařízení, která jste přidali, a najít kontaktní informace na správce IT. Udělujete tím také správci IT oprávnění ke správě vašich zařízení, aby bylo možné lépe chránit informace společnosti na daném zařízení. Způsob přidávání jednotlivých zařízení se může lišit. Některá lze přidat z nastavení na zařízení, jiná stažením aplikace z obchodu s aplikacemi pro konkrétní zařízení.

## <a name="BKMK_IT_can_see"></a>Co IT oddělení uvidí a neuvidí po registraci zařízení v Intune
Postup pro registraci zařízení v rámci Intune najdete v článku [Registrace zařízení v Microsoft Intune](../Topic/Enroll_your_device_in_Microsoft_Intune.md).

|IT neuvidí|IT uvidí|
|--------------|------------|
|-   Historie volání<br />-   Textové zprávy<br />-   Osobní e-maily, kontakty a kalendář<br />-   Webová historie<br />-   Umístění<br />-   Z fotoaparátu<br />-   Osobní data|-   Vlastník<br />-   Název zařízení<br />-   Sériové číslo<br />-   Výrobce<br />-   Model<br />-   Operační systém<br />-   Firemní aplikace<br />-   Osobní aplikace|
Další podrobnosti získáte výběrem odkazu, který odpovídá typu vašeho zařízení:

-   [Windows Vista, Windows 7, Windows 8 a Windows 8.1 Enterprise a Professional a Windows 10](#BKMK_what_happens_vista)

-   [Windows RT](#BKMK_what_happens_rt)

-   [Windows Phone 8 nebo Windows Phone 8.1](#BKMK_what_happens_phone8)

-   [Zařízení se systémem iOS (iPhone a iPad)](#BKMK_what_happens_ios)

-   [Zařízení se systémem Android](#BKMK_what_happens_android)

-   [Zařízení nakonfigurovaná pouze pro e-mail](#BKMK_what_happens_email)

## <a name="BKMK_what_happens_vista"></a>Windows Vista, Windows 7, Windows 8 a Windows 8.1 Enterprise a Professional a Windows 10
Když přidáte počítač:

-   Budete mít v počítači nainstalován speciální software, prostřednictvím kterého bude moci správce IT počítač spravovat a díky kterému budete mít přístup k prostředkům společnosti, jako jsou aplikace a informace o podpoře. Tento software může být automaticky aktualizován správcem IT.

-   [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] V počítači může být nainstalovaná taky služba Endpoint Protection. Tento software v počítači zjišťuje přítomnost virů a malwaru. Další informace naleznete v tématu [Endpoint Protection Privacy Statement (Prohlášení o zásadách ochrany osobních údajů ve službě Endpoint Protection)](http://go.microsoft.com/fwlink/?LinkID=247324).

-   Správce IT může inventarizovat veškerý software nainstalovaný v počítači, včetně softwaru, který jste doinstalovali vy.

-   Vyžadovat, abyste přijali smluvní podmínky.

-   Správce IT může shromažďovat nebo odstraňovat data z pevného disku vašeho počítače. Může dokonce odstranit celý obsah vašeho pevného disku.

-   Může do vašeho počítače instalovat aplikace a aktualizace.

-   Může ve vašem počítači vynutit dodržování určitých zásad. Například může vyžadovat, abyste si v počítači nastavili heslo nebo PIN kód, přičemž v případě příliš velkého počtu chybných pokusů o zadání hesla může dojít k zablokování počítače nebo odstranění všech dat z pevného disku počítače.

## <a name="BKMK_what_happens_rt"></a>Windows RT
Když přidáte zařízení se systémem Windows RT, udělujete správci IT oprávnění k přístupu k zařízení. Může provádět například následující akce:

-   Obnovit v zařízení výchozí tovární nastavení. To je užitečné v případě ztráty nebo odcizení zařízení.

-   Odebrat veškerá firemní data a všechny nainstalované firemní aplikace. Vaše osobní údaje a nastavení se při tom neodeberou.

-   Vyžadovat, abyste přijali smluvní podmínky.

-   Požadovat, abyste si v zařízení nastavili heslo nebo PIN kód, přičemž v případě příliš velkého počtu chybných pokusů o zadání hesla může dojít k zablokování zařízení nebo obnovení zařízení do výchozího továrního nastavení.

-   Povolit nebo zakázat používání obrázkových hesel v zařízení.

-   Instalovat do zařízení aktualizace aplikací.

    > [!NOTE]
    > Platí pouze pro aktualizace. Správce IT nemůže vynutit instalace nových aplikací do vašeho zařízení, můžete si však podle vlastního výběru nainstalovat aplikace, které vidíte na portálu společnosti.

## <a name="BKMK_what_happens_phone8"></a>Windows Phone 8 nebo Windows Phone 8.1
Když přidáte zařízení Windows Phone, udělujete správci IT oprávnění k přístupu k zařízení. Může provádět například následující akce:

-   Obnovit v zařízení výchozí tovární nastavení. To je užitečné v případě ztráty nebo odcizení zařízení.

-   Odebrat veškerá firemní data a všechny nainstalované firemní aplikace. Vaše osobní údaje a nastavení se při tom neodeberou.

-   Požadovat, abyste si v zařízení nastavili heslo nebo PIN kód, přičemž v případě příliš velkého počtu chybných pokusů o zadání hesla může dojít k zablokování zařízení nebo obnovení zařízení do výchozího továrního nastavení.

-   Vynutit šifrování všech dat v zařízení. Tím jsou data chráněna v případě ztráty nebo odcizení zařízení.

-   Vyžadovat, abyste přijali smluvní podmínky.

-   Zakázat používání SD karet.

-   Instalovat do zařízení aktualizace aplikací. Platí pouze pro aktualizace. Správce IT nemůže vynutit instalace nových aplikací do vašeho zařízení, můžete si však podle vlastního výběru nainstalovat aplikace, které vidíte na portálu společnosti.

-   Jakmile je zařízení přidáno na portál společnosti, pak přibližně každých 8 hodin proběhne následující:

    -   Stažení všech zásad nebo aktualizací aplikací, které vám správce IT zpřístupnil.

    -   Odeslání všech aktualizací inventáře hardwaru.

    -   Odeslání všech aktualizací inventáře aplikací společnosti.

## <a name="BKMK_what_happens_ios"></a>Zařízení se systémem iOS (iPhone a iPad)
Když přidáte zařízení iPhone nebo iPad, udělujete správci IT oprávnění k přístupu k zařízení. Může provádět například následující akce:

-   Obnovit v zařízení výchozí tovární nastavení. To je užitečné v případě ztráty nebo odcizení zařízení.

-   Odebrat veškerá firemní data a všechny nainstalované firemní aplikace. Vaše osobní údaje a nastavení se při tom neodeberou.

-   Vynutit používání hesla nebo PIN kódu v zařízení.

-   Vyžadovat, abyste přijali smluvní podmínky.

-   Povolit nebo zakázat používání fotoaparátu/kamery v zařízení.

-   Povolit nebo zakázat procházení webu v zařízení.

-   Povolit nebo zakázat zálohování na serveru služby iCloud.

-   Povolit nebo zakázat synchronizaci dokumentů na serveru služby iCloud.

-   Povolit nebo zakázat datový proud fotografií na serveru služby iCloud.

-   Povolit nebo zakázat datový roaming v zařízení. Pokud je povolen datový roaming, mohou vám za něj být účtovány poplatky.

-   Povolit nebo zakázat hlasový roaming v zařízení. Pokud je povolen hlasový roaming, mohou vám za něj být účtovány poplatky.

-   Povolit nebo zakázat automatickou synchronizaci souborů v režimu roamingu v zařízení. Pokud je povolena automatická synchronizace souborů, mohou vám být účtovány poplatky za roaming.

## <a name="BKMK_what_happens_android"></a>Zařízení se systémem Android
> [!IMPORTANT]
> Pokud na svém zařízení zapnete podrobné protokolování a budete zasílat protokoly správci, budou odesílané protokoly obsahovat vaši e-mailovou adresu.

Když přidáte zařízení se systémem Android, udělujete správci IT oprávnění k přístupu k zařízení. Může provádět například následující akce:

-   Obnovit v zařízení výchozí tovární nastavení. To je užitečné v případě ztráty nebo odcizení zařízení.

-   Odebrat veškerá firemní data. Vaše osobní údaje a nastavení se při tom neodeberou.

-   Požadovat, abyste si v zařízení nastavili heslo nebo PIN kód, přičemž v případě příliš velkého počtu chybných pokusů o zadání hesla může dojít k zablokování zařízení nebo obnovení zařízení do výchozího továrního nastavení.

-   Vyžadovat, abyste přijali smluvní podmínky.

-   Povolit nebo zakázat používání fotoaparátu/kamery v zařízení.

-   Vynutit šifrování všech dat v zařízení, včetně firemních a osobních údajů. Tím jsou data chráněna v případě ztráty nebo odcizení zařízení.

-   Jakmile je zařízení přidáno na portál společnosti, pak přibližně každých 8 hodin proběhne následující:

    -   Stažení všech zásad nebo aktualizací aplikací, které vám správce IT zpřístupnil.

    -   Odeslání všech aktualizací inventáře hardwaru (tyto aktualizace neobsahují osobní informace).

    -   Odeslání všech aktualizací inventáře aplikací společnosti (tyto aktualizace neobsahují osobní informace).

## <a name="BKMK_what_happens_email"></a>Zařízení nakonfigurovaná pouze pro e-mail
Pokud nastavíte zařízení tak, abyste mohli používat firemní e-mail, udělujete správci IT oprávnění k přístupu k zařízení. Příklad akcí, které může správce IT provádět:

-   Ruční obnovení zařízení do výchozího továrního nastavení nebo konfigurace zařízení, které chcete obnovit, pokud dojde k příliš mnoha neúspěšným pokusům o zadání hesla. To je užitečné v případě ztráty nebo odcizení zařízení.

    > [!IMPORTANT]
    > Obnovením zařízení do výchozího továrního nastavení dojde k odebrání všech podnikových a osobní dat a aplikací, které jste nainstalovali.

-   Vyžadovat šifrování zařízení a jakýchkoli vyměnitelných paměťových karet.

-   Povolit nebo zakázat stahování příloh e-mailů v zařízení.

-   Určit, jak často bude zařízení kontrolovat firemní e-maily.

-   Povolit nebo zakázat procházení webu v zařízení.

-   Požadovat používání hesla a PIN kódu v zařízení. Může například provádět tyto akce:

    -   Požadovat, abyste používali heslo určité délky – od 4 do 18 písmen nebo číslic.

    -   Vyžadovat, že heslo musí obsahovat konkrétní kombinaci velkých a malých písmen.

    -   Požadovat, abyste kromě číslic použili i písmena a symboly.

    -   Určit, jak dlouho může být zařízení neaktivní, než bude uzamčeno, přičemž pro jeho odemčení bude nutné zadat heslo.

    -   Zabránit vám v použití již dříve použitého hesla.

    -   Vynutit obnovení zařízení do výchozího továrního nastavení, pokud bude zaznamenán příliš velký počet chybných pokusů o zadání hesla. Tím je zařízení chráněno v případě jeho ztráty nebo odcizení.

