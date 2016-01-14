---
description: na
keywords: na
title: Troubleshoot client setup in Microsoft Intune
search: na
ms.date: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e46d292b-1d16-46db-a87f-d53eefa4d22a
---
# Řešen&#237; pot&#237;ž&#237; s instalac&#237; klientů v Microsoft Intune

## Řešení potíží s instalací klientů
Při odstraňování běžných problémů s instalací klientů vám můžou pomoct informace uvedené v následujících částech.

### Co dělat, když se instalace klienta nepovede

-   Pokud [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] nezobrazuje pro příslušný počítač žádné výstrahy týkající se nasazení klientského softwaru, zkontrolujte připojení počítače k internetu a konfiguraci proxy serveru a na adrese URL [https://manage.microsoft.com](https://manage.microsoft.com) se ujistěte, že počítač může se službou komunikovat. Pak zkuste klientský software nainstalovat znova.

-   Konfigurací pravidla oznámení v pracovním prostoru **Správce** můžete zajistit, aby se v případě výstrahy týkající se chyby nasazení klientského softwaru odeslal vybraným příjemcům e-mail. Další informace najdete v části [Upozorňování pomocí výstrah služby Microsoft Intune](../Topic/Get_notified_by_Microsoft_Intune_alerts.md).

-   Pokud se nepovede klientský software nasadit, zobrazí [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] kritickou výstrahu **Chyba nasazení klientského softwaru**. Bude se zobrazovat na stránce **Přehled systému** a na stránkách **Výstrahy** konzoly [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)]. Výstrahy můžete zkontrolovat tímto způsobem:

##### Kontrola výstrah týkajících se neúspěšných instalací

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com/) klikněte na **Výstrahy** &gt; **Přehled**.

2.  Na stránce **Přehled výstrah** najdete tyto informace:

    -   První tři výstrahy, které se dají řadit podle data, kategorie nebo závažnosti

    -   Celkový počet aktivních výstrah

3.  Kliknutím na **Všechny výstrahy** zobrazíte na stránce **Výstrahy** následující informace. Jako první se zobrazují kritické výstrahy:

    -   **Název** – název typu generované výstrahy.

    -   **Zdroj** – odkaz na zdroj výstrahy.  Pokud je prahová hodnota pro zobrazení tohoto typu výstrahy nastavená na **Vše**, zobrazí tento odkaz jedno zařízení, kterého se výstraha týká.  Když je prahová hodnota pro zobrazení tohoto typu výstrahy nastavená na nějakou hodnotu, zobrazí tento odkaz seznam všech zařízení, kterých se tato výstraha týká.

    -   **Poslední aktualizace** – ukazuje čas poslední změny výstrahy. Pokud je výstraha zavřená, zobrazuje se čas zavření výstrahy.

    -   **Závažnost** – označuje závažnost výstrahy.

### <a name="BKMK_Whattodo"></a>Co dělat, když se klient z konzoly pro správu Microsoft Intune neodinstaluje

##### Odebrání klientského softwaru pomocí nástroje příkazového řádku Microsoft Intune

1.  Otevřete příkazový řádek v režimu správce.

2.  Přejděte do složky *%programfiles%\Microsoft\OnlineManagement\Common*.

3.  Spusťte tento příkaz: **ProvisioningUtil.exe /UninstallAgents /MicrosoftIntune**.

### Kódy chyb instalace klientů
Kódy chyb, které se zobrazují na stránce **Výstrahy**, když se instalace klientského softwaru nepovede, popisuje následující tabulka. Obsahuje taky návrhy, jak příslušný problém vyřešit.

|Kód chyby|Možný problém|Navržené řešení|
|-------------|-----------------|-------------------|
|**0x80CF0437**|Na hodinách klientského počítače není nastavený správný čas.|Zkontrolujte, jestli jsou na klientském počítači správně nastavené hodiny a časové pásmo.|
|**0x80240438**, **0x80CF0438**, **0x80CF401B**|Nedá se připojit ke službě [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]. Zkontrolujte nastavení proxy serveru klienta.|Ověřte, že [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] konfiguraci proxy serveru na klientském počítači podporuje a že má klientský počítač přístup na internet. Další informace o podporovaných konfiguracích proxy serveru najdete v tématu [Pomoc se zabezpečením počítačů s Windows pomocí služby Endpoint Protection pro Microsoft Intune](../Topic/Help_secure_Windows_PCs_with_Endpoint_Protection_for_Microsoft_Intune.md).|
|**0x80CF402C**|Nedá se připojit ke službě [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]. Zkontrolujte připojení k síti.|Ověřte, že je počítač připojený k síti. Zkontrolujte, jestli je připojený síťový kabel, případně jestli je zapnutá bezdrátová síť.|
|**0x80240438, 0x80CF0438**|Není nakonfigurované nastavení proxy serveru v Internet Exploreru a v místním systému.|Zkontrolujte nastavení proxy serveru klienta a ověřte, že [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] konfiguraci proxy serveru na klientském počítači podporuje a že má klientský počítač přístup na internet. Další informace o podporovaných konfiguracích proxy serveru najdete v tématu [Pomoc se zabezpečením počítačů s Windows pomocí služby Endpoint Protection pro Microsoft Intune](../Topic/Help_secure_Windows_PCs_with_Endpoint_Protection_for_Microsoft_Intune.md).|
|**0x80043001**|Registrační balíček je zastaralý.|Z pracovního prostoru **Správce** si stáhněte aktuální balíček klientského softwaru a nainstalujte ho. Pokyny najdete v tématu [Instalace klienta na počítači s Windows pomocí Microsoft Intune](../Topic/Install_the_Windows_PC_client_with_Microsoft_Intune.md).|
|**0x80043004**|Předplatné neexistuje nebo je deaktivované.|Ověřte, že je váš účet a předplatné [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] pořád aktivní. Jestli se chcete podívat na nastavení svého účtu, přihlaste se k němu na [portálu účtů Microsoft Intune](http://go.microsoft.com/fwlink/?LinkId=247978).|
|**0x80043002**|Účet je v režimu údržby.|Když je účet v režimu údržby, nemůžete registrovat nové klientské počítače. Jestli se chcete podívat na nastavení svého účtu, přihlaste se k němu na [portálu účtů Microsoft Intune](http://go.microsoft.com/fwlink/?LinkId=247978).|
|**0x80043003**|Účet je odstraněný.|Ověřte, že je váš účet a předplatné [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] pořád aktivní. Jestli se chcete podívat na nastavení svého účtu, přihlaste se k němu na [portálu účtů Microsoft Intune](http://go.microsoft.com/fwlink/?LinkId=247978).|
|**0x80043005**|Klientský počítač je vyřazený.|Pár hodin počkejte, odeberte z počítače všechny starší verze klientského softwaru s pak zkuste nainstalovat klientský software znova. Pokyny naleznete v části [What to do if the client will not uninstall from the Microsoft Intune administrator console](../Topic/Troubleshoot_Endpoint_Protection_in_Microsoft_Intune.md#BKMK_Whattodo).|
|**0x80043006**|Bylo dosaženo maximálního počtu licencí povolených pro účet.|Abyste mohli ve službě zaregistrovat víc klientských počítačů, musí si vaše organizace koupit další licence.|
|**0x80043007**|Ve složce s instalačním programem se nenašel soubor certifikátu.|Než začnete s instalací, extrahujte všechny soubory. Žádné extrahované soubory nepřejmenovávejte ani nepřemísťujte: všechny soubory musí být ve stejné složce, jinak se instalace nepovede. Další informace najdete v části [Instalace klienta na počítači s Windows pomocí Microsoft Intune](../Topic/Install_the_Windows_PC_client_with_Microsoft_Intune.md).|
|**0x8024D015**, **0x00240005**, **0x80070BC2**, **0x80070BC9**, **0x80CFD015**|Software nejde nainstalovat, protože se čeká na restartování klientského počítače.|Restartujte počítač a pak zkuste nainstalovat klientský software znova.|
|**0x80070032**|Na klientském počítači se nenašel nejmíň jeden softwarový produkt, který je podmínkou pro instalaci klientského softwaru.|Ujistěte se, že jsou na klientském počítači nainstalované všechny požadované aktualizace, a pak zkuste nainstalovat klientský software znova. Další informace o součástech požadovaných pro instalaci klientského softwaru najdete v tématu [Požadavky na síťovou infrastrukturu pro Microsoft Intune](../Topic/Network_infrastructure_requirements_for_Microsoft_Intune.md).|
|**0x80043008**|Nešlo spustit službu Microsoft Online Management Updates.|Kontaktujte [podporu](http://go.microsoft.com/fwlink/?LinkID=246606).|
|**0x80043009**|Klientský počítač je ve službě už zaregistrovaný.|Abyste mohli klientský počítač ve službě zaregistrovat znovu, musíte ho nejdřív vyřadit. Pokyny naleznete v části [What to do if the client will not uninstall from the Microsoft Intune administrator console](../Topic/Troubleshoot_Endpoint_Protection_in_Microsoft_Intune.md#BKMK_Whattodo).|
|**0x8004300B**|Instalační balíček klientského softwaru nejde spustit, protože verze Windows, která běží na klientovi, není podporovaná.|[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] nepodporuje verzi Windows, která běží na klientském počítači. Seznam podporovaných operačních systémů najdete v tématu [Požadavky na síťovou infrastrukturu pro Microsoft Intune](../Topic/Network_infrastructure_requirements_for_Microsoft_Intune.md).|
|**0xAB2**|Instalační služba systému Windows nemohla získat přístup k modulu VBScript runtime pro vlastní akci.|Tato chyba je způsobená nějakou vlastní akcí založenou na dynamických knihovnách DLL (Dynamic-Link Library). Při odstraňování problémů s knihovnou DLL budete nejspíš muset použít nástroje popsané v [článku 198038 znalostní báze podpory Microsoftu: Užitečné nástroje při problémech s balíčky a nasazením](http://go.microsoft.com/fwlink/?LinkID=234255).|
|**0x8004300f**|Software se nedá nainstalovat, protože už je nainstalovaný klient nástroje System Center Configuration Manager.|Odeberte klienta nástroje Configuration Manager a pak zkuste nainstalovat klientský software znova.|
|**0x80043010**|Software se nedá nainstalovat, protože už je nainstalovaný klient OMADM (Open Mobile Alliance Device Management).|Zrušte registraci klienta OMADM a pak zkuste nainstalovat klientský software znova.|
Pokud se budou problémy s instalací vyskytovat i dál, kontaktujte [podporu](http://go.microsoft.com/fwlink/?LinkID=246606). Je potřeba mít připravený protokol o registraci klientského počítače (najdete ho tady: %*programfiles*%\Microsoft\OnlineManagement\Logs\Enrollment.log a %*userprofile*%\AppData\Local\Microsoft\OnlineManagement\Logs\Enrollement.log) a protokol služby Windows Update (%*windir*%\windowsupdate.log), abyste ho mohli ukázat technikům podpory.

