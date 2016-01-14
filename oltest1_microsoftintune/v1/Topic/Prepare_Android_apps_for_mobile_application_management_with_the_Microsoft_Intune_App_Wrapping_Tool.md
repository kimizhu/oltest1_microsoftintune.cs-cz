---
description: na
keywords: na
title: Prepare Android apps for mobile application management with the Microsoft Intune App Wrapping Tool
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e9c349c8-51ae-4d73-b74a-6173728a520b
---
# Př&#237;prava aplikac&#237; pro Android na spr&#225;vu mobiln&#237;ch aplikac&#237; n&#225;strojem Microsoft Intune App Wrapping Tool
Pokud chcete změnit chování aplikací pro Android na pracovišti, tak abyste mohli nastavovat omezení funkcí aplikací pro Android beze změny kódu aplikace, použijte nástroj **Microsoft Intune App Wrapping Tool for Android**.

Nástroj je aplikace příkazového řádku Windows, která běží v prostředí PowerShell a vytvoří v okolí vaší aplikace „obálku“. Po zpracování aplikace můžete změnit její funkce pomocí [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] zásady správy mobilní aplikace (viz [Ochrana dat pomocí zásad správy mobilních aplikací v Microsoft Intune](../Topic/Configure_and_deploy_mobile_application_management_policies_in_the_Microsoft_Intune_console.md)).

Jestli vaše aplikace používá knihovnu Azure Active Directory Authentication Library (ADAL), musíte před zabalením aplikace dokončit kroky v tématu [Postup při zabalení aplikací, které používají knihovnu Azure Active Directory Library (ADAL)](#BKMK_ADAL_android). Pokud si nejste jistí, jestli vaše aplikace tuto knihovnu používá, obraťte se na vývojáře aplikace.

Před spuštěním nástroje zkontrolujte [Důležité informace o zabezpečení při spuštění nástroje pro zabalení aplikace](../Topic/Prepare_Android_apps_for_mobile_application_management_with_the_Microsoft_Intune_App_Wrapping_Tool.md#BKMK_androidappwraptool). Nástroj si můžete stáhnout na stránce [Microsoft Intune App Wrapping pro Android](http://www.microsoft.com/en-us/download/details.aspx?id=47267).

## Krok 1: Splnění požadavků na používání nástroje App Wrapping

-   Nástroj pro zabalení aplikace se musí spustit v počítači s Windows 7 nebo novějším systémem.

-   Vstupní aplikace musí být platný balíček aplikace pro Android se souborem s přílohou **.apk** a:

    -   Nedá se zašifrovat.

    -   Nesmí už být zabalený pomocí nástroje pro zabalení aplikace.

    -   Musí být napsaný pro Android 4.0 nebo vyšší.

-   Aplikace musí být vyvinutá vaší společností nebo pro ni. Tento nástroj se nedá používat ke zpracování aplikací stažených z Google Play Storu.

-   Pokud chcete spustit nástroj pro zabalení aplikace, nainstalujte nejnovější verzi [prostředí Java Runtime](http://java.com/download/) a ověřte, jestli je proměnná cesty Java v proměnných prostředí Windows nastavená na **C:\ProgramData\Oracle\Java\javapath**. Další nápovědu najdete v [dokumentaci Java](http://java.com/download/help/).

    > [!NOTE]
    > V některých případech může 32bitová verze Javy způsobit potíže s pamětí. Doporučujeme nainstalovat místo toho 64bitovou verzi.

## Krok 2: Instalace nástroje App Wrapping

#### Instalace nástroje pro zabalení aplikace

1.  Stáhněte si instalační soubor nástroje pro zabalení aplikace ze služby Stažení softwaru a nainstalujte ho do počítače s Windows.

2.  Přijměte licenční smlouvu a dokončete instalaci.

Poznamenejte si složku, do které jste nainstalovali nástroj. Výchozí umístění: **C:\Program Files (x86)\Microsoft Intune Mobile Application Management\Android\App Wrapping Tool**.

## Krok 3: Spuštění nástroje App Wrapping

1.  Na počítači s Windows, na který jste nainstalovali nástroj pro zabalení aplikace, otevřete okno PowerShell.

2.  Ze složky, do které jste nástroj nainstalovali, importujte modul PowerShell nástroje pro zabalení aplikace:

    ```
    Import-Module .\IntuneAppWrappingTool.psm1
    ```

3.  Spusťte nástroj pomocí příkazu **invoke-AppWrappingTool** společně s následujícími parametry. Parametry, které jsou označené jako „volitelné“, jsou určené pro aplikace využívající knihovnu ADAL (Azure Active Directory Library). Další informace naleznete v části [Postup při zabalení aplikací, které používají knihovnu Azure Active Directory Library (ADAL)](#BKMK_ADAL_android).

    |Parametr|Další informace|
    |------------|-------------------|
    |**-InputPath** *&lt;řetězec&gt;*|Cesta ke zdrojové aplikaci pro Android (.apk).|
    |**-OutputPath** *&lt;řetězec&gt;*|Cesta k „výstupní“ aplikaci pro Android. Když je to cesta ke stejnému adresáři jako InputPath, vytváření balíčků selže.|
    |**-KeyStorePath** *&lt;řetězec&gt;*|Cesta k souboru úložiště klíčů, který obsahuje pár veřejného a privátního klíče pro podepisování.|
    |**-KeyStorePassword** *&lt;zabezpečený_řetězec&gt;*|Heslo použité k dešifrování úložiště klíčů.|
    |**-KeyAlias** *&lt;řetězec&gt;*|Název klíče, který se má použít pro podepisování.|
    |**-KeyPassword** *&lt;zabezpečený_řetězec&gt;*|Heslo použité k dešifrování privátního klíče, který se použije pro podepisování.|
    |**-SigAlg** *&lt;zabezpečený_řetězec&gt;*|Název podpisového algoritmu, který se má použít k podepsání. Algoritmus musí být kompatibilní s privátním klíčem.<br /><br />Příklady: SHA256withRSA, SHA1withRSA, MD5withRSA|
    |**-ClientID** *&lt;identifikátor GUID&gt;*|ID klienta Azure Active Directory vstupní aplikace (volitelné).|
    |**-AuthorityURI** *&lt;identifikátor Uri&gt;*|Identifikátor URI autority Azure Active Directory vstupní aplikace (volitelné).|
    |**-SkipBroker** *&lt;hodnota typu Boolean&gt;*|Určuje, jestli vstupní aplikace podporuje zprostředkované jednotné přihlašování v celém zařízení (volitelné).<br /><br />-   True – vstupní aplikace nepodporuje zprostředkované jednotné přihlašování v celém zařízení. Použijte parametr NonBrokerRedirectURI.<br />-   False – vstupní aplikace podporuje zprostředkované jednotné přihlašování v celém zařízení.|
    |**-NonBrokerRedirectURI** *&lt;identifikátor URI&gt;*|Identifikátor URI pro přesměrování služby Azure Active Directory, pokud má SkipBroker hodnotu true (volitelné).|
    |*&lt;společné parametry&gt;*|(volitelné – podporuje společné parametry prostředí PowerShell jako podrobné nastavení, ladění atd.)<br /><br />Seznam společných parametrů najdete v [Centru skriptů Microsoftu](https://technet.microsoft.com/library/hh847884.aspx).|
    Pokud chcete zobrazit nápovědu k nástroji, zadejte příkaz:

    ```
    Help Invoke-AppWrappingTool
    ```
    Další informace o integraci služby Azure Active Directory (AAD) najdete [tady](https://technet.microsoft.com/library/dn878028.aspx).

    **Příklad:**

    ```
    Import-Module "C:\Program Files (x86)\Microsoft Intune Mobile Application Management\Android\App Wrapping Tool\IntuneAppWrappingTool.psm1" Invoke-AppWrappingTool –InputPath <input-app.apk> -OutputPath <output-app.apk> -KeyStorePath <path-to-signing.keystore> -KeyAlias <signing-key-name> -ClientID <xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx> -AuthorityURI <http://AzureActivieDirectory.Authority.URL> -SkipBroker<$True|$False> -NonBrokerRedirectURI <urn:xxx:xx:xxxx:xx:xxx>
    ```
    Pak se zobrazí výzva k zadání parametrů **KeyStorePassword** a **KeyPassword**.

Zabalená aplikace se generuje a uloží se souborem protokolu do zadané výstupní cesty.

## <a name="BKMK_androidappwraptool"></a>Důležité informace o zabezpečení při spuštění nástroje pro zabalení aplikace
Pro zabránění potenciálnímu falšování identity, zpřístupnění informací a zvýšení oprávnění pro útoky zajistěte toto:

-   Vstupní obchodní aplikace, výstupní aplikace a Java KeyStore musí být ve stejném počítači, na kterém je spuštěný nástroj pro zabalení aplikace.

-   Importujte výstupní aplikaci do konzoly Intune na stejném počítači, na kterém je nástroj spuštěný.

-   Pokud jsou výstupní aplikace a nástroj v cestě Universal Naming Convention (UNC) a nespustíte nástroj a vstupní soubory na stejném počítači, nakonfigurujte prostředí tak, aby bylo zabezpečené, pomocí protokolů [Internet Protocol Security (IPsec)](http://en.wikipedia.org/wiki/IPsec) nebo [podepsání protokolu Server Message Block (SMB)](https://support.microsoft.com/en-us/kb/887429).

-   Ujistěte se, jestli aplikace pochází z důvěryhodného zdroje, zvlášť pokud používáte službu Azure Active Directory (AAD), která může aplikaci umožnit přístup k tokenu AAD v běhovém prostředí.

-   Zabezpečte výstupní adresář, který obsahuje zabalenou aplikaci. Zvažte použití adresáře na úrovni uživatele pro výstup.

## <a name="BKMK_ADAL_android"></a>Postup při zabalení aplikací, které používají knihovnu Azure Active Directory Library (ADAL)
Jestli vaše aplikace používá knihovnu Azure Active Directory Authentication Library (ADAL), musíte před zabalením aplikace dokončit tyto kroky.

### Krok 1: Ověření, že splňujete požadavky pro ADAL
Pro aplikace, které používají ADAL, musí platit následující:

-   Aplikace musí mít verzi ADAL větší nebo rovnou hodnotě 1.0.2.

-   Vývojář musí [grant their app access to the Intune Mobile Application Management resource](../Topic/Prepare_iOS_apps_for_mobile_application_management_with_the_Microsoft_Intune_App_Wrapping_Tool.md#BKMK_AD).

### <a name="BKMK_review_IDs"></a>Krok 2: Kontrola identifikátorů, které potřebujete získat při registraci aplikace
V dalším kroku použijete portál pro správu Azure k registraci aplikací (které používají ADAL se službou Azure Active Directory (AAD)) a k získání jedinečných identifikátorů uvedených v následující tabulce. Identifikátory pak předáte vývojářům při integraci knihovny ADAL s aplikací. Další informace o hodnotách těchto identifikátorů najdete v tématu [Knihovna Microsoft Azure Active Directory Authentication Library (ADAL) pro Android](https://github.com/AzureAD/azure-activedirectory-library-for-android/blob/master/README.md).

|Identifikátor|Další informace|Výchozí hodnota|
|-----------------|-------------------|-------------------|
|**ID klienta**|Jedinečný identifikátor GUID, který se vygeneruje pro aplikaci po dokončení registrace ve službě AAD.<br /><br />Pokud víte ID klienta aplikace, zadejte tuto hodnotu. Jinak použijte výchozí hodnotu.|6c7e8096-f593-4d72-807f-a5f86dcc9c77|
|**URI autority**|Hodnota URI (Uniform Resource Identifier) autority pro objekty AAD, například uživatele a skupiny.<br /><br />U nástroje pro zabalení aplikace je parametr AuthorityURI volitelný. Pokud tento parametr nepoužijete, použije se výchozí URI.|https://login.windows.net/common/|
|**SkipBroker**|Hodnota označující, jestli se portál společnosti použije jako zprostředkovatel.<br /><br />-   **True** – portál společnosti se nepoužije pro ověřování ADAL.<br />-   **False** – portál společnosti se použije pro ověřování ADAL. Portál společnosti používá registrovaného uživatele pro účely jednotného přihlašování.||
|**Identifikátor URI pro přesměrování bez zprostředkovatele**|Přihlašovací identifikátor URI, který se použije, když ADAL nepoužívá aplikaci zprostředkovatele (portál společnosti služby Intune).|urn:ietf:wg:oauth:2.0:oob|
|**ID prostředku**|Ukazatel na prostředky AAD aplikace.|https://intunemam.microsoftonline.com|

### <a name="BKMK_AD"></a>Krok 3: Konfigurace přístupu ke správě mobilních aplikací v AAD
Než budete moct v nástroji pro zabalení aplikace použít hodnoty registrace AAD aplikace, musí vývojář aplikace udělit této aplikaci přístup k prostředku správy mobilní aplikace Intune pomocí následujícího postupu:

1.  Přihlaste se k existujícímu účtu AAD na portálu pro správu Azure.

2.  Klikněte na **existující registraci aplikace LOB**.

3.  V části **konfigurace** zvolte **Konfigurovat přístup k webovým rozhraním API v ostatních aplikacích**.

4.  V prvním rozevíracím seznamu v části **Oprávnění k ostatním aplikacím** vyberte **Správa mobilní aplikace Intune**.

Teď můžete použít ID klienta aplikace v nástroji pro zabalení aplikace. ID klienta aplikace najdete na portálu pro správu Azure Active Directory podle popisu v tabulce v [Krok 2: Kontrola identifikátorů, které potřebujete získat při registraci aplikace](#BKMK_review_IDs).

### Krok 4: Použití hodnot identifikátoru AAD v nástroji App Wrapping
Použijte hodnoty identifikátorů, které jste získali při registraci, a v nástroji pro zabalení aplikace zadejte hodnoty jako vlastnosti příkazového řádku. Aby koncoví uživatelé mohli aplikaci úspěšně ověřit, musíte zadat všechny hodnoty v tabulce. Když nezadáte hodnotu, použijí se výchozí hodnoty.

|Identifikátor|Parametr|
|-----------------|------------|
|ID klienta|ClientID|
|URI autority|Authority-URI|
|SkipBroker|SkipBroker|
|Identifikátor URI pro přesměrování bez zprostředkovatele|NonBrokerRedirectURI|
|ID prostředku|ResourceID|
Při balení aplikace byste měli brát v úvahu následující pravidla:

-   Nástroj pro zabalení aplikace nehledá v aplikaci binární soubory ADAL (pokud existují). Pokud aplikace odkazuje na zastaralou verzi binárních souborů a jsou zapnuté zásady ověřování, můžou se během přihlašování objevit chyby za běhu.

-   Pro kontrolu, jestli ověření proběhlo úspěšně, [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] načte token AAD přidružený k MAM resource-id. Token se ale nepoužije v žádném volání, které by ověřilo jeho platnost.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] přečte jen hlavní název (UPN) přihlášeného uživatele a zjistí přístup k aplikaci. Token AAD se nepoužívá pro žádná další servisní volání.

-   Tokeny ověřování se sdílejí mezi aplikacemi od stejného vydavatele, protože jsou uložené ve sdíleném řetězci klíčů. Když chcete izolovat konkrétní aplikaci, použijte jiný podpisový certifikát, úložiště klíčů profilu zřizování a alias klíče pro tuto aplikaci.

-   Zadáním ID klienta a identifikátoru URI autority zabráníte zdvojení výzev k přihlášení. Přístup k publikovanému ID prostředku MAM v řídicím panelu AAD [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] vyžaduje registraci ID klienta. Když ID klienta nezaregistrujete, uživatelům při spuštění aplikace selže přihlašování.

## Další kroky
Další informace o tom, jak nasadit zabalené aplikace, najdete v tématu [Nasazení aplikací do mobilních zařízení v Microsoft Intune](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune_-_deleted.md).

## Viz také
[Ochrana dat pomocí zásad správy mobilních aplikací v Microsoft Intune](../Topic/Configure_and_deploy_mobile_application_management_policies_in_the_Microsoft_Intune_console.md)

