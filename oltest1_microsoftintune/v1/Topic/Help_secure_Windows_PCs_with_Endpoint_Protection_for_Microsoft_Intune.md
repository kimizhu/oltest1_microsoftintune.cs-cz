---
description: na
keywords: na
title: Help secure Windows PCs with Endpoint Protection for Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 682a83ec-bcf4-46ed-9a74-61b87b6a86a3
---
# Pomoc se zabezpečen&#237;m poč&#237;tačů s Windows pomoc&#237; služby Endpoint Protection pro Microsoft Intune
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] vám může pomoci zabezpečit spravované počítače řadou různých způsobů, včetně použití služby Endpoint Protection, která zajišťuje ochranu v reálném čase proti hrozbám malwaru, zajišťuje aktuálnost definicí malwaru a automaticky kontroluje počítače.[!INCLUDE[epshort](../Token/epshort_md.md)] také poskytuje nástroje, které pomáhají se správou a monitorováním malwarových útoků.

Pokud jste ještě klienta [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] na počítače nenainstalovali, přečtěte si část [Instalace klienta na počítači s Windows pomocí Microsoft Intune](../Topic/Install_the_Windows_PC_client_with_Microsoft_Intune.md).

Informace v následujících částech vám pomohou s konfigurací, nasazením a monitorováním služby [!INCLUDE[epshort](../Token/epshort_md.md)].

## Používání Endpoint Protection v Microsoft Intune

### Než začnete
Jedno z vašich nejdůležitějších priorit jako správce IT je udržovat počítače, které spravujete, bez malwaru a virů. Před nasazením [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] do klientských počítačů ve vaší organizaci byste měli rozhodnout, jak počítače chránit, zvolením některé z následujících možností a konfigurováním nastavení příslušných zásad:

|Chci:|Nastavení zásad Endpoint Protection|Další informace|
|---------|---------------------------------------|-------------------|
|Použít [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] jenom v případě, že není nainstalovaná žádná aplikace koncové ochrany třetí strany<br /><br />[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] můžete použít na všech počítačích, kde není nainstalovaná aplikace koncové ochrany třetí strany.|-   Nainstalovat službu Endpoint Protection = **Ano**<br />-   Povolit službu Endpoint Protection = **Ano**<br />-   Nainstalovat službu Endpoint Protection i v případě, že byla nainstalována aplikace koncové ochrany třetích stran = **Ne**|Pokud se detekuje aplikace koncové ochrany třetí strany, služba [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] [!INCLUDE[epshort](../Token/epshort_md.md)] se nenainstaluje nebo se odinstaluje, pokud už nainstalovaná byla.|
|Použít [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] i v případě, že je nainstalovaná aplikace koncové ochrany třetí strany<br /><br />S tímto přístupem budete používat současně [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] [!INCLUDE[epshort](../Token/epshort_md.md)] a aplikaci koncové ochrany třetí strany (pokud je nainstalovaná). Taková konfigurace se nedoporučuje kvůli možným problémům s výkonem.|-   Nainstalovat službu Endpoint Protection = **Ano**<br />-   Povolit službu Endpoint Protection = **Ano**<br />-   Nainstalovat službu Endpoint Protection i v případě, že byla nainstalována aplikace koncové ochrany třetích stran = **Ano**|Použijte, když:<br /><br />-   Chcete přejít k používání [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)].<br />-   Nasazujete nového klienta, který bude používat [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] [!INCLUDE[epshort](../Token/epshort_md.md)]<br />-   Upgradujete libovolného klienta, který bude používat [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] [!INCLUDE[epshort](../Token/epshort_md.md)].|
|Použít [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] bez [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)]<br /><br />V takovém případě nebudete používat [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] k ochraně počítačů před malwarem a viry. Místo toho budete spoléhat na aplikaci koncové ochrany třetí strany.|-   Nainstalovat službu Endpoint Protection = **Ne**|Pokud nepoužíváte aplikaci koncové ochrany třetí strany, tato konfigurace se nedoporučuje, protože by počítače vaší organizace mohla vystavit malwaru nebo jiným útokům.<br /><br />Řešení [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] [!INCLUDE[epshort](../Token/epshort_md.md)] se nenainstaluje, a pokud bylo dřív nainstalované, tak se odinstaluje.|
Pokud chcete přejít ze současné aplikace koncové ochrany na [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)], postupujte podle následujících kroků, které jsou dále v tomto tématu vysvětlené podrobněji:

1.  Při nasazování klientského softwaru [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] do počítačů nechte stávající aplikaci koncové ochrany spuštěnou.

2.  Ověřte, že je [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] nainstalované a pomáhá zabezpečit klientské počítače.

3.  Odeberte software koncové ochrany třetí strany:

    -   Pomocí softwarové distribuce [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] k nasazení nástroje pro odebrání softwaru, který poskytuje výrobce aplikace koncové ochrany. Další informace naleznete v části [Nasazení a konfigurace aplikací v Microsoft Intune](../Topic/Deploy_and_configure_apps_with_Microsoft_Intune.md).

    -   Ručním odebráním aplikace koncové ochrany třetí strany.

> [!NOTE]
> [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] aplikace koncové ochrany třetích stran neodinstaluje.

### <a name="BKMK_HowtoConf"></a>Jak nakonfigurovat Microsoft Intune Endpoint Protection
Pomocí následujícího postupu se dá konfigurovat [!INCLUDE[epshort](../Token/epshort_md.md)] pro [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)].[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] může spravovat [!INCLUDE[epshort](../Token/epshort_md.md)] pro Windows 10 Technical Preview. Některá nastavení zásad jsou dostupná jenom pro Windows 10.

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com/) klikněte na **Zásady** &gt; **Přidat zásadu**.

2.  Konfigurujte a nasaďte zásady **nastavení agenta Microsoft Intune** pro nastavení [!INCLUDE[epshort](../Token/epshort_md.md)]. Můžete použít doporučená nastavení nebo nastavení upravit. Pokud potřebujete další informace o tom, jak vytvořit a nasadit zásady, přečtěte si téma [Běžné úlohy správy počítačů s Windows pomocí počítačového klienta Microsoft Intune](../Topic/Common_Windows_PC_management_tasks_with_the_Microsoft_Intune_computer_client.md).

    Tabulky po tomto postupu zobrazují hodnoty, které můžete v zásadách konfigurovat, a taky doporučené hodnoty, které se použijí, pokud zásady neupravíte. Tato nastavení najdete v části **Endpoint Protection**.

Nasazené zásady [!INCLUDE[epshort](../Token/epshort_md.md)] můžete zobrazit na stránce **Všechny zásady** pracovního prostoru **Zásady**.

#### Nastavení služby Endpoint Protection

|Nastavení zásad|Další informace|
|-------------------|-------------------|
|**Nainstalovat službu Endpoint Protection**|Nastavte na **Ano**, pokud chcete nainstalovat [!INCLUDE[epshort](../Token/epshort_md.md)] na spravované počítače. Pokud se v průběhu instalace detekuje aplikace koncové ochrany třetí strany, [!INCLUDE[epshort](../Token/epshort_md.md)] se nainstaluje jenom v případě, že je zásada **Nainstalovat službu Endpoint Protection i v případě, že byla nainstalována aplikace koncové ochrany třetích stran** nastavená na **Ano**. **Note:** Intune [!INCLUDE[epshort](../Token/epshort_md.md)] se na spravované počítače ve výchozím nastavení instaluje. Pokud nechcete, aby se služba [!INCLUDE[epshort](../Token/epshort_md.md)] na spravované počítače instalovala, musíte tuto zásadu explicitně nastavit na **Ne**. Pokud už služba [!INCLUDE[epshort](../Token/epshort_md.md)] byla dříve nainstalovaná a zásada se aktualizuje na **Ne**, pak se klient [!INCLUDE[epshort](../Token/epshort_md.md)] odinstaluje.<br />Doporučená hodnota: **Ano**|
|**Nainstalovat službu Endpoint Protection i v případě, že byla nainstalována aplikace koncové ochrany třetích stran**|Nastavte na **Ano**, pokud chcete [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] instalovat i v případě, že se detekuje aplikace koncové ochrany třetí strany.<br /><br />Doporučená hodnota: **Ano**|
|**Povolit službu Endpoint Protection**|Nastavte na **Ano**, pokud chcete povolit [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] na počítačích, které mají klienta [!INCLUDE[epshort](../Token/epshort_md.md)].<br /><br />Pokud je zásada nastavená na **Ne** a služba [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] je nainstalovaná, uživatelské rozhraní klienta [!INCLUDE[epshort](../Token/epshort_md.md)] se uživatelům nezobrazí a všechny funkce ochrany jsou neaktivní.<br /><br />Doporučená hodnota: **Ano**|
|**Zakázat uživatelské rozhraní klienta**|Nastavte na **Ano**, pokud chcete uživatelům skrýt uživatelské rozhraní klienta [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] (vyžaduje restartování počítače klienta).<br /><br />Doporučená hodnota: **Ne**|
|**Nainstalovat službu Endpoint Protection i v případě, že byla nainstalována aplikace koncové ochrany třetích stran**|Nastavte na **Ano**, pokud chcete vynutit instalaci [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] i v případě, že se detekuje aplikace koncové ochrany třetí strany.<br /><br />Doporučená hodnota: **Ne**|
|**Vytvořit bod obnovení systému před nápravou škod způsobených nebezpečným softwarem**|Nastavte na **Ano**, pokud chcete vytvořit bod obnovení systému Windows před zahájením nápravy škod způsobených malwarem.<br /><br />Doporučená hodnota: **Ano**|
|**Sledovat vyřešené problémy s malwarem (dny)**|Umožňuje službě [!INCLUDE[epshort](../Token/epshort_md.md)] po určitou dobu sledovat vyřešené problémy s malwarem, abyste mohli ručně zkontrolovat dříve infikované počítače.<br /><br />Můžete určit hodnotu od 0 do 30 dnů.<br /><br />Doporučená hodnota: **7 dnů**|
Pokud jste nastavili hodnoty zásad **Nainstalovat službu Endpoint Protection** a **Povolit službu Endpoint Protection** na **Ano** a hodnotu zásady **Nainstalovat službu Endpoint Protection i v případě, že byla nainstalována aplikace koncové ochrany třetích stran** na **Ne**, [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] zjistí, že je nainstalovaná jiná aplikace koncové ochrany a nenainstaluje se, případně se odinstaluje, pokud už nainstalovaná byla ([!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] ale bude hlásit stav jiné aplikace koncové ochrany v rozhraní [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)]).

#### Nastavení ochrany v reálném čase

|Nastavení zásad|Další informace|
|-------------------|-------------------|
|**Povolit ochranu v reálném čase**|Umožňuje sledování a kontrolu všech souborů a aplikací, ke kterým se přistupuje. Blokuje taky všechny škodlivé soubory a aplikace ještě před jejich spuštěním na počítačích.<br /><br />Doporučená hodnota: **Ano**|
|**Kontrolovat všechny stahované soubory**|Umožňuje kontrolu všech souborů a příloh, které se stahují z internetu do počítačů.<br /><br />Doporučená hodnota: **Ano**|
|**Sledovat činnost souborů a programů v počítačích**|Umožňuje sledování příchozích a odchozích souborů a aktivitu programů na počítačích. S tímto nastavením může [!INCLUDE[epshort](../Token/epshort_md.md)] sledovat, když se soubory a programy spouštějí, a upozornit vás na všechny akce, které samy provádějí, nebo akce, které se s nimi provádějí.<br /><br />Doporučená hodnota: **Ano**|
|**Sledované soubory**|Pokud je povolená zásada **Sledovat činnost souborů a programů v počítačích**, toto nastavení umožňuje zvolit, jestli se mají sledovat jenom příchozí, jenom odchozí nebo všechny soubory.<br /><br />Doporučená hodnota: **Monitorovat všechny soubory**|
|**Povolit monitorování chování**|Umožňuje, aby služba [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)][!INCLUDE[epshort](../Token/epshort_md.md)] kontrolovala určité vzorce podezřelých aktivit na klientských počítačích.<br /><br />Doporučená hodnota: **Ano**|
|**Povolit systém kontroly sítě**|Povolí systém kontroly sítě (NIS) na klientských počítačích. Systém NIS používá signatury známých slabých míst z [Centra společnosti Microsoft pro ochranu před škodlivým softwarem](http://go.microsoft.com/fwlink/?LinkId=234249) ke zjištění a blokování škodlivého síťového provozu.<br /><br />Doporučená hodnota: **Ano**|

#### Nastavení plánu kontroly

|Nastavení zásad|Další informace|
|-------------------|-------------------|
|**Naplánovat každodenní rychlou kontrolu**|Naplánuje denní rychlou kontrolu často používaných souborů a důležitých systémových souborů na počítačích. Tato rychlá kontrola má minimální vliv na výkon.<br /><br />Doporučená hodnota: **Ano**|
|**Spustit rychlé prověřování, pokud nebyla provedena dvě po sobě následující prověřování**|Nakonfiguruje službu [!INCLUDE[epshort](../Token/epshort_md.md)], aby na počítačích automaticky spustila rychlou kontrolu, pokud na nich neproběhly dvě po sobě následující naplánované rychlé kontroly.<br /><br />Doporučená hodnota: **Ano**|
|**Naplánovat úplnou kontrolu**|Nakonfiguruje úplnou kontrolu všech souborů a prostředků na místních pevných discích počítačů. Tato kontrola může nějakou dobu trvat a může ovlivnit výkon počítače (v závislosti na počtu kontrolovaných souborů a prostředků).<br /><br />Doporučená hodnota: **Ne**|
|**Spustit úplné prověřování, pokud nebyla provedena dvě po sobě následující prověřování**|Nakonfiguruje službu [!INCLUDE[epshort](../Token/epshort_md.md)], aby na počítačích automaticky spustila úplnou kontrolu, pokud na nich neproběhly dvě po sobě následující naplánované úplné kontroly.<br /><br />Doporučená hodnota: Není nakonfigurováno|

#### Nastavení možností kontroly

|Nastavení zásad|Další informace|
|-------------------|-------------------|
|**Po instalaci služby Endpoint Protection spustit úplnou kontrolu**|Nakonfiguruje službu [!INCLUDE[epshort](../Token/epshort_md.md)], aby po instalaci na počítačích automaticky spustila úplnou kontrolu systému. Tato kontrola běží jenom v případě, že jsou počítače v nečinnosti, aby se minimalizoval vliv na produktivitu uživatelů.<br /><br />Doporučená hodnota: **Ano**|
|**Automaticky spouštět úplnou kontrolu v případě potřeby po odebrání malwaru**|Nastavte na **Ano**, pokud chcete, aby služba [!INCLUDE[epshort](../Token/epshort_md.md)] automaticky spustila úplnou kontrolu systému na počítačích po odstranění malwaru kvůli ověření, že nedošlo k ovlivnění ostatních souborů.<br /><br />Doporučená hodnota: **Ano**|
|**Spustit naplánovanou kontrolu pouze v případě, že je počítač v nečinnosti**|Nastavte na **Ano**, pokud chcete zabránit spouštění naplánovaných kontrol, když se počítače používají, aby nedocházelo ke snížení produktivity uživatelů.<br /><br />Doporučená hodnota: **Ano**|
|**Před zahájením kontroly zkontrolovat nejnovější definice malwaru**|Nastavte na **Ano**, pokud chcete, aby služba [!INCLUDE[epshort](../Token/epshort_md.md)] před spuštěním kontroly na počítačích automaticky vyhledala nejnovější definice malwaru.<br /><br />Doporučená hodnota: **Ano**|
|**Prohledat archivní soubory**|Nastavte na **Ano**, pokud chcete konfigurovat, aby služba [!INCLUDE[epshort](../Token/epshort_md.md)] kontrolovala malware v souborech archivu (jako jsou soubory ZIP nebo CAB) na počítačích.<br /><br />Doporučená hodnota: **Ne**|
|**Kontrolovat e-mailové zprávy**|Nastavte na **Ano**, pokud chcete konfigurovat, aby služba [!INCLUDE[epshort](../Token/epshort_md.md)] kontrolovala příchozí e-mailové zprávy, když dorazí do počítačů.<br /><br />Doporučená hodnota: **Ano**|
|**Kontrolovat soubory otevřené ze síťových sdílených složek**|Nastavte na **Ano**, pokud chcete konfigurovat, aby služba [!INCLUDE[epshort](../Token/epshort_md.md)] kontrolovala soubory otvírané ze sdílených složek v síti. Obvykle jsou to soubory, ke kterým se přistupuje pomocí cesty UNC. Povolení této funkce může způsobit problémy uživatelům, kteří mají přístup jenom pro čtení, protože nemůžou malware odebrat.<br /><br />Doporučená hodnota: **Ne**|
|**Kontrolovat namapované síťové jednotky**|Nastavte na **Ano**, pokud chcete konfigurovat, aby služba [!INCLUDE[epshort](../Token/epshort_md.md)] kontrolovala soubory na namapovaných síťových jednotkách. Povolení této funkce může způsobit problémy uživatelům, kteří mají přístup jenom pro čtení, protože nemůžou malware odebrat.<br /><br />Doporučená hodnota: **Ne**|
|**Kontrolovat vyměnitelné jednotky**|Nastavte na **Ano**, pokud chcete konfigurovat, aby služba [!INCLUDE[epshort](../Token/epshort_md.md)] kontrolovala malware nebo nežádoucí software v obsahu vyměnitelných jednotek, jako jsou jednotky USB flash, když na počítačích spustíte úplnou kontrolu.<br /><br />Doporučená hodnota: **Ano**|
|**Omezit využití procesoru při prověřování**|Konfiguruje maximální procento využití procesoru, které se smí využít při naplánovaných kontrolách na počítačích. Tuto hodnotu můžete nastavit od 1 do 100 procent.<br /><br />Doporučená hodnota: **50 %**|

#### Nastavení výchozích akcí

|Nastavení zásad|Další informace|
|-------------------|-------------------|
|**Zvolte, jak má služba Endpoint Protection postupovat v případě následujících stupňů výstrahy před malwarem**|Určuje výchozí akci, kterou [!INCLUDE[epshort](../Token/epshort_md.md)] provede, když zjistí malware s různými stupni výstrahy.<br /><br />Při každém stupni výstrahy můžete malware odebrat, dát ho do karantény nebo provést akci doporučenou společností Microsoft.<br /><br />Doporučená hodnota: **Doporučená akce**|

#### Nastavení vyloučených souborů a složek

|Nastavení zásad|Další informace|
|-------------------|-------------------|
|**Soubory a složky, které mají být vyloučeny z kontroly a ochrany v reálném čase**|Vyloučí určité soubory nebo složky, když se spustí kontrola nebo když se použije ochrana v reálném čase.|

#### Nastavení vyloučených procesů

|Nastavení zásad|Další informace|
|-------------------|-------------------|
|**Vyloučit procesy při použití prověřování nebo ochrany v reálném čase**|Umožňuje vyloučit konkrétní procesy při spuštění kontroly nebo použití ochrany v reálném čase. Můžete vyloučit jenom soubory s těmito příponami: **.exe**, **.com** nebo **.scr**.|

#### Nastavení vyloučených typů souborů

|Nastavení zásad|Další informace|
|-------------------|-------------------|
|**Vyloučit přípony souborů při použití prověřování nebo ochrany v reálném čase**|Umožňuje vyloučit konkrétní přípony názvů souborů při spuštění kontroly nebo použití ochrany v reálném čase na počítačích.|

#### Nastavení služby Microsoft Active Protection Service
Služba Microsoft Active Protection Service je online komunita poskytující pomoc při rozhodování, jak reagovat na případné hrozby. Tato komunita taky pomáhá zastavit šíření nových napadení malwarem.

|Nastavení zásad|Další informace|
|-------------------|-------------------|
|**Připojit ke službě Microsoft Active Protection Service**|Hodnota **Ano** automaticky odesílá informace o zjištěném malwaru do služby Microsoft Active Protection Service. Společnost Microsoft nepoužívá získané informace k tomu, aby vás identifikovala nebo kontaktovala.<br /><br />Doporučená hodnota: **Ano**|
|**Úroveň členství**|Pokud jste vybrali možnost připojení se ke službě Microsoft Active Protection Service, toto nastavení umožňuje vybrat jednu z následujících úrovní členství:<br /><br />-   **Základní** – odesílá společnosti Microsoft základní informace o zjištěném malwaru. Jsou to například informace o tom, odkud software pochází, jaké používáte akce nebo jaké akce automaticky používá [!INCLUDE[epshort](../Token/epshort_md.md)] a jestli byly akce úspěšné.<br />-   **Rozšířené** – odesílá společnosti Microsoft informace o malwaru, spywaru nebo potenciálně nežádoucím softwaru. Jsou to například informace o umístění softwaru, názvech souborů, jak software funguje a jak ovlivnil počítač.<br /><br />Doporučená hodnota: **Rozšířené**|
|**Přijímat dynamické definice založené na zprávách služby Microsoft Active Protection Service**|Hodnota **Ano** umožňuje počítačům přijímat dynamické definice malwaru na základě informací o zjištěném malwaru, které [!INCLUDE[epshort](../Token/epshort_md.md)] odesílá do služby Microsoft Active Protection Service (pokud jste se k ní připojili).<br /><br />Doporučená hodnota: **Ano**|

### Úlohy správy pro službu Endpoint Protection
Následující úlohy umožňují provádět různé úlohy správy na spravovaných počítačích, na kterých běží [!INCLUDE[epshort](../Token/epshort_md.md)].

|Co chci|V konzole [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]|Na spravovaném počítači|
|-----------|-------------------------------------------------------------------|---------------------------|
|Aktualizovat definice malwaru|V pracovním prostoru **Skupiny** vyberte počítače, který chcete aktualizovat.<br /><br />Klikněte na **Vzdálené úlohy** &gt; **Aktualizovat definice malwaru**.|Z oznamovací oblasti systému Windows spusťte klientský software [!INCLUDE[epshort](../Token/epshort_md.md)].<br /><br />Klikněte na kartu **Aktualizace** a pak na **Aktualizovat**.|
|Spustit kontrolu malwaru|V pracovním prostoru **Skupiny** vyberte počítače, který chcete zkontrolovat.<br /><br />Klikněte na **Spustit úplné prověřování zaměřené na malware** nebo **Spustit rychlé prověřování zaměřené na malware**.|Z oznamovací oblasti systému Windows spusťte klientský software [!INCLUDE[epshort](../Token/epshort_md.md)].<br /><br />Vyberte **Rychlé**, **Úplné** nebo **Vlastní** a pak klikněte na **Zkontrolovat**.|
Stav vzdálené úlohy můžete zobrazit kliknutím na odkaz **Vzdálené úlohy** v pravém dolním rohu rozhraní [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)].

Dialogové okno **Stav vzdálené úlohy** zobrazuje aktuální vzdálené úlohy, stav úloh, název zařízení, všechny ohlášené chyby a v případě potřeby obsahuje odkaz na informace o odstraňování potíží.

### <a name="BKMK_SCEPmon"></a>Sledování služby Endpoint Protection
Stav malwaru na počítačích se sleduje pomocí pracovního prostoru **Ochrana** v [konzole pro správu Microsoft Intune](https://manage.microsoft.com/). Tento pracovní prostor obsahuje dvě stránky:

|Název stránky|Další informace|
|-----------------|-------------------|
|**Přehled služby Endpoint Protection**|Zobrazuje důležité problémy jako odkazy, které po kliknutí zobrazí další informace. Mezi zobrazované problémy patří:<br /><br />-   **Instance malwaru vyžadující následné akce** – kliknutím na odkaz zobrazíte seznam problémů s malwarem včetně následné akce, kterou je potřeba provést k vyřešení problému. V tomto seznamu můžete zobrazit další podrobnosti a zobrazit tak počítače, které jsou ovlivněné.<br />-   **Počítače s malwarem vyžadující následnou akci** – kliknutím na odkaz zobrazíte všechny počítače s nevyřešenými problémy s malwarem včetně následné akce, kterou je potřeba provést k vyřešení problému.<br />-   **Zařízení, které nejsou chráněna** – kliknutím na odkaz zobrazíte počítače, které nejsou chráněné žádným softwarem koncové ochrany, protože žádný takový software není nainstalovaný, nebo protože došlo k chybě. Vybráním počítače zobrazíte další podrobnosti.<br />-   **Zařízení, na kterých je spuštěna jiná aplikace ochrany koncových bodů** – kliknutím na odkaz zobrazíte počítače, na kterých je spuštěná aplikace koncové ochrany třetí strany.|
|**Veškerý malware**|Zobrazí seznam veškerého aktivního malwaru nalezeného na počítačích. V tomto seznamu můžete zobrazit další podrobnosti a zobrazit tak všechny počítače, které jsou postižené konkrétním malwarem, nebo můžete vybrat některou z následujících úloh:<br /><br />-   **Zobrazit vlastnosti** – otevře stránku s dalšími informacemi o vybrané malwaru.<br />-   **Další informace o tomto malwaru** – otevře téma z Centra společnosti Microsoft pro ochranu před škodlivým softwarem s dalšími informacemi o malwaru.|
> [!IMPORTANT]
> Pracovní prostor **Ochrana** se v konzole pro správu nezobrazí, dokud nenainstalujete klienta aspoň na jeden počítač, který budete úspěšně spravovat.

### Jak zobrazit nedávné cesty zjišťování malwaru na počítačích
Intune může na zařízení zobrazit cesty až 10 naposledy zjištěných instancí malwaru. Možnost **Nedávno kontrolované cesty** je ve výchozím nastavení vypnutá. Postup pro zapnutí tohoto zobrazení:

##### Povolení možnosti zjišťování posledních cest malwaru

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com/) klikněte na **Skupiny** &gt; **Všechna zařízení**.**Malware**.

2.  Klikněte pravým tlačítkem myši na záhlaví sloupce. Zobrazí se seznam dostupných sloupců.

3.  V seznamu zaškrtněte políčko **Nedávno kontrolované cesty**. Zobrazí se sloupec **Nedávno kontrolované cesty**, ve kterém bude uvedeno až 10 posledních instancí malwaru zjištěných na zařízení.

## Potřebujete další pomoc?
Další nápovědu a podporu najdete v tématu [Řešení potíží se službou Endpoint Protection v Microsoft Intune](../Topic/Troubleshoot_Endpoint_Protection_in_Microsoft_Intune.md).

## Viz také
[Správa počítačů s Windows pomocí Intune](../Topic/Manage_Windows_PCs_with_Microsoft_Intune.md)

