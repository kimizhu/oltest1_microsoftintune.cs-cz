---
description: na
keywords: na
title: Mobile device management with Exchange ActiveSync and Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: eb9618d2-dc90-48be-b921-8044b7e693ac
---
# Spr&#225;va mobiln&#237;ch zař&#237;zen&#237; pomoc&#237; protokolu Exchange ActiveSync a služby Microsoft Intune
Aby mohla služba [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] přímo spravovat mobilní zařízení, musí uživatelé tato zařízení v [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] zaregistrovat. U mobilních zařízení, která uživatelé nezaregistrovali, můžete povolit správu pomocí protokolu Exchange ActiveSync s použitím konektoru Exchange. Zařízení Exchange se dají spravovat na místních serverech i prostřednictvím hostovaného Exchange v Microsoft Office 365 v cloudu. Konektor Exchange slouží jako propojení s nasazením Exchange a umožňuje vám spravovat mobilní zařízení prostřednictvím konzoly [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], kde můžete dělat toto:

-   Nasazovat zásady skupinám uživatelů a líp tak zabezpečit podniková data uložená na mobilních zařízeních (třeba hesla, šifrování a přílohy)

-   Definovat pravidla přístupu k mobilním zařízením podle řady a modelu zařízení a nastavit tak, která mobilní zařízení budou mít přístup k protokolu Exchange ActiveSync

-   Registrovat, přejmenovávat a rušit registraci zařízení

-   Vymazávat mobilní zařízení, třeba v případě jejich ztráty nebo odcizení

Toto téma obsahuje následující části:

-   [Konfigurace konektoru Microsoft Intune On-premises Connector pro místní nebo hostovaný Exchange](../Topic/Mobile_device_management_with_Exchange_ActiveSync_and_Microsoft_Intune.md#bkmk_EX_OP): Tato část obsahuje informace o konfiguraci místní infrastruktury s místním nebo hostovaným Exchangem.

-   [Konfigurace konektoru Intune Service to Service Connector pro hostovaný Exchange](../Topic/Mobile_device_management_with_Exchange_ActiveSync_and_Microsoft_Intune.md#bkmk_S_S)

-   [Ověření připojení k Exchangi](../Topic/Mobile_device_management_with_Exchange_ActiveSync_and_Microsoft_Intune.md#bkmk_val_ex)

-   [Vymazání mobilních zařízení spravovaných Exchangem](../Topic/Mobile_device_management_with_Exchange_ActiveSync_and_Microsoft_Intune.md#bkmk_EXCap)

-   [Zásady pro mobilní zařízení spravovaná Exchangem](../Topic/Mobile_device_management_with_Exchange_ActiveSync_and_Microsoft_Intune.md#bkmk_pol)

-   [Pravidla přístupu k Exchangi pro mobilní zařízení](../Topic/Mobile_device_management_with_Exchange_ActiveSync_and_Microsoft_Intune.md#bkmk_acc)

## <a name="bkmk_EX_OP"></a>Konfigurace konektoru Microsoft Intune On-premises Connector pro místní nebo hostovaný Exchange
Podle informací uvedených v této části můžete nakonfigurovat místní infrastrukturu s místním nebo hostovaným Exchangem.

### Požadavky
Abyste mohli [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] připojit ke svému Exchange Serveru, musíte nejdřív splnit následující požadavky. Možná jste se o splnění těchto požadavků postarali už při nastavování [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

|Požadavek|Další informace|
|-------------|-------------------|
|Nastavení autority pro správu mobilních zařízení na [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]|[Nastavení autority správy mobilních zařízení na Microsoft Intune](../Topic/Set_mobile_device_management_authority_and_configure_Microsoft_Intune.md)|
|Ověření splnění požadavků na hardware pro konektor On-premises Connector|[Požadavky na konektor On-Premises Connector](../Topic/Network_infrastructure_requirements_for_Microsoft_Intune.md#BKMK_ExchanceConnectorReqs)|
|Konfigurace takových oprávnění pro uživatelský účet, která umožňují spouštět určený seznam rutin prostředí Windows PowerShell|Rutiny prostředí PowerShell pro konektor On-Premises Exchange Connector (viz níže)|

### <a name="bkmk_PS_onprem"></a>Rutiny prostředí PowerShell pro konektor On-Premises Exchange Connector
Musíte vytvořit uživatelský účet služby Active Directory, který bude konektor [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] Exchange Connector používat. Tento účet musí mít oprávnění ke spouštění těchto požadovaných rutin prostředí Windows PowerShell:

-   Get-ActiveSyncOrganizationSettings, Set-ActiveSyncOrganizationSettings

-   Get-CasMailbox, Set-CasMailbox

-   Get-ActiveSyncMailboxPolicy, Set-ActiveSyncMailboxPolicy, New-ActiveSyncMailboxPolicy, Remove-ActiveSyncMailboxPolicy

-   Get-ActiveSyncDeviceAccessRule, Set-ActiveSyncDeviceAccessRule, New-ActiveSyncDeviceAccessRule, Remove-ActiveSyncDeviceAccessRule

-   Get-ActiveSyncDeviceStatistics

-   Get-ActiveSyncDevice

-   Get-ExchangeServer

-   Get-ActiveSyncDeviceClass

-   Get-Recipient

-   Clear-ActiveSyncDevice, Remove-ActiveSyncDevice

-   Set-ADServerSettings

-   Get-Command

### Stažení, instalace a konfigurace konektoru Microsoft Intune Exchange Connector
Pokud chcete nastavit připojení umožňující komunikaci [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] s Exchange Serverem, který je hostitelem poštovních schránek mobilních zařízení, musíte si z konzoly pro správu [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] stáhnout nástroj On-Premises Connector a nakonfigurovat ho.

##### Stažení instalačního balíčku softwaru On-Premises Connector

1.  Otevřete program [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)].

2.  V podokně zástupců pracovních prostorů klikněte na **Správa**.

3.  V navigačním podokně rozbalte v části **Správa mobilního zařízení** položku **Microsoft Exchange** a potom klikněte na **Nastavit připojení k systému Exchange**.

4.  Na stránce **Nastavit připojení k systému Exchange** klikněte na **Stáhnout software On-Premises Connector**.

5.  Software On-Premises Connector je v komprimované složce (.zip), která se dá otevřít nebo uložit. V dialogovém okně **Stažení souboru** klikněte na **Uložit** a uložte komprimovanou složku do zabezpečeného umístění.

> [!IMPORTANT]
> Extrahované soubory nepřejmenovávejte ani nepřesouvejte, jinak se instalace softwaru On-Premises Connector nepovede.

Při instalaci konektoru [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] On-Premises Connector postupujte podle následujících kroků.

> [!IMPORTANT]
> Konektor On-Premises Connector se dá nainstalovat jenom jednou pro každé předplatné [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] a jenom na jeden počítač. Když zkusíte nainstalovat konektor On-Premises Connector podruhé, nahradíte tím počáteční připojení k Exchangi.

##### Instalace konektoru On-Premises Connector

1.  Extrahuje soubory ze složky **Exchange_Connector_Setup.zip** do zabezpečeného umístění.

2.  Po extrahování souborů poklikejte na **Exchange_Connector_Setup.exe** a nainstalujte konektor On-Premises Connector.

    > [!IMPORTANT]
    > Pokud cílová složka není v zabezpečeném umístění, měli byste po instalaci konektoru On-Premises Connector odstranit soubor certifikátu **WindowsIntune.accountcert**.

> [!NOTE]
> Pro každý účet [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] můžete nastavit jenom jedno připojení k Exchangi. Když zkusíte nakonfigurovat další připojení, nahradí se původní připojení tímto novým připojením.

##### Konfigurace konektoru On-Premises Exchange Connector

1.  V poli **Server Exchange** vyberte typ prostředí serveru Exchange, a to buď **Místní Exchange Server**, nebo **Hostovaný Exchange Server** (pro Exchange v Microsoft Office 365).

2.  V případě místního serveru Exchange zadejte název serveru nebo plně kvalifikovaný název domény serveru Exchange, který je hostitelem role serveru Klientský přístup.

3.  U serveru Exchange hostovaného v Microsoft Office 365 zadejte adresu serveru Exchange.  Adresu URL hostovaného serveru Exchange najdete takto:

    1.  Otevřete Outlook Web App pro Office 365.

    2.  Klikněte na ikonu „?“ v levém horním rohu a vyberte **O aplikaci**.

    3.  Najděte hodnotu **Externí nastavení POP**.

4.  V případě vyhrazeného hostovaného serveru Exchange zadejte název serveru nebo plně kvalifikovaný název domény vyhrazeného serveru Exchange, který je hostitelem role serveru Klientský přístup.

5.  Klikněte na **Proxy server** a zadejte nastavení proxy serveru pro svůj hostovaný server Exchange.

    1.  Vyberte **Používat proxy server při synchronizaci informací mobilních zařízení**.

    2.  Zadejte **název proxy serveru** a **číslo portu** pro přístup na server.

    3.  Pokud je potřeba zadat přihlašovací údaje uživatele pro přístup na proxy server, vyberte Použít pověření k připojení k proxy serveru a zadejte položku **doména\uživatel** a **heslo**.

    4.  Klikněte na **OK**.

6.  Zadejte přihlašovací údaje potřebné pro připojení k serveru Exchange.

7.  Zadejte přihlašovací údaje správce potřebné pro odesílání oznámení do poštovní schránky Exchange uživatele. Tato oznámení se dají konfigurovat prostřednictvím zásad podmíněného přístupu v Intune. Další informace o těchto zásadách najdete v tématu [Povolení přístupu k prostředkům společnosti se službou Microsoft Intune](../Topic/Enable_access_to_company_resources_with_Microsoft_Intune_-_deleted.md).

    Zkontrolujte, že je na serveru Exchange pro klientský přístup nainstalovaná služba Automatická konfigurace a Webové služby systému Exchange. Další informace najdete v tématu [Server pro klientský přístup](https://technet.microsoft.com/library/dd298114.aspx).

8.  Do pole **Heslo** zadejte heslo pro tento účet, aby měla služba [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] přístup k Exchange Serveru.

9. Klikněte na možnost **Připojit**.

    Nastavení připojení může pár minut trvat.

    Konektor [!INCLUDE[wit_exch_2](../Token/wit_exch_2_md.md)] během konfigurace uloží vaše nastavení proxy serveru, aby byl zajištěný přístup na internet. Pokud se vaše nastavení proxy serveru změní, budete muset konektor [!INCLUDE[wit_exch_2](../Token/wit_exch_2_md.md)] překonfigurovat tak, aby konektor [!INCLUDE[wit_exch_2](../Token/wit_exch_2_md.md)] používal aktualizované nastavení proxy serveru.

Až konektor [!INCLUDE[wit_exch_2](../Token/wit_exch_2_md.md)] připojení nastaví, mobilní zařízení přidružená k uživatelům spravovaným v [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] se automaticky synchronizují a přidají se do konzoly [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)]. Dokončení této synchronizace může chvíli trvat.

Jestli se chcete podívat na stav připojení a zjistit, kdy naposledy proběhla úspěšná synchronizace, klikněte v konzole [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] na pracovní prostor **Správa** a v části **Správa mobilního zařízení** klikněte na **Exchange**.

> [!NOTE]
> Pokud máte nainstalovaný konektor On-Premises Connector a odstraníte připojení k Exchangi, musíte konektor On-Premises Connector z počítače, na kterém je nainstalovaný, odinstalovat.

## <a name="bkmk_S_S"></a>Konfigurace konektoru Intune Service to Service Connector pro hostovaný Exchange
Podle informací uvedených v této části můžete propojit [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] a hostovaný Exchange bez místní infrastruktury.

### Požadavky
Abyste mohli [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] připojit ke svému Exchange Serveru, musíte udělat následující věci:

|Požadavek|Další informace|
|-------------|-------------------|
|Nastavení autority pro správu mobilních zařízení na [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]|[Příprava registrace zařízení v Microsoft Intune](../Topic/Get_ready_to_enroll_devices_in_Microsoft_Intune.md)|
|Ověření splnění požadavků na hardware pro konektor On-premises Connector|[Požadavky na konektor Service to Service Connector](../Topic/Network_infrastructure_requirements_for_Microsoft_Intune.md#BKMK_ServiceConnectorReqs)|
|Konfigurace takových oprávnění pro uživatelský účet, která umožňují spouštět určený seznam rutin prostředí Windows PowerShell|Rutiny prostředí PowerShell pro konektor Service to Service Connector (viz níže)|

### <a name="Bkmk_PS_STS"></a>Rutiny prostředí PowerShell pro konektor Service to Service Connector
Musíte vytvořit uživatelský účet Exchange Online, který bude konektor [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] Exchange Connector používat. Tento účet musí mít oprávnění ke spouštění požadovaných rutin prostředí Windows PowerShell uvedených v následujícím seznamu.

-   Get-ActiveSyncOrganizationSettings, Set-ActiveSyncOrganizationSettings

-   Get-MobileDeviceMailboxPolicy, Set-MobileDeviceMailboxPolicy, New-MobileDeviceMailboxPolicy, Remove-MobileDeviceMailboxPolicy

-   Get-ActiveSyncDeviceAccessRule, Set-ActiveSyncDeviceAccessRule, New-ActiveSyncDeviceAccessRule, Remove-ActiveSyncDeviceAccessRule

-   Get-MobileDeviceStatistics

-   Get-MobileDevice

-   Get-ActiveSyncDeviceClass

-   Get-Recipient

-   Clear-MobileDevice, Remove-MobileDevice

### Nastavení konektoru Service to Service Connector

1.  Otevřete program [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)].

2.  V podokně zástupců pracovních prostorů klikněte na **Správa**.

3.  V navigačním podokně rozbalte v části **Správa mobilního zařízení** položku **Microsoft Exchange** a potom klikněte na **Nastavit připojení k systému Exchange**.

4.  Na stránce **Nastavit připojení k systému Exchange** klikněte na **Nastavit konektor Service to Service Connector**.

Konektor Service to Service Connector se automaticky nakonfiguruje a synchronizuje s prostředím hostovaného Exchange.

## <a name="bkmk_val_ex"></a>Ověření připojení k Exchangi

-   Po úspěšné konfiguraci konektoru [!INCLUDE[wit_exch_2](../Token/wit_exch_2_md.md)] klikněte v konzole [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] na pracovní prostor **Správa** a v části **Správa mobilního zařízení** klikněte na **Microsoft Exchange** a ověřte, že se v části **Informace o připojení systému Exchange** zobrazují podrobnosti, které jste zadali.

-   Můžete se taky podívat na datum a čas posledního úspěšného pokusu o synchronizaci.

## <a name="bkmk_EXCap"></a>Vymazání mobilních zařízení spravovaných Exchangem
Možnosti vyřazení/vymazání prostřednictvím protokolu Exchange ActiveSync popisuje následující tabulka.

|Typ vymazání|Windows 8.1 a Windows RT 8.1|Windows RT|Windows Phone 8|iOS|Android|
|----------------|--------------------------------|--------------|-------------------|-------|-----------|
|Úplné vymazání|Odebere poštovní účet a poštu v mezipaměti.|Odebere poštovní účet a poštu v mezipaměti.|Obnoví výrobní nastavení.|Obnoví výrobní nastavení.|Obnoví výrobní nastavení.|
|Selektivní vymazání/e-mail|Odebere e-mailový účet.|Odebere e-mailový účet.|Není podporováno.|Není podporováno.|Není podporováno.|
|Selektivní vymazání/zásady|Odebere se vynucení zásad, ale nastavení se nezmění.|Odebere se vynucení zásad, ale nastavení se nezmění.|Odebere se vynucení zásad, ale nastavení se nezmění.|Odebere se vynucení zásad, ale nastavení se nezmění.|Odebere se vynucení zásad, ale nastavení se nezmění.|

## <a name="bkmk_pol"></a>Zásady pro mobilní zařízení spravovaná Exchangem
Nastavení zásad se dá použít prostřednictvím konzoly [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Podívejte se na téma [Správa nastavení a funkcí v zařízeních pomocí zásad Microsoft Intune](../Topic/Manage_settings_and_features_on_your_devices_with_Microsoft_Intune_policies.md). Podrobný seznam nastavení zásad Exchange ActiveSync a funkcí podporovaných konkrétními mobilními zařízeními najdete v tématu [Srovnávací tabulka klientů Exchange ActiveSync](http://go.microsoft.com/fwlink/?LinkId=247270).

> [!NOTE]
> Po připojení [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] k prostředí Microsoft Exchange budou mít všichni uživatelé spravovaní přes [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] svoje zásady EAS nastavené na aktuální výchozí zásady na serveru Microsoft Exchange (pokud nejsou v [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] definované nějaké specifičtější zásady).

## <a name="bkmk_acc"></a>Pravidla přístupu k Exchangi pro mobilní zařízení
Pravidla přístupu k Exchangi pro mobilní zařízení určují úroveň přístupu k Exchangi udělenou mobilním zařízením. Tato nastavení ovlivní všechna mobilní zařízení, i mobilní zařízení, která nejsou zaregistrovaná v [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Můžete začít tak, že definujete **Výchozí pravidlo**, které bude platit pro všechna mobilní zařízení, u kterých se nepoužívá vlastní pravidlo. Úrovně přístupu spravované protokolem Exchange ActiveSync jsou uvedené v následující tabulce:

|Úroveň přístupu|Popis|
|-------------------|---------|
|**Povolit všem mobilním zařízením přístup k systému Exchange, pokud uživatelské pravidlo neurčí jinak.**|Ve stavu povoleného přístupu se může mobilní zařízení synchronizovat prostřednictvím protokolu Exchange ActiveSync a připojovat se k serveru Exchange za účelem načtení e-mailů a zpracování informací z kalendáře, kontaktů, úkolů a poznámek. Tento stav bude trvat, dokud bude zařízení v souladu se **zásadami zabezpečení mobilních zařízení** v [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], které jste nakonfigurovali (pokud správce Exchange uživatele nebo určité mobilní zařízení nezablokoval).|
|**Blokovat všem mobilním zařízením přístup k systému Exchange, pokud uživatelské pravidlo neurčí jinak.**|Mobilní zařízení blokované nastavením přístupu mobilního zařízení, které jste nakonfigurovali, se nebude moct připojit k serveru Exchange a budou se zobrazovat chyby protokolu HTTP 403 informující o zákazu. Uživatel dostane ze serveru Exchange zprávu, že byl přístup mobilního zařízení k příslušné poštovní schránce zablokován. Uživatel si nebude moct tuto e-mailovou zprávu na blokovaném mobilním zařízení přečíst. Do této zprávy můžete přidat vlastní text a dát tak uživatelům, jejichž zařízení jsou zablokovaná, příslušné pokyny. Dá se to udělat pomocí úkolu **Nastavit oznámení uživatele**.|
|**Umístit všechna mobilní zařízení do karantény, aby o každém z nich bylo možné rozhodnout později, pokud uživatelské pravidlo neurčí jinak.**|Pokud je mobilní zařízení v karanténě, nemůže se k serveru Exchange připojit. Má jenom omezený přístup k datům. Uživatel může přidávat obsah do vlastních složek Kalendář, Kontakty, Úkoly a Poznámky, ale server nedovolí zařízení načíst žádný obsah z poštovní schránky uživatele. Uživatel dostane jednu e-mailovou zprávu s oznámením, že je mobilní zařízení v karanténě. Tuto zprávu dostane zařízení a bude dostupná taky v poštovní schránce uživatele. Do této zprávy můžete přidat vlastní text a dát tak uživatelům, jejichž zařízení jsou v karanténě, příslušné pokyny. Dá se to udělat pomocí úkolu **Nastavit oznámení uživatele**.|
Strategie přístupu je tvořená kombinací nastavení **Výchozí pravidlo** a **Vlastní pravidla**, která platí pro všechna mobilní zařízení připojená k Exchangi. Některé příklady strategií přístupu jsou uvedené v následující tabulce.

|Strategie přístupu|Popis|
|----------------------|---------|
|Seznam povolených položek|Pomocí seznamu povolených položek můžete udělit přístup známým zařízením na seznamu a všem ostatním zařízením přístup zakázat. K tomu musíte vytvořit vlastní pravidla, která požadovaným zařízením povolí přístup k poštovním schránkám uživatelů. Až takové pravidlo vytvoříte, musíte nastavit výchozí pravidlo přístupu, které všechna ostatní zařízení zablokuje nebo je dá do karantény. Nové zařízení můžete do seznamu povolených položek přidat vytvořením nového vlastního pravidla.|
|Seznam blokovaných položek|Pomocí seznamu blokovaných položek můžete ve výchozím nastavení udělit přístup všem zařízením a zablokovat přístup skupině zařízení, kterým v organizaci nechcete povolit přístup. Seznam blokovaných položek můžete vytvořit tak, že vytvoříte vlastní pravidla pro blokování zařízení, která nechcete synchronizovat s poštovními schránkami organizace. Výchozí pravidlo by mělo být nastavené tak, aby umožňovalo přístup všem zařízením, která nejsou explicitně blokovaná existujícími pravidly. Nové zařízení nebo skupinu zařízení můžete do seznamu blokovaných položek přidat tak, že vytvoříte nové vlastní pravidlo.|
|Kombinace seznamů povolených a blokovaných položek|Kromě vytvoření seznamu povolených a blokovaných položek můžete mobilní zařízení, která jsou v organizaci nová a zatím je vyhodnocujete, dát do karantény. Když třeba máte seznam blokovaných položek pro mobilní zařízení, která nejsou v organizaci povolená, a seznam povolených položek pro mobilní zařízení, které jsou v organizaci povolená, můžete nastavit ještě výchozí pravidlo pro karanténu. Všechna ostatní zařízení se automaticky umístí do karantény, takže můžete nově zaváděná zařízení v organizaci vyzkoušet a rozhodnout se, jestli je přidáte do seznamu povolených položek, nebo do seznamu zakázaných položek.|
Postup vytvoření vlastního pravidla je popsaný v následující části.

#### Vytvoření výchozího pravidla přístupu

1.  Otevřete program [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)].

2.  V podokně zástupců pracovního prostoru klikněte na ikonu **Zásady** a klikněte na **Přístup k systému Exchange pro mobilní zařízení**.

3.  V seznamu **Výchozí pravidlo** vyberte pravidlo přístupu, které chcete použít u všech mobilních zařízení, pro která neplatí pravidlo nebo osobní výjimka. Klikněte na **Uložit**.

Postup vytvoření vlastního pravidla je popsaný v následující části.

#### Vytvoření vlastního pravidla přístupu

1.  Otevřete program [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)].

2.  V podokně zástupců pracovního prostoru klikněte na ikonu **Zásady** a klikněte na **Přístup k systému Exchange pro mobilní zařízení**.

3.  V seznamu **Vlastní pravidla** klikněte na **Přidat pravidlo** a vytvořte vlastní pravidlo. Klikněte na **Uložit**.

## Viz také
[Příprava registrace zařízení v Microsoft Intune](../Topic/Get_ready_to_enroll_devices_in_Microsoft_Intune.md)

