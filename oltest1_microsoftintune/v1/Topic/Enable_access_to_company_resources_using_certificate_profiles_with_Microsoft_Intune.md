---
description: na
keywords: na
title: Enable access to company resources using certificate profiles with Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8cbb8499-611d-4217-a7b4-e9b864785dd0
---
# Povolen&#237; př&#237;stupu k firemn&#237;m prostředkům pomoc&#237; profilů certifik&#225;tů v Microsoft Intune
Profily certifikátů jsou zásady [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] sloužící ke konfiguraci spravovaných zařízení s certifikáty, které potřebují, aby se uživatelé zařízení mohli připojit k místním firemním prostředkům pomocí připojení, jako jsou sítě Wi-Fi nebo virtuální privátní sítě (VPN). Když nasadíte profily certifikátů, zřídíte pro zařízení důvěryhodný kořenový certifikát pro infrastrukturu veřejných klíčů a nakonfigurujete je, aby vyžadovala certifikáty pro konkrétní zařízení.

Můžete vytvořit tři typy profilů certifikátů:

-   Profil certifikátů PKCS #12 (.PFX): Tento typ můžete používat s Androidem 4.0 nebo novějším a se systémem Windows 10 (v desktopové i mobilní verzi) a novějším.

-   Profil certifikátu SCEP: Je možné používat s iOS 6.0 a novějším, Androidem 4.0 nebo novějším a s Windows Phonem 8.1 a novějším.

-   Profil důvěryhodného certifikátu: Je možné používat s iOS 6.0 a novějším, Androidem 4.0 nebo novějším a s Windows Phonem 8.1 a novějším.

|O profilech certifikátů|Podrobnosti|
|---------------------------|---------------|
|Využití profilů certifikátů:|-   Automaticky konfigurujte zařízení tak, aby se k firemním prostředkům dalo přistupovat bez nutnosti ruční instalace certifikátů nebo pomocí přístupu mimo IP síť.<br />-   Pomozte zabezpečit firemní prostředky pomocí vaší podnikové infrastruktury veřejných klíčů (PKI).<br />-   Umožňují vám používat ověřování serveru pro všechna připojení jako Wi-Fi a VPN, protože na spravovaných zařízeních máte zřízené požadované certifikáty.|
|Profily certifikátů nabízejí následující možnosti správy:|<ul><li>Zápisy a obnovení certifikátů z certifikační autority (CA) organizace pro zařízení s těmito platformami:<br /><br /><ul><li>Android</li><li>iOS</li><li>Windows 8.1</li><li>Windows Phone 8.1</li></ul></li></ul>Tyto certifikáty pak jde použít pro připojení k naší místní infrastruktuře.<br /><br />-   Nasazení certifikátů důvěryhodné kořenové certifikační autority a certifikátů zprostředkující certifikační autority ke konfiguraci řetězu certifikátů u zařízení pro připojení, která vyžadují ověření serveru.<br />-   Monitorování a vytváření sestav s informacemi o instalovaných certifikátech.|
|Příklady použití profilů certifikátů:|-   Zaměstnanci musí mít možnost připojení k Wi-Fi hotspotům v různých sídlech společnosti. To můžete provést tak, že pomocí profilů certifikátů nasadíte certifikáty požadované pro zabezpečení připojení Wi-Fi.<br />-   Máte vytvořenou infrastrukturu PKI a chcete přejít na flexibilnější a bezpečnější metodu zajišťování certifikátů, která umožní uživatelům přístup k prostředkům společnosti z jejich osobních zařízení, aniž by tím bylo narušeno zabezpečení. Za tím účelem můžete konfigurovat profily certifikátů obsahující nastavení a protokoly podporované určitými platformami zařízení. Zařízení si pak mohou tyto certifikáty automaticky vyžádat ze serveru zápisu, který je připojen k Internetu. Následně můžete konfigurovat profily VPN, aby používaly tyto certifikáty, a umožnit tak přístup k prostředkům společnosti ze zařízení.|

|Typy profilů certifikátů|Podrobnosti|
|----------------------------|---------------|
|**Profil důvěryhodný kořenový certifikát**|Pomocí tohoto profilu můžete nasadit certifikát důvěryhodné kořenové certifikační autority nebo certifikát zprostředkující certifikační autority do zařízení:<br /><br />-   Vytvořte profil důvěryhodný kořenový certifikát pro každou platformu, kterou používáte. Ten spárujete s každým profilem certifikátu SCEP, který vytvoříte pro stejnou platformu.|
|**Profil certifikátu .PFX**|Pomocí tohoto profilu nasaďte nastavení konkrétní platformy pro požadavky certifikátů zařízení:<br /><br />-   Vytvořte profil certifikátu .PFX pro každou platformu, kterou používáte, a spárujte ho s profilem certifikátu důvěryhodné certifikační autority.<br />-   K dokončení úlohy vytvoření profilu certifikátu .PFX musíte zvolit dříve vytvořený profil certifikátu důvěryhodné certifikační autority.|
|**Profil nastavení protokolu SCEP (Simple Certificate Enrollment Protocol)**|Pomocí tohoto profilu nasaďte nastavení konkrétní platformy pro požadavky certifikátů zařízení:<br /><br />-   Vytvořte profil certifikátu SCEP pro každou platformu, kterou používáte, a spárujte ho s profilem certifikátu důvěryhodné certifikační autority.<br />-   K dokončení úlohy vytvoření profilu certifikátu SCEP musíte zvolit dříve vytvořený profil certifikátu důvěryhodné certifikační autority.|
Pokud chcete použít profily certifikátů SCEP, musíte integrovat následující místní infrastrukturu s [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]:

-   Server, na kterém běží služba zápisu síťových zařízení

-   Certifikační autorita organizace

-   Intune Certificate Connector, který se instaluje na Windows Server 2012 R2, na kterém běží NDES

Pokud chcete použít profily certifikátů .PFX, musíte integrovat následující místní infrastrukturu s [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]:

-   Certifikační autorita organizace

-   Počítač, který může komunikovat s certifikační autoritou, nebo použijte přímo počítač certifikační autority.

-   Intune Certificate Connector běžící na počítači, který může komunikovat se službou certifikační autority

V tomto tématu:

-   [Požadavky na profily certifikátů](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md#BKMK_CertProfileRequirements)

-   [Konfigurace infrastruktury](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md#BKMK_ConfigureInfrastructure)

-   [Konfigurace profilů certifikátů](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md#BKMK_ConfigProfiles)

-   [Nasazení profilů certifikátů](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md#BKMK_Deploy)

## <a name="BKMK_CertProfileRequirements"></a>Požadavky na profily certifikátů

### <a name="BKMK_OnPremises"></a>Místní infrastruktura

|Infrastruktura|Podrobnosti|
|------------------|---------------|
|**Doména služby Active Directory**|Všechny servery uvedené v této části (s výjimkou proxy serveru webové aplikace) musí být připojené k vaší doméně služby Active Directory.|
|**Server certifikační autority**|Označuje se jako vydávající certifikační autorita. Musíte mít certifikační autoritu organizace, která běží na verzi Enterprise systému [!INCLUDE[nextref_server_7](../Token/nextref_server_7_md.md)] nebo novějšího.<br /><br />-   Samostatná certifikační autorita není podporovaná.<br /><br />Návod, jak nastavit certifikační autoritu, najdete v tématu [Instalace certifikační autority](http://technet.microsoft.com/library/jj125375.aspx).<br /><br />Pokud certifikační autorita používá Windows Server 2008 R2, musíte [instalovat opravu hotfix z KB2483564](http://support.microsoft.com/kb/2483564/).|
|Jenom pro profily SCEP: **Server NDES**|Na serveru, na kterém běží [!INCLUDE[winblue_server_2](../Token/winblue_server_2_md.md)] nebo novější, musíte nastavit službu zápisu síťových zařízení (NDES):<br /><br />-   [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] nepodporuje používání služby zápisu síťových zařízení, pokud běží na serveru, na kterém běží taky certifikační autorita organizace.<br />-   Pokyny k tomu, jak konfigurovat [!INCLUDE[winblue_server_2](../Token/winblue_server_2_md.md)] k hostování služby zápisu síťových zařízení, najdete v tématu [Příručka ke Službě zápisu síťových zařízení](http://technet.microsoft.com/library/hh831498.aspx).|
|Jenom pro profil certifikátu .PFX: **Počítač, který může komunikovat s certifikační autoritou**|Můžete taky použít přímo počítač certifikační autority.|
|**Server proxy webové aplikace** (volitelné)|Jako server proxy webové aplikace (WAP) můžete použít server, na kterém běží [!INCLUDE[winblue_server_2](../Token/winblue_server_2_md.md)] nebo novější. Tato konfigurace:<br /><br />-   Umožňuje zařízením získat certifikáty pomocí připojení k internetu.<br />-   Je doporučeným zabezpečením v případě, že se zařízení připojují prostřednictvím internetu za účelem příjmu a obnovení certifikátů.<br /><br />Server, který je hostitelem WAP, [musí nainstalovat aktualizaci](http://blogs.technet.com/b/ems/archive/2014/12/11/hotfix-large-uri-request-in-web-application-proxy-on-windows-server-2012-r2.aspx) umožňující podporu dlouhých adres URL, které používá služba zápisu síťových zařízení. Tato aktualizace je součástí [kumulativní aktualizace z prosince 2014](http://support.microsoft.com/kb/3013769) nebo jde instalovat jednotlivě z [KB3011135](http://support.microsoft.com/kb/3011135).<br /><br />Server, který je hostitelem WAP, musí taky:<br /><br />-   Mít certifikát SSL, který odpovídá názvu publikovanému externím klientům.<br />-   Důvěřovat certifikátu SSL, který se používá na serveru NDES.<br /><br />Tyto certifikáty umožňují serveru WAP ukončit připojení protokolem SSL od klientů a vytvořit nové připojení SSL k serveru NDES.<br /><br />Informace o certifikátech pro WAP najdete v části **Plánování certifikátů** tématu [Plánování publikování aplikací pomocí serveru proxy webových aplikací](https://technet.microsoft.com/en-us/library/dn383650.aspx).<br /><br />Obecné informace o serverech WAP najdete v tématu [Práce se serverem proxy webových aplikací](http://technet.microsoft.com/library/dn584113.aspx).|
|**Microsoft Intune Certificate Connector**|Prostřednictvím konzoly pro správu [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] můžete stáhnout instalační program konektoru **Certificate Connector** (**ndesconnectorssetup.exe**). Pak můžete soubor **ndesconnectorssetup.exe** spustit na počítači, kde chcete konektor Certificate Connector nainstalovat. V případě profilů certifikátů .PFX nainstalujte Certificate Connector v počítači, který komunikuje s certifikační autoritou.|

### <a name="BKMK_CertsAndTemplates"></a>Certifikáty a šablony

|Objekt|Podrobnosti|
|----------|---------------|
|**Šablona certifikátu**|Tuto šablonu konfigurujete na své vydávající certifikační autoritě.|
|**Certifikát pro ověřování klientů**|Tento certifikát vyžádaný z vaší vydávající certifikační autority nebo veřejné certifikační autority nainstalujte na server NDES.|
|**Ověřovací certifikát serverů**|Tento certifikát SSL vyžádaný z vaší vydávající certifikační autority nebo veřejné certifikační autority nainstalujte a připojte ve službě IIS na serveru NDES.|
|**Certifikát důvěryhodné kořenové certifikační autority**|Ten exportujete jako soubor **.cer** z vydávající certifikační autority nebo jakéhokoli zařízení, které důvěřuje vydávající certifikační autoritě, a nasadíte ho do zařízení pomocí profilu certifikátu důvěryhodné certifikační autority.<br /><br />-   Použijete jeden certifikát důvěryhodné kořenové certifikační autority na každou platformu operačního systému a přidružíte ho ke každému profilu důvěryhodného kořenového certifikátu, který vytvoříte.<br />-   Pokud potřebujete, můžete vytvořit další certifikáty důvěryhodné kořenové certifikační autority. Můžete to třeba udělat, abyste vytvořili vztah důvěryhodnosti k certifikační autoritě, která podepisuje ověřovací certifikáty serverů pro vaše přístupové body Wi-Fi.|

### <a name="BKMK_Accounts"></a>Účty

|Název|Podrobnosti|
|---------|---------------|
|**Účet služby NDES**|Zadáte účet uživatele domény, který chcete použít jako účet služby NDES.|

## <a name="BKMK_ConfigureInfrastructure"></a>Konfigurace infrastruktury
Před konfigurací profilů certifikátů musíte provést následující úlohy, které vyžadují znalosti systému Windows Server 2012 R2 a služby AD CD (Active Directory Certificate Services):

**Úloha 1** – konfigurace šablon certifikátů v certifikační autoritě 
**Úloha 2** (jenom pro profil SCEP) – konfigurace požadavků na server NDES 
**Úloha 3** (jenom pro profil SCEP) – konfigurace NDES pro použití se službou [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] 
**Úloha 4** – povolení, instalace a konfigurace konektoru certifikátů služby Intune

### <a name="BKMK_ConfigOnPremTask1"></a>Úloha 1 – konfigurace šablon certifikátů v certifikační autoritě
V této úloze:

-   Vytvoříte účet služby NDES

    > [!NOTE]
    > K odvolání certifikátů vyžaduje účet služby NDES oprávnění *Vydávat a spravovat certifikáty* ke každé šabloně certifikátu používané profilem certifikátu.

-   Konfigurujete šablonu certifikátu pro NDES

-   Publikujete šablonu certifikátu pro NDES

##### Konfigurace certifikační autority

1.  Vytvořte účet uživatele domény, který chcete použít jako účet služby NDES. Tento účet zadáte při konfiguraci šablon ve vydávající certifikační autoritě před instalací a konfigurací NDES.

2.  Ve vydávající certifikační autoritě použijte modul snap-in Šablony certifikátů k vytvoření nové vlastní šablony nebo zkopírování existující šablony a následnému upravení existující šablony (jako je šablona Uživatel) pro použití s NDES.

    Šablona musí obsahovat následující konfigurace:

    -   Zadejte popisný **zobrazovaný název šablony**.

    -   Na kartě **Název subjektu** vyberte možnost **Dodán v žádosti**. (Zabezpečení je vynucené modulem zásad [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] pro NDES).

    -   Na kartě **Rozšíření** zkontrolujte, jestli **Popis zásad použití** obsahuje **Ověření klienta**.

        > [!IMPORTANT]
        > V případě šablon certifikátů iOS na kartě **Rozšíření** upravte **Použití klíče** a ujistěte se, že není vybraná možnost **Podpis je důkazem původu**.

    -   Na kartě **Zabezpečení** přidejte účet služby NDES a poskytněte šabloně oprávnění ke **čtení** a **zápisu**.

3.  Zkontrolujte **Období platnosti** na kartě **Obecné** šablony. Ve výchozím nastavení [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] používá hodnotu nakonfigurovanou v šabloně. Máte ale možnost konfigurovat, aby certifikační autorita žadateli umožňovala určit jinou hodnotu, kterou pak můžete nastavit v konzole pro správu [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Pokud chcete vždy používat hodnotu v šabloně, zbývající část tohoto kroku přeskočte.

    > [!IMPORTANT]
    > Platforma iOS vždy používá hodnotu nastavenou v šabloně bez ohledu na ostatní konfigurace, které provedete.

    Pokud chcete certifikační autoritu konfigurovat, aby žadateli umožňovala určit dobu platnosti, spusťte v certifikační autoritě následující příkazy:

    1.  **certutil - setreg Policy\EditFlags +EDITF_ATTRIBUTEENDDATE**

    2.  **net stop certsvc**

    3.  **net start certsvc**

4.  Ve vydávající certifikační autoritě použijte modul snap-in Certifikační autorita k publikování šablony certifikátu.

    1.  Vyberte uzel **Šablony certifikátů**, klikněte na **Akce**-&gt; **Nové** &gt; **Vystavovaná šablona certifikátu** a pak vyberte šablonu, kterou jste vytvořili v kroku 2.

    2.  Ověřte, že je šablona publikovaná, jejím zobrazením ve složce **Šablony certifikátů**.

5.  Pro profily .PFX: Na počítači certifikační autority (CA) zkontrolujte, že má počítač, který je hostitelem Certificate Connectoru, oprávnění k registraci, aby měl přístup k šabloně použité při vytváření profilu .PFX. Nastavte tato oprávnění na kartě **Zabezpečení** vlastností počítače certifikační autority.

### <a name="BKMK_ConfigOnPremTask2"></a>Úloha 2 (jenom profil SCEP) – Konfigurace požadavků na serveru NDES
V této úloze:

-   Přidáte NDES do Windows Serveru a konfigurujete službu IIS pro podporu NDES

-   Přidáte účet služby NDES do skupiny IIS_IUSR

-   Nastavíte hlavní název služby (SPN) pro účet služby NDES

##### Konfigurace požadavků pro server NDES

1.  Na serveru, který bude hostitelem NDES, se musíte přihlásit jako **Správce podnikové sítě** a potom pomocí [Průvodce přidáním rolí a funkcí](https://technet.microsoft.com/library/hh831809.aspx) instalovat NDES:

    1.  V průvodci vyberte možnost **Služba AD CS (Active Directory Certificate Services)**, abyste získali přístup ke službám rolí ve službě AD CS. Vyberte **Službu zápisu síťových zařízení**, zrušte zaškrtnutí políčka **Certifikační autorita** a pak dokončete průvodce.

        > [!TIP]
        > Na stránce průvodce **Průběh instalace** neklikejte na **Zavřít**. Místo toho klikněte na odkaz **Konfigurovat službu AD CS (Active Directory Certificate Services) na cílovém serveru**. Tím se otevře průvodce **Konfigurace služby AD CS**, který použijete pro další krok. Po otevření Konfigurace služby AD CS můžete zavřít Průvodce přidáním rolí a funkcí.

    2.  Když se na server přidá NDES, průvodce nainstaluje taky službu IIS. Ujistěte se, že má služba IIS následující konfigurace:

        -   **Webový Server** &gt; **Zabezpečení** &gt; **Filtrování požadavků**

        -   **Webový Server** &gt; **Vývoj aplikací** &gt; **ASP.NET 3.5**. Instalace technologie ASP.NET 3.5 nainstaluje rozhraní .NET Framework 3.5. Při instalaci rozhraní .NET Framework 3.5 nainstalujte základní **rozhraní .NET Framework 3.5** i **Aktivaci protokolem HTTP**.

        -   **Webový Server** &gt; **Vývoj aplikací** &gt; **ASP.NET 4.5**. Instalace technologie ASP.NET 4.5 nainstaluje rozhraní .NET Framework 4.5. Při instalaci rozhraní .NET Framework 4.5 nainstalujte základní **rozhraní .NET Framework 4.5**, **ASP.NET 4.5** a funkci **Služby WCF** &gt; **Aktivace protokolem HTTP**.

        -   **Nástroje pro správu** &gt; **Kompatibilita správy služby IIS 6** &gt; **Kompatibilita metabáze služby IIS 6**

        -   **Nástroje pro správu** &gt; **Kompatibilita správy služby IIS 6** &gt; **Kompatibilita metabáze služby IIS 6 WMI**

2.  Na serveru přidejte účet služby NDES jako člena skupiny **IIS_IUSR**.

3.  Spusťte následující příkaz pro nastavení hlavního názvu služby (SPN) účtu služby NDES:

    -   **setspn -s http/&lt;název DNS serveru NDES&gt; &lt;název_domény&gt;\&lt;název účtu služby NDES&gt;**

    Například pokud je název serveru NDES **Server01**, vaše doména je **Contoso.com** a účet služby je **NDESService**, použijte:

    -   **setspn – s http/Server01.contoso.com contoso\NDESService**

### <a name="BKMK_ConfigOnPremTask3"></a>Úloha 3 (jenom profil SCEP) – Konfigurace NDES pro použití s [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]
V této úloze:

-   Nakonfigurujete NDES pro použití s vydávající certifikační autoritou

-   Vytvoříte vazbu certifikátu serveru ověřování (SSL) ve službě IIS

-   Konfigurujete filtrování požadavků ve službě IIS

##### Konfigurace NDES pro použití se službou [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]

1.  Na serveru NDES otevřete průvodce Konfigurace služby AD CS a pak proveďte následující konfigurace.

    > [!TIP]
    > Pokud jste klikli na odkaz v předchozí úloze, je už tento průvodce otevřený. Jinak spusťte Správce serveru, abyste získali přístup ke konfiguraci po nasazení pro službu AD CS (Active Directory Certificate Services).

    -   Na stránce **Služby rolí** vyberte **Služba zápisu síťových zařízení**.

    -   Na stránce **Účet Služby zápisu síťových zařízení** zadejte účet služby NDES.

    -   Na stránce **Certifikační autorita pro Službu zápisu síťových zařízení** klikněte na **Vybrat** a pak vyberte vydávající certifikační autoritu, kam jste nakonfigurovali šablonu certifikátu.

    -   Na stránce **Kryptografie pro Službu zápisu síťových zařízení** nastavte délku klíče podle požadavků vaší společnosti.

    Na stránce **Potvrzení** klikněte na **Konfigurovat** a dokončete průvodce.

2.  Po dokončení průvodce upravte následující klíč registru na serveru NDES:

    -   **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Cryptography\MSCEP\**

    Pokud tento klíč chcete upravit, identifikujte **Účel** šablony certifikátu, jak je uvedený na kartě **Vyřízení žádosti**, a pak upravte odpovídající položku v registru nahrazením stávajících dat názvem šablony certifikátu (ne zobrazovaným názvem šablony), který jste zadali v úloze 1. Následující tabulka mapuje účel šablony certifikátu na hodnoty v registru:

    |Účel šablony certifikátu (na kartě Vyřízení žádosti)|Upravovaná hodnota registru|Hodnota zobrazená v konzole pro správu [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] pro profil SCEP|
    |--------------------------------------------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------|
    |-   Podpis|-   SignatureTemplate|-   Digitální podpis|
    |-   Šifrování|-   EncryptionTemplate|-   Šifrování klíče|
    |-   Podpis a šifrování|-   GeneralPurposeTemplate|-   Šifrování klíče<br />-   Digitální podpis|
    Pokud je třeba účelem šablony certifikátu **Šifrování**, pak upravte hodnotu **EncryptionTemplate**, aby byla názvem vaší šablony certifikátu.

3.  Po úpravě registru spusťte na serveru **iisreset**, abyste server přinutili načíst nedávné změny konfigurace.

##### Instalace a vytvoření vazby certifikátů na serveru NDES

1.  Na serveru NDES vyžádejte a nainstalujte **ověřovací certifikát serveru** z vaší interní nebo veřejné certifikační autority. Pro tento certifikát SSL pak vytvoříte vazbu ve službě IIS.

    > [!TIP]
    > Po vytvoření vazby certifikátu SSL ve službě IIS nainstalujete taky certifikát pro ověřování klientů. Tento certifikát může být vydaný certifikační autoritou, která je důvěryhodná pro server NDES. I když se nejedná o osvědčený postup, můžete použít stejný certifikát pro ověřování serverů i klientů, pokud má obě rozšířená použití klíče (EKU). Informace o těchto ověřovacích certifikátech najdete v následujících krocích.

    1.  Po obdržení ověřovacího certifikátu serverů otevřete **Správce služby IIS**, vyberte **Výchozí webový server** v podokně **Připojení** a pak klikněte na **Vazby** v podokně **Akce**.

    2.  Klikněte na **Přidat**, nastavte **Typ** na **https** a pak se ujistěte, že port je **443**. (Pro samostatnou službu [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] je podporovaný jenom port 443).

    3.  Jako **Certifikát SSL** zadejte ověřovací certifikát serverů.

        > [!NOTE]
        > Pokud server NDES používá externí i interní název pro jednu síťovou adresu, musí mít ověřovací certifikát serverů **Název subjektu** s názvem externího veřejného serveru a **Alternativní název subjektu**, který obsahuje název interního serveru.

2.  Na serveru NDES vyžádejte a nainstalujte certifikát pro **ověřování klientů** z vaší interní certifikační autority nebo z veřejné certifikační autority. Může to být stejný certifikát jako ověřovací certifikát serverů, pokud má tento certifikát obě schopnosti.

    Certifikát pro ověřování klientů musí mít následující vlastnosti:

    -   **Rozšířené použití klíče** – musí obsahovat **Ověření klienta**.

    -   **Název subjektu** – musí být stejný jako název DNS serveru, na který instalujete certifikát (server NDES).

##### Konfigurace filtrování požadavků služby IIS

1.  Na serveru NDES otevřete **Správce služby IIS**, vyberte **Výchozí webový server** v podokně **Připojení** a pak otevřete **Filtrování požadavků**.

2.  Klikněte na **Upravit nastavení funkce** a pak nastavte tohle:

    -   **řetězec dotazu (bajty)** = **65534**

    -   **Maximální délka adresy URL (bajty)** = **65534**

3.  Zkontrolujte následující klíč registru:

    -   **HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\Services\HTTP\Parameters**

    Ujistěte se, že následující hodnoty jsou nastavené jako položky DWORD:

    -   Název: **MaxFieldLength**, s desetinnou hodnotou **65534**

    -   Název: **MaxRequestBytes**, s desetinnou hodnotou **65534**

4.  Restartujte server NDES. Server je teď připravený na podporu konektoru Certificate Connector.

### <a name="BKMK_ConfigOnPremTask4"></a>Úloha 4 – Povolení, instalace a konfigurace Intune Certificate Connectoru – pro certifikáty SCEP a .PFX
V této úloze:

-   Povolíte podporu NDES ve službě [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]

-   Stáhnete, nainstalujete a nakonfigurujete konektor Certificate Connector na serveru NDES.

##### Povolení podpory pro Certificate Connector

1.  Otevřete [konzolu pro správu služby Intune](https://manage.microsoft.com), klikněte na **Správce** &gt; **Certificate Connector**.

2.  Klikněte na **Konfigurace místního Certificate Connectoru**.

3.  Vyberte **Zapnout Certificate Connector** a potom klikněte na **OK**.

##### Stažení, instalace a konfigurace konektoru Certificate Connector

1.  Otevřete [konzolu pro správu služby Intune](https://manage.microsoft.com) a potom klikněte na **Správce** &gt; **Správa mobilních zařízení** &gt; **Certificate Connector** &gt; **Stáhnout Certificate Connector**.

2.  Po dokončení stahování spusťte stažený instalační program (**ndesconnectorssetup.exe**):

    -   Pro certifikáty .PFX spusťte instalační program na počítači, který se bude moct připojit k certifikační autoritě. Zvolte distribuci .PFX a klikněte na Nainstalovat. Po dokončení instalace pokračujte vytvoření profilu certifikátu.

    -   Pro certifikáty SCEP spusťte instalační program na Windows Serveru 2012 R2.

    Pro možnost SCEP instalační program nainstaluje také modul zásad pro NDES a webovou službu CRP. (Webová služba CRP, CertificateRegistrationSvc, běží ve službě ve službě IIS jako aplikace).

    > [!NOTE]
    > Při instalaci NDES pro samostatnou službu [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] se služba CRP automaticky nainstaluje s konektorem Certificate Connector. Při použití služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] se Správcem konfigurace nainstalujete bod registrace certifikátu (CRP) jako samostatnou roli serveru.

3.  Pokud budete vyzváni k zadání klientského certifikátu pro konektor Certificate Connector, klikněte na **Vybrat** a vyberte certifikát pro **ověřování klientů**, který jste nainstalovali na server NDES v úloze 3.

    Po vybrání certifikátu pro ověřování klientů se vrátíte na plochu **Klientský certifikát pro konektor Certificate Connector služby Microsoft Intune**. I když vybraný certifikát není zobrazený, kliknutím na **Další** zobrazte vlastnosti certifikátu. Pak klikněte na **Další** a pak klikněte na **Nainstalovat**.

4.  Po dokončení průvodce klikněte před jeho zavřením na **Spustit uživatelské rozhraní konektoru Certificate Connector**.

    > [!TIP]
    > Pokud průvodce zavřete před spuštěním uživatelského rozhraní konektoru Certificate Connector, můžete ho znovu otevřít spuštěním následujícího příkazu:
    > 
    > -   **&lt;instalační_cesta&gt;\NDESConnectorUI\NDESConnectorUI.exe**

5.  V uživatelském rozhraní **Certificate Connectoru** :

    -   Klikněte na **Přihlásit** a zadejte své přihlašovací údaje správce služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] nebo přihlašovací údaje správce klienta s oprávněním pro globální správu.

    -   Pokud vaše organizace používá proxy server a ten je vyžadovaný pro přístup serveru NDES přístup k internetu, klikněte na **Použít proxy server** a pak zadejte název proxy serveru, port a přihlašovací údaje účtu pro připojení.

    -   Vyberte kartu **Upřesnit** a pak zadejte přihlašovací údaje pro účet, který má oprávnění **Vydávat a spravovat certifikáty** ve vaší vydávající certifikační autoritě, a pak klikněte na **Použít**.

    Teď můžete zavřít uživatelského rozhraní Certificate Connectoru.

6.  Otevřete příkazový řádek a zadejte **services.msc** a pak stiskněte **Enter**, klikněte pravým tlačítkem na **službu konektoru Certificate Connector** a pak klikněte na **Restartovat**.

Pokud chcete ověřit, jestli je služba spuštěná, spusťte prohlížeč a zadejte následující adresu URL, která by měla vrátit chybu **403**:

-   **http:// &lt;FQDN_serveru_NDES&gt;/certsrv/mscep/mscep.dll**

Teď jste připravení konfigurovat profily certifikátů.

## <a name="BKMK_ConfigProfiles"></a>Konfigurace profilů certifikátů
Po konfiguraci infrastruktury a certifikátů můžete konfigurovat profily certifikátů:

**Úloha 1** – Export certifikátu důvěryhodné kořenové certifikační autority 
**Úloha 2** – Vytvoření profilů certifikátů důvěryhodné certifikační autority 
**Úloha 3** – Jedna ze dvou možností:

-   Vytvoření profilů certifikátů SCEP

-   Vytvoření profilů certifikátů .PFX

### <a name="BKMK_ConfigExportRootCA"></a>Úloha 1 – export certifikátu důvěryhodné kořenové certifikační autority
Exportujte certifikát důvěryhodné kořenové certifikační autority jako soubor **.cer** z vydávající certifikační autority nebo jakéhokoli zařízení, které vaší vydávající certifikační agentuře důvěřuje. Privátní klíč neexportujete.

Tento certifikát budete importovat při konfiguraci profilu certifikátu důvěryhodné certifikační autority.

### <a name="BKMK_ConfigRootCA"></a>Úloha 2 – vytvoření profilů certifikátů důvěryhodné certifikační autority
**Profil certifikátu důvěryhodné certifikační autority** musíte vytvořit před vytvořením **profilu nastavení protokolu SCEP (Simple Certificate Enrollment Protocol)**. Oba profily jsou požadované pro každou platformu mobilního zařízení.

##### Vytvoření profilu důvěryhodného certifikátu

1.  Otevřete [konzolu pro správu služby Intune](https://manage.microsoft.com) a klikněte na **Zásady** &gt; **Přidat zásadu**.

2.  Nakonfigurujte jeden z následujících typů zásad:

    -   **Android &gt; profil důvěryhodného certifikátu (Android 4 a novější)**

    -   **iOS &gt; Profil důvěryhodného certifikátu (iOS 5 a novější)**

    -   **Windows Phone a zaregistrovaná zařízení Windows &gt; profil důvěryhodného certifikátu (Windows 8.1 a novější)**

    -   **Windows Phone a zaregistrovaná zařízení Windows &gt; profil důvěryhodného certifikátu (Windows 8.1 a novější)**

    Další informace: [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

3.  Pomocí těchto informací konfigurujte nastavení profilu důvěryhodného certifikátu pro Android, iOS, Windows 8.1 nebo Windows Phone 8.1:

    |Název nastavení|Platforma|Další informace|
    |-------------------|-------------|-------------------|
    |**Název**|Všechny|Zadejte popisný název profilu certifikátu.|
    |**Popis**|Všechny|Zadejte volitelný popis certifikátu.|
    |**Soubor certifikátu**|Všechny|Klikněte na **Import** a pak vyberte certifikát důvěryhodné kořenové certifikační autority (**.cer**), který jste exportovali z vydávající certifikační autority.|
    |**Cílové úložiště**|Windows 8.1|U zařízení, která mají víc úložišť certifikátů, určete, kam se má certifikát uložit. Vyberte z těchto možností:<br /><br />-   **Úložiště certifikátů počítače – kořenové**<br />-   **Úložiště certifikátů počítače – zprostředkující**<br />-   **Úložiště certifikátů uživatele – zprostředkující**<br /><br />U zařízení, která mají jenom jedno úložiště, se toto nastavení bude ignorovat.|

4.  Po dokončení klikněte na **Uložit zásadu**.

Nové zásady se zobrazí v pracovním prostoru **Zásady** a můžete je teď nasadit.

### <a name="BKMK_ConfigSCEP"></a>Úloha 3 – Vytvoření profilů certifikátů SCEP nebo .PFX
Po vytvoření profilu certifikátu důvěryhodné certifikační autority vytvořte profily certifikátů SCEP nebo .PFX pro každou platformu, kterou chcete použít. Při vytváření profilu certifikátu SCEP musíte zadat profil certifikátu důvěryhodné certifikační autority pro stejnou platformu. Tím se oba profily certifikátů propojí, i když každý profil musíte nasadit samostatně.

##### Vytvoření profilu certifikátu SCEP

1.  Otevřete [konzolu pro správu služby Intune](https://manage.microsoft.com), klikněte na **Zásady** &gt; **Přidat zásadu**.

2.  Nakonfigurujte jeden z následujících typů zásad:

    -   **Android &gt; Profil certifikátu SCEP (Android 4 a novější)**

    -   **iOS &gt; Profil certifikátu SCEP (iOS 5 a novější)**

    -   **Windows Phone a zaregistrovaná zařízení Windows &gt; profil certifikátu SCEP (Windows 8.1 a novější)**

    -   **Windows Phone a zaregistrovaná zařízení Windows &gt; profil certifikátu SCEP (Windows Phone 8.1 a novější)**

    Další informace: [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

3.  Pomocí těchto informací konfigurujte nastavení profilu certifikátu SCEP pro Android, iOS, Windows 8.1 a Windows Phone 8.1:

    |Název nastavení|Platforma|Další informace|
    |-------------------|-------------|-------------------|
    |**Název**|Všechny|Zadejte popisný název profilu certifikátu.|
    |**Popis**|Všechny|Zadejte volitelný popis certifikátu.|
    |**Prahová hodnota obnovení (%)**|Všechny|Zadejte procento životnosti certifikátu zbývající v okamžiku, kdy zařízení požádá o obnovení certifikátu.|
    |**Zprostředkovatel úložiště klíčů**|Android <br />Windows 8.1 <br />Windows Phone 8.1|Určete, kam se má uložit klíč k certifikátu. Vyberte jednu z následujících možností:<br /><br />-   **Instalovat do čipu TPM (Trusted Platform Module), pokud je k dispozici** – nainstaluje klíč do čipu TPM. Pokud čip TPM neexistuje, nainstaluje se klíč do poskytovatele úložiště klíčů pro software.<br />-   **Instalovat do čipu TPM (Trusted Platform Module), jinak selhání** – nainstaluje klíč do čipu TPM. Pokud čip TPM neexistuje, instalace se nezdaří.<br />-   **Instalovat do zprostředkovatele úložiště klíčů pro software** – nainstaluje klíč do zprostředkovatele úložiště klíčů pro software.|
    |**Adresa URL serveru SCEP**|Všechny|Zadejte adresu URL (s předponou **http://** nebo **https://**) a pak klikněte na **Přidat** nebo vyberte adresu URL a pak klikněte na **Odstranit**.<br /><br />Adresa URL serveru SCEP třeba může vypadat takto: **https://mdmndes1.contoso.com/certsrv/mscep/mscep.dll**<br /><br />Každý profil SCEP podporuje jednu adresu URL serveru SCEP.|
    |**Formát názvu subjektu**|Android <br />Windows 8.1 <br />Windows Phone 8.1|Ze seznamu vyberte způsob, jak má nástroj [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] automaticky vytvořit název subjektu v žádosti o certifikát. Pokud je certifikát určený pro uživatele, můžete do názvu subjektu zahrnout taky e-mailovou adresu uživatele.<br /><br />Můžete vybrat **Běžné jméno** nebo **Běžné jméno a e-mailovou adresu**.|
    |**Alternativní název subjektu**|Všechny|Vyberte **E-mailovou adresu**, **Hlavní název uživatele (UPN)** nebo obojí.|
    |**Období platnosti certifikátu**|Všechny|Zadejte dobu, než vyprší platnost certifikátu.|
    |**Použití klíče**|Všechny|Zadejte možnosti použití klíče pro certifikát. Vybírat můžete z těchto možností:<br /><br />-   **Digitální podpis** (SignatureTemplate) – použijte k digitálnímu podepisování dat.<br />-   **Zakódování klíče** (EncryptionTemplate) – použijte k šifrování.<br />-   **Šifrování klíče + Digitální podpis** (GeneralPurposeTemplate) – použijte k digitálnímu podepisování a šifrování dat.|
    |**Velikost klíče (bity)**|Všechny|Vyberte velikost klíče v bitech, který je podporovaný vaším zařízením.<br /><br />Vyberte **1024** nebo **2048**.|
    |**Algoritmus hash**|Android <br />Windows 8.1 <br />Windows Phone 8.1|Vyberte jeden z dostupných typů algoritmu hash, který chcete s tímto certifikátem použít. Vyberte nejsilnější úroveň zabezpečení, kterou připojované zařízení podporuje.<br /><br />Vyberte **SHA-1**, **SHA-2** nebo obojí.|
    |**Rozšířené použití klíče**|Všechny|Kliknutím na možnost **Vybrat** přidejte hodnoty pro zamýšlený účel certifikátu. Ve většině případů certifikát vyžaduje **Ověření klienta**, aby se mohl uživatel nebo zařízení ověřit na serveru. Můžete ale přidat jakákoli další použití klíče podle potřeby.|
    |**Vybrat kořenový certifikát**|Všechny|Kliknutím na možnost **Vybrat** zvolte profil certifikátu od kořenové certifikační autority, který jste nakonfigurovali a nasadili pro uživatele nebo zařízení. Tento certifikát certifikační autority musí být kořenovým certifikátem pro certifikační autoritu, která vydává certifikát konfigurovaný v tomto profilu.|

4.  Po dokončení klikněte na **Uložit zásadu**.

Nové zásady se zobrazí v pracovním prostoru **Zásady** a můžete je teď nasadit.

##### Vytvoření profilu certifikátu .PFX

1.  Otevřete [konzolu pro správu služby Intune](https://manage.microsoft.com), klikněte na **Zásady** &gt; **Přidat zásadu**.

2.  Nakonfigurujte jeden z následujících typů zásad:

    -   **Android &gt; Profil certifikátu .PFX (Android 4 a novější)**

    -   **Windows Phone a zaregistrovaná zařízení Windows &gt; Profil certifikátu .PFX (Windows 10 a novější)**

    -   **Windows Phone a zaregistrovaná zařízení Windows &gt; Profil certifikátu .PFX (Windows Phone 10 a novější)**

    Další informace: [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

3.  Pomocí těchto informací nakonfigurujte nastavení profilu certifikátu .PFX pro Android, iOS, Windows 10 a Windows Phone 10:

    |Název nastavení|Platforma|Další informace|
    |-------------------|-------------|-------------------|
    |**Název**|Android <br />Windows 10 <br />Windows Phone 10|Zadejte popisný název profilu certifikátu.|
    |**Popis**|Android <br />Windows 10 <br />Windows Phone 10|Zadejte volitelný popis certifikátu.|
    |**Prahová hodnota obnovení (%)**|Android <br />Windows 10 <br />Windows Phone 10|Zadejte procento životnosti certifikátu zbývající v okamžiku, kdy zařízení požádá o obnovení certifikátu.|
    |**Certifikační autorita**|Android <br />Windows 10 <br />Windows Phone 10|Zadejte plně kvalifikovaný název domény certifikačního autority, například *device.certs.contoso.com*.|
    |**Název certifikační autority**|Android <br />Windows 10 <br />Windows Phone 10|Zadejte název certifikační autority, například *device-contoso-CA*.|
    |**Název šablony certifikace**|Android <br />Windows 10 <br />Windows Phone 10|Zadejte název šablony certifikace (ne zobrazovaný název).|
    |**Formát názvu subjektu**|Android <br />Windows 10 <br />Windows Phone 10|Zadejte jeden formát názvu subjektu z uvedených možností:<br /><br />-   Příjmení<br />-   Příjmení a e-mailová adresa|
    |**Alternativní název subjektu**|Android <br />Windows 10 <br />Windows Phone 10|Zvolte alternativní názvy subjektů.|
    |**Období platnosti certifikátu**|Android <br />Windows 10 <br />Windows Phone 10|Zadejte dobu, než vyprší platnost certifikátu.|

4.  Po dokončení klikněte na **Uložit zásadu**.

Nové zásady se zobrazí v pracovním prostoru **Zásady** a můžete je teď nasadit.

## <a name="BKMK_Deploy"></a>Nasazení profilů certifikátů
Když nasadíte profily certifikátů, soubor certifikátu z profilu certifikátu důvěryhodné certifikační autority se nainstaluje do zařízení a zařízení použije profil certifikátu SCEP nebo .PFX k vytvoření žádosti o certifikát.

Profily certifikátů se nainstalují jenom na příslušná zařízení podle platformy, kterou použijete při vytváření profilu.

-   Profily certifikátů můžete nasadit na kolekce uživatelů nebo kolekce zařízení.

    > [!TIP]
    > Pokud chcete umožnit, aby se certifikáty do zařízení publikovaly rychle po zaregistrování zařízení, nasaďte profil certifikátu do skupiny uživatelů (ne skupiny zařízení). Pokud ho nasadíte do skupiny zařízení, musí proběhnout úplná registrace zařízení, než zařízení obdrží zásady.

-   Přestože se každý profil nasazuje samostatně, musí se nasadit jak profil důvěryhodného kořenového certifikátu i profil SCEP/.PFX, jinak se zásady certifikátu SCEP/.PFX nezdaří.

Profily certifikátů se nasazují stejným způsobem jako jiné zásady pro [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Informace o tom, jak nasadit a spravovat zásady, najdete v tématu [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

## Viz také
[Povolení přístupu k prostředkům společnosti se službou Microsoft Intune](../Topic/Enable_access_to_company_resources_with_Microsoft_Intune_-_deleted.md)

