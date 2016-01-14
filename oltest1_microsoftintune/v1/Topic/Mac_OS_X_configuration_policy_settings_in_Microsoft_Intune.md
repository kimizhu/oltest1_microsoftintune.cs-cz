---
description: na
keywords: na
title: Mac OS X configuration policy settings in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 98b2f19b-bee8-42d7-a215-a716d56a25a3
---
# Nastaven&#237; z&#225;sad konfigurace pro Mac OS X v Microsoft Intune
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]**Zásadu obecné konfigurace pro Mac OS X** můžete použít ke konfiguraci těchto nastavení:

-   **Nastavení zabezpečení zařízení** – vyberte některou možnost ze seznamu předdefinovaných nastavení, která umožňují kontrolovat rozsah vlastností a funkcí zařízení.

-   **Seznam aplikací dodržujících a nedodržujících předpisy** – Určete seznam aplikací, které splňují nebo nesplňují předpisy ve vaší společnosti. Sestavu aplikací nesplňujících požadavky můžete použít k zobrazení shody aplikací, které zadáte v seznamu, s aplikacemi, které si uživatelé nainstalovali (sestava neslouží ke skutečnému zablokování instalace aplikací).

## Vytvoření obecných zásad konfigurace pro Mac OS X

#### Zadání základního nastavení pro zásadu konfigurace

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com) klikněte na **Zásady** &gt; **Přehled** &gt; **Přidat zásadu**.

2.  Klikněte na **Mac OS X** &gt; **Obecná konfigurace** a pak klikněte na **Vytvořit zásadu**.

    > [!NOTE]
    > Nedaří se vám vytvořit zásadu konfigurace pomocí doporučovaného nastavení. Je potřeba vytvořit vlastní zásadu.

3.  V části **Obecné** stránky **Vytvořit zásadu** zadejte název a popis nové zásady.

4.  Informace v následujících částech vám pomůžou zadat nastavení zásad.

5.  Po dokončení klikněte na **Uložit zásadu**.

Nová zásada se zobrazí v uzlu **Zásady konfigurace** pracovního prostoru **Zásady**.

## Nastavení pro zařízení Mac OS X
Pokud se hledané nastavení v seznamu nezobrazí, můžete k jeho vytvoření použít vlastní zásady systému Mac OS X, které umožňují importovat nastavení vytvořená v nástroji Apple Configurator. Další informace naleznete v části [Nastavení vlastních zásad pro Mac OS X v Microsoft Intune](../Topic/Mac_OS_X_custom_policy_settings_in_Microsoft_Intune.md).

### Nastavení hesla

|Název nastavení|Popis|
|-------------------|---------|
|**Vyžadovat heslo k odemknutí zařízení**|Určuje, jestli uživatel musí pro přístup k počítači Mac použít heslo. **Important:** Na rozdíl od zařízení iOS se na zařízení Mac OS X uživateli hned nezobrazí upozornění, že si má aktualizovat heslo, aby byla tato zásada dodržena.|
|**Vyžadovaný typ hesla**|Určuje, jestli je možné použít jenom číselné heslo nebo je potřeba použít **alfanumerické** heslo (obsahuje písmena i číslice). **Important:** Toto nastavení je podporované jenom v Mac OS X 10.10.3 a v novějších verzích.|
|**Počet složitých znaků požadovaných v hesle**|Určuje požadovaný počet složitých znaků v hesle (**0** až **4**).<br /><br />Složitý znak je třeba otazník (**?**).|
|**Minimální délka hesla**|Určuje minimální délku hesla (**4** až **14** znaků).|
|**Povolit jednoduchá hesla**|Dovoluje jednoduchá hesla, jako je „**0000**“ nebo „**1234**“.|
|**Počet minut nečinnosti před vyžadováním hesla**|Určuje, jak dlouho musí být počítač neaktivní, aby k jeho odemčení bylo potřeba heslo.|
|**Vypršení platnosti hesla (dny)**|Určuje, jek dlouho si může uživatel nechat stejné heslo, než ho bude muset změnit (**1**–**255** dnů).|
|**Pamatovat si historii hesel**|Nastavení brání uživateli, aby opakovaně použil už jednou použité heslo. Pokud nastavení použijete, můžete taky nastavit **Zakázat opakované použití předchozích hesel** a zadat počet použitých hesel, která se nesmí znova použít (**1**–**24**).|
|**Počet minut nečinnosti před aktivací šetřiče obrazovky**|Určuje, jak dlouho musí být počítač nečinný, než se aktivuje šetřič obrazovky.|

## Nastavení pro aplikace dodržující a nedodržující předpisy
V **seznamu kompatibilních a nekompatibilních aplikací pro Mac OS X** aktivujte **Spravované nastavení pro zařízení** a pak zadejte seznam kompatibilních a nekompatibilních aplikací. Můžete použít následující informace:

> [!NOTE]
> Jedna zásada může obsahovat seznam jenom kompatibilních, nebo jenom nekompatibilních aplikací. Nejde zadat oba seznamy v jedné zásadě.
> 
> [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] umožňuje generovat sestavu zařízení s nekompatibilními aplikacemi. Služba neblokuje instalaci nekompatibilních aplikací, ani je neodebírá.

|Název nastavení|Popis|
|-------------------|---------|
|**Ohlásit nekompatibilitu, když uživatelé nainstalují aplikace ze seznamu**|Seznam aplikací pro Mac OS X, které uživatelé nesmí instalovat. Pokud si uživatelé některé z těchto aplikací nainstalují, objeví se na **sestavách aplikací nesplňujících požadavky**.|
|**Ohlásit nekompatibilitu, když uživatelé nainstalují aplikace, které nejsou na seznamu**|Seznam aplikací pro Mac OS X, které uživatelé smí instalovat. Pokud si uživatelé nainstalují nějaké jiné aplikace, objeví se na **sestavách aplikací nesplňujících požadavky**.|
|**Přidat**|Přidá aplikaci do vybraného seznamu. Zadejte vybraný název aplikace, můžete taky zadat jejího vydavatele a ID sady. **Tip:** Pokud chcete na počítači Mac s nainstalovanou aplikací zjistit ID sady, použijte následující postup:<ol><li>Otevřete složku, ve které je aplikace nainstalovaná (třeba **/Applikace**).</li><li>Vyberte sadu *&lt;Název aplikace&gt;***.app** a zvolte **Zobrazit obsah balíčku**.</li><li>Otevřete soubor **Info.plist**.</li><li>Zkontrolujte hodnotu přiřazenou klíči **CFBundleIdentifier**.</li></ol>Formát ID sady je **com.contoso.nazevaplikace**.|
|**Importovat aplikace**|Importuje seznam aplikací, které jste zadali v souboru hodnot oddělených čárkami. Použije se formát, název aplikace, vydavatel a ID sady aplikace v souboru.|
|**Upravit**|Umožňuje upravit název, vydavatele a ID sady vybrané aplikace.|
|**Odstranit**|Odstraní vybranou aplikaci ze seznamu.|
> [!TIP]
> Další informace o sestavách nástroje [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] naleznete v tématu [Pochopení operací Microsoft Intune pomocí sestav](../Topic/Understand_Microsoft_Intune_operations_by_using_reports.md).

## Nasazení zásad konfigurace
Nasaďte zásadu konfigurace do jedné nebo víc skupin uživatelů nebo zařízení ve vaší organizaci.

Další informace o nasazování zásad najdete v tématu [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

Souhrn stavu a výstrahy v pracovním prostoru **Zásada** určují problémy se zásadou, které vyžadují vaši pozornost. Kromě toho se v pracovním prostoru **Řídicí panel** zobrazí shrnutí stavu.

> [!IMPORTANT]
> Když je zařízení s Mac OS X v režimu spánku, zásady a profily nejdou doručovat ani inventarizovat. Konzola [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] tak může dočasně zobrazovat stav **Nastavení zásad obsahující chybu**, dokud se zařízení nevzbudí z režimu spánku.

## Monitorování aplikací, které splňují a nesplňují předpisy
Pokud se chcete podívat, jestli se dodržuje seznam zadaných aplikací, použijte **sestavy aplikací nesplňujících požadavky**.

#### Spuštění sestavy

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com) klikněte na **Sestavy** &gt; **Sestavy aplikací nesplňujících požadavky**.

2.  Vyberte skupiny zařízení, které chcete zkontrolovat, určete, jestli kontrolovat kompatibilní aplikace, nekompatibilní aplikace nebo obojí a pak klikněte na **Zobrazit sestavu**.

## Viz také
[Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

