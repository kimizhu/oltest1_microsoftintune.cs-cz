---
description: na
keywords: na
title: Prepare iOS apps for mobile application management with the Microsoft Intune App Wrapping Tool
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 99ab0369-5115-4dc8-83ea-db7239b0de97
---
# Př&#237;prava aplikac&#237; pro iOS na spr&#225;vu mobiln&#237;ch aplikac&#237; n&#225;strojem Microsoft Intune App Wrapping Tool
Pokud chcete změnit chování interních aplikací iOS tak, abyste mohli nastavovat omezení funkcí aplikace beze změny jejího kódu, použijte nástroj **Microsoft Intune App Wrapping pro iOS**.

Tento nástroj je aplikace příkazového řádku Mac OS, která kolem aplikace vytváří „obálku“. Po zpracování aplikace můžete změnit její funkce pomocí zásady správy mobilní aplikace [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], kterou nakonfigurujete (viz [Ochrana dat pomocí zásad správy mobilních aplikací v Microsoft Intune](../Topic/Configure_and_deploy_mobile_application_management_policies_in_the_Microsoft_Intune_console.md)).

Nástroj si můžete stáhnout na stránce [Microsoft Intune App Wrapping pro iOS](http://www.microsoft.com/en-us/download/details.aspx?id=45218).

## <a name="BKMK_Prereq"></a>Krok 1: Splnění požadavků na používání nástroje pro zabalení aplikace

|Požadavek|Podrobnosti a další informace|
|-------------|---------------------------------|
|Podporované operační systémy a sady nástrojů|Nástroj pro zabalení aplikace musíte spustit na počítači Mac se systémem OS X 10.8.5 nebo novějším, na kterém je nainstalovaná sada nástrojů XCode verze 5 nebo novější.|
|Podpisový certifikát a profil pro zřizování|Musíte mít podpisový certifikát Apple a profil pro zřizování. Informace najdete v [dokumentaci pro vývojáře Apple](https://developer.apple.com/).|
|Zpracování aplikace pomocí nástroje App Wrapping|Postup zpracování aplikace pomocí nástroje App Wrapping:<br /><br />-   Aplikace musela vyvinout a podepsat vaše společnost nebo nezávislý dodavatel softwaru (ISV). Tento nástroj se nedá používat ke zpracování aplikací z Apple Storu.<br />-   Aplikace musí být napsaná pro iOS 7.0 nebo novější.<br />-   Aplikace musí být ve formátu Position Independent Executable (PIE). Další informace o formátu PIE najdete v dokumentaci pro vývojáře Apple.<br />-   Aplikace musí mít příponu **.app** nebo **.ipa**.|
|Aplikace, které nástroj App Wrapping nedokáže zpracovat|-   Zašifrované aplikace<br />-   Nepodepsané aplikace<br />-   Aplikace s rozšířenými atributy souborů|
|Aplikace, které používají knihovnu ADAL (Azure Active Directory Library)|Pokud vaše aplikace používá knihovnu ADAL:<br /><br />-   Aplikace musí mít verzi ADAL větší nebo rovnou hodnotě 1.0.2.<br />-   Vývojář musí své aplikaci udělit přístup k prostředku Správa mobilních aplikací Intune.<br /><br />Informace o použití knihovny ADAL najdete v části [Informace pro aplikace, které používají knihovnu Azure Active Directory Library (ADAL)](../Topic/Prepare_iOS_apps_for_mobile_application_management_with_the_Microsoft_Intune_App_Wrapping_Tool.md#BKMK_ADAL) v tomto článku.|
|Nastavení oprávnění pro vaši aplikaci|Před zabalením aplikace je potřeba nastavit oprávnění, která poskytnou aplikaci další práva a schopnosti nad běžný rámec. Pokyny najdete v části [Nastavení oprávnění aplikace](#BKMK_ios_entitlements).|

## Krok 2: Instalace nástroje App Wrapping

1.  Ze stránky **Microsoft Intune App Wrapping Tool for iOS** ve službě [Stažení softwaru](http://www.microsoft.com/en-us/download/default.aspx) stáhněte instalační soubor nástroje pro zabalení aplikace do počítače Mac.

2.  Na počítači Mac poklikejte na instalační soubor **Microsoft Intune App Wrapping Tool for iOS.dmg**.

3.  Kliknutím na **Agree** (Souhlasím) přijměte podmínky licenční smlouvy s koncovým uživatelem (EULA). Instalační program se připojí a zobrazuje na počítači Mac.

4.  Spusťte instalační program a zkopírujte zobrazené soubory do nové složky na počítači Mac. Teď můžete odpojit připojenou jednotku instalačního programu.

    Teď můžete nástroj pro zabalení aplikace spustit.

## Krok 3: Spuštění nástroje App Wrapping

1.  Na počítači Mac otevřete okno Terminal (Terminál) a přejděte do složky, do které jste soubory uložili. Protože je spustitelný soubor uvnitř balíčku, je potřeba příkaz spustit takto:

    ```
    ./IntuneMAMPackager.app/Contents/MacOS/IntuneMAMPackager –i /<path of input app>/<app filename> -o /<path to output folder>/<app filename> –p /<path to provisioning profile> –c <SHA1 hash of the certificate> -a <client ID of input app> -r <reply URI of input app> -v true
    ```
    > [!NOTE]
    > Některé parametry jsou volitelné. Viz následující tabulka.

    **Příklad:** V tomto ukázkovém příkazu se nástroj pro zabalení aplikace spouští v aplikaci s názvem **MyApp.ipa**. Je zadaný profil zřizování a hash SHA-1. Zpracovaná aplikace se vytvoří a uloží do složky **/users/myadmin/Documents** na Macu.

    ```
    /users/myadmin/Downloads/IntuneMAMPackager.app/Contents/MacOS/IntuneMAMPackager -i /users/myadmin/Downloads/MyApp.ipa -o /users/myadmin/Documents/MyApp_Wrapped.ipa -p /users/myadmin/Downloads/My_Provisioning_Profile_.mobileprovision -c 12A3BC45D67EF8901A2B3CDEF4ABC5D6E7890FAB –a 20e1cd0d-268e-4308-9583-02ae97dd353e –r https://contoso/ -v true
    ```
    S nástrojem pro zabalení aplikace můžete používat následující vlastnosti příkazového řádku:

    |Vlastnost|Další informace|
    |-------------|-------------------|
    |**-h**|Zobrazí dostupné vlastnosti příkazového pro nástroj pro zabalení aplikace.|
    |**-i**|Určuje cestu a název souboru vstupní aplikace.|
    |**-o**|Určuje cestu, do které uložíte zpracovanou aplikaci.|
    |**-p**|Určuje cestu k profilu zřizování pro aplikace iOS.|
    |**-c**|Určuje algoritmus hash SHA1 podpisového certifikátu.|
    |**-a**|ID klienta vstupní aplikace (ve formátu identifikátoru GUID), pokud aplikace používá knihovny Azure Active Directory (volitelné).|
    |**-r**|Identifikátor URI přesměrování vstupní aplikace, pokud aplikace používá knihovny Azure Active Directory (volitelné).|
    |**-v**|Výstup podrobných zpráv do konzoly (volitelné).|

2.  Po dokončení zpracování se zobrazí zpráva **The application was successfully wrapped** (Aplikace byla úspěšně zabalená).

    V případě chyby najdete nápovědu v [Chybovými zprávami](../Topic/Prepare_iOS_apps_for_mobile_application_management_with_the_Microsoft_Intune_App_Wrapping_Tool.md#BKMK_Error).

3.  Zabalená aplikace se uloží do výstupní složky, kterou jste určili předtím. Teď můžete aplikaci nahrát do [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] a přidružit k zásadám správy mobilní aplikace. Další informace najdete v tématu [Nasazení aplikací do mobilních zařízení v Microsoft Intune](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune_-_deleted.md).

    > [!IMPORTANT]
    > Aplikaci musíte nahrát jako novou aplikaci. Nejde aktualizovat starší, rozbalenou verzi aplikace.

    Teď můžete aplikaci nasadit do skupin služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] a aplikace se bude spouštět v zařízení s omezeními, která určíte.

## Chybové zprávy a soubory protokolu
K řešení potíží s nástrojem App Wrapping použijte následující informace.

### <a name="BKMK_Error"></a>Chybovými zprávami
Pokud se nepodaří úspěšně dokončit nástroj pro zabalení aplikace, zobrazí se některá z následujících chybových zpráv:

|Chybová zpráva|Další informace|
|------------------|-------------------|
|Je nutné zadat platný profil zřizování iOS.|Váš profil zřizování nemusí být platný. Ověřte, jestli máte správná oprávnění pro zařízení a jestli je váš profil správně zacílený na vývoj nebo distribuci. Je taky možné, že vypršela platnost vašeho profilu zřizování.|
|Zadejte platný vstupní název aplikace.|Ujistěte se, že je správný název vstupní aplikace, který jste zadali.|
|Zadejte platnou cestu k výstupní aplikaci.|Ujistěte se, jestli existuje cesta k výstupní aplikace, kterou jste zadali, a jestli je správná.|
|Zadejte platný vstupní profil zřizování.|Ujistěte se, jestli jste zadali platný název a příponu profilu zřizování. V profilu zřizování můžou chybět oprávnění nebo jste nezahrnuli možnost příkazového řádku **–p**.|
|Nenašla se zadaná vstupní aplikace. Zadejte platný název a cestu vstupní aplikace.|Přesvědčte se, jestli je cesta ke vstupní aplikaci platná a existuje. Ujistěte se, jestli vstupní aplikace existuje v tomto umístění.|
|Zadaný soubor vstupního profilu zřizování se nenašel. Zadejte platný soubor vstupního profilu zřizování.|Ujistěte se, jestli je cesta k vstupnímu souboru profilu zřizování platná a jestli existuje soubor, který jste zadali.|
|Zadaná složka výstupní aplikace se nenašla. Zadejte platnou cestu k výstupní aplikaci.|Ujistěte se, jestli je zadaná výstupní cesta platná a existuje.|
|Výstupní aplikace nemá příponu .ipa.|Nástroj pro zabalení aplikace přijímá jenom aplikace s příponou **.app** a **.ipa**. Ujistěte se, že výstupní má platnou příponu.|
|Je zadaný neplatný podpisový certifikát. Zadejte platný podpisový certifikát Apple.|Ujistěte se, jestli jste stáhli správný podpisový certifikát stažený z portálu pro vývojáře Apple. Je taky možné, že vypršela platnost certifikátu. Pokud se dá váš profil certifikátu a zřizování apple použít ke správnému podepsání aplikace v rámci Xcodu, pak jsou platné pro nástroj pro zabalení aplikace.|
|Zadaná vstupní aplikace je neplatná. Zadejte platnou aplikaci.|Ujistěte se, že máte platnou aplikaci iOS, která je kompilovaná jako soubor .app nebo .ipa.|
|Zadaná vstupní aplikace je zašifrovaná. Zadejte platnou nezašifrovanou aplikaci.|Nástroj pro zabalení aplikace nepodporuje šifrované aplikace. Zadejte nezašifrovanou aplikaci.|
|Zadaná vstupní aplikace není ve formátu Position Independent Executable (PIE). Zadejte platnou aplikaci ve formátu PIE.|Aplikace Position Independent Executable (PIE) se dají při spuštění nahrát s náhodnou adresou paměti. To je výhodné pro zabezpečení. Další informace najdete v Dokumentaci pro vývojáře Apple.|
|Zadaná vstupní aplikace už je zabalená. Zadejte platnou nezabalenou aplikaci.|Nejde zpracovat aplikaci, kterou už nástroj zpracoval. Pokud chcete ke aplikaci znovu zpracovat, spusťte nástroj pomocí původní verze aplikace.|
|Zadaná vstupní aplikace není podepsaná. Zadejte platnou podepsanou aplikaci.|Nástroj pro zabalení aplikace vyžaduje, aby aplikace byla podepsaná. Vyhledejte v dokumentaci pro vývojáře, jak podepsat zabalenou aplikaci.|
|Zadaná vstupní aplikace musí být ve formátu .ipa nebo .app.|Nástroj pro zabalení aplikace přijímá jenom přípony .app a .ipa. Ujistěte se, že vstupní soubor má platnou příponu a je kompilovaný jako soubor .app nebo .ipa.|
|Vstupní aplikace, kterou jste zadali, už je zabalená a má nejnovější verzi šablony zásad.|Nástroj pro zabalení aplikace znovu nezabalí existující zabalenou aplikaci s nejnovější verzí šablony zásad.|
|Uvedené ID klienta Azure Active Directory není správně formátovaný GUID. Zadejte prosím platné ID klienta.|Při použití parametru ID klienta zadejte platné ID klienta ve formátu GUID.|
|Identifikátor URI odpovědi Azure Active Directory není správně formátovaný URI. Zadejte platný identifikátor URI odpovědi.|Pokud použijete vlastnost příkazového řádku URI odpovědi, ověřte, jestli jste zadali platný URI odpovědi.|
|UPOZORNĚNÍ: Nezadali jste hash SHA1 certifikátu. Ujistěte se, že zabalená aplikace je před nasazením podepsaná.|Zadejte platný hash SHA (pomocí vlastnosti příkazového řádku **– c**).|

### Soubory protokolu pro nástroj sbalení aplikace
Aplikace zabalené pomocí nástroje pro zabalení aplikace generují protokoly zapsané do konzoly klientského zařízení iOS. Tyto informace jsou užitečné v situacích, kdy máte problémy s aplikací a potřebujete diagnostikovat, jestli tento problém souvisí s nástrojem pro zabalení aplikace. Pro načtení těchto informací použijte následující kroky:

1.  Reprodukujte problém spuštěním aplikace.

2.  Shromážděte výstup konzoly podle pokynů společnosti Apple k [ladění nasazených aplikací iOS](https://developer.apple.com/library/ios/qa/qa1747/_index.html).

3.  Vyfiltrujte uložené protokoly pro výstup omezení aplikace zadáním následujícího skriptu do konzoly:

    ```
    grep “IntuneAppRestrictions” <text file containing console output> > <required filtered log file name>
    ```
    Filtrované protokoly můžete odeslat do Microsoftu.

    > [!NOTE]
    > Položka verze buildu v souboru protokolu označuje verzi buildu pro Xcode.

    Zabalené aplikace taky uživatelům nabídnou možnost odeslat protokoly přímo ze zařízení prostřednictvím e-mailu v případě chyby aplikace. Uživatelé můžou vám můžou protokol zaslat k ověření a předání Microsoftu, pokud je potřeba.

### <a name="BKMK_ADAL"></a>Informace pro aplikace, které používají knihovnu Azure Active Directory Library (ADAL)
Informace v této části se vztahují jenom na aplikace, které používají knihovnu Azure Active Directory (ADAL). Pokud si nejste jistí, jestli vaše aplikace tuto knihovnu používá, obraťte se na vývojáře aplikace.

Aplikace musí mít verzi ADAL větší nebo rovnou hodnotě 1.0.2.

Pro aplikace, které používají ADAL, musí platit následující:

-   Aplikace musí mít verzi ADAL větší nebo rovnou hodnotě 1.0.2

-   Vývojář musí své aplikaci udělit přístup k prostředku Správa mobilních aplikací Intune podle popisu v části [Postup pro aplikace, které používají knihovnu ADAL](#BKMK_step_use_adal).

#### <a name="BKMK_adal_overview"></a>Přehled identifikátorů, které je potřeba získat
Aplikace, které používají ADAL, se musí registrovat prostřednictvím portálu pro správu Azure, aby mohly získat dva jedinečné identifikátory pro svou aplikaci:

|Identifikátor|Další informace|Výchozí hodnota|
|-----------------|-------------------|-------------------|
|**ID klienta**|Jedinečný identifikátor GUID se generuje pro každou aplikaci po registraci na Azure Active Directory.<br /><br />Pokud znáte konkrétní ID klienta aplikace, můžete tuto hodnotu zadat. Jinak je potřeba použít výchozí hodnotu.|6c7e8096-f593-4d72-807f-a5f86dcc9c77|
|**Identifikátor URI pro přesměrování**|Hodnota identifikátoru URI, kterou můžou vývojáři poskytnout při registraci své aplikace na Azure Active Directory pro zajištění, že ověřovací tokeny jsou vráceny speciálně do tohoto koncového bodu.<br /><br />Poskytnutí identifikátoru URI pro přesměrování je volitelný parametr nástroje pro zabalení aplikace. Pokud není zadaný, použije se výchozí identifikátor URI.|urn:ietf:wg:oauth:2.0:oob|
Pokud nezadáte výše uvedené hodnoty do nástroje; automaticky se použijí následující další hodnoty:

-   **URI autority** – https://login.windows.net/common/oauth2/authorize

-   **ID prostředku** – https://intunemam.microsoft.com

#### <a name="BKMK_step_use_adal"></a>Postup pro aplikace, které používají knihovnu ADAL

1.  Projděte si část [Přehled identifikátorů, které je potřeba získat](#BKMK_adal_overview) a určete hodnoty, které potřebujete získat.

2.  Pomocí tohoto postupu nakonfigurujte přístup ke správě mobilních aplikací ve službě Azure Active Directory:

    1.  Přihlaste se k existujícímu účtu Azure Active Directory na portálu pro správu Azure.

    2.  V Azure Active Directory klikněte na **existující registraci aplikace LOB**.

    3.  V části konfigurace zvolte **Konfigurovat přístup k webovým rozhraním API v ostatních aplikacích**.

    4.  V části **Oprávnění k ostatním aplikacím** vyberte v prvním rozevíracím seznamu **Správa mobilní aplikace Intune**.

        Teď můžete použít ID klienta aplikace v nástroji App Wrapping. ID klienta aplikace najdete na portálu pro správu služby Azure Active Directory podle popisu v části [Přehled identifikátorů, které je potřeba získat](#BKMK_adal_overview).

3.  Hodnoty **ID klienta** (pomocí vlastnosti **– a**) a **Redirect-URI** použijte v nástroji App Wrapping jako vlastnosti na příkazovém řádku. Pokud tyto hodnoty nemáte, použijí se výchozí hodnoty. Je potřeba zadat obě hodnoty, jinak nebude moct koncový uživatel úspěšně ověřit zpracovanou aplikaci.

#### Požadavky na certifikát, profil pro zřizování a ověřování

|Požadavek|Podrobnosti|
|-------------|---------------|
|Profil pro zřizování|**Ujistěte se, že je profil zřizování platný a teprve potom ho zahrňte** – nástroj pro zabalení aplikace nekontroluje, jestli při zpracování aplikace pro iOS vypršelo zřizování profilu. Když je zadaný profil zřizování s ukončenou platností, bude nástroj pro zabalení aplikace zahrnovat tento profil a vy nepoznáte, jestli existuje problém, dokud neselže instalace aplikace na zařízení iOS.|
|Certifikát|-   **Před zadáním certifikátu ověřte, že je platný** – Nástroj při zpracovávání aplikací pro iOS nekontroluje, jestli je certifikát prošlý. Pokud je zadaný hash pro prošlý certifikát, nástroj zpracuje a podepíše aplikaci, ale nenainstaluje ji na zařízení.<br />-   **Ujistěte se, jestli má certifikát zadaný pro podepsání zabalené aplikace nějakou odpovídající položku v profilu zřizování** – nástroj neověřuje, jestli má tento profil odpovídající položku certifikátu poskytnutého pro podepsání zabalené aplikace.|
|Ověřování|-   Na zařízeních, na která jste nasadili zabalenou aplikaci, bude dotykové ovládání stavového řádku zařízení vyžadovat opakované ověření uživatele pomocí [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Výchozí zásada v zabalené aplikaci je *Ověřit při opětovném spuštění*. iOS zpracovává všechna externí oznámení (například telefonní hovor) jako při ukončení a dalším spuštění aplikace.<br />-   Šifrování funguje, jenom pokud má zařízení nastavený PIN.<br />-   U zabalených aplikací se jméno prvního uživatel přihlášeného k jakékoli zabalené aplikaci od stejného vydavatele uloží do mezipaměti. Od této chvíle má přístup k aplikaci dovolený jenom tento uživatel.<br />-   Resetování tohoto uživatele vyžaduje zrušení registrace a opakovanou registraci uživatele.|

#### Řešení potíží a technické poznámky o službě ADAP

-   Pokud nenajdete žádné prostředky ADAL, nástroj zahrne dynamickou knihovnu ADAL. Nástroj vyhledá knihovnu ADAL s názvem **ADALiOS.bundle** v kořenové složce.

-   Nehledá v aplikaci binární soubory ADAL (pokud existují). Pokud aplikace odkazuje na zastaralou verzi a jsou zapnuté zásady ověřování, můžou se během přihlašování objevit chyby za běhu.

-   [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] načte token AAD na prostředku [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] MAM resource-id pro ověřování. Token se ale nepoužije v žádném volání, které by ověřilo jeho platnost.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] přečte jenom hlavní název (UPN) přihlášeného uživatele a zjistí přístup k aplikaci. Token AAD se nepoužívá pro žádná další servisní volání.

-   Tokeny ověřování jsou sdílené mezi aplikacemi od stejného vydavatele, protože jsou sdílené ve sdíleném řetězci klíčů. Pokud chcete izolovat konkrétní aplikaci, pak musíte použít jiný podpisový certifikát a profil zřizování pro tuto aplikaci.

-   Pokud zadáte ID klienta a identifikátor URI pro přesměrování, zabráníte tím zdvojnásobení výzev k přihlášení. Přístup k publikovanému ID prostředku MAM v řídicím panelu AAD [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] vyžaduje registraci tohoto ID klienta. Když to neuděláte, selže přihlašování při spuštění aplikace.

## <a name="BKMK_ios_entitlements"></a>Nastavení oprávnění aplikace
Před zabalením aplikace, můžete udělit **oprávnění**, která poskytnout aplikaci další práva a schopnosti nad běžný rámec.   Při podepisování kódu se pomocí **souboru nároků** určí v aplikaci speciální oprávnění (například přístup ke sdílenému řetězci klíčů). Během vývoje aplikace se v prostředí Xcode povolí konkrétní aplikační služby, které se nazývají **schopnosti**. Jakmile se tyto schopnosti povolí, odrazí se to v souboru oprávnění. Další informace o oprávněních a schopnostech najdete v článku [Přidání schopností](https://developer.apple.com/library/ios/documentation/IDEs/Conceptual/AppDistributionGuide/AddingCapabilities/AddingCapabilities.html) na webu iOS Developer Library. Úplný seznam podporovaných schopností najdete v části [Podporované schopnosti](https://developer.apple.com/library/ios/documentation/IDEs/Conceptual/AppDistributionGuide/SupportedCapabilities/SupportedCapabilities.html).

### Podporované schopnosti nástroje App Wrapping pro iOS

|Funkce|Popis|Doporučené pokyny|
|----------|---------|---------------------|
|Skupiny aplikací|Pomocí skupin aplikací můžete více aplikacím povolit přístup ke sdíleným kontejnerům a povolit meziprocesovou komunikaci mezi aplikacemi.<br /><br />Pokud chcete povolit skupiny aplikací, otevřete podokno **Schopnosti** a klikněte na přepínač **ZAPNOUT** v části **Skupiny aplikací**. Můžete přidat nové skupiny aplikací nebo vybrat stávající.|U skupin aplikací používejte zpětný zápis DNS:<br /><br />*skupina.com.nazev_spolecnosti.skupina_aplikaci*|
|Režimy pozadí|Pokud povolíte režimy pozadí, vaše aplikace iOS bude moct být spuštěná na pozadí.||
|Data Protection|Ochrana dat přidá do souborů, které aplikace iOS uložení na disk, úroveň zabezpečení. Ochrana dat využívá integrovaný šifrovací hardware přítomný v určitých zařízeních k ukládání souborů na disk v zašifrovaném formátu. Pokud má vaše aplikace používat ochranu dat, musí být zřízená.||
|Nákupy v aplikaci|Funkce Nákupy v aplikaci vloží přímo do aplikace obchod, takže se budete moct připojit k obchodu a zpracovávat zabezpečené platby od uživatele. Pomocí funkce Nákupy v aplikaci můžete vybírat platby za rozšířené funkce nebo další obsah, který se dá v aplikaci použít.||
|Sdílení řetězce klíčů|Pokud povolíte sdílení řetězce klíčů, bude moct vaše aplikace sdílet hesla v řetězci klíčů s jinými aplikacemi vyvinutými vaším týmem.|Pokud používáte sdílení řetězce klíčů, použijte zpětný zápis DNS:<br /><br />*com.nazev_spolecnosti.skupina_retezcu_klicu*|
|Osobní síť VPN|Můžete povolit osobní síť VPN, aby mohla vaše aplikace vytvářet a řídit vlastní systémovou konfiguraci sítě VPN s využitím rámce pro rozšíření sítě.||
|Nabízená oznámení|Služba APNs (Apple Push Notification service) umožňuje aplikaci, která není spuštěná v popředí, zobrazit uživateli oznámení o dostupných informacích.|Nabízená oznámení fungují jenom tehdy, když pro konkrétní aplikaci použijete profil zřizování.<br /><br />Postupujte podle návodu v [dokumentaci pro vývojáře Apple](https://developer.apple.com/library/ios/documentation/IDEs/Conceptual/AppDistributionGuide/AddingCapabilities/AddingCapabilities.html).|
|Konfigurace bezdrátového příslušenství|Povolením konfigurace bezdrátového příslušenství přidáte do svého projektu rámec externích příslušenství a umožníte své aplikaci konfigurovat příslušenství MFi s připojením Wi-Fi.||

### Postup pro povolení oprávnění

1.  Povolení schopností v aplikaci:

    1.  V prostředí Xcode přejděte na cíl své aplikace a klikněte na podokno **Schopnosti**.

    2.  Zapněte příslušné schopnosti. Podrobné informace o jednotlivých schopnostech a o tom, jak určit správné hodnoty, najdete v článku [Přidání schopností](https://developer.apple.com/library/ios/documentation/IDEs/Conceptual/AppDistributionGuide/AddingCapabilities/AddingCapabilities.html) na webu iOS Developer Library.

    3.  Poznamenejte si všechna ID, která v průběhu procesu vytvoříte.

    4.  Sestavte a podepište aplikaci, kterou chcete zabalit.

2.  Ve svém profilu pro zřizování povolte oprávnění:

    1.  Přihlaste do Centra pro vývojáře Apple.

    2.  Vytvořte pro svoji aplikaci profil pro zřizování. Pokyny najdete v článku [Splnění předpokladů pro nástroj Intune App Wrapping pro iOS](http://blogs.technet.com/b/microsoftintune/archive/2015/02/25/how-to-obtain-the-prerequisites-for-the-intune-app-wrapping-tool-for-ios.aspx).

    3.  V profilu pro zřizování povolte stejná oprávnění, jaká máte ve své aplikaci. Budete muset zadat stejná ID, která jste zadali během vývoje aplikace.

    4.  Dokončete průvodce profilem pro zřizování a stáhněte soubor.

3.  Ujistěte se, že jste splnili všechny předpoklady, a zabalte aplikaci.

### Řešení potíží s běžnými chybami spojenými s oprávněními
Pokud nástroj App Wrapping pro iOS zobrazí chybu oprávnění, vyzkoušejte následující postupy pro řešení potíží.

|Problém|Příčina|Řešení|
|-----------|-----------|----------|
|Nepodařilo se analyzovat oprávnění vygenerovaná vstupní aplikací.|Nástroj App Wrapping nemůže přečíst soubor oprávnění extrahovaný z aplikace. Soubor oprávnění může být poškozený.|Zkontrolujte soubor oprávnění pro svoji aplikaci. Postupujte podle níže uvedených pokynů. Při kontrole souboru oprávnění hledejte případy poškozené syntaxe. Soubor by měl být ve formátu XML.|
|V profilu pro zřizování chybí oprávnění (s uvedením chybějících oprávnění). Znovu zabalte aplikaci pomocí profilu pro zřizování, který má tato oprávnění.|Oprávnění povolená v profilu pro zřizování neodpovídají schopnostem povoleným v aplikaci. Tato neshoda se týká také ID přidružených k určitým schopnostem (tedy skupin aplikací, přístupu k řetězcům klíčů atd.).|Obecně platí, že můžete vytvořit nový profil pro zřizování, který povolí stejné schopnosti jako aplikace. Pokud ID v profilu neodpovídají ID v aplikaci, nástroj App Wrapping tato ID nahradí, pokud to bude možné.|

#### Vyhledání stávajících oprávnění v podepsané aplikaci
Postup pro kontrolu oprávnění v podepsané aplikaci a profilu pro zřizování:

1.  Najděte soubor .ipa a změňte jeho příponu na .zip.

2.  Rozbalte soubor .zip. Vznikne tak složka datové části, která obsahuje sadu .app.

3.  Pomocí nástroje codesign ověřte oprávnění k sadě .app:

    ```
    $ codesign -d --entitlements :- "Payload/YourApp.app"
    ```
    kde `YourApp.app` je skutečný název vaší sady .app.

4.  Pomocí nástroje security ověřte oprávnění k vloženému profilu pro zřizování aplikace:

    ```
    $ security -D -i "Payload/YourApp.app/embedded.mobileprovision"
    ```
    kde `YourApp.app` je skutečný název vaší sady .app.

## Zabezpečení a ochrana osobních údajů nástroje pro zabalení aplikace
Při používání nástroje pro zabalení aplikace použijte následující doporučené postupy pro zabezpečení a ochranu osobních údajů.

-   Podpisový certifikát, profil zřizování a obchodní aplikace, které zadáte, musí být na stejném počítači Mac, jaký používáte pro spouštění nástroje pro zabalení aplikace. Pokud jsou soubory v cestě UNC, ujistěte se, že jsou přístupné z počítače Mac. Cesta musí být zabezpečená pomocí protokolu IPsec nebo podepsání SMB.

    Zabalená aplikace naimportovaná do konzoly [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] by měla být na stejném počítači, na kterém jste nástroj spustili. Pokud je soubor v cestě UNC, zajistěte, aby byl přístupný na počítači se spuštěnou konzolou [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Cesta musí být zabezpečená pomocí protokolu IPsec nebo podepsání SMB.

-   V prostředí, do kterého jste nástroj pro zabalení aplikace stáhli ze služby Stažení softwaru, musí být zabezpečené pomocí protokolu IPsec nebo podepsání SMB.

-   Zpracovávaná aplikace musí být z důvěryhodného zdroje kvůli zajištění ochrany před útoky.

-   Zadaná výstupní složka v nástroji pro zabalení aplikace musí být zabezpečená, zvlášť pokud je to vzdálená složka.

-   Aplikace iOS, která zahrnuje dialog pro nahrání souboru, může uživatelům umožnit obejít vyjmutí, zkopírování a vložení omezení použitých na aplikaci. Uživatel může například pomocí dialogového okna pro nahrání souboru nahrát snímek obrazovky dat aplikace.

-   Když uživatelé sledují složku dokumentů na zařízení ze zabalené aplikace, může se jim zobrazit složka **.msftintuneapplauncher**. Pokud tuto složku změníte nebo odstraníte, může to mít vliv na správné fungování aplikací s omezeními.

## Viz také
[Ochrana dat pomocí zásad správy mobilních aplikací v Microsoft Intune](../Topic/Configure_and_deploy_mobile_application_management_policies_in_the_Microsoft_Intune_console.md)

