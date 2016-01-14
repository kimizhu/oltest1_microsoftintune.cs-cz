---
description: na
keywords: na
title: Get started with a 30-day trial of Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: get-started-article
ms.assetid: 619a1d11-3d22-4635-8f70-770eba3e1712
---
# Zač&#237;n&#225;me s bezplatnou 30denn&#237; zkušebn&#237; verz&#237; Microsoft Intune
Nastavení bezplatné 30denní zkušební verze Microsoft Intune pro správu mobilních zařízení a počítačů je rychlé a snadné. Pomocí několika jednoduchých kroků můžete ve zkušební verzi přidat až 100 uživatelů a zařízení, nastavit skupiny, nakonfigurovat zásady dodržování předpisů a registrovat a spravovat mobilní zařízení a počítače. V tomto tématu se dozvíte základní informace o zprovoznění zkušební verze Intune a získáte o službě Intune přehled, abyste mohli vyhodnotit její funkce a možnosti.

Podívejte se na tuto pětiminutovou ukázku, ve které se dozvíte, jak je snadné začít s bezplatnou zkušební verzi Microsoft Intune a využít ji ke správě zařízení:

![](../Image/EM_Intune_30_Day_Trial.PNG)

## Před zahájením
Před zahájením práce s Intune budete potřebovat:

-   Zařízení s webovým prohlížečem, který podporuje technologii Silverlight a který můžete použít pro přístup k webům, kde vytvoříte uživatelské účty Intune (**portál účtů Intune**) a kde budete spravovat zařízení, skupiny a zásady (**konzola pro správu Intune**)

-   Druhé zařízení s webovým prohlížečem, které použijete k testování toho, jak budou uživatelé [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] zapisovat a spravovat svá zařízení pomocí portálu společnosti. Budete taky testovat, jak budou uživatelé moct hledat a instalovat aplikace a požádat správce o pomoc. Místo použití druhého zařízení s webovým prohlížečem můžete použít „režim ochrany osobních údajů“ ve stejném prohlížeči, který používáte pro správu [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] (třeba v Internet Exploreru můžete kliknout na **Nástroje** &gt; **Procházení InPrivate**).

-   Pokud máte stávající účet služeb Microsoft Online Services, budete pro něj potřebovat přihlašovací údaje správce. Pokud uvedený účet nemáte nebo chcete tohoto klienta Intune použít jenom pro účely hodnocení, pak tyto přihlašovací údaje správce potřebovat nebudete.

-   Pokud budete spravovat zařízení s iOS nebo Windows Phone pomocí zkušební verze Intune, budete potřebovat certifikáty (nebo klíče) a účty k načtení těchto certifikátů (viz následující tabulka). Zařízení s Androidem žádné další certifikáty nepotřebují.

    |Platforma|Požadavky na certifikát|Další informace|
    |-------------|---------------------------|-------------------|
    |Windows Phone 8.1 a [!INCLUDE[winphone8_client_1](../Token/winphone8_client_1_md.md)]|Pro uživatele Windows Phone 8.1, kteří si aplikaci portálu společnosti nainstalují ze Storu, žádný certifikát potřeba není. Pro Windows Phone 8.0 nebo v případě použití Intune k nasazení aplikace portálu společnosti na zařízení s Windows Phone 8.1 se vyžaduje certifikát Symantec.|Tyto pokyny předpokládají, že uživatelé aplikaci portálu společnosti získají ze Storu na zařízení s Windows Phone 8.1 nebo novějším. Informace o podpoře Windows Phone 8.0 najdete v tématu [Nastavení správy pro zařízení Windows Phone v Microsoft Intune](../Topic/Set_up_Windows_Phone_management_with_Microsoft_Intune.md).|
    |Zařízení se systémy Windows 10, [!INCLUDE[winblue_winrt_2](../Token/winblue_winrt_2_md.md)], [!INCLUDE[win8RT_client_1](../Token/win8RT_client_1_md.md)] nebo [!INCLUDE[winblue_client_2](../Token/winblue_client_2_md.md)]|Na registraci zařízení s Windows RT a Windows nejsou žádné požadavky.|[Instalace klienta na počítači s Windows pomocí Microsoft Intune](../Topic/Install_the_Windows_PC_client_with_Microsoft_Intune.md).|
    |iOS 7.1 nebo novější|Získání certifikátu služby Apple Push Notification:|Požádejte o certifikát služby Apple Push Notification od Applu podle postupu popsaného tady: [Nastavení správy iOS pomocí Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md)|

## <a name="Step1"></a>Krok 1: Registrace nebo přihlášení k Intune
Ještě než se zaregistrujete nebo přihlásíte k Intune, měli byste si odpovědět na následující otázky:

-   Má už vaše organizace pracovní nebo školní účet služeb Microsoft Online Services?

-   Máte s Microsoftem smlouvu Enterprise nebo ekvivalentní multilicenční smlouvu?

-   Plánujete používat klienta služby Intune po vypršení platnosti 30denní zkušební verze?

|Pokud platí některá z následujících věcí, zaregistrujte si NOVÝ účet:|Přihlaste se pomocí svého PRACOVNÍHO nebo ŠKOLNÍHO účtu, pokud:|
|-------------------------------------------------------------------------|-------------------------------------------------------------------|
|-   **Nemáte pracovní nebo školní účet.** Pracovní nebo školní účet získáte při podpisu multilicenční smlouvy s Microsoftem nebo přihlášení k odběru Office 365. Pokud vaše organizace neuzavřela s Microsoftem smlouvu Enterprise nebo podobnou multilicenční smlouvu (nebo má účet Office 365), nemáte účet služeb Microsoft Online Services, který můžete použít pro přihlášení ke službám Microsoft Online Services.<br />-   **Po skončení platnosti 30denní zkušební verze se váš klient Intune zruší.** Pokud používáte bezplatné předplatné zkušební verze [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] jenom pro účely hodnocení a chcete se po skončení zkušební verze vrátit ke svému nastavení služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] a zřizování zařízení, musíte si zaregistrovat nový účet. Tato možnost se doporučuje, když chcete používat [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] s nástrojem System Center Configuration Manager 2012. **Important:** Pokud registrujete nový účet, nebudete moct později použít stávající pracovní nebo školní účet ke správě tohoto účtu, nebo ho spojovat se stávajícími multilicenčními smlouvami.|**Máte pracovní nebo školní účet s multilicenční smlouvou nebo předplatné Office 365 a používáte tuto zkušební verzi k hodnocení [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].** **Important:** Pokud nastavujete [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] ve stávajícím účtu, doporučujeme vám přečíst si téma [Úvod do Microsoft Intune](../Topic/Introduction_to_Microsoft_Intune.md), než budete pokračovat v těchto krocích.|

### <a name="BKMK_ToSignUpforSubscription"></a>Registrace nebo přihlášení k Intune

1.  Nejdřív [kliknutím sem přejděte na stránku registrace Intune](https://portal.office.com/Signup/Signup.aspx?OfferId=40BE278A-DFD1-470a-9EF7-9F2596EA7FF9&dl=INTUNE_A&ali=1#0%20).

2.  Na stránce **Registrovat** máte dvě možnosti:

    -   **Přihlášení k odběru z pracovního nebo školního účtu služeb Microsoft Online Services**: Pokud už máte svůj pracovní nebo školní účet a pro přihlášení k odběru obou služeb chcete použít stejný účet, klikněte na **Přihlásit**. Pokud používáte stejný účet pro víc služeb, používají tyto služby stejnou infrastrukturu Azure AD a jsou klienty Azure AD. Azure AD poskytuje základní adresářové funkce a funkce správy identit pro cloudové služby Microsoftu.

    -   **Přihlášení jenom k odběru Intune**: Pokud ještě nemáte přihlášený odběr cloudové služby, přihlaste se k odběru [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] vyplněním formuláře na stránce registrace.

        > [!NOTE]
        > Ve výchozím nastavení je název domény přidružený k vašemu předplatnému a k uživatelským účtům, které přidáte do služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Po přihlášení k odběru můžete přidat a používat název domény, který už vlastníte, nebo můžete dál používat bezplatnou doménu **onmicrosoft.com**.

Po vyplnění registračního formuláře a přijetí smlouvy Microsoft Online Subscription Agreement budete automaticky přihlášení k [!INCLUDE[wit_icp_1](../Token/wit_icp_1_md.md)] pomocí účtu správce klienta. Na e-mailovou adresu, kterou jste zadali během registrace, vám přijde e-mailová zpráva s informacemi o účtu. Ta potvrzuje, že je vaše předplatné aktivní.

## <a name="Step2"></a>Krok 2: Přidání uživatelů do Intune
Teď, když jste nastavili svůj účet, použijte buď **Průvodce pro nové uživatele** pro přidání jednotlivých uživatelských účtů do [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], nebo **Průvodce hromadným přidáním uživatelů** pro přidání uživatelů hromadně (viz pokyny v této části).  Než s tím začnete, je důležité, abyste rozuměli tomu, jak Intune zachází s účty správců.

Správce klienta používá k přidání uživatele do **Skupiny uživatelů** Microsoft Intune portál účtů. Přidání uživatelů do **Skupiny uživatelů** přiřadí uživatelům licence předplatného Intune a zároveň se tak tito uživatelé objeví v konzole pro správu Microsoft Intune.

Účty správce služby Intune se na rozdíl od běžných uživatelských účtů nevytváří v portálu účtů. Místo toho můžete uživatelům pomocí konzoly pro správu v pracovním prostoru **Správa** v rámci **Řízení správy** přiřadit oprávnění správce s přístupem jen pro čtení nebo s plným přístupem. Správci služeb, kteří mají přiřazená oprávnění jen pro čtení, nemůžou měnit nastavení Intune, ale můžou zobrazovat data a spouštět sestavy. Správci služeb s úplným přístupem mají k dispozici všechna práva správce.

Pomocí konzoly pro správu služby Intune je možné zobrazit informace správce klienta, ale není tady možné správce klientů vytvořit. Ve výchozím nastavení se vlastník předplatného stává správcem klienta pro daný účet služby Microsoft Intune a má úplný přístup k portálu účtů služby Intune a konzole pro správu služby Intune. Doporučujeme, abyste prostřednictvím portálu účtů vytvořili nejmíň jeden další účet správce klienta, který vám pomůže delegovat úkoly a zároveň zaručí, že nezůstanete bez přístupu k účtu správce služby Intune, kdybyste zapomněli heslo.

### Přidání jednotlivých uživatelských účtů
Pomocí následujících kroků můžete ve zkušební verzi klienta vytvořit další uživatelské účty. Pamatujte si, že každý přidaný uživatelský účet se počítá jako jedna ze 100 licencí, které jste získali v rámci bezplatné zkušební verze [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

1.  Spusťte průvodce **Noví uživatelé** tak, že klikněte na [Portálu účtů Microsoft Intune](https://account.manage.microsoft.com) na **Přidat uživatele** &gt; **Nový** &gt;**Uživatel**.

2.  Na stránce **Podrobnosti** vyplňte požadovaná pole.

3.  Na stránce **Nastavení** nastavte **umístění** pro uživatele.

4.  Na stránce **Skupina** klikněte na **Další**. Tím přijmete výchozí hodnoty a přiřadíte k uživatelskému účtu licenci pro [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

5.  Na stránce **E-mail** můžete zadat až pět e-mailových adres, na které přijde upozornění na uživatelské jméno a dočasné heslo k účtu. Jednotlivé e-mailové adresy oddělte středníkem (;). Až to uděláte, přidejte uživatele k předplatnému tím, že kliknete na **Vytvořit**.

6.  Na stránce **Výsledky** se zobrazí název nového účtu a jeho dočasné heslo.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] automaticky vytvoří dočasné heslo.

7.  Až se nový uživatel zobrazí v uzlu **Uživatelé** portálu účtů, ověřte, že byl nový uživatel úspěšně vytvořený:

    1.  V [konzole pro správu Intune](https://manage.microsoft.com/) klikněte na **Správa** &gt; **Portál společnosti** a posuňte se k dolnímu okraji obrazovky. Zkopírujte adresu URL v části **Portál společnosti Intune**.

    2.  Otevřete nové okno prohlížeče v režimu ochrany osobních údajů (v Internet Exploreru klikněte na **Nástroje** &gt; **Procházení se službou InPrivate**) nebo otevřete nové okno prohlížeče na jiném zařízení a potom přejděte na adresu URL, kterou jste zkopírovali v předchozím kroku. Pokud se uživatel přihlašuje poprvé, musí zadat nové heslo účtu.

### Hromadné přidání uživatelů
Pro hromadné přidání uživatelů do Intune použijte **Průvodce hromadným přidáním uživatelů**, kde můžete nahrát textový soubor s oddělovači (.csv) obsahující uživatelská data. Odkazy v průvodci umožňují stáhnout prázdnou šablonu a ukázkový soubor CSV. První řádek souboru CSV musí ve správném pořadí obsahovat popisky jednotlivých sloupců dat uživatele. Pak musíte pro každého uživatele v souboru .csv uvést **uživatelské jméno** (třeba **bob@contoso.com**) a **zobrazované jméno** (třeba **Bob Kelly**).

1.  Na [portálu účtu Microsoft Intune](https://account.manage.microsoft.com) klikněte na **Uživatelé** &gt; **Nový**.

2.  Kliknutím na **Hromadné přidání** spustíte Průvodce hromadným přidáním uživatelů.

3.  Na stránce **Vybrat soubor** klikněte na **Procházet** a najděte a nahrajte existující soubor .csv z vašeho počítače. Můžete si taky stáhnout ukázkový soubor .csv nebo prázdný soubor šablony pomocí odkazů v průvodci .

4.  Na stránce **Ověření** si zkontrolujte výsledky a potom zobrazte další podrobnosti kliknutím na **Zobrazit**.

5.  Na stránce **Nastavení** zkontrolujte, že stav přihlášení je **Povoleno**, a nastavte **umístění**. Tato nastavení se vztahují na všechny uživatelské účty přidané prostřednictvím souboru .csv.

6.  Na stránce **Skupina** klikněte na **Další**. Tím přijmete výchozí hodnoty a všem uživatelským účtům, které jste přidali pomocí souboru .csv, přiřadíte licenci pro [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Ve výchozím nastavení je zaškrtnuté políčko, kterým se ke všem uživatelským účtům přiřadí licence pro [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

7.  Na stránce **E-mail** můžete zadat až pět e-mailových adres, na které přijde upozornění na uživatelská jména a dočasná hesla, která [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] pro jednotlivé účty vytvoří. Jednotlivé e-mailové adresy oddělte středníkem (;). Až to budete mít, klikněte na **Vytvořit** a uživatelské účty se přidají k předplatnému.

8.  Na stránce **Výsledky** se zobrazí názvy uživatelských účtů a jejich dočasná hesla.

Všechny uživatelské účty, které jste přidali metodou importování, se teď zobrazují v uzlu **Uživatelé** portálu účtu. Noví uživatelé musí při prvním přihlášení zadat nové heslo ke svému uživatelskému účtu.

## <a name="Step3"></a>Krok 3: Vytvoření skupiny pro uspořádání uživatelů a zařízení
Skupiny ve [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] poskytují flexibilitu pro správu zařízení a uživatelů. Můžete nastavit skupiny podle potřeb vaší organizace (třeba podle zeměpisné polohy, oddělení nebo vlastností hardwaru) a použít je k provádění řady úloh správy se škálováním od nastavení zásad pro sadu uživatelů po nasazení aplikací na sadu zařízení.

### Vytvoření skupiny zařízení
Použijte skupiny zařízení k nasazení softwaru a aktualizací a ke konfiguraci zásad nastavení agenta služby Microsoft Intune a brány Windows Firewall. Můžete třeba nastavit skupinu Moje zařízení zkušební verze podle těchto kroků:

1.  V [konzole pro správu Intune](https://manage.microsoft.com/) klikněte na **Skupiny** &gt; **Přehled** &gt; **Vytvořit skupinu**.

2.  Jako **název skupiny** zadejte Moje zařízení zkušební verze, ze seznamu nadřazených skupin vyberte **Všechna zařízení** a potom klikněte na **Další**.

3.  Na stránce **Definovat kritéria členství** vyberte **Všechna zařízení**, což znamená, že skupina zahrnuje mobilní zařízení i počítače.

4.  Na stránce **Definovat přímé členství** klikněte na **Další**. Pokud jste dřív vytvořili skupinu, která neobsahuje všechna zařízení, a chtěli byste do nové skupiny přidat určitá zařízení, můžete to udělat tady.

5.  Na stránce **Souhrn** si prohlédněte akce, které se provedou, a pak klikněte na **Dokončit**.

Nově vytvořenou skupinu najdete v seznamu **Skupiny** v pracovním prostoru **Skupiny** v části **Všechna zařízení**. Tady můžete skupinu i upravit nebo odstranit.

### Vytvoření skupiny uživatelů
Skupiny uživatelů můžete použít k nasazení softwaru a zásad zařízení. Můžete třeba nastavit skupinu Moji uživatelé zkušební verze podle těchto kroků:

1.  V [konzole pro správu Intune](https://manage.microsoft.com/) klikněte na **Skupiny** &gt; **Přehled** &gt; **Vytvořit skupinu**.

2.  Jako **název skupiny** zadejte Moji uživatelé zkušební verze, ze seznamu nadřazených skupin vyberte **Všichni uživatelé** a potom klikněte na **Další**.

3.  Na stránce **Definovat kritéria členství** nastavte možnost **Začít členství ve skupině s** na **Všichni uživatelé v nadřazené skupině**.

4.  Vedle **Vyloučit členy z těchto skupin zabezpečení** klikněte na **Procházet** a potom vyberte **Správce společnosti**. Toto vyloučení vám umožní spravovat skupinu Moji uživatelé zkušební verze bez vlivu na účet správce společnosti (taky označovaný jako správce klienta).

5.  Na stránce **Definovat přímé členství** klikněte na **Další**. Tady nemusíte nic dělat, protože chcete, aby skupina Moji uživatelé zkušební verze obsahovala všechny uživatele kromě správce společnosti.

6.  Na stránce **Souhrn** si prohlédněte akce, které se provedou, a pak klikněte na **Dokončit**.

Nově vytvořenou skupinu najdete v seznamu **Skupiny** v pracovním prostoru **Skupiny** v části **Všichni uživatelé**. Tady můžete skupinu i upravit nebo odstranit.

Další informace o použití skupin naleznete v tématu [Použití skupin pro správu uživatelů a zařízení s Microsoft Intune](../Topic/Use_groups_to_manage_users_and_devices_with_Microsoft_Intune.md).

## <a name="Step4"></a>Krok 4: Vytvoření zásad a publikování aplikace
Zásady [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] vám nabízejí nastavení, které pomáhá řídit nastavení zabezpečení na mobilních zařízeních, spravovat nastavení brány Windows Firewall a Endpoint Protection pro počítače a nasazovat aplikace. Pokud chcete Intune používat pro zařízení, která máte nakonfigurovaná tak, že se po uplynutí zkušební verze použijí v produkčním prostředí, je bezpodmínečně nutné postupovat podle pokynů v částech [Správa nastavení a funkcí v zařízeních pomocí zásad Microsoft Intune](../Topic/Manage_settings_and_features_on_your_devices_with_Microsoft_Intune_policies.md) a [Pomoc se zabezpečením počítačů s Windows pomocí služby Endpoint Protection pro Microsoft Intune](../Topic/Help_secure_Windows_PCs_with_Endpoint_Protection_for_Microsoft_Intune.md).

Pomocí Intune můžete provádět dva typy instalace aplikací. První je **požadovaná instalace**, která aplikaci automaticky nasadí do spravovaných počítačů. Druhá je **dostupná instalace**, která nasadí aplikaci nebo odkaz na aplikaci na portálu společnosti Intune, aby si mohli uživatelé vybrat, jestli ji chtějí mít nainstalovanou na počítači nebo na mobilním zařízení.

Než použijete Intune k nasazení aplikací, zkontrolujte, že máte příslušné licence k publikování, distribuci a použití aplikace. Pracovní prostor **Licence** umožňuje přidávat a spravovat informace o licenční smlouvě pro aplikace nebo software zakoupené prostřednictvím multilicenční smlouvy s Microsoftem a pro aplikace nebo software Microsoftu nebo jiného subjektu než Microsoftu zakoupené jiným způsobem. Potom můžete vytvořit sestavy licencí, které budou zobrazovat informace o využití spravovaných licencí ve vaší společnosti, abyste měli pořád přehled, nebo informace o aktivitě využití licencí.

V následujícím postupu nastavíte zásady konfigurace mobilního zařízení a zásady brány firewall počítače s Windows a nakonfigurujete Skype jako instalaci dostupnou pro mobilní zařízení po jejich registraci. Po přidání a nasazení nových zásad zdědí všichni uživatelé nebo zařízení ve skupině, do které jste zásadu nasadili, tato nastavení jako svoje základní zásady. Podrobnosti těchto zásad můžete později kdykoli zkontrolovat nebo upravit v pracovním prostoru **Zásady** v konzole pro správu.

#### Vytvoření a nasazení zásady konfigurace mobilních zařízení

1.  Otevřete [konzolu pro správu Intune](https://manage.microsoft.com/).

2.  V levém podokně klikněte na ikonu **Zásady**.

3.  V seznamu **Úlohy** na stránce **Přehled zásad** klikněte na **Přidat zásadu**.

4.  V seznamu zásad rozbalte platformu, pro kterou chcete vytvořit zásadu, vyberte **Všeobecná konfigurace**, zvolte **Vytvoření a nasazení zásad s doporučeným nastavením** a potom klikněte na **Vytvořit zásadu**.

5.  Po zobrazení výzvy **Vyberte skupiny, do kterých chcete nasadit tuto zásadu** vyberte ze seznamu skupinu **Moji uživatelé zkušební verze** a klikněte na **Přidat** &gt; **OK**.

Vaše zásada se zobrazí v seznamu zásad konfigurace a byla nasazena do skupiny **Moji uživatelé zkušební verze**. Nastavení zásady zobrazíte tak, že na zásadu dvakrát kliknete.

#### Publikování aplikace Skype pro mobilní zařízení

1.  V [konzole pro správu Intune](https://manage.microsoft.com/) klikněte na ikonu **Aplikace** a pak na **Aplikace** &gt; **Přidat aplikaci**. Po zobrazení výzvy zadejte své přihlašovací údaje do [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

    > [!NOTE]
    > Při prvním spuštění **Intune Software Publisheru** může instalace aplikace chvíli trvat.

2.  Přečtěte si upozornění zabezpečení a klikněte na **Spustit**.

3.  Na stránce **Než začnete** klikněte na **Další**.

4.  Na stránce **Instalace softwaru** v části **Vyberte, jakým způsobem má být tento software zpřístupněn pro zařízení** vyberte **Externí odkaz**.

5.  Zadejte externí odkaz pro software v části **Zadejte adresu URL** a klikněte na **Další**. Ujistěte se, že adresa URL začíná na **http://**. Pro aplikaci Skype použijte odkaz dole odpovídající platformě mobilního zařízení, kterou používáte:

    -   **iOS:**[https://itunes.apple.com/us/app/skype-for-iphone/id304878510?mt%3D8](https://itunes.apple.com/us/app/skype-for-iphone/id304878510?mt%3D8)

    -   **Android:** [https://play.google.com/store/apps/details?id=com.skype.raider](https://play.google.com/store/apps/details?id=com.skype.raider)

    -   **Windows Phone 8 nebo Windows Phone 8.1:** [http://www.windowsphone.com/cs-cz/store/app/skype/c3f8e570-68b3-4d6a-bdbb-c0a3f4360a51](http://www.windowsphone.com/en-us/store/app/skype/c3f8e570-68b3-4d6a-bdbb-c0a3f4360a51)

6.  Na stránce **Popis softwaru** zadejte informace k softwaru, které mají uživatelé vidět na firemním portálu, a klikněte na **Další**. Dostupná jsou tato nastavení (tento příklad se týká Skypu):

    -   **Vydavatel:** Zadejte název vydavatele (Microsoft).

    -   **Název:** Zadejte **Skype**.

    -   **Popis:** Zadejte popis softwaru, třeba **Komunikační aplikace Skype**.

    -   **Kategorie:** Vyberte kategorii, která nejlíp odpovídá tomuto softwaru, třeba **Spolupráce**.

    -   **Zobrazit tuto aplikaci jako doporučenou aplikaci a zvýraznit ji na portálu společnosti:** Po výběru této možnosti bude při prohlížení na mobilních zařízeních aplikace zřetelně zobrazená na firemním portálu.

    -   **Ikona:** (Volitelné) Určete, jestli chcete k softwaru přidružit ikonu. Maximální velikost ikony je 250 x 250 pixelů, ale doporučená velikost je 32 x 32 pixelů.

7.  Na stránce **Souhrn** zkontrolujte zadané informace o softwaru a klikněte na **Odeslat**. Průvodce ukončíte kliknutím na **Zavřít**.

8.  V [konzole pro správu Intune](https://manage.microsoft.com/) klikněte na **Aplikace** &gt; **Aplikace** &gt; **Skype** &gt; **Spravovat nasazení**.

9. Na stránce **Vybrat skupiny** vyberte **Moji uživatelé zkušební verze** pro nasazení softwaru do této skupiny uživatelů a potom klikněte na **Přidat** &gt; **Další**.

10. Na stránce **Akce nasazení** vyberte **Dostupná instalace** ze sloupce **Schválení** pro vaši skupinu.

11. Klikněte na tlačítko **Dokončit**.

Aplikace Skype je teď dostupná k instalaci na mobilních zařízeních z portálu společnosti, ale nejdřív je potřeba nainstalovat na počítačích a mobilních zařízeních software [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

## <a name="Step5"></a>Krok 5: Zápis počítačů do Intune
Klientský software [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] můžete na počítačích nainstalovat následujícím způsobem:

-   Uživatelé můžou použít instalační program poskytnutý správcem k ručnímu zápisu.

-   Software [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] se dá zahrnout do image operačního systému nebo nasadit pomocí zásad skupiny.

-   Koncoví uživatelé můžou svoje zařízení sami zaregistrovat prostřednictvím portálu společnosti [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)].

Každý zaregistrovaný počítač se propojí s uživatelským účtem použitým při instalaci klientského softwaru. Během instalace klienta Intune na počítačích se ve výchozím nastavení nainstaluje taky Microsoft Intune Endpoint Protection. Endpoint Protection pomáhá se zabezpečením počítačů ve vaší organizaci tím, že poskytuje ochranu před potenciálními hrozbami v reálném čase, udržuje definice škodlivého softwaru aktuální a automaticky spouští plánovanou kontrolu. Pro zvýšení zabezpečení můžete zásady Intune použít taky pro správu nastavení brány Windows Firewall na spravovaných počítačích.

Co potřebujete vědět, než začnete:

-   Aby mohl uživatel klientský software nainstalovat, musí být na počítači správcem.

-   Vlastní registrace uživatelem vyžaduje, aby byl na klientském počítači nainstalovaný Internet Explorer.

-   Pokaždé, když uživatel sám zaregistruje počítač, použije se licence [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)].

-   Abyste si mohli sami zaregistrovat počítač, musíte použít pracovní nebo školní účet služeb Microsoft Online Services. Je to účet, který jste použili k přihlášení, nebo účet správce vytvořený při registraci bezplatné zkušební verze.

Pro tuto zkušební verzi použijte následující postup, který využívá metodu vlastní registrace:

1.  V [konzole pro správu Intune](https://manage.microsoft.com/) klikněte na **Správa** &gt; **Portál společnosti** a posuňte se k dolnímu okraji obrazovky. Zkopírujte adresu URL v části **Firemní portál Intune**.

2.  V Internet Exploreru přejděte na adresu URL firemního portálu, kterou jste získali v předchozím kroku, a přihlaste se pomocí přihlašovacích údajů správce.

3.  Klikněte na **Přidat zařízení**.

4.  Klikněte na **Stáhnout software** a potom na **Spustit**.

5.  Kliknutím na **Další** spusťte průvodce instalací [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)].

6.  Po dokončení průvodce instalací klikněte na **Dokončit**.

Další informace o správě počítačů ve [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] najdete v části [Instalace klienta na počítači s Windows pomocí Microsoft Intune](../Topic/Install_the_Windows_PC_client_with_Microsoft_Intune.md).

Další informace o správě softwaru ve [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] najdete v části [Nasazení a konfigurace aplikací v Microsoft Intune](../Topic/Deploy_and_configure_apps_with_Microsoft_Intune.md).

## <a name="Step6"></a>Krok 6: Registrace mobilních zařízení a instalace aplikace
Abyste v Intune nastavili správu mobilních zařízení, musíte nejdřív nastavit autoritu pro správu mobilního zařízení, povolit správu pro platformu zařízení a zaregistrovat svoje zařízení v aplikaci portálu společnosti. Pak můžete nasadit aplikaci Microsoft Skype, kterou jste publikovali.

1.  **Nastavení Intune jako autority pro správu mobilního zařízení**
    V [konzole pro správu Intune](https://manage.microsoft.com/) klikněte na **Správa** &gt; **Správa mobilních zařízení** a pod **Úkoly** klikněte na **Nastavit autoritu MDM**.  V dialogu **Autorita MDM** klikněte na **Ano**.

2.  **Povolení MDM pro platformu zařízení**
    Povolte správu mobilních zařízení pro platformu zařízení, kterou chcete spravovat. V závislosti na platformě je potřeba splnit různé požadavky:

    -   **iOS**: informace najdete v článku [Nastavení správy iOS pomocí Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md).

    -   **Windows Phone**: informace najdete v článku [Nastavení správy pro zařízení Windows Phone v Microsoft Intune](../Topic/Set_up_Windows_Phone_management_with_Microsoft_Intune.md).

    -   **Android**: Mobilní zařízení s Androidem umožňují uživatelům registraci pomocí aplikace portálu společnosti dostupné na webu Google Play. Žádná další konfigurace v Intune se nevyžaduje.

3.  **Registrace zařízení:**

    -   **Android** – Nainstalujte si aplikaci **Portál společnosti Intune** od Microsoft Corporation dostupnou na [Google Play](http://go.microsoft.com/fwlink/p/?LinkId=386612) a přihlaste se pomocí uživatelských přihlašovacích údajů Intune přidaných nahoře.

    -   **iOS** – Nainstalujte si aplikaci **Portál společnosti služby Microsoft Intune** od Microsoft Corporation dostupnou na App Storu a přihlaste se pomocí uživatelských přihlašovacích údajů Intune přidaných nahoře. Abyste přidali svoje zařízení, zobrazte **Registrovaná zařízení**.

    -   **Windows Phone 8.1** – Uživatelé si instalují aplikaci **Portál společnosti** od Microsoft Corporation dostupnou na Windows Phone Storu a přihlašují se pomocí uživatelských přihlašovacích údajů Intune přidaných nahoře.  Abyste přidali svoje zařízení, zobrazte **Registrovaná zařízení**.

    -   **Windows Phone 8.0**  – Uživatelé kliknou na **Nastavení systému** &gt; **Firemní aplikace** a přihlásí se pomocí uživatelských přihlašovacích údajů Intune přidaných výše. Aplikace portálu společnosti se nasadí na váš telefon.

    Pokud se vám zobrazí výzva, abyste zadali **adresu serveru**, zadejte manage.microsoft.com.

4.  Na mobilním zařízení otevřete portál společnosti, zvolte **Aplikace** a pak nainstalujte **Microsoft Skype**.

Další informace o správě mobilních zařízení ve [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] najdete v části [Příprava registrace zařízení v Microsoft Intune](../Topic/Get_ready_to_enroll_devices_in_Microsoft_Intune.md).

## Další možnosti a funkce Intune

### Výstrahy, oznámení a sestavy
V konzole pro správu [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] se **výstrahy** používají k rychlému posouzení celkového stavu spravovaných zařízení ve vaší organizaci. Výstrahy můžete nakonfigurovat a přizpůsobit tak, aby oznamovaly a zobrazovaly jen informace, které potřebujete pro svoji organizaci. Můžete nastavit, jestli chcete výstrahu povolit nebo zakázat, nakonfigurovat závažnost, určit podle prahové hodnoty zobrazení, jak často se musí událost výstrahy aktivovat před zobrazením výstrahy, a taky nakonfigurovat nastavení, která jsou specifická pro určité typy výstrah.

**Oznámení** jsou e-maily sloužící k informování správců (a ostatních uživatelů) při aktivaci určitých typů výstrahy.

**Sestavy** slouží k zodpovězení celé řady dotazů, třeba v kolika počítačích je nainstalovaná určitá aplikace nebo aktualizace, jaký malware byl zablokovaný nebo kteří uživatelé potřebovali za poslední měsíc Vzdálenou pomoc.

Další informace o výstrahách, oznámeních a sestavách najdete v části [Monitorování a sestavy v Microsoft Intune](../Topic/Monitoring_and_reports_with_Microsoft_Intune.md).

### Možnosti Intune
Kromě možností uvedených v tomto krátkém průvodci nastavením má [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] ještě celou řadu různých funkcí. Mezi ně třeba patří:

-   **Řízení přístupu ke službě Exchange a Office 365.** Podrobnosti najdete v tématu [Správa přístupu k e-mail a SharePointu pomocí Microsoft Intune](../Topic/Manage_access_to_email_and_SharePoint_with_Microsoft_Intune.md).

-   **Správa zařízení iOS vlastněných společností.** Podrobnosti najdete v tématu [Registrace zařízení iOS vlastněných společností v Microsoft Intune](../Topic/Enroll_corporate-owned_iOS_devices_in_Microsoft_Intune.md).

-   **Správa mobilních aplikací.** Spravované mobilní aplikace pracují se zásadami správy mobilních aplikací a omezují určité operace aplikací, třeba kopírování a vkládání nebo funkci snímku obrazovky. Podrobnosti najdete v tématech [Ochrana dat pomocí zásad správy mobilních aplikací v Microsoft Intune](../Topic/Configure_and_deploy_mobile_application_management_policies_in_the_Microsoft_Intune_console.md) a [Správa přístupu k internetu pomocí zásad spravované prohlížeče v Microsoft Intune](../Topic/Manage_Internet_access_using_managed_browser_policies_with_Microsoft_Intune.md).

-   **Řízení přístupu k firemním prostředkům.** Do mobilních zařízení můžete nasadit certifikáty, e-mailové profily, profily VPN a profily Wi-Fi a usnadnit tak rychlé nastavení těchto zařízení. Podrobnosti najdete v tématu [Povolení přístupu k prostředkům společnosti se službou Microsoft Intune](../Topic/Enable_access_to_company_resources_with_Microsoft_Intune_-_deleted.md).

Další informace o všech možnostech [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] najdete v části [Možnosti správy mobilních zařízení v Microsoft Intune](../Topic/Mobile_device_management_capabilities_in_Microsoft_Intune.md), [Možnosti správy počítačů s Windows v Microsoft Intune](../Topic/Windows_PC_management_capabilities_in_Microsoft_Intune.md) a [Popis služby Microsoft Intune](../Topic/Microsoft_Intune_Service_Description.md).

Další informace o možnostech nedávno zavedených pro [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] najdete v tématu [Co je nového ve Microsoft Intune](../Topic/What_s_new_in_Microsoft_Intune.md).

Možnosti podpory jsou popsané v části [Jak získat podporu pro Microsoft Intune](../Topic/How_to_get_support_for_Microsoft_Intune.md) a kromě toho se můžete zapojit do diskusí o [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] na [fórech Microsoft Intune](https://social.technet.microsoft.com/Forums/en-US/home?forum=microsoftintuneprod).

## <a name="BKMK_BuyIntune"></a>Jste připravení přejít na placené předplatné Intune?
Pokud si koupíte nejmíň 150 licencí na Microsoft Intune v rámci opravňujícího plánu, můžete využít benefit Centra FastTrack. Jde o službu, kdy vám specialista Microsoftu pomůže připravit vaše prostředí na Intune. Přečtěte si [Popis výhod služby Microsoft Intune](https://technet.microsoft.com/library/mt228265.aspx).

Bezplatnou zkušební verzi Intune můžete převést na placené předplatné následujícími způsoby:

-   **Předplatné služby Intune:** Licence vázaná na jednotlivé uživatele. Další informace najdete v tématu [Jak koupit Microsoft Intune](http://www.microsoft.com/en-us/server-cloud/products/microsoft-intune/Purchasing.aspx). Po dokončení nákupu postupujte podle kroků v tématu [Začněte s placeným předplatným Microsoft Intune](../Topic/Get_started_with_a_paid_subscription_to_Microsoft_Intune.md) a projděte si další konfigurační kroky, až budete začínat s Intune.

-   **Sada Enterprise Mobility:** Nabízí služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], Azure Active Directory Premium a Azure RMS. Další informace vám poskytne váš account manažer Microsoftu nebo místní prodejce. Můžete si taky přečíst další [informace o sadě Enterprise Mobility](https://www.microsoft.com/en-us/server-cloud/enterprise-mobility/overview.aspx) a podívat se na [ceny sady Enterprise Mobility](http://www.microsoft.com/en-us/server-cloud/products/enterprise-mobility-suite/Purchasing.aspx).

-   **Smlouva Enterprise Agreement** (více než 250 uživatelů) – Ideální licenční program pro organizace s víc než 250 uživateli. Poskytuje vám flexibilitu zvolit si takový místní software a online služby, které nejvíc vyhovují potřebám vašich uživatelů a pomáhají vám optimalizovat náklady na technologie. Další informace vám poskytne váš account manažer Microsoftu nebo místní prodejce nebo navštivte [web multilicenčního programu Enterprise](http://www.microsoft.com/licensing/licensing-options/enterprise.aspx).

-   **Online program předplatných** (méně než 250 uživatelů) – Program [multilicencí online služeb](http://www.microsoft.com/licensing/online-services/default.aspx) je určený speciálně pro organizace s méně než 250 uživateli. Tento program můžete použít pro předplatné, správu a nasazení služeb [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

## Viz také
[Začněte s placeným předplatným Microsoft Intune](../Topic/Get_started_with_a_paid_subscription_to_Microsoft_Intune.md)

