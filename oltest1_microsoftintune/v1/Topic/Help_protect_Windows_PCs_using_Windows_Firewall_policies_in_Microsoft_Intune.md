---
description: na
keywords: na
title: Help protect Windows PCs using Windows Firewall policies in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 62c44f36-d866-439e-8553-948cc0ea2504
---
# Pomoc při ochraně poč&#237;tačů s Windows pomoc&#237; z&#225;sad br&#225;ny Windows Firewall v Microsoft Intune
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] vám může pomoci zabezpečit spravované počítače mnoha různými způsoby, včetně použití zásad, které vám umožní nakonfigurovat nastavení brány Windows Firewall v klientských počítačích.

Pokud jste ještě klienta [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] na počítače nenainstalovali, přečtěte si část [Instalace klienta na počítači s Windows pomocí Microsoft Intune](../Topic/Install_the_Windows_PC_client_with_Microsoft_Intune.md).

Informace v následujících částech vám pomohou s konfigurací, nasazováním a monitorováním zásad brány Windows Firewall na klientských počítačích.

## <a name="BKMK_Firewall"></a>Používání zásad Microsoft Intune pro správu brány Windows Firewall
Zásady brány Windows Firewall umožňují vytvářet a nasazovat nastavení, která řídí bránu Windows Firewall na spravovaných počítačích. Není možné spravovat vlastní výjimky pro bránu Windows Firewall a tato nastavení neovlivní brány firewall třetích stran.

> [!NOTE]
> Pokud jsou zásady [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] a zásady skupiny nakonfigurované pro správu stejných nastavení na počítači, pak nastavení zásad skupiny přepisuje zásady[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]. Informace o tom, jak zamezit konfliktům mezi zásadami [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] a zásadami skupiny, najdete v článku [Řešení konfliktů GPO a zásad Microsoft Intune](../Topic/Resolve_GPO_and_Microsoft_Intune_policy_conflicts.md).
> 
> Pokud chcete nasadit nastavení brány Windows Firewall do počítačů se systémem Windows Vista, musíte na tyto počítače nejdřív nainstalovat [opravu Hotfix KB971800](http://support2.microsoft.com/kb/971800).

> [!IMPORTANT]
> Pokud chcete spravovat bránu Windows Firewall pomocí [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], musí být na počítačích, které budete spravovat, povolené následující dvě služby:
> 
> -   Brána Windows Firewall
> -   Agent zásad protokolu IPsec

#### Konfigurace zásad brány Windows Firewall

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com/) klikněte na **Zásady** &gt; **Přidat zásadu**.

2.  Konfigurujte a nasaďte zásady **nastavení brány Windows Firewall**. Můžete použít doporučená nastavení nebo nastavení upravit. Pokud potřebujete další informace o tom, jak vytvořit a nasadit zásady, přečtěte si téma [Běžné úlohy správy počítačů s Windows pomocí počítačového klienta Microsoft Intune](../Topic/Common_Windows_PC_management_tasks_with_the_Microsoft_Intune_computer_client.md).

    Tabulky po tomto postupu zobrazují hodnoty, které můžete v zásadách konfigurovat, a taky doporučené hodnoty, které se použijí, pokud zásady neupravíte.

Nasazené zásady brány Windows Firewall můžete zobrazit na stránce **Všechny zásady** pracovního prostoru **Zásady**.

### Nastavení zásad brány Windows Firewall

#### Zapnout bránu Windows Firewall

|Nastavení zásad|Další informace|
|-------------------|-------------------|
|**Doménový profil**|Aktivuje bránu Windows Firewall na spravovaných počítačích, pokud jsou připojené k doménovým sítím, například na pracovišti.<br /><br />Doporučená hodnota: **Ano**|
|**Soukromý profil**|Aktivuje bránu Windows Firewall na spravovaných počítačích, pokud jsou připojené k důvěryhodným sítím, například v domácí síti.<br /><br />Doporučená hodnota: **Ano**|
|**Veřejný profil**|Aktivuje bránu Windows Firewall na spravovaných počítačích, pokud jsou připojené k nedůvěryhodným sítím na veřejných místech, například v kavárně.<br /><br />Doporučená hodnota: **Ano**<br /><br />Požadovaný operační systém: [!INCLUDE[firstref_vista](../Token/firstref_vista_md.md)] nebo novější verze|

#### Blokování všech příchozích připojení, včetně připojení uvedených na seznamu povolených programů
> [!IMPORTANT]
> Obsahuje-li dané prostředí spravované počítače, v nichž je spuštěn systém Windows Vista bez nainstalovaných aktualizací Service Pack, je nutné nainstalovat aktualizaci uváděnou ve znalostní bázi Microsoft Knowledge Base v [článku 971800](http://go.microsoft.com/fwlink/?LinkId=188405) nebo jinak vypnout nastavení zásady **Blokovat všechna příchozí připojení** v zásadách nasazených v těchto počítačích.

|Nastavení zásad|Další informace|
|-------------------|-------------------|
|**Doménový profil**|Blokuje všechna příchozí připojení, pokud jsou počítače připojené k doménovým sítím, například na pracovišti. Zahrnuta jsou připojení uvedená v seznamu výjimek.<br /><br />Doporučená hodnota: **Ne**|
|**Soukromý profil**|Blokuje všechna příchozí připojení, pokud jsou počítače připojené k důvěryhodným sítím, například v domácí síti. Zahrnuta jsou připojení uvedená v seznamu výjimek.<br /><br />Doporučená hodnota: **Ne**|
|**Veřejný profil**|Blokuje všechna příchozí připojení, pokud jsou počítače připojené k nedůvěryhodným sítím na veřejných místech, například v kavárně. Zahrnuta jsou připojení uvedená v seznamu výjimek.<br /><br />Doporučená hodnota: **Ne**<br /><br />Požadovaný operační systém: [!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] nebo novější verze|

#### Oznámit uživatelům blokování nového programu bránou Windows Firewall

|Nastavení zásad|Další informace|
|-------------------|-------------------|
|**Doménový profil**|Upozorní uživatele, když brána Windows Firewall blokuje nový program, pokud jsou počítače připojené k doménovým sítím, například na pracovišti.<br /><br />Doporučená hodnota: **Ano**|
|**Soukromý profil**|Upozorní uživatele, když brána Windows Firewall blokuje nový program, pokud jsou počítače připojené k důvěryhodným sítím, například v domácí síti.<br /><br />Doporučená hodnota: **Ano**|
|**Veřejný profil**|Upozorní uživatele, když brána Windows Firewall blokuje nový program, pokud jsou počítače připojené k nedůvěryhodným sítím na veřejných místech, například v kavárně.<br /><br />Doporučená hodnota: **Ano**<br /><br />Požadovaný operační systém: [!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] nebo novější verze|

#### Předdefinované výjimky

|Nastavení zásad|Další informace|
|-------------------|-------------------|
|**Služba BranchCache – načítání obsahu**|Pokud je povoleno, umožňuje klientům služby BranchCache prostřednictvím protokolu HTTP načítat obsah vzájemně jeden z druhého (v distribuovaném režimu) a z hostované mezipaměti (v režimu hostované mezipaměti). Toto nastavení využívá protokol HTTP.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[firstref_client_7](../Token/firstref_client_7_md.md)] nebo novější).|
|**Služba BranchCache – klient hostované mezipaměti**|Pokud je povoleno, umožňuje klientům služby BranchCache používat hostovanou mezipaměť. Toto nastavení využívá protokol HTTPS.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_client_7](../Token/nextref_client_7_md.md)] nebo novější).|
|**Služba BranchCache – server hostované mezipaměti**|Pokud je povoleno, umožňuje klientům služby BranchCache používat hostovanou mezipaměť ke komunikaci s ostatními klienty. Toto nastavení využívá protokol HTTPS.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_client_7](../Token/nextref_client_7_md.md)] nebo novější).|
|**Služba BranchCache – zjišťování rovnocenných zařízení**|Pokud je povoleno, umožňuje klientům služby BranchCache používat protokol WS Discovery k vyhledání dostupnosti obsahu v místní podsíti.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_client_7](../Token/nextref_client_7_md.md)] nebo novější).|
|**Ukládání do sdílené mezipaměti BITS**|Pokud je povoleno, umožňuje klientům používat službu inteligentního přenosu na pozadí (BITS) k vyhledání a sdílení souborů uložených v mezipaměti BITS na klientských počítačích ve stejné podsíti. Toto nastavení využívá rozhraní WSDAPI a RPC.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] nebo novější).|
|**Připojení k síťovému projektoru**|Pokud je povoleno, umožňuje uživatelům připojit se k projektorům prostřednictvím drátových nebo bezdrátových sítí a promítat prezentací. Toto nastavení využívá rozhraní WSDAPI.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] nebo novější).|
|**Základní síťové služby**|Pokud je povoleno, umožňuje klientům používat protokoly IPv4 a IPv6 pro připojení k síťovým prostředkům.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] nebo novější).|
|**Koordinátor distribuovaných transakcí**|Pokud je povoleno, umožňuje spravovaným počítačům koordinovat transakce, které aktualizují prostředky s ochranou transakcí, jako jsou databáze, fronty zpráv nebo souborové systémy.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] nebo novější).|
|**Sdílení souborů a tiskáren**|Pokud je povoleno, umožňuje uživatelům sdílet místní soubory a tiskárny s dalšími uživateli v síti. Toto nastavení využívá rozhraní NetBIOS, LLMNR, SMB a RPC.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />(Windows XP nebo novější).|
|**Domácí skupina**|Pokud je povoleno, umožňuje spravovaným počítačům účast v síti domácí skupiny.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_client_7](../Token/nextref_client_7_md.md)] nebo novější).|
|**Služba iSCSI**|Pokud je povoleno, umožňuje spravovaným počítačům připojení k serverům a zařízením iSCSI.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] nebo novější).|
|**Služba správy klíčů**|Pokud je povoleno, umožňuje spočítání počítačů kvůli shodě s licencí v podnikovém prostředí.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] nebo novější).|
|**Zařízení Media Center Extender**|Pokud je povoleno, umožňuje zařízením Media Center Extender komunikovat s počítači se systémem Windows Media Center. Toto nastavení využívá protokol SSDP a službu qWave.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] nebo novější).|
|**Služba Netlogon**|Pokud je povoleno, konfiguruje zabezpečený kanál mezi klienty v doméně a řadičem domény za účelem ověřování totožnosti uživatelů a služeb. Toto nastavení využívá protokol RPC.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] nebo novější).|
|**Zjišťování sítě**|Pokud je povoleno, umožňuje počítačům zjišťovat jiná zařízení a být zjištěny jinými zařízeními v síti. Toto nastavení používá službu publikování a hostitele rozpoznávání funkcí a taky síťové protokoly SSDP, NetBIOS, LLMNR a UPnP.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] nebo novější).|
|**Výstrahy a protokolování výkonu**|Pokud je povoleno, umožňuje vzdálenou správu služby Výstrahy a protokolování výkonu. Toto nastavení využívá protokol RPC.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] nebo novější).|
|**Vzdálená správa**|Pokud je povoleno, umožňuje vzdálenou správu počítače.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] nebo novější).|
|**Vzdálená pomoc**|Pokud je povoleno, umožňuje uživatelům spravovaných počítačů žádat o vzdálenou pomoc od jiných uživatelů v síti. Toto nastavení používá síťové protokoly SSDP, PNRP, Teredo a UPnP.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />(Windows XP nebo novější).|
|**Vzdálená plocha**|Pokud je povoleno, umožňuje počítači přistupovat k jiným počítačům pomocí vzdálené plochy.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />(Windows XP nebo novější).|
|**Vzdálená správa protokolu událostí**|Pokud je povoleno, umožňuje vzdálené zobrazení a správu protokolů událostí klienta. Toto nastavení využívá pojmenované kanály a rozhraní RPC.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] nebo novější).|
|**Vzdálená správa naplánovaných úloh**|Pokud je povoleno, umožňuje vzdálenou správu služby plánování úloh. Toto nastavení využívá protokol RPC.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] nebo novější).|
|**Vzdálená správa služeb**|Pokud je povoleno, umožňuje vzdálenou správu místních služeb na klientech. Toto nastavení využívá pojmenované kanály a rozhraní RPC.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] nebo novější).|
|**Vzdálená správa svazků**|Pokud je povoleno, umožňuje vzdálenou softwarovou a hardwarovou správu svazku disku. Toto nastavení využívá protokol RPC.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] nebo novější).|
|**Směrování a vzdálený přístup**|Pokud je povoleno, umožňuje příchozí připojení VPN a připojení se vzdáleným přístupem k počítačům.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] nebo novější).|
|**Protokol SSTP**|Pokud je povoleno, umožňuje příchozí připojení VPN ke spravovaným počítačům pomocí protokolu SSTP (Secure Socket Tunneling Protocol). Toto nastavení využívá protokol HTTPS.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] nebo novější).|
|**Zachytávání pro službu SNMP**|Pokud je povoleno, umožňuje spravovaným počítačů příjem přenosů služby depeší protokolu SNMP.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] nebo novější).|
|**Architektura UPnP**|Pokud je povoleno, konfiguruje službu Architektura UPnP na počítačích, aby mohly zjišťovat a používat certifikovaná zařízení UPnP.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />(Windows XP nebo novější).|
|**Služba registrace názvu počítače pro Centrum spolupráce**|Pokud je povoleno, umožňuje počítačům najít a další počítače a komunikovat s nimi pomocí protokolu PNRP (Peer Name Resolution Protocol). Toto nastavení využívá protokol SSDP a PNRP.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] nebo novější).|
|**Windows Media Player**|Pokud je povoleno, umožňuje uživatelům přijímat média streamovaná prostřednictvím protokolu UDP.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] nebo novější).|
|**Služba Windows Media Player Network Sharing**|Pokud je povoleno, umožňuje uživatelům sdílet média přes síť. Toto nastavení používá síťové protokoly SSDP, qWave a UPnP.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] nebo novější).|
|**Služba Windows Media Player Network Sharing (Internet)**|Pokud je povoleno, umožňuje uživatelům sdílet domácí média prostřednictvím internetu.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_client_7](../Token/nextref_client_7_md.md)] nebo novější).|
|**Centrum spolupráce**|Pokud je povoleno, umožňuje uživatelům spolupracovat přes síť a sdílet tak dokumenty, programy nebo plochy. Toto nastavení používá službu DFSR a P2P.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] nebo novější).|
|**Základ spolupráce rovnocenných počítačů**|Pokud je povoleno, konfiguruje různé programy a technologie peer-to-peer, aby se mohly připojit. Toto nastavení využívá protokol SSDP a PNRP.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] nebo novější).|
|**Vzdálená správa systému Windows (režim kompatibility)**|Pokud je povoleno, umožňuje vzdálenou správu spravovaných počítačů pomocí služby vzdálené správy systému Windows (WS-Management), což je protokol založený na webových službách pro vzdálenou správu operačních systémů a zařízení.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] nebo novější).|
|**Vzdálená správa systému Windows**|Pokud je povoleno, umožňuje vzdálenou správu spravovaných počítačů pomocí služby vzdálené správy systému Windows (WS-Management), což je protokol založený na webových službách pro vzdálenou správu operačních systémů a zařízení.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />(Windows 8 nebo novější)|
|**Windows Virtual PC**|Pokud je povoleno, umožňuje virtuálním počítačům komunikovat s dalšími počítači.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />(jenom [!INCLUDE[nextref_client_7](../Token/nextref_client_7_md.md)])|
|**Bezdrátová přenosná zařízení**|Pokud je povoleno, umožňuje přenos médií z fotoaparátu nebo mediálního zařízení připojeného k síti do spravovaných počítačů pomocí protokolu MTP (Media Transfer Protocol). Toto nastavení používá síťové protokoly SSDP a UPnP.<br /><br />Doporučená hodnota: Nenakonfigurováno<br /><br />([!INCLUDE[nextref_vista](../Token/nextref_vista_md.md)] nebo novější).|

## Viz také
[Správa počítačů s Windows pomocí Intune](../Topic/Manage_Windows_PCs_with_Microsoft_Intune.md)

