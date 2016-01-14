---
description: na
keywords: na
title: Ways to do enterprise mobility
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2d91b8b5-bf44-4562-ab4a-6611584f9674
---
# Způsoby zajištěn&#237; podnikov&#233; mobility
Microsoft poskytuje několik možností pro správu vašich mobilních zařízení. Informace na této stránce vám pomůžou se mezi těmito možnostmi rozhodnout a zajistit tak potřeby vaší podnikové mobility:

-   [Volba mezi Intune a MDM pro Office 365](#BKMK_MDMOfferings)

-   [Můžete si zvolit mezi samostatným Intune nebo integrací Intune se System Center Configuration Managerem.](#BKMK_HybridOfferings)

## <a name="BKMK_MDMOfferings"></a>Volba mezi Intune a MDM pro Office 365

|Aspekty|MDM pro Office 365|[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]|
|-----------|----------------------|---------------------------------------------------------|
|Náklady|Je součástí mnoha [komerčních předplatných Office 365](http://products.office.com/business/enterprise-productivity-tools).|Vyžaduje [placené předplatné pro Microsoft Intune](http://www.microsoft.com/en-us/server-cloud/products/microsoft-intune/Purchasing.aspx) nebo se dá zakoupit se [sadou Enterprise Mobility](http://www.microsoft.com/en-us/server-cloud/products/enterprise-mobility-suite/Purchasing.aspx).|
|Jakým způsobem spravovat zařízení|Zařízení spravujte pomocí [Centra pro správu Office 365](https://support.office.com/article/About-the-Office-365-admin-center-58537702-d421-4d02-8141-e128e3703547).|Pokud [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] používáte samostatně, spravujete zařízení přes [konzolu správce služby Intune](https://technet.microsoft.com/library/dn646966.aspx).<br /><br />Pokud Intune integrujete se System Center 2012 Configuration Managerem, budete ke správě zařízení místně i v cloudu používat konzolu Configuration Manageru.|
|Zařízení, která můžete spravovat|Cloudová správa pro:<br /><br />-   iOS<br />-   Android<br />-   Windows Phone|Cloudová správa pro:<br /><br />-   iOS<br />-   Mac OS X<br />-   Android<br />-   Windows Phone<br />-   Počítače s Windows|
|Hlavní možnosti|-   Zajistíte přístup k podnikovým e-mailům a dokumentům Office 365 jedině z telefonů a tabletů, které spravuje vaše společnost a které vyhovují vašim IT zásadám.<br />-   Můžete nastavovat a spravovat zásady zabezpečení, jako je například zamknutí PIN kódem na úrovni zařízení a zjištění jailbreaku na zařízení. To vám umožní zabránit neoprávněným uživatelům v přístupu k podnikovému e-mailu a k datům v zařízení v případě jeho ztráty nebo odcizení.<br />-   Ze zařízení zaměstnance můžete odebrat data Office 365 společnosti a nechat v něm uložené osobní data.<br /><br />Nejnovější informace o možnostech Office 365 MDM najdete v článku o [schopnostech integrované správy mobilních zařízení pro Office 365](https://technet.microsoft.com/library/ms.o365.cc.devicepolicysupporteddevice.aspx).|Možnosti MDM pro Office 365 a navíc:<br /><br />-   Umožníte uživatelům zabezpečený přístup k podnikovým prostředkům pomocí certifikátů, Wi-Fi, sítě VPN a e-mailových profilů.<br />-   Můžete také registrovat a spravovat kolekce zařízení vlastněných podnikem, což výrazně zjednodušuje nasazování zásad a aplikací.<br />-   Nasadíte uživatelům interní podnikové aplikace a aplikace v obchodech s aplikacemi.<br />-   Zajistíte uživatelům zabezpečený přístup k podnikovým informacím pomocí mobilních aplikací Office a podnikových aplikací, které znají, a zároveň zajistíte zabezpečení dat omezením akcí typu *Kopírovat*, *Vyjmout*, *Vložit* a *Uložit jako* jenom na aplikace, které se spravují přes [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].<br />-   Umožníte zabezpečené procházení webu pomocí aplikace prohlížeče spravované přes [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].<br />-   Počítače PC můžete spravovat z cloudu pomocí [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] bez nutnosti infrastruktury, nebo [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] připojit k nástroji [!INCLUDE[cm5short](../Token/cm5short_md.md)] a spravovat všechna svoje zařízení včetně počítačů PC, Mac, Linux a UNIX serverů a mobilních zařízení z jedné konzoly pro správu.|
Od října 2015 můžou správci spravovat uživatele a jejich mobilní zařízení na stejném tenantovi pomocí Intune a Office 365 současně. Umožní vám to rozhodnout, které řešení je nejlepší pro konkrétní uživatele a jejich příslušná zařízení. Potom můžete určit, jestli se uživatel a jeho zařízení budou spravovat pomocí Office 365 MDM nebo funkčně bohatšího řešení správy Intune.

## <a name="BKMK_HybridOfferings"></a>Můžete si zvolit mezi samostatným Intune nebo integrací Intune se System Center Configuration Managerem.

|Samostatnou službu [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] si můžete vybrat v tomto případě:|Kombinaci [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] + Configuration Manager si můžete vybrat, pokud:|
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
|-   Chcete spravovat mobilní zařízení.<br />-   Chcete spravovat počítače, které nejsou připojené k doméně.<br />-   Spravujete míň než 50 000 zařízení.<br />-   Nemáte žádnou místní infrastrukturu IT (nebo jenom omezenou). **Note:**     [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] nevyžaduje místní infrastrukturu IT, ale může využívat možnosti Exchange ActiveSync nebo Active Directory Domain Services, pokud je máte nainstalované.<br />-   Máte mobilní nebo hodně rozptýlenou síť pracovníků. Cloudová správa zařízení vám umožňuje spravovat mobilní zařízení a počítače kdekoliv na světě.|-   Chcete spravovat počítače, které jsou připojené k doméně.<br />-   Chcete spravovat servery.<br />-   Chcete z jedné konzoly spravovat počítače s klientem Configuration Manageru, počítače Mac, Linux a UNIX servery a mobilní zařízení zaregistrovaná přes Intune.<br />-   Spravujete víc než 50 000 zařízení.<br />-   Používáte místní infrastrukturu IT nebo se chystáte takovou infrastrukturu nasadit. Při této konfiguraci je správa zařízení a prostředků naprosto jednotná.<br />-   Uživatelská jména a hesla jsou synchronizovaná a zároveň uživatelům poskytují jeden účet používaný pro přístup k podnikovým prostředkům, ať už z počítače připojeného k doméně, nebo z mobilního zařízení.|

### Podrobné porovnání možností
V následující tabulce najdete porovnání možností správy zařízení a aplikací dostupných při používání samostatného [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], samostatného Configuration Manageru nebo řešení, které využívá oba produkty.

Další informace o používání nástroje Configuration Manager s [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] najdete v tématu [Správa mobilních zařízení s Configuration Managerem](http://msdn.microsoft.com/en-us/library/2c6bd0e5-d436-41c8-bf38-30152d76be10).

#### Podpora zařízení

|Platforma|[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]|System Center 2012 Configuration Manager SP2|System Center 2012 Configuration Manager SP2 a [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]|
|-------------|---------------------------------------------------------|------------------------------------------------|------------------------------------------------------------------------------------------------------|
|Microsoft Windows|Ano|Ano|Ano|
|Microsoft Windows Server|Ne|Ano|Ano|
|Windows Phone|Ano|Ne|Ano|
|Windows RT|Ano|Ne|Ano|
|iOS|Ano|Ne|Ano|
|Android a Samsung KNOX|Ano|Ne|Ano|
|Mac OS X|Ano|Ano|Ano|
|Servery Unix/Linux|Ne|Ano|Ano|

#### Možnosti produktu
> [!TIP]
> Tam, kde je vyznačené (R2), vyžadují uvedené možnosti Microsoft System Center 2012 R2 Configuration Manager nebo novější.

|Scénář|[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]|System Center 2012 Configuration Manager SP2|System Center 2012 Configuration Manager SP2 a [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]|
|----------|---------------------------------------------------------|------------------------------------------------|------------------------------------------------------------------------------------------------------|
|**Nastavení dodržování předpisů**||||
|Nasazení a přizpůsobení nastavení konfigurace počítače s Windows (např. WMI, registr)|Ne|Ano|Ano|
|Nasazení a přizpůsobení nastavení konfigurace Mac OS X|Ano|Ano|Ano|
|Nasazení nastavení konfigurace do mobilních zařízení|Ano|Ano|Ano|
|Nasazení vlastních nastavení mobilních zařízení (například OMA-URI a Apple Configurator)|Ano|Ano|Ano|
|**Nasazení**||||
|Nasazení aplikací do zařízení a počítačů s Windows|Ano|Ano|Ano|
|Nasazení operačních systémů Windows|Ne|Ano|Ano|
|**Bezpečnost a soukromí**||||
|Správa aktualizací softwaru Windows|Ano|Ano|Ano|
|Monitorování malwaru v počítačích s Windows pomocí Endpoint Protection|Ano|Ano|Ano|
|**Správa a vytváření sestav**||||
|Monitorování a hlášení četnosti použití softwaru pomocí monitorování míry využití softwaru|Ne|Ano|Ano|
|Inventář hardwaru a softwaru|Ano|Ano|Ano|
|Rozšíření inventáře hardwaru a softwaru pro počítače s Windows|Ne|Ano|Ano|
|Použití správy a vytváření sestav podle rolí k řízení, kdo má přístup k možnostem produktu|Ne|Ano|Ano|
|Spouštění sestav pro počítače s Windows a zaregistrovaná mobilní zařízení z jedné konzoly|Ne|Ne|Ano|
|Přizpůsobení stávajících sestav a psaní vlastních sestav pomocí služby SQL Server Reporting Services|Ne|Ano|Ano|
|**Ochrana dat pro mobilní zařízení**||||
|Nasazení nastavení zabezpečení do mobilních zařízení|Ano|Ano|Ano|
|Vzdálené vymazání|Ano|Ano|Ano|
|Vzdálené uzamčení|Ano|Ano|Ano|
|Resetování hesla|Ano|Ano|Ano|
|**Přístup k prostředkům společnosti**||||
|E-mailové profily|Ano|Ano (R2)|Ano (R2)|
|Profily sítě Wi-Fi|Ano|Ano (R2)|Ano (R2)|
|Profily sítě VPN|Ano|Ano (R2)|Ano (R2)|
|Profily certifikátů|Ano|Ano (R2)|Ano (R2)|
|Správa přístupu k e-mailu Exchange a SharePointu s podmíněným přístupem|Ano|Ano|Ano|
|Správa mobilních aplikací|Ano|Ano|Ano|
|Zásady dodržování předpisů pro aplikace (vyhovující a nevyhovující aplikace)|Ano|Ano|Ano|
|Celoobrazovkový režim|Ano|Ano|Ano|
|Zásady spravovaného internetového prohlížeče|Ano|Ano|Ano|
|**Automation**||||
|Použití PowerShellu k automatizaci operací|Ne|Ano|Ano|

## Viz také
[Úvod do Microsoft Intune](../Topic/Introduction_to_Microsoft_Intune.md)

