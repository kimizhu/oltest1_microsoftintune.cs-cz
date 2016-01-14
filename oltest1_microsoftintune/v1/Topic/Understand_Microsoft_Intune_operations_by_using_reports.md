---
description: na
keywords: na
title: Understand Microsoft Intune operations by using reports
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 857309c2-61c9-4c22-becf-4839fedeaece
---
# Pochopen&#237; operac&#237; Microsoft Intune pomoc&#237; sestav
Informace v tomto tématu vám pomůžou vytvářet a spravovat sestavy [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)], které obsahují informace o softwaru, hardwaru a licencích k softwaru ve vaší organizaci.

## Používání sestav
Sestavy [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] obsahují informace o softwaru, hardwaru a licencích k softwaru ve vaší organizaci. Sestavy vám můžou pomoct potvrdit aktuální potřeby a předpovídat budoucí výdaje. Pracovní prostor **Sestavy** poskytuje nástroje k vytváření a správě sestav. Další informace o sestavách najdete v tématu [Pochopení operací Microsoft Intune pomocí sestav](../Topic/Understand_Microsoft_Intune_operations_by_using_reports.md).

### Typy sestav

|Typ sestavy|Popis|
|---------------|---------|
|**Sestavy aktualizací**|Zobrazují úspěšné aktualizace softwaru na počítačích ve vaší organizaci a taky aktualizace, které se nezdařily, čekají na vyřízení nebo jsou potřeba. Další informace o aktualizacích softwaru najdete v tématu [Udržování počítačů s Windows v aktuálním stavu díky softwarovým aktualizacím v Microsoft Intune](../Topic/Keep_Windows_PCs_up_to_date_with_software_updates_in_Microsoft_Intune.md).|
|**Sestavy zjištěného softwaru**|Zobrazují software nainstalovaný na počítačích ve vaší organizaci včetně verzí softwaru. Zobrazené informace můžete filtrovat na základě vydavatele softwaru a kategorie softwaru. Kliknutím na směrovou šipku vedle položky seznamu můžete aktualizace v seznamu rozbalit a zobrazit tak další podrobnosti (třeba počítače, na kterých jsou nainstalované). **Note:** Když v [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] vyřadíte počítače z provozu nebo změníte jejich členství ve skupinách, může trvat několik minut, než se tyto změny v sestavě zjištěného softwaru projeví. Pokud chcete nejaktuálnější data inventáře softwaru, po vyřazení počítačů nebo změně jejich členství ve skupinách počkejte několik minut a až pak spusťte sestavu zjištěného softwaru zahrnující tyto počítače.|
|**Sestavy inventáře počítačů**|Zobrazují informace o spravovaných počítačích ve vaší organizaci. Pomocí této sestavy můžete plánovat nákupy hardwaru a lépe porozumět hardwarovým potřebám uživatelů ve vaší organizaci. Další informace o práci se spravovanými počítači najdete v tématu [Správa počítačů s Windows pomocí Intune](../Topic/Manage_Windows_PCs_with_Microsoft_Intune.md).|
|**Sestavy inventáře mobilních zařízení**|Zobrazují informace o mobilních zařízeních ve vaší organizaci. Zobrazené informace můžete filtrovat podle skupin, podle toho, jestli byl v zařízení provedený jailbreak nebo rootování, a podle operačního systému.|
|**Sestavy zakoupených licencí**|Zobrazují názvy softwaru pro všechen licencovaný software ve vybraných skupinách licencí podle jejich licenčních smluv. Jsou k dispozici tyto filtry:<br /><br />-   **Všechny smlouvy** – zobrazí všechny licencované softwarové produkty, které jsou spravované prostřednictvím [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].<br />-   **Multilicenční smlouvy** – zobrazí jenom softwarové produkty VLSC.<br />-   **Licenční smlouvy na ostatní software** – zobrazí softwarové produkty, které jsou spravované mimo VLSC. **Note:** Pokud se informace o licencích softwaru déle než 24 hodin neaktualizují, aktualizují se při vygenerování sestavy licencí.<br />Sestava licencí není přesný výčet názvů používaného softwaru ani doklad o souladu se smlouvami. Sestava je nástroj, který vám pomůže provádět rozhodnutí týkající se licencování pro vaši organizaci.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] nemusí rozpoznat některé produkty, které mohou mít multilicenci Microsoftu.|
|**Sestavy instalací licencí**|Porovnávají software nainstalovaný na počítačích ve vaší organizaci s aktuálními licenčními smlouvami podle webu VLSC (Volume Licensing Service Center). Filtry zahrnují:<br /><br />-   **Všechny smlouvy** – zobrazí všechny licencované softwarové produkty, které jsou spravované prostřednictvím [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].<br />-   **Multilicenční smlouvy** – zobrazí jenom softwarové produkty VLSC.<br />-   **Licenční smlouvy na ostatní software** – zobrazí softwarové produkty, které jsou spravované mimo VLSC.|
|**Sestavy podmínek a ujednání**|Zobrazují, jestli uživatelé přijali podmínky a ujednání, které jste nasadili, a kterou verzi přijali. Můžete zadat až 10 uživatelů, u nichž se zobrazí jejich přijetí všech podmínek a ujednání, které jim byly nasazené, nebo zobrazit stav přijetí pro konkrétní nasazenou podmínku.|
|**Sestavy nekompatibilních aplikací**|Zobrazují informace o uživatelích s nainstalovanými aplikacemi, které jsou na vašem seznamu kompatibilních a nekompatibilních aplikací. Tato sestava slouží k vyhledání uživatelů a zařízení, která nejsou v souladu s vašimi firemními zásadami pro aplikace.|
|**Sestavy o shodě certifikátů**|Zobrazují, které certifikáty byly vydané uživatelům a zařízením prostřednictvím Služby zápisu síťových zařízení. Tato sestava slouží k vyhledání certifikátů, které jsou vydané, mají ukončenou platnost nebo jsou odvolané.|
|**Sestavy o historii zařízení**|Zobrazují historický protokol akcí vyřazení, vymazání a odstranění. Tato sestava slouží k zobrazení, kdo v minulosti akce v zařízeních inicioval.|
|**Mac OS X – sestava hardwaru**|Zobrazuje podrobnosti o hardwaru všech registrovaných zařízení se systémem Mac OS X ve vybraných skupinách. Informace o inventáři hardwaru shromážděné z těchto zařízení najdete v tématu [Seznámení se zařízeními s inventářem v Microsoft Intune](../Topic/Understand_your_devices_with_inventory_in_Microsoft_Intune.md).|
|**Mac OS X – sestava softwaru**|Zobrazuje software nainstalovaný na všech zařízeních se systémem Mac OS X ve vybraných skupinách. Tato sestava uvádí:<br /><br />-   Název softwaru (jako ID sady)<br />-   Zkrácený (nebo uživatelsky přívětivý) název<br />-   Verzi<br />-   Počet zařízení s nainstalovaným softwarem|

#### Vytvoření sestavy

1.  V rozhraní [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] klikněte na **Sestavy** a pak klikněte na typ sestavy, kterou chcete vygenerovat, podle popisu ve výše uvedené tabulce.

2.  Na stránce **Vytvořit novou sestavu** přijměte výchozí hodnoty, případně je upravte, aby se vyfiltrovaly výsledky, které bude sestava obsahovat. Můžete třeba vybrat, aby se v sestavě zjištěného softwaru zobrazil jenom software vydávaný Microsoftem.

3.  Kliknutím na **Zobrazit sestavu** otevřete sestavu v novém okně.

Pokud chcete sestavu seřadit podle kteréhokoli zobrazeného sloupce, klikněte na jeho záhlaví. Kromě toho některé sestavy umožňují rozbalit položky na seznamu a zobrazit více podrobností.

## Další akce sestav
Sestavy navíc podporují následující akce:

|Akce|Další informace|
|--------|-------------------|
|**Tisk**|V otevřené sestavě klikněte na ikonu tisku a postupujte podle pokynů.|
|**Export**|V otevřené sestavě klikněte na ikonu exportu a postupujte podle pokynů. Sestavy můžete exportovat do formátu hodnot oddělených čárkou (CSV) nebo formátu HTML.|
|**Uložení**|Na stránce **Vytvořit novou sestavu** může každý uživatel uložit až 100 sestav. Konfigurujte parametry sestavy podle svých požadavků a pak klikněte na **Uložit** nebo **Uložit jako** (pokud chcete použít jiný název).|
|**Načítání**|Na stránce **Vytvořit novou sestavu** klikněte na **Načíst**, pokud chcete načíst kteroukoli dříve uloženou sady parametrů sestavy.|
|**Odstranit**|V pracovním prostoru **Sestavy** vyberte požadovaný typ sestavy, klikněte na **Načíst** a pak na seznamu sestav klikněte na ikonu odstranění (x) vedle sestavy.|

## Viz také
[Monitorování a sestavy v Microsoft Intune](../Topic/Monitoring_and_reports_with_Microsoft_Intune.md)

