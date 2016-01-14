---
description: na
keywords: na
title: Troubleshoot app deployment problems in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 28ac298e-fb73-4c1c-b3fd-8336639e05e6
---
# Řešen&#237; probl&#233;mů s nasazen&#237;m aplikac&#237; v Microsoft Intune
Toto téma obsahuje materiály, které pomáhají při řešení problémů s nasazením aplikací přes [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)].

## <a name="BKMK_TypicalProblems"></a>Pomoc při řešení obvyklých problémů s nasazováním aplikací

#### Pokud se nemůže přihlásit k [!INCLUDE[wit_iwportal_1](../Token/wit_iwportal_1_md.md)]

1.  Zkontrolujte, jestli účet existuje v [!INCLUDE[wit_icp_1](../Token/wit_icp_1_md.md)] nebo jestli není zakázaný.

2.  Ujistěte se, že je pro vás zřízený tento účet v aplikaci [!INCLUDE[wit_icp_1](../Token/wit_icp_1_md.md)].

3.  V aplikaci [!INCLUDE[wit_icp_1](../Token/wit_icp_1_md.md)] musíte používat správné uživatelské jméno a heslo k přihlášení do [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] ve formátu **joe@domain.com**.

#### Pokud v aplikaci Portál společnosti chybí kontaktní informace na IT oddělení

1.  V konzole [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] klikněte na **Správce** &gt; **Portál společnosti**.

2.  Nastavte kontaktní údaje pro **kontaktování IT oddělení**.

#### Pokud nevidíte konkrétní aplikace v seznamu

1.  Ujistěte se, že se díváte seznam aplikací pro uživatele nebo zařízení, pro které se aplikace nasadila.

2.  Ujistěte se, že zařízení splňuje nezbytné požadavky na zařízení.

#### Pokud se vám při stahování aplikace zobrazí chybová zpráva

1.  Ujistěte se, že na jednotlivé uživatele nepřipadá moc velký počet souběžných stahování. Každý uživatel může najednou stahovat jenom jednu aplikaci.

2.  Ujistěte se, že na jednotlivé účty nepřipadá moc velký počet souběžných stahování. Počkejte několik minut a potom to zkuste znova.

3.  Pokud se zobrazí nativní zpráva iOS s informacemi o tom, že nemůžete instalovat, že instalace je zrušená nebo že to musíte zkusit znova, může to být způsobené aktuálně vysokou návštěvností. Počkejte několik minut a potom to zkuste znova.

4.  Pokud indikátor průběhu stahování iOS aplikace ukazuje dokončení, ale aplikace nejde nainstalovat, bude nejspíš chyba v souborech aplikace, které jste dali k dispozici.

#### Pokud kliknutím na odkaz na iOS aplikaci přejdete do předchozího umístění v iTunes App Storu

1.  Aktuální relace iTunes App Storu se otevírá na předchozí stránce aplikace.

2.  Zavřete iTunes App Store na zařízení a zkuste odkaz použít znovu.

#### Pokud se vám při spouštění iOS aplikace zobrazí chyba

1.  Datum vypršení platnosti aplikace nemusí být platné.

#### Pokud se vám aplikace „zasekne“ při nahrávání

1.  Při nahrávání aplikace se nejdřív přidají metadata a pak balíček aplikace. Až se nahrají metadata, začne se aktualizovat průběh nahrávání aplikace. Pokud zjistíte, že vám aplikace zůstala viset v jednom stavu průběhu nahrávání po neobvykle dlouhou dobu, odstraňte aplikaci a nahrajte ji znovu.

2.  Pokud takto aplikace takto zůstane viset, nespravujte její nasazení.

#### Pokud dojde k chybě při instalaci iOS aplikace

1.  Ujistěte se, že brána firewall vaší organizace umožňuje přístup na weby zřizování a certifikace společnosti Apple.

2.  Další informace najdete v dokumentaci pro vývojáře Apple.

#### Pokud spravované aplikace nehlásí stav instalace

-   Stav instalace se pro instalace spravovaných aplikací před aktualizací služby Microsoft Intune v listopadu 2014 neshromažďoval. Pro zařízení, na které se nainstalovaly spravované aplikace před aktualizací této služby, aktualizujte nasazení každé přidružené aktualizace pomocí odpovídající akce nasazení (například **Dostupná instalace**). Každé zařízení aplikaci aktualizuje během automatického zjišťování dostupnosti aplikací. Další informace naleznete v části [Aktualizace aplikací pomocí služby Microsoft Intune](../Topic/Update_apps_using_Microsoft_Intune.md).

## <a name="BKMK_SoftDistErrorCodes"></a>Kódy chyb nasazení aplikací
V následující tabulce najdete běžné chyby, ke kterým může dojít během nasazování aplikací [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], pravděpodobné příčiny a možná řešení.

|Kód chyby|Možný problém|Navržené řešení|
|-------------|-----------------|-------------------|
|0x80073CFF<br /><br />0x80CF201C (chyba klienta)|Pro instalaci této aplikace musíte mít systém s podporou zkušebního načtení.|Ujistěte se, že je balíček aplikace podepsaný důvěryhodným podpisem a nainstalovaný na zařízení připojeném k doméně, které má povolenou zásadu AllowAllTrustedApps, nebo zařízení, které má licenci pro zkušební načtení systému Windows s povolenou zásadou AllowAllTrustedApps (aplikuje se při registraci zařízení s Windows RT).|
|0x80073CF0|Balíček se nepodařilo otevřít.|Možné příčiny:<br /><br />-   Balíček není podepsaný.<br />-   Název vydavatele neodpovídá subjektu podpisového certifikátu.<br /><br />Další informace najdete v protokolu událostí AppxPackagingOM.|
|0x80073CF3|Selhalo ověření aktualizace, závislostí nebo konfliktů balíčku.|Možné příčiny:<br /><br />-   Příchozí balíček je v konfliktu s nainstalovaným balíčkem.<br />-   Nebyla nalezena zadaná závislost balíčku.<br />-   Balíček nepodporuje správnou architekturu procesoru.<br /><br />Další informace najdete v protokolu událostí AppXDeployment-Server.|
|0x80073CFB|Zadaný balíček je už nainstalovaný a přeinstalace balíčku je blokovaná.|Tato chybová zpráva se může zobrazit při instalaci balíčku, který není totožný s balíčkem, který už je nainstalovaný. Potvrďte, že součástí balíčku je i digitální podpis. Pokud se balíček znovu vytvoří nebo znovu podepíše, nebude už tento balíček při bitovém porovnání totožný s dříve nainstalovaným balíčkem. Tuto chybu můžete odstranit jedním ze dvou způsobů:<br /><br />-   Zvýšíte číslo verze aplikace a pak balíček znova sestavíte a podepíšete.<br />-   Než budete instalovat nový balíček, odeberte starý balíček pro každého uživatele v systému.|

## Viz také
[Řešení potíží s Microsoft Intune](../Topic/Troubleshoot_Microsoft_Intune.md)
[Nasazení a konfigurace aplikací v Microsoft Intune](../Topic/Deploy_and_configure_apps_with_Microsoft_Intune.md)

