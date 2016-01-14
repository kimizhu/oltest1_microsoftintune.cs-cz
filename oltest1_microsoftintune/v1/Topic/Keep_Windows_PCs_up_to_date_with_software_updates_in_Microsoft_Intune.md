---
description: na
keywords: na
title: Keep Windows PCs up to date with software updates in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 64ba8e58-fab1-4480-a440-164268810138
---
# Udržov&#225;n&#237; poč&#237;tačů s Windows v aktu&#225;ln&#237;m stavu d&#237;ky softwarov&#253;m aktualizac&#237;m v Microsoft Intune
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] vám může pomoct zabezpečit spravované počítače mnoha způsoby, včetně správy softwarových aktualizací, které udržují počítače v aktuálním stavu, protože zajišťují, že se rychle nainstalují nejnovější opravy a aktualizace.

Pokud jste ještě klienta [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] na počítače nenainstalovali, přečtěte si část [Instalace klienta na počítači s Windows pomocí Microsoft Intune](../Topic/Install_the_Windows_PC_client_with_Microsoft_Intune.md).

Jakmile jsou nové aktualizace dostupné na webu Microsoft Update nebo jste vytvořili aktualizaci jiného výrobce a tyto aktualizace se dají použít pro spravované počítače, na stránce **Přehled** pracovního prostoru **Aktualizace** se zobrazí oznámení. Po kliknutí na tenhle odkaz oznámení pak můžete dělat různé operace, třeba zobrazit další informace o aktualizaci, přijmout nebo nepřijmout aktualizaci a zobrazit počítače, na které se tahle aktualizace bude po schválení instalovat.

> [!IMPORTANT]
> Pracovní prostor **Aktualizace** se v konzole pro správu nezobrazí, dokud nenainstalujete klienta aspoň na jeden počítač, který budete úspěšně spravovat.

Když aktualizace schválíte a nainstalujete, můžete v pracovním prostoru **Aktualizace** konzoly [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] zkontrolovat, jestli byla instalace úspěšná nebo neúspěšná.

V dalších částech se dozvíte, jak udržovat software na spravovaných počítačích v aktuálním stavu.

## Než začnete
Než začnete vytvářet a schvalovat aktualizace softwaru, nakonfigurujte a nasaďte zásady na svých počítačích, které určují, kdy a jak se budou aktualizace instalovat.

#### Konfigurace nastavení zásad aktualizací

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com/) klikněte na **Zásady** &gt; **Přehled** &gt; **Přidat zásadu**.

2.  Nakonfigurujte a nasaďte zásady **nastavení agenta Microsoft Intune** pro nastavení aktualizací. Můžete použít doporučená nastavení nebo nastavení upravit. Pokud potřebujete další informace o tom, jak vytvořit a nasadit zásady, přečtěte si téma [Běžné úlohy správy počítačů s Windows pomocí počítačového klienta Microsoft Intune](../Topic/Common_Windows_PC_management_tasks_with_the_Microsoft_Intune_computer_client.md).

    Následující tabulka zobrazuje hodnoty, které můžete v zásadách konfigurovat, a taky doporučené hodnoty, které se použijí, pokud zásady neupravíte. Tahle nastavení najdete v části **Aktualizace**.

    |Nastavení zásad|Další informace|
    |-------------------|-------------------|
    |**Četnost detekce aktualizací a aplikací (hodiny)**|Určuje, jak často (od 8 do 22 hodin) [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] kontroluje nové aktualizace a aplikace.<br /><br />Doporučená hodnota: **8** hod.|
    |**Automatizovaná instalace aktualizací a aplikací nebo instalace aktualizací a aplikací s výzvami**|Určuje, jestli se mají aktualizace instalovat automaticky nebo jestli se má před instalací uživateli zobrazit výzva. Kromě toho vám tohle nastavení umožňuje naplánovat instalaci aktualizací a aplikací.<br /><br />-   **Instalace aktualizací a aplikací automaticky podle plánu** umožňuje instalovat aktualizace a aplikace, které používají určený plán.<br />    **Používat automatickou údržbu pro počítače se systémem Windows** jako závislé nastavení zásad určuje, jestli se mají aktualizace a aplikace instalovat při zobrazení okna automatické údržby Windows.<br />-   **Zobrazit uživateli výzvu k instalaci** vyzývá uživatele k instalaci aktualizací, jakmile jsou připravené.<br /><br />Doporučené hodnoty:<br /><br />-   Pokud vyberete **Instalovat aktualizace a aplikace automaticky podle plánu**<br />-   **Naplánovaný den: Denně**<br />-   **Naplánovaný čas: 3:00**<br />-   Pokud vyberete **Používat automatickou údržbu pro počítače se systémem Windows**|
    |**Umožnit okamžitou instalaci aktualizací, které nenaruší běh systému Windows**|-   Možnost **Povolit** umožňuje instalovat aktualizace hned po stažení s výjimkou aktualizací, které by přerušily nebo restartovaly Windows. Tyto aktualizace se instalují v závislosti na konfiguraci nastavení **Automatizovaná instalace aktualizací nebo instalace aktualizací s výzvami**.<br />-   Možnost **Nepovolit** umožňuje instalovat aktualizace závislosti na konfiguraci **Automatizovaná instalace aktualizací nebo instalace aktualizací s výzvami**.<br /><br />Doporučená hodnota: **Povolit**|
    |**Zpoždění restartu systému Windows po instalaci plánovaných aktualizací a aplikací (minuty)**|Určuje (1 až 30 minut) dobu čekání na restartování Windows po instalaci naplánovaných aktualizací a aplikací.<br /><br />Doporučená hodnota: **15 min.**|
    |**Zpoždění po restartu systému Windows při zahájení instalace dosud neprovedených plánovaných aktualizací nebo aplikací (minuty)**|Určuje (1 až 60 minut), jak dlouho se má čekat na spuštění instalace aktualizací a aplikací po restartování Windows, pokud nebyla nainstalovaná plánovaná aktualizace.<br /><br />Doporučená hodnota: **5 min.**|
    |**Povolit přihlášenému uživateli řídit restart systému Windows po instalaci plánovaných aktualizací a aplikací**|Určuje, jestli může přihlášený uživatel zpozdit restartování Windows (pokud se nastaví **Ano**), nebo jestli se má zobrazit upozornění na automatické restartování Windows (pokud se nastaví **Ne**). Pokud není po dokončení naplánované instalaci aktualizací a aplikací přihlášený žádný uživatel, Windows se v případě potřeby restartuje automaticky. Pokud nastavíte **Ne**, nastaví se ve výchozím nastavení doba před restartování Windows na 5 minut.<br /><br />Doporučená hodnota: **Ano**|
    |**Vyzvat uživatele k restartování Windows během povinných aktualizací klientského agenta [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]**|Určuje, jestli má být přihlášený uživatel vyzván k restartování Windows, pokud povinná aktualizace klienta [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] vyžaduje restartování Windows.<br /><br />Doporučená hodnota: **Ano**|
    |**Plán instalace povinných aktualizací klientského agenta Microsoft**|Umožňuje vytvořit plán při instalaci aktualizací klienta.<br /><br />Doporučená hodnota: nenakonfigurováno|
    |**Zpoždění mezi výzvami k restartu systému Windows po instalaci plánovaných aktualizací a aplikací (minuty)**|Určuje, jak často (1 až 1440 v minut) bude uživatel vyzván k restartování Windows při instalaci plánované aktualizace nebo aplikace, která vyžaduje restartování Windows, a uživatel zpozdí restartování.<br /><br />Doporučená hodnota: **30 min.**|

## Aktualizace softwaru od Microsoftu
Aktualizace softwaru Microsoftu nevyžaduje ze strany uživatele příliš mnoho zásahů. Než ale začnete, měli byste nakonfigurovat tahle dvě nastavení:

-   **Kategorie produktů a klasifikace aktualizací** – definuje kategorie a klasifikace aktualizací, které mají být dostupné pro počítače. Můžete se třeba rozhodnout, že chcete instalovat jen důležité aktualizace Microsoft Office.

-   **Pravidla pro automatické schválení** – tahle pravidla umožňují automaticky schválit určené typy aktualizace a snížit vaše režijní náklady na správu. Může se třeba stát, že budete chtít automaticky schvalovat všechny důležité aktualizace softwaru.

Použijte tyto dva postupy, které vám pomůžou s používáním aktualizací softwaru:

#### Konfigurace kategorií produktů a klasifikace aktualizací, které chcete zpřístupnit pro spravované počítače

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com/) klikněte na **Správce** &gt; **Aktualizace**.

2.  Na stránce **Nastavení služby: Aktualizace** vyberte v seznamu **Kategorie produktů** kategorie aktualizací, které mají být dostupné pro počítače. Ve výchozím nastavení jsou vybrané nejběžnější aktualizace.

    > [!IMPORTANT]
    > Aby počítače získávaly aktualizace schválené správcem, nesmí se nastavení zásady skupiny služby Windows Server Update Services (WSUS) **Určení umístění intranetového serveru služby Microsoft Update** použít na počítače, které byly zaregistrované s [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)].

3.  V seznamu **Klasifikace aktualizací** vyberte třídy aktualizace, která má být dostupná pro spravované počítače. Ve výchozím nastavení jsou opět vybrané nejběžnější možnosti.

4.  Požadovaný výběr uložíte kliknutím na **Uložit**.

#### Konfigurace pravidel automatického schvalování pro aktualizace softwaru

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com/) klikněte na **Správce** &gt; **Aktualizace**.

2.  V části **Pravidla automatického schvalování** stránky **Nastavení serveru: Aktualizace** klikněte na **Nový**.

3.  Na stránce **Obecné** v průvodci vytvořením pravidla automatického schvalování zadejte název a volitelný popis pravidla.

4.  Na stránce **Kategorie produktů** vyberte všechny produkty, pro které chcete automaticky schvalovat aktualizace.

5.  Na stránce **Klasifikace aktualizací** zadejte klasifikace aktualizací, které se mají automaticky schvalovat.

6.  Na stránce **Nasazení** udělejte tohle:

    -   Vyberte skupiny počítačů, na které chcete nasadit nové pravidlo, a klikněte na **Přidat**.

    -   Pokud chcete určit termín instalace aktualizací, zaškrtněte políčko **Vynutit konečný termín instalace těchto aktualizací** a pak v seznamu **Konečný termín instalace** vyberte termín instalace.

        > [!NOTE]
        > Pokud zadáte termín instalace, je možné, že budete muset spravovaný počítač po uplynutí intervalu konečného termínu jednou nebo víckrát restartovat.

    -   Jakmile budete hotovi, klikněte na **Další**.

7.  Na stránce **Souhrn** zkontrolujte nastavení pro nové pravidlo a klikněte na **Dokončit**.

Nové pravidlo najdete v části **Pravidla automatického schvalování** stránky **Nastavení služby: Aktualizace**.

> [!NOTE]
> Vytvořené pravidlo automatického schvalování bude schvalovat jen budoucí aktualizace, ale nebude automaticky schvalovat dřívější aktualizace, které jsou už ve [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Ke schválení těchto aktualizací musíte spustit pravidlo automatického schvalování. Další informace najdete v níže uvedeném tématu [Úpravy, spuštění nebo odstranění pravidla automaticky schválené aktualizace](../Topic/Keep_Windows_PCs_up_to_date_with_software_updates_in_Microsoft_Intune.md#BKMK_editrun).

### <a name="BKMK_editrun"></a>Úpravy, spuštění nebo odstranění pravidla automaticky schválené aktualizace

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com/) klikněte na **Správce** &gt; **Aktualizace**.

2.  V části **Pravidla automatického schvalování** vyberte pravidlo a pak udělejte jednu z těchhle věcí:

    -   Pokud chcete upravit pravidlo, klikněte na **Upravit** a změňte parametry pravidla v **průvodci vytvořením pravidla pro schválení automatické aktualizace**.

    -   Pravidlo spustíte kliknutím na **Spustit vybrané**.

    -   Pravidlo odstraníte kliknutím na **Odstranit**.

        > [!NOTE]
        > Odstranění pravidla nemá vliv na předchozí aktualizace schválené odstraněným pravidlem.

## Aktualizace jiného softwaru než od Microsoftu
Můžete nasadit aktualizace pro software jiného výrobce než Microsoftu. K tomu můžete použít průvodce **nahráváním aktualizací**, který vám umožňuje nahrát aktualizace do úložiště v cloudu, a pak aktualizaci schválit nebo odmítnout podobně jako u softwaru Microsoftu.

### <a name="procstartwiz"></a>Nahrání a konfigurace aktualizace jiného výrobce

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com/) klikněte na **Aktualizace** &gt; **Přehled** &gt; **Nahrát**.

2.  Na stránce **Soubory aktualizace** klikněte na **Procházet** a vyberte instalační soubory potřebné k instalaci balíčku aktualizace. Tímto souborem může být soubor instalační služby Windows (.msi), soubor opravy instalační služby Windows (.msp) nebo soubor programu .exe. Dále můžete přidat libovolné soubory a složky, které jsou ve stejné složce jako instalační soubor.

    Zobrazí se celková velikost vybraných souborů, které chcete nahrát. Tato velikost nezahrnuje velikost nekomprimovaných nebo rozbalených instalačních souborů.

3.  Po zadání instalačních souborů se na stránce **Popis aktualizace** zobrazí název, popis a klasifikace informací o softwaru, které [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] extrahoval z instalačních souborů softwaru. Můžete vybrat klasifikaci pro označení typu nasazované aktualizace (aktualizace, důležité aktualizace, aktualizace zabezpečení, kumulativní aktualizace nebo aktualizace Service Pack). Jakmile jste hotovi, klikněte na **Další**.

4.  Na stránce **Požadavky** v průvodci zvolte architekturu (32bitovou verzi, 64bitovou verzi nebo obě) a operační systémy spravovaných počítačů, na které se tato aktualizace použije.

5.  Na stránce **Pravidla detekce** nastavte, jak má [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] zjistit, jestli je už aktualizace na spravovaných počítačích. Pokud použijete výchozí možnost **Použít výchozí pravidla zjišťování**, [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] vždy nainstaluje balíček aktualizace na každém cílovém počítači jednou.

    > [!NOTE]
    > Pokud je zadaným instalačním souborem aktualizace soubor instalační služby Windows nebo soubor .msp, stránka **Pravidla detekce** v průvodci se nezobrazí. Je to proto, že soubory instalační služby Windows a soubory .msp obsahují vlastní pokyny pro zjišťování předchozích instalací aktualizace.

    Výběrem jednoho nebo více pravidel určíte, jestli je aktualizace už nainstalovaná na spravovaných počítačích:

    -   **Soubor existuje.**

    -   **Kód produktu MSI existuje.**

    -   **Klíč registru existuje.**

6.  Zadejte další informace, které jsou potřeba ke konfiguraci pravidla detekce, třeba cestu k souboru a jeho název, kód produktu instalační služby Windows nebo klíč registru, a potom klikněte na **Další**.

7.  Na stránce **Požadavky** v průvodci určete software, který už musí být nainstalovaný před instalací této aktualizace. Můžete zadat **Žádný** a vybrat softwarový balíček, který jste už přidali do služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], která ho spravuje, nebo můžete nastavit některé z těchto pravidel pro popis softwaru:

    -   **Soubor existuje.**

    -   **Kód produktu MSI existuje.**

    -   **Klíč registru existuje.**

8.  Zadejte další informace, které jsou potřeba ke konfiguraci pravidla detekce, třeba cestu k souboru a jeho název, kód produktu instalační služby Windows nebo klíč registru, a potom klikněte na **Další**.

9. Na stránce **Argumenty příkazového řádku** v průvodci můžete přidáním požadovaných vlastností instalace na příkazový řádek instalace upravit chování instalačního souboru. Některý software třeba podporuje vlastnost **/q**, která umožňuje tichou instalaci. Informace o všech podporovaných argumentech příkazového řádku najdete v dokumentaci k vašemu softwarovému balíčku. Zadejte všechny potřebné argumenty příkazového řádku a klikněte na **Další**.

    > [!NOTE]
    > Pokud aktualizace nepodporuje tichou instalaci, nemůžete ji v [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] instalovat.

10. Na stránce **Návratové kódy** v průvodci můžete určit, jak se interpretují návratové kódy z instalace aktualizací. Ve výchozím nastavení [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] používá návratové kódy podle oborových standardů k oznámení neúspěšné nebo úspěšné instalace balíčku aktualizace. Zadané návratové kódy:

    |Návratový kód|Interpretace|
    |-----------------|----------------|
    |**0**|Úspěch|
    |**3010**|Restartování proběhlo úspěšně|
    Všechny neuvedené návratové kódy se považují za chybu.

    Některé aktualizace používají pro návratové kódy nestandardní interpretace. V takovém případě můžete zadat své vlastní interpretace návratových kódů.

    Zadejte nebo upravte požadované návratové kódy a klikněte na **Další**.

11. Na stránce **Souhrn** v průvodci zkontrolujte akce, které se mají provést, a pak kliknutím na **Nahrát** kroky průvodce dokončete.

Nahraná aktualizace se uloží v cloudovém úložišti [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], které jste zakoupili. Pokud máte dost volného místa pro nahrání balíčku aktualizace, budete na to během procesu nahrávání upozorněni.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] může zjistit, jestli máte dost volného místa, až po zahájení nahrávání aktualizace, protože komprimované instalační soubory vyžadují po dekomprimaci víc místa.

Jakmile se aktualizace jiného výrobce nahraje do [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], zobrazí se v pracovním prostoru **Aktualizace** v podokně **Všechny aktualizace**. Pak budete moct aktualizaci schválit a nasadit. Další informace najdete v části [Schválení a odmítnutí aktualizací](../Topic/Keep_Windows_PCs_up_to_date_with_software_updates_in_Microsoft_Intune.md#BKMK_Approve1) v tomto tématu.

## <a name="BKMK_Approve1"></a>Schválení a odmítnutí aktualizací
Jakmile jsou aktualizace připravené k instalaci, zobrazí se o tom zpráva na stránce **Přehled aktualizací** pracovního prostoru **Aktualizace** v části **Stav aktualizace**. Kliknutím na tuto zprávu otevřete stránku **Všechny aktualizace**, na které uvidíte, jaké aktualizace jsou připravené ke schválení.

Abyste usnadnili hledání aktualizací, můžete použít seznam **Filtry**. Můžete třeba zobrazit jen aktualizace, které se nepodařilo nainstalovat nebo které byly nahrazené.

Po výběru aktualizace ze seznamu budete moct použít další příkazy, které umožňují spravovat aktualizace a které jsou uvedené v této tabulce:

|Úloha|Další informace|
|---------|-------------------|
|**Zobrazit vlastnosti**|Zobrazí podrobné informace o aktualizaci včetně počtu počítačů, na které se vztahuje.|
|**Upravit**|Používá se jen pro aktualizace jiného výrobce než Microsoftu. Umožňuje upravit vlastnosti aktualizace.|
|**Schválit**|Schválí vybranou aktualizaci a umožní vám nakonfigurovat, do jakých skupin se nasadí. Další informace najdete v části [Schválení aktualizací](../Topic/Keep_Windows_PCs_up_to_date_with_software_updates_in_Microsoft_Intune.md#BKMK_Approve) v tomto tématu.|
|**Odmítnout**|Odebere všechna předchozí schválení aktualizace a skryje aktualizaci z výchozích zobrazení. Kromě toho se odeberou všechna data sestavy pro tuto aktualizaci.<br /><br />Pokud chcete později hledat odmítnuté aktualizace, nastavte filtr na stránce **Všechny aktualizace** na **Odmítnuto**. Tuto aktualizaci pak můžete podle potřeby schválit. **Note:** Pokud byla aktualizace odmítnutá z důvodu vypršení její platnosti v Microsoft Update, nebude možné ji schválit v [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)]. **Note:** Když odstraníte zásady aktualizací nasazené na počítače, hodnoty nastavení zásad těchto aktualizací se vrátí do výchozího stavu pro operační systém nainstalovaný na počítačích.|
|**Odstranit**|Používá se jen pro aktualizace jiného výrobce než Microsoftu. Odstraní vybranou aktualizaci.|
|**Nahrát**|Spustí průvodce **nahráním aktualizací**, který vám umožní nahrát aktualizace jiného výrobce než Microsoftu, které chcete nasadit.|

### <a name="BKMK_Approve"></a>Schválení aktualizací

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com/) klikněte na **Aktualizace** &gt; **Přehled** &gt; **Nové aktualizace ke schválení**.

    V pracovním prostoru **Aktualizace** klikněte na **Přehled** &gt; **Nové aktualizace ke schválení**.

    > [!NOTE]
    > Odkaz **Nové aktualizace ke schválení** se zobrazí v oblasti **Stav aktualizací**, jen když máte aspoň jeden spravovaný počítač, který vyžaduje schválení aktualizace.

2.  Vyberte aktualizaci, kterou chcete schválit, v dolní části stránky se podívejte na její vlastnosti, a potom klikněte na **Schválit**. Můžete vybrat víc aktualizací tím, že při výběru jednotlivých položek podržíte stisknutou klávesu **CTRL**.

3.  Na stránce **Vybrat skupiny** vyberte skupinu, do které chcete nasadit aktualizace, a klikněte na **Přidat**. Jakmile budete s výběrem skupin hotovi, klikněte na **Další**.

4.  Na stránce **Akce nasazení** udělejte pro každou skupinu v seznamu tohle:

    -   V seznamu **Schválení** vyberte některou z těchto možností:

        -   **Požadovaná instalace** – nainstaluje aktualizaci na počítače v určené skupině.

        -   **Neinstalovat** – zobrazí jen informace o použitelnosti a aktualizaci nenainstaluje.

        -   **Dostupná instalace** – uživatel může nainstalovat aplikaci na vyžádání z firemního portálu.

        -   **Odinstalovat** – odebere aktualizace z počítačů v cílové skupině.

            > [!IMPORTANT]
            > Aktualizace se odebere, i když nebyla nainstalovaná v [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

    -   V seznamu **Termín** vyberte některou z těchto možností:

        -   **Žádný** – označuje, že pro instalaci aktualizace nebyl vynucený žádný termín a uživatelé můžou aktualizaci průběžně odmítat.

        -   **Co nejdříve** – nainstaluje aktualizaci při nejbližší příležitosti na cílové počítače.

        -   **Vlastní** – určuje datum a čas instalace schválených aktualizací.

        -   **Jeden týden**, **Dva týdny**, **Jeden měsíc** – nainstaluje aktualizaci během zadaného časového období.

5.  Kliknutím na **Dokončit** nastavení uložíte nebo kliknutím na **Zrušit** nastavení zrušíte a vrátíte se k seznamu aktualizací.

    > [!IMPORTANT]
    > Pokud jste pro podřízenou skupinu explicitně nenakonfigurovali akci **Neinstalovat**, **Požadovaná instalace** nebo **Odinstalovat**, zdědí všechny podřízené skupiny akci nakonfigurovanou pro nadřazenou skupinu.

6.  Na panelu podrobností v dolní části stránky **Všechny aktualizace** můžete vidět zprávy s připomenutím ohledně aktualizací.

## Potřebujete další pomoc?
Další nápovědu a podporu najdete v tématu [Řešení potíží se službou Endpoint Protection v Microsoft Intune](../Topic/Troubleshoot_Endpoint_Protection_in_Microsoft_Intune.md).

## Viz také
[Správa počítačů s Windows pomocí Intune](../Topic/Manage_Windows_PCs_with_Microsoft_Intune.md)

