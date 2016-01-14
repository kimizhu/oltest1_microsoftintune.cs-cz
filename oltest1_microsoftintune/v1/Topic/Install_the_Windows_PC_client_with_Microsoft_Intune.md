---
description: na
keywords: na
title: Install the Windows PC client with Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 64c11e53-8d64-41b9-9550-4b4e395e8c52
---
# Instalace klienta na poč&#237;tači s Windows pomoc&#237; Microsoft Intune
Tento průvodce vám pomůže nastavit správu vašich počítačů pomocí [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)].

## <a name="BKMK_Before"></a>Než začnete
Před zahájením instalace klientského softwaru [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] si přečtěte téma [Řešení konfliktů GPO a zásad Microsoft Intune](../Topic/Resolve_GPO_and_Microsoft_Intune_policy_conflicts.md), abyste zjistili, co musíte zajistit pro správnou instalaci klienta, a pak se k těmto pokynům vraťte.

## Instalace klienta
Pomocí těchto kroků nainstalujte klienta:

-   [Stažení klientského softwaru](../Topic/Install_the_Windows_PC_client_with_Microsoft_Intune.md#BKMK_DL)

Pak klienta nechte nainstalovat pomocí jednoho nebo více z těchto způsobů:

-   [Ruční nasazení klientského softwaru](../Topic/Install_the_Windows_PC_client_with_Microsoft_Intune.md#BKMK_Manual)

-   [Automatické nasazení klientského softwaru pomocí zásad skupiny](../Topic/Install_the_Windows_PC_client_with_Microsoft_Intune.md#BKMK_GP)

-   [Jak můžou uživatelé svoje počítače sami zaregistrovat](../Topic/Install_the_Windows_PC_client_with_Microsoft_Intune.md#BKMK_Allow)

-   [Instalace klientského softwaru Microsoft Intune v rámci bitové kopie](../Topic/Install_the_Windows_PC_client_with_Microsoft_Intune.md#BKMK_Image)

Pokud už počítač s [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] spravovat nepotřebujete, můžete ho vyřadit. Tím se taky z počítače odebere klientský software. Další informace naleznete v části [Běžné úlohy správy počítačů s Windows pomocí počítačového klienta Microsoft Intune](../Topic/Common_Windows_PC_management_tasks_with_the_Microsoft_Intune_computer_client.md).

### <a name="BKMK_DL"></a>Stažení klientského softwaru

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com/) klikněte na **Správce** &gt; **Stažení klientského softwaru**

2.  Na stránce **Stažení klientského softwaru** klikněte na **Stáhnout klientský software** a uložte balíček **Microsoft_Intune_Setup.zip** obsahující software do zabezpečeného umístění v síti.

    > [!NOTE]
    > Instalační balíček klientského softwaru [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] obsahuje informace o vašem účtu. Pokud k instalačnímu balíčku získají přístup neoprávnění uživatelé, můžou zaregistrovat počítače k účtu, který je zastoupený svým vloženým certifikátem.

3.  Extrahujte obsah instalačního balíčku do zabezpečeného umístění v síti.

    > [!IMPORTANT]
    > Soubor **ACCOUNTCERT**, který se extrahuje, nepřejmenovávejte ani neodebírejte, jinak se instalace klientského softwaru nezdaří.

### <a name="BKMK_Manual"></a>Ruční nasazení klientského softwaru

1.  Na počítači přejděte do složky, kde se nacházejí instalační soubory klientského softwaru, a spuštěním souboru **Microsoft_Intune_Setup.exe** klientský software nainstalujte.

    > [!NOTE]
    > Stav instalace se zobrazí, když ukazatel myši přesunete na ikonu v oznamovací oblasti v klientském počítači.

### <a name="BKMK_GP"></a>Automatické nasazení klientského softwaru pomocí zásad skupiny

1.  Ve složce, která obsahuje soubory **Microsoft_Intune_Setup.exe** a **MicrosoftIntune.accountcert**, spusťte následující příkaz k extrakci instalačních programů založených na Instalační službě systému Windows pro 32bitové a 64bitové počítače:

    ```
    Microsoft_Intune_Setup.exe/Extract <destination folder>
    ```

2.  Zkopírujte soubory **Microsoft_Intune_x86.msi**, **Microsoft_Intune_x64.msi** a **MicrosoftIntune.accountcert** do umístění v síti, ke kterému mají přístup všechny počítače, na které se má klientský software nainstalovat.

    > [!IMPORTANT]
    > Soubory od sebe neoddělujte ani nepřejmenovávejte, jinak se instalace klientského softwaru nezdaří.

3.  Pomocí zásad skupiny nasaďte software do počítačů v síti.

    Další informace o tom, jak automaticky nasadit software pomocí zásad skupiny, najdete v dokumentaci k Windows Serveru.

### <a name="BKMK_Allow"></a>Jak můžou uživatelé svoje počítače sami zaregistrovat
Uživatelé můžou každý ze svých počítačů sami zaregistrovat prostřednictvím firemního portálu [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]. Každý zaregistrovaný počítač se propojí s uživatelským účtem použitým při instalaci klientského softwaru.

> [!NOTE]
> -   Aby mohl uživatel klientský software nainstalovat, musí být na počítači správcem.
> -   Vlastní registrace uživatelem vyžaduje, aby byl na klientském počítači nainstalovaný Internet Explorer.
> -   Pokaždé, když uživatel sám zaregistruje počítač, použije se licence [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].
> -   Pro vlastní registraci počítače musíte použít pracovní nebo školní účet. Pomocí účtu Microsoft sami počítač zaregistrovat nemůžete.
> -   Pokud je už klientský software na počítači nainstalovaný, koncovému uživateli se zobrazí chyba.

##### Vlastní registrace počítače (informace pro koncové uživatele)

1.  Přihlaste se k firemnímu portálu z počítače, který chcete zaregistrovat.

2.  Klikněte na **Přidat zařízení**.

3.  Klikněte na **Stáhnout software** a potom na **Spustit**.

4.  Kliknutím na **Další** spusťte průvodce instalací [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)].

5.  Po dokončení průvodce instalací klikněte na **Dokončit**.

### <a name="BKMK_Image"></a>Instalace klientského softwaru Microsoft Intune v rámci bitové kopie
Klientský software [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] můžete do počítačů nasadit v rámci bitové kopie operačního systému. Jako příklad poslouží tento základní postup:

1.  Zkopírujte instalační soubory klienta, **Microsoft_Intune_Setup.exe** a **MicrosoftIntune.accountcert**, do složky **%Systemdrive%\Temp\Microsoft_Intune_Setup** na referenčním počítači.

2.  Vytvořte položku registru **WindowsIntuneEnrollPending** přidáním následujícího příkazu do skriptu **SetupComplete.cmd**:

    ```
    %windir%\system32\reg.exe add HKEY_LOCAL_MACHINE\Software\Microsoft\Onlinemanagement\Deployment /v WindowsIntuneEnrollPending /t REG_DWORD /d 1
    ```

3.  Přidáním následujícího příkazu do skriptu **setupcomplete.cmd** spusťte registrační balíček s argumentem příkazového řádku /PrepareEnroll:

    ```
    %systemdrive%\temp\Microsoft_Intune_Setup\Microsoft_Intune_Setup.exe /PrepareEnroll
    ```
    > [!TIP]
    > Skript **SetupComplete.cmd** umožňuje, aby instalační program systému Windows provedl změny systému před přihlášením uživatele. Argument příkazového řádku **/PrepareEnroll** připraví cílový počítač, aby se po dokončení instalačního programu systému Windows automaticky zaregistroval do [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

4.  Skript **SetupComplete.cmd** umístěte do složky **%Windir%\Setup\Scripts** na referenčním počítači.

5.  Vytvořte bitovou kopii referenčního počítače a pak ji nasaďte do cílových počítačů.

Když se cílový počítač po dokončení instalačního programu systému Windows restartuje, vytvoří se klíč registru **WindowsIntuneEnrollPending**. Registrační balíček ověří, jestli je počítač zaregistrovaný. Pokud je počítač zaregistrovaný, neprovede se žádná další akce. Pokud počítač zaregistrovaný není, registrační balíček vytvoří automatickou úlohu registrace [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)].

Když se automatická úloha registrace [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] v následujícím naplánovaném čase spustí, zkontroluje existenci hodnoty registru **WindowsIntuneEnrollPending** a pokusí se cílový počítač zaregistrovat do [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Pokud se registrace z jakéhokoli důvodu nezdaří, při dalším spuštění úlohy se pokus o registraci opakuje. Opakované pokusy pokračují po dobu jednoho měsíce.

Automatická úloha registrace [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], hodnota registru **WindowsIntuneEnrollPending** a certifikát účtu se z cílového počítače po úspěšné registraci nebo po jednom měsíci odstraní.

## <a name="BKMK_Monitor"></a>Sledování a ověření úspěšného nasazení klienta
Pomocí některého z následujících postupů můžete sledovat a ověřit úspěšné nasazení klienta.

#### Ověření instalace klientského softwaru v konzole správce Microsoft Intune

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com/) klikněte na **Skupiny** &gt; **Všechna zařízení** &gt; **Všechny počítače**.

2.  Posuňte se dolů na seznamu počítačů a najděte spravované počítače, které komunikují pomocí [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], nebo vyhledejte konkrétní spravovaný počítač zadáním názvu počítače nebo libovolné části názvu do pole **Vyhledat zařízení**.

3.  Ve spodním podokně konzole zkontrolujte stav počítače a vyřešte případné chyby.

#### Vytvoření sestavy inventáře počítače pro zobrazení všech zaregistrovaných počítačů

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com/) klikněte na **Sestavy** &gt; **Sestavy inventáře počítače**.

2.  Na stránce **Vytvořit novou sestavu** nechte ve všech polích výchozí hodnoty (pokud nechcete použít filtry) a klikněte na **Zobrazit sestavu**.

3.  Stránka **Sestava inventáře počítače** se otevře v novém okně s uvedením všech počítačů, které jsou úspěšně zaregistrované v [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

    > [!TIP]
    > Kliknutím na záhlaví libovolného sloupce v sestavě seřadíte seznam podle obsahu sloupce.

## Potřebujete další pomoc?
Další nápovědu a podporu najdete v tématu [Řešení potíží se službou Endpoint Protection v Microsoft Intune](../Topic/Troubleshoot_Endpoint_Protection_in_Microsoft_Intune.md).

## Viz také
[Správa počítačů s Windows pomocí Intune](../Topic/Manage_Windows_PCs_with_Microsoft_Intune.md)

