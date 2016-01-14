---
description: na
keywords: na
title: Learn how to deploy a solution for protecting company email and documents
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2e10af43-3138-45c0-b2f7-14a1d2bfb237
---
# Informace o nasazen&#237; řešen&#237; pro ochranu firemn&#237;ho e-mailu a dokumentů
Společnosti stále častěji umožňují svým zaměstnancům, aby zvyšovali svou produktivitu tím, že pro přístup k e-mailu, dokumentům a prostředkům společnosti budou využívat svá mobilní zařízení. Objem důvěrných dat, která jsou uložená v podnikových e-mailech a dokumentech, ale pro společnosti představuje významné bezpečnostní riziko.

Tato příručka je určena pro vás, IT profesionály. Pomůže vám pro vaši firmu určit a nasadit nejlepší řešení pro vynucení podmíněného přístupu v jedné z konfigurací, které jsou popsané níž. Zaměstnanci tak budou moct pro přístup k firemnímu e-mailu využívat svá mobilní zařízení a firemní data přitom budou chráněná.

> [!TIP]
> Kopii celého tohoto tématu ke stažení najdete v [Galerii TechNet](https://gallery.technet.microsoft.com/Deploying-Enterprise-16499404).

## Úvod
Ochrana firemních dat je životně důležitá a je stále náročnější, protože stále víc zaměstnanců používá pro přístup k prostředkům společnosti, včetně e-mailů a e-mailových příloh, svá mobilní zařízení. Jako správce IT chcete zajistit, aby firemní data byla chráněná i v případě, že tato mobilní zařízení jsou mimo fyzické umístění společnosti.

Microsoft Enterprise Mobility Suite (EMS) tuto situaci řeší tím, že poskytuje komplexní ochranu firemního e-mailu a dokumentů ve čtyřech vrstvách – identita, zařízení, aplikace a data. EMS kromě jiného zajišťuje, aby zaměstnanci měli přístup k podnikovému e-mailu jenom ze zařízení, která spravuje Microsoft Intune a která jsou kompatibilní se zásadami IT.

Ochrana podnikových e-mailů má dva hlavní cíle:

-   **Povolit přístup k firemnímu e-mailu jenom kompatibilním zařízením:** Důležitým krokem při ochraně firemních dat je omezení přístupu k zařízením, která nepoužívají silné heslo, nemají jailbreak nebo nejsou šifrovaná.  Microsoft Intune vám dává možnost nastavit podmínky, které uživatelé musí splnit, aby získali přístup k firemním prostředkům. To se označuje jako podmíněný přístup.

-   **Chránit obsah v e-mailech a přílohách:** Přestože podmíněný přístup umožňuje zajistit, že přístup k e-mailu mají jenom kompatibilní zařízení, otázka ochrany obsahu e-mailů a e-mailových příloh zůstává otevřená.  Obsah se dá kopírovat, přesunout, uložit do jiného umístění nebo sdílet s jiným uživatelem.  EMS tento problém řeší pomocí zásad správy mobilních aplikací.

    Spravované aplikace jsou aplikace, u kterých jsou použité zásady správy mobilních aplikací, díky kterým jsou kompatibilní s požadavky na zabezpečení vaší společnosti. Máte přímou kontrolu nad nasazením těchto aplikací, jejich průběžnou správou, jako je inventarizace nebo aktualizace, a selektivním vymazáním těchto aplikací a jejich přidružených dat. Pomocí sady zásad správy mobilních aplikací (MAM) Intune navíc umožňuje měnit funkce aplikací a omezovat sdílení dat. Další informace o tom, jak toto řešení funguje, včetně podrobností o použité architektuře, najdete v tématu [Ochrana podnikových e-mailů a dokumentů](https://technet.microsoft.com/en-us/library/mt574220.aspx).

    > [!NOTE]
    > Můžete vytvořit a nasadit e-mailový profil a pak nasadit zásady kompatibility, které určují, že e-mailové profily musí spravovat Intune (doporučeno). Získáte tak možnost vymazat e-maily z vyřazených zařízení a přitom je pro iOS  zajištěné, že přílohy jsou otvírat jenom v aplikacích, které spravuje Intune. Další informace najdete v části [Krok 5: Vytvořte zásady dodržování předpisů a nasaďte je uživatelům.](../Topic/Use_conditional_access_with_Intune_and_Configuration_Manager.md#Step_5).

### <a name="Step_5"></a>Řešení popsaná v tomto článku
Tato část obsahuje základní přehled jednotlivých řešení – implementace Configuration Manageru s Intune, samotná služba Intune, správa mobilních zařízení a služba Azure Rights Management.

-   Správa přístupu k e-mailu pomocí podmíněného přístupu

    Ke správě a vynucení podmíněného přístupu na všech typech počítačů a mobilních zařízení bez ohledu na jejich umístění můžete využívat hybrid Configuration Manageru s Intune nebo samotnou službu Intune současně s Exchangem Online nebo místním Exchange Serverem. Vynucení podmíněného přístupu v tomto typu prostředí vám umožní zajistit vyšší produktivitu uživatelů a zachovat přitom zabezpečení firemních dat.

-   Ochrana dat a příloh e-mailů pomocí řešení MAM

    V Intune můžete vynutit zásady správy mobilních aplikací (MAM) a změnit tak funkce aplikací, které ve vaší společnosti nasadíte. Můžete třeba omezit operace vyjmutí, kopírování a vložení v rámci spravované aplikace nebo aplikaci nakonfigurovat tak, aby všechny webové odkazy otevírala ve spravovaném prohlížeči. Zajistíte tak, že tyto operace odpovídají zásadám zabezpečení a dodržování předpisů vaší společnosti.

-   Služba Azure Rights Management pro zásady prevence ztráty dat

    Azure Rights Management (Azure RMS) využívá zásady ověřování, identity a šifrování k tomu, aby napomohla zabezpečení souborů a e-mailu v různých zařízeních, jako jsou telefony, tablety a počítače. Informace se dají chránit uvnitř vaší společnosti i mimo ni, protože ochrana zůstává s daty, i když opustí prostory vaší společnosti.

### Vyhodnocení požadované implementace
Vzhledem ke spoustě různých možností  návrhu a konfigurací pro správu mobilních zařízení je obtížné určit, která kombinace bude nejlíp vyhovovat potřebám vaší společnosti.[Příručka Průvodce aspekty návrhu správy mobilních zařízení](https://technet.microsoft.com/en-us/library/mt143180.aspx) vám pomůže pochopit požadavky na návrh správy mobilních zařízení a podrobně popisuje kroky a postupy, které vám pomůžou při návrhu řešení, které co nejlíp odpovídá obchodním a technologických požadavkům vaší společnosti.

### Činnost koncového uživatele z globálního pohledu
Po dokončení implementace řešení budou koncoví uživatelé moct přistupovat k firemnímu e-mailu jenom ze spravovaných **a** kompatibilních zařízení. Jakmile budou mít v zařízení možnost přístupu k e-mailu, budou firemní data chráněná, obsažená v ekosystému aplikací a dostupná jenom příslušným uživatelům. Když zařízení přestane být kompatibilní, je možné přístup kdykoli odvolat.

Zásady podmíněného přístupu nastavené v Intune zajišťují, že zařízení mají přístup k e-mailu, jenom když jsou kompatibilní se zásadami dodržování předpisů, které nastavíte. Akce, jako je kopírování a vkládání nebo ukládání s využitím služeb osobního cloudového úložiště, je možné omezit pomocí zásad správy mobilních aplikací. Služba Azure Rights Managements se dá použít k zajištění toho, aby citlivá e-mailová data a předané přílohy mohli číst jenom zamýšlení příjemci. Prostředí koncového uživatele je podrobněji popisuje téma [Činnost koncového uživatele s podmíněným přístupem](../Topic/End-user_experience_of_conditional_access.md).

## Viz také
[Používání podmíněného přístupu s Intune a Configuration Managerem](../Topic/Use_conditional_access_with_Intune_and_Configuration_Manager.md)
[Činnost koncového uživatele s podmíněným přístupem](../Topic/End-user_experience_of_conditional_access.md)

