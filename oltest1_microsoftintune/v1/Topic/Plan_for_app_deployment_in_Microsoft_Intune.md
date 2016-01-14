---
description: na
keywords: na
title: Plan for app deployment in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2b770f4f-6d36-41e4-b535-514b46e29aaa
---
# Zač&#237;n&#225;me s nasazov&#225;n&#237;m aplikac&#237; v Microsoft Intune
Před správou a nasazením aplikací v [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] pro vás můžou být užitečné následující informace:

-   [Pracovní prostor Aplikace](../Topic/Plan_for_app_deployment_in_Microsoft_Intune.md#BKMK_SoftwareWorkspace)

-   [Microsoft Intune Software Publisher](../Topic/Plan_for_app_deployment_in_Microsoft_Intune.md#BKMK_SoftwarePublisher)

-   [Požadavky na operační systém](../Topic/Plan_for_app_deployment_in_Microsoft_Intune.md#BKMK_OSRequirements)

-   [Typy instalace softwaru](../Topic/Plan_for_app_deployment_in_Microsoft_Intune.md#BKMK_Types)

-   [Obecný proces nasazení aplikací](../Topic/Plan_for_app_deployment_in_Microsoft_Intune.md#BKMK_SoftwareDistProcess)

-   [Vysvětlení akcí nasazení aplikace](../Topic/Plan_for_app_deployment_in_Microsoft_Intune.md#BKMK_Depl)

## <a name="BKMK_SoftwareWorkspace"></a>Pracovní prostor Aplikace
Pracovní prostor **Aplikace** v [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] uvádí informace o zjištěných a spravovaných aplikacích. K dispozici jsou následující stránky:

|Stránka Pracovní prostor Aplikace|Podrobnosti|
|-------------------------------------|---------------|
|**Přehled**|Uvádí seznam výstrah nasazení aplikace a aktuální stav cloudového úložiště.|
|**Zjištěný software**|Zobrazuje data inventáře softwaru, který [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] zjistí na spravovaných počítačích. Inventář softwaru je dostupný jenom pro počítače.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] proto nezjišťuje ani neuvádí aplikace pro spravovaná mobilní zařízení. Z pracovního prostoru **Zjištěný software** můžete provádět následující úlohy:<br /><br />-   Zobrazení vlastností aplikace<br />-   Přidání licenčních smluv pro zjištěný software|
|**Aplikace**|Na stránce **Aplikace** se průběžně nahrávají, nasazují a spravují aplikace, které chcete nasadit do spravovaných počítačů a mobilních zařízení. Můžete provádět následující úlohy:<br /><br />-   Zobrazení a úpravy vlastností aplikace<br />-   Přidávání licenčních smluv do spravovaných aplikací<br />-   Správa nasazení aplikaci<br />-   Přidávání nových aplikací<br />-   Úprava vlastností spravovaných aplikací<br />-   Odstranění aplikací|

## <a name="BKMK_SoftwarePublisher"></a>Microsoft Intune Software Publisher
Spustí se **Vydavatel softwaru Microsoft Intune**, kde můžete přidávat nebo upravovat aplikace z konzoly [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)]. Od vydavatele vyberete typ instalačního programu softwaru, který bude nahrávat aplikace (programy pro počítače nebo aplikace pro mobilní zařízení) k uložení do cloudového úložiště [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] nebo odkaz na online úložiště nebo webovou aplikaci.

### <a name="BKMK_PublisherRequirements"></a>Vydavatel softwaru Microsoft Intune – požadavky na systém
Než začnete používat Vydavatel softwaru [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)], musíte nainstalovat plnou verzi rozhraní Microsoft .NET Framework 4.0. Po instalaci rozhraní .NET Framework bude nejspíš nutné restartovat počítač, aby se Vydavatel softwaru [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] správně otevřel. Podrobnosti najdete v tématu [Microsoft .NET Framework 4 (webová instalační služba)](http://www.microsoft.com/download/details.aspx?id=17851).

### <a name="BKMK_CloudStorage"></a>Požadavky na cloudové úložiště
Všechny aplikace, které nasazujete, musí být zabalené a nahrané do cloudového úložiště [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]. Před nasazením aplikací se ujistěte, že máte v úložišti dost místa pro nahrání aplikace. Zkušební předplatné [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] zahrnuje 2 gigabajty (GB) cloudového úložiště, které se používá k ukládání spravovaných aplikací a aktualizací. Placené předplatné zahrnuje 20 GB s možností přikoupit dodatečné úložiště postupně po 1 GB pomocí doplňku [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] – rozšíření úložiště. Následující pravidla platí při nákupu dalšího cloudového úložiště pro [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]:

-   Další úložiště není možné dokoupit v rámci předběžné verze nebo zkušebního období [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

-   Nákup dalšího úložiště vyžaduje aktivní placené předplatné.

-   Další úložiště můžou nakupovat jenom správci fakturace nebo globální správci služby Microsoft Online Service přes portál účtů [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Tyto správce může přidávat, odstraňovat nebo spravovat jenom globální správce přihlášený k portálu účtů [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

-   Pokud jste zákazník s multilicenční smlouvou, který si koupil [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] nebo doplněk [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] v rámci smlouvy Enterprise, zeptejte se na informace o cenách a možnost přikoupení úložiště account manažera nebo partnera Microsoftu.

##### Přikoupení dalšího úložiště

1.  Na [portálu účtů Microsoft Intune](https://account.manage.microsoft.com) v levém podokně klikněte v části **Předplatná** na **Správa**.

2.  Na stránce **Fakturace a správa předplatného** klikněte na předplatné [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], pro které chcete přikoupit úložiště.

3.  Na stránce **Podrobnosti předplatného** klikněte vedle **Volitelná rozšíření** na **Přidat další**.

4.  Na stránce **Vybrat počet licencí** zadejte v části **Volitelná rozšíření** další počet GB úložiště, které chcete pro doplněk Microsoft Intune – rozšíření úložiště přikoupit. Pokud třeba teď máte 20 GB a chcete přidat dalších 10 GB, zadejte 10.

5.  Na stránce  **Zkontrolujte důležité informace** si projděte informace o souhrnu objednávky, a pokud budou správné, klikněte na **Odešlete objednávku**.

6.  Otevře se **stránka Potvrzení objednávky** s podrobnostmi o objednávce. Kliknutím na **Dokončit** proces dokončete.

## <a name="BKMK_OSRequirements"></a>Požadavky na operační systém
Na mobilních zařízeních a počítačích musí běžet podporovaný operační systém, aby bylo možné instalovat aplikace nasazené pomocí [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

**Mobilní zařízení**

Úplný seznam podporovaných operačních systémů pro mobilní zařízení najdete v části [Možnosti správy mobilních zařízení v Microsoft Intune](../Topic/Mobile_device_management_capabilities_in_Microsoft_Intune.md).

**Počítače**

Úplný seznam podporovaných operačních systémů pro spravované počítače najdete v části [Možnosti správy počítačů s Windows v Microsoft Intune](../Topic/Windows_PC_management_capabilities_in_Microsoft_Intune.md).

## <a name="BKMK_Types"></a>Typy instalace softwaru
[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] umožňuje nasadit následující typy instalace softwaru:

### <a name="BKMK_SoftwareInstallers"></a>Instalační program softwaru
Typ instalace **Instalační program softwaru** použijte v následujících případech:

-   Nahrání podepsaného balíčku aplikací do cloudového úložiště Microsoft Intune a zpřístupnění aplikace uživatelům prostřednictvím [!INCLUDE[wit_iwportal_1](../Token/wit_iwportal_1_md.md)].

-   Nahrání aplikací, které se nasadí do počítačů s klientem [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

-   Instalace aplikací na spravovaná mobilní zařízení z instalačního souboru obejitím obchodu s aplikacemi (říká se jí také zkušební načtení).

Následující tabulka vysvětluje různé typy souborů instalačního programu softwaru:

|||
|-|-|
|**Typ instalačního programu softwaru**|**Požadavky**|
|**Instalační služba systému Windows (&#42;.exe, &#42;.msi)**|-   Soubory Instalační služby systému Windows musí podporovat tichou instalaci, to znamená instalaci, která nevyžaduje zásah uživatele. Pokud vaše aplikace používá jiný typ instalačního souboru nebo během instalace vyžaduje zásah uživatele, není možné aplikaci pomocí [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] nainstalovat.<br />    V dokumentaci aplikace najdete příslušné parametry příkazového řádku (například /q k vynucení tiché instalace aplikace na spravovaných počítačích).<br />-   Jakékoli další soubory a složky, které vyžaduje instalační program aplikace, musí být dostupné z umístění, které určíte pro instalační soubory aplikace.<br />-   Instalační služba systému Windows (.msi) a oprava instalační služby systému Windows (.msp) nevyžadují ve většině případů instalaci žádných argumentů příkazového řádku pro [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Podívejte se do dokumentace aplikace. Pokud se vyžadují argumenty příkazového řádku, musí být zadané jako název=dvojice hodnot (například TRANSFORMS=custom_transform.mst).|
|**Balíček aplikace pro systém Android (soubor &#42;.apk)**|Balíček aplikace pro systém Android není k dispozici jako typ instalačního programu softwaru, dokud nenastavíte autoritu pro správu mobilních zařízení na [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)].<br /><br />Podrobnosti najdete v tématu [Nastavení správy systému Android pomocí Microsoft Intune](../Topic/Set_up_Android_management_with_Microsoft_Intune.md).|
|**Balíček aplikace pro systém iOS (soubor &#42;.ipa)**|-   Pokud chcete nasadit iOS aplikace, budete potřebovat platný balíček .ipa.<br />-   Balíček .ipa musí být podepsané společností Apple a datum vypršení platnosti uvedené v profilu zřizování musí být pořád platné.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] může distribuovat aplikace iOS s podnikovým certifikátem. Nejsou podporované všechny aplikace certifikátu vývojáře Apple.<br />-   Vaše organizace musí mít zaregistrovaný iOS Developer Enterprise Program.<br />-   Ujistěte se, že brána firewall vaší organizace umožňuje přístup na weby zřizování a certifikace pro iOS.<br /><br />Podrobnosti najdete v tématu [Nastavení správy iOS pomocí Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md).|
|**Balíček aplikace pro Windows Phone (&#42;.xap, .appx, .appxbundle)**|Než budete distribuovat balíček aplikace pro Windows Phone 8 nebo Windows Phone 8.1, musíte nastavit autoritu pro správu mobilních zařízení na [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)], nastavit uživatele a získat podnikový mobilní certifikát pro podepisování kódu. Podrobnosti najdete v tématu [Nastavení správy pro zařízení Windows Phone v Microsoft Intune](../Topic/Set_up_Windows_Phone_management_with_Microsoft_Intune.md).|
|**Balíček aplikace pro systém Windows (.appx, .appxbundle)**|Balíček Windows appx pro Windows RT a zaregistrovaná zařízení Windows 8.1 nejsou k dispozici, dokud nenastavíte autoritu správy mobilních zařízení na [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)], nezajistíte zřízení uživatelů a nezískáte certifikát pro podpis kódu a klíče aktivace produktu pro zkušební načtení. Podrobnosti najdete v tématu [Nastavení správy pro zařízení Windows Phone v Microsoft Intune](../Topic/Set_up_Windows_Phone_management_with_Microsoft_Intune.md).<br /><br />Níže najdete informace o instalaci obchodních aplikací pro Univerzální platformu Windows v kombinaci se službou [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].|
|**Instalační služba systému Windows pomocí MDM (&#42;.msi)**|Tento typ instalačního programu umožňuje vytvářet a nasazovat aplikace založené na Instalační službě systému Windows na zaregistrovaná zařízení s Windows 10.<br /><br />Když použijete tento typ instalačního programu, platí následující aspekty:<br /><br />-   Můžete nahrát jenom jeden soubor s příponou **.msi**.<br />-   Kód produktu a verze produktu v souboru se používají ke zjišťování aplikací.<br />-   Použije se výchozí chování aplikace při restartování.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] ho neřídí.<br />-   Balíčky MSI na uživatele se nainstalují pro jednoho uživatele.<br />-   Balíčky MSI na zařízení se nainstalují pro všechny uživatele v zařízení.<br />-   Balíčky MSI v duálním režimu se momentálně nainstalují jenom pro všechny uživatele v zařízení.<br />-   Aktualizace aplikací jsou podporované, když kód produktu MSI jednotlivých verzí je stejný.|

#### Podpora aplikací pro Univerzální platformu Windows
Zařízení s Windows 10 nevyžadují k instalaci obchodních aplikací klíč pro zkušební načtení. Kvůli povolení zkušebního načtení ale musí mít klíč registru **HKEY_LOCAL_MACHINE\Software\Policies\Microsoft\Windows\Appx\AllowAllTrustedApps** hodnotu **1**.

Pokud není tento klíč registru nakonfigurovaný, [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] při prvním nasazení aplikace do zařízení automaticky nastaví hodnotu **1**. Pokud nastavíte hodnotu **0**, [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] ji nemůže automaticky změnit a instalace obchodních aplikací se nezdaří.

Obchodní aplikace pro Univerzální platformu Windows musí být podepsané certifikátem pro podpis kódu, který musí být důvěryhodný pro všechna zařízení, ve kterých chcete aplikaci nasadit. Můžete použít certifikáty z interní infrastruktury PKI nebo certifikát z veřejného kořenového certifikátu od jiného výrobce nainstalovaný v zařízení.

V zařízeních se systémem Windows 10 Mobile můžete k podepisování univerzálních aplikací **.appx** používat jiný certifikát pro podepisování kódu než certifikát Symantec. U aplikací **.xap** a balíčků **.appx** sestavených pro systém Windows Phone 8.1, které chcete nainstalovat do zařízení se systémem Windows 10 Mobile, musíte použít certifikát pro podepisování kódu Symantec.

### <a name="BKMK_ExternalLinks"></a>Externí odkaz
Typ instalace **Externí odkaz** použijte, když máte následující položky:

-   **Adresa URL**, která umožňuje uživatelům stáhnout si aplikaci z online obchodu. Tento typ instalace je podporovaný následujícími platformami zařízení:

    -   Windows 8 nebo novější

    -   Windows RT

    -   Windows Phone 8 nebo novější

    -   iOS

    -   Zařízení se systémem Android

-   **Odkaz** na webovou aplikaci, která se spouští z webového prohlížeče.

    Tento typ instalace je dostupný na všech zařízeních podporovaných službou [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

Externí odkazy jsou k dispozici uživatelům přes [!INCLUDE[wit_iwportal_1](../Token/wit_iwportal_1_md.md)].

### Spravované aplikace pro iOS z obchodu s aplikacemi
Typ instalace **Spravovaná aplikace pro iOS z App Storu** použijte ke správě a nasazení iOS aplikací, které jsou zadarmo dostupné v obchodě s aplikacemi pro iOS. Tento typ instalačního programu můžete nasadit jako požadovanou instalaci, která bude na spravovaných zařízeních povinná (čímž se také zpřístupní její instalace z mobilního webového portálu) nebo ji nasadit podle potřeby, aby si ji uživatelé mohli stáhnout z mobilního webového portálu. Taky můžete přidružit zásady správy mobilních aplikací k aplikacím, které splňují předpisy, a zkontrolovat jejich stav v konzole pro správu. Spravované iOS aplikace nejsou uložené v cloudovém úložišti [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

## <a name="BKMK_SoftwareDistProcess"></a>Obecný proces nasazení aplikací
Tato část obsahuje přehled procesu nasazení aplikací v [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

|Krok|Další informace|
|--------|-------------------|
|Ujistěte se, že je aplikace, kterou chcete nasadit, podporovaná ve [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].|[Začínáme s nasazováním aplikací v Microsoft Intune](../Topic/Plan_for_app_deployment_in_Microsoft_Intune.md)|
|Vytvořte skupiny uživatelů nebo zařízení, do kterých můžete nasadit aplikaci.|[Použití skupin pro správu uživatelů a zařízení s Microsoft Intune](../Topic/Use_groups_to_manage_users_and_devices_with_Microsoft_Intune.md)|
|Publikujte aplikaci v cloudovém úložišti [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)].|[Publish mobile device apps to Microsoft Intune cloud storage](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune_-_deleted.md#BKMK_PublishSoftware)<br /><br />[Publish computer apps to Microsoft Intune cloud storage](../Topic/Deploy_apps_to_Windows_PCs_in_Microsoft_Intune.md#BKMK_PublishSoftware)|
|Nasaďte aplikaci do mobilních zařízení nebo počítačů pomocí požadované akce nasazení.|[Nasazení aplikací do mobilních zařízení v Microsoft Intune](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune_-_deleted.md)<br /><br />[Nasazení aplikací do počítačů s Windows v Microsoft Intune](../Topic/Deploy_apps_to_Windows_PCs_in_Microsoft_Intune.md)|
|Monitorujte nasazení aplikace.|[Monitor mobile device apps](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune_-_deleted.md#BKMK_MonitorSoftware)<br /><br />[Monitor computer apps](../Topic/Deploy_apps_to_Windows_PCs_in_Microsoft_Intune.md#BKMK_MonitorSoftware)|

## <a name="BKMK_Depl"></a>Vysvětlení akcí nasazení aplikace
Při nasazování aplikací můžete zvolit jednu z následujících akcí nasazení:

-   **Požadovaná instalace** – Aplikace se nainstaluje na zařízení bez nutnosti zásahu koncového uživatele.

    > [!NOTE]
    > Pro zařízení s iOS, která nejsou v dohledovém režimu, musí uživatel před tím, než se aplikace nainstaluje, přijmout nabídku aplikace.  Informace o používání [dohledového režimu](http://support.apple.com/en-is/HT202837) v Microsoft Intune najdete v tématu [Nastavení zásad konfigurace pro iOS v Microsoft Intune](../Topic/iOS_configuration_policy_settings_in_Microsoft_Intune.md).
    > 
    > Už nemůžete vytvářet nová nasazení aplikací do zařízení iOS se starší verzí operačního systému než iOS 7.1. Všechna stávající nasazení aplikací do zařízení se starší verzí operačního systému než iOS 7.1 budou dál fungovat a bude je spravovat [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

    > [!NOTE]
    > Pro zařízení s Androidem musí uživatel před tím, než se aplikace nainstaluje, přijmout nabídku aplikace.

-   **Dostupná instalace** – Aplikace se zobrazuje na podnikovém portálu a koncoví uživatelé ji můžou instalovat na vyžádání.

-   **Odinstalace** – Aplikace se ze zařízení odinstaluje.

-   **Není k dispozici** – Aplikace se nezobrazuje na podnikovém portálu a není nainstalovaná na žádném zařízení.

|Platforma|Požadovaná instalace|Dostupná instalace|Odinstalovat|Nelze použít|
|-------------|------------------------|----------------------|----------------|----------------|
|Balíček aplikací pro Windows (nasazený pro skupinu uživatelů)|Ano|Ano|Ano|Ano|
|Balíček aplikací pro Windows (nasazený pro skupinu zařízení)|Ano|Ne|Ano|Ano|
|Balíček aplikace pro mobilní zařízení (nasazený pro skupinu uživatelů)|Ano|Ano|Ano|Ano|
|Balíček aplikace pro mobilní zařízení (nasazený pro skupinu zařízení)|Ano|Ne|Ano|Ano|
|Instalační služba systému Windows (nasazené pro skupinu uživatelů)|Ne|Ano|Ne|Ano|
|Instalační služba systému Windows (nasazené pro skupinu zařízení)|Ano|Ne|Ano|Ano|
|Externí odkaz (nasazený pro skupinu uživatelů)|Ne|Ano|Ne|Ano|
|Externí odkaz (nasazený pro skupinu zařízení)|Ne|Ne|Ne|Ne|
|Spravovaná aplikace pro iOS z App Storu (nasazené pro skupinu uživatelů)|Ano|Ano|Ano|Ano|
|Spravovaná aplikace pro iOS z App Storu (nasazené pro skupinu zařízení)|Ano|Ne|Ano|Ano|
Při dvou nasazeních platí při přijetí stejné akce nasazení na zařízení následující pravidla:

-   Nasazení pro skupinu zařízení má přednost před nasazením pro skupinu uživatelů. Pokud je ale aplikace nasazená pro skupinu uživatelů pomocí akce nasazení **Dostupné** a v případě, že je stejná aplikace nasazená taky pro skupinu zařízení pomocí akce nasazení **Není k dispozici**, aplikace bude dostupná na podnikovém portálu a uživatelé si ji můžou nainstalovat.

-   Záměr správce IT má přednost před koncovým uživatelem.

-   Akce instalace má přednost před akcí odinstalace.

-   Pokud zařízení přijme požadovanou i dostupnou instalaci, akce se zkombinují (aplikace je požadovaná i dostupná).

## Viz také
[Nasazení a konfigurace aplikací v Microsoft Intune](../Topic/Deploy_and_configure_apps_with_Microsoft_Intune.md)

