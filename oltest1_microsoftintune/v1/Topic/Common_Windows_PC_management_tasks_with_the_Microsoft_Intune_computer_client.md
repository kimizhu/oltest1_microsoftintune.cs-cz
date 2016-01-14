---
description: na
keywords: na
title: Common Windows PC management tasks with the Microsoft Intune computer client
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: eb912c73-54d2-4d78-ac34-3cbe825804c7
---
# Běžn&#233; &#250;lohy spr&#225;vy poč&#237;tačů s Windows pomoc&#237; poč&#237;tačov&#233;ho klienta Microsoft Intune
Když si přečte informace uvedené v tomto tématu, dozvíte se, jak spravovat počítače, na kterých běží klient [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]. Jestli jste si tohoto klienta na počítače ještě nenainstalovali, přečtěte si téma [Instalace klienta na počítači s Windows pomocí Microsoft Intune](../Topic/Install_the_Windows_PC_client_with_Microsoft_Intune.md).

## <a name="BKMK_PolicyTasks"></a>Úlohy, při kterých se používají zásady Microsoft Intune

### Použití zásad ke správě brány Windows Firewall
Zásady zjednodušují správu nastavení brány Windows Firewall na spravovaných počítačích. Podrobnosti najdete v tématu [Pomoc se zabezpečením počítačů s Windows pomocí služby Endpoint Protection pro Microsoft Intune](../Topic/Help_secure_Windows_PCs_with_Endpoint_Protection_for_Microsoft_Intune.md).

### Použití zásad ke správě centra Microsoft Intune Center
Pomocí centra [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Center můžou uživatelé dělat toto:

-   Získávat aplikace z portálu společnosti

-   Kontrolovat aktualizace

-   Spravovat službu [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] [!INCLUDE[epshort](../Token/epshort_md.md)]

-   Žádat o vzdálenou pomoc

Centrum [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Center je nainstalované na všech spravovaných počítačích. V zásadách centra [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Center můžete nakonfigurovat následující nastavení, která se uživatelům zobrazí v centru [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] Center:

|Nastavení zásad|Další informace|
|-------------------|-------------------|
|**Název**|Jméno správce, který spravuje příslušný počítač<br /><br />Maximální délka: 40 znaků|
|**Telefonní číslo**|Telefonní číslo správce, který spravuje příslušný počítač<br /><br />Maximální délka: 20 znaků|
|**E-mailová adresa**|Emailová adresa správce, který spravuje příslušný počítač<br /><br />Maximální délka: 40 znaků|
|**Název webu**|Název vašeho webu pro podporu uživatelů<br /><br />Maximální délka: 40 znaků|
|**Adresa URL webu**|Adresa URL vašeho webu podpory<br /><br />Maximální délka: 150 znaků|
|**Poznámky**|Poznámka, která se zobrazuje uživatelům<br /><br />Maximální délka: 120 znaků|

### Použití zásad ke správě nastavení aktualizací softwaru
Pomocí zásad můžete nakonfigurovat nastavení, která budou spravované počítače používat k hledání a stahování aktualizací softwaru od Microsoftu i jiných výrobců. Další informace naleznete v části [Udržování počítačů s Windows v aktuálním stavu díky softwarovým aktualizacím v Microsoft Intune](../Topic/Keep_Windows_PCs_up_to_date_with_software_updates_in_Microsoft_Intune.md).

### Použití zásad ke správě nastavení služby Endpoint Protection
Pomocí zásad můžete nakonfigurovat nastavení pro službu [!INCLUDE[epshort](../Token/epshort_md.md)], která pak můžete nasadit na spravované počítače. Můžou to být třeba plány kontrol, akce, které se mají udělat v případě detekce malwaru, a další věci. Další informace naleznete v části [Pomoc se zabezpečením počítačů s Windows pomocí služby Endpoint Protection pro Microsoft Intune](../Topic/Help_secure_Windows_PCs_with_Endpoint_Protection_for_Microsoft_Intune.md).

## <a name="BKMK_Inventory"></a>Zobrazení inventáře hardwaru a softwaru
[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] shromažďuje podrobné informace o hardwaru a softwaru spravovaných počítačů. V následujících postupech se dozvíte toto:

-   Jak vytvořit sestavu s informacemi o hardwarových možnostech vašich počítačů

-   Jak vytvořit sestavu se seznamem softwaru nainstalovaného na jednotlivých počítačích

-   Jak aktualizovat inventář počítačů, abyste měli jistotu, že jsou data v sestavě aktuální

#### Zobrazení informací o počítačích

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com/) klikněte na **Sestavy** &gt; **Sestavy inventáře počítače**.

2.  Na stránce **Vytvořit novou sestavu** přijměte výchozí hodnoty, případně je upravte, aby se vyfiltrovaly výsledky, které bude sestava obsahovat. Můžete třeba vybrat, aby se v sestavě zobrazily jenom počítače, na kterých běží Windows 8.1.

3.  Kliknutím na **Zobrazit sestavu** otevřete **sestavu inventáře počítače** v novém okně.

    Když kliknete na záhlaví příslušných sloupců, jako je třeba **Název**, **Typ skříně** nebo **Výrobce**, můžete sestavu podle těchto sloupců seřadit.

#### Zobrazení softwaru nainstalovaného na počítačích

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com/) klikněte na **Sestavy** &gt; **Zjištěné zprávy o softwaru**.

2.  Na stránce **Vytvořit novou sestavu** přijměte výchozí hodnoty, případně je upravte, aby se vyfiltrovaly výsledky, které bude sestava obsahovat. Můžete třeba vybrat, aby se v sestavě zobrazil jenom software publikovaný Microsoftem.

3.  Kliknutím na **Zobrazit sestavu** otevřete **sestavu rozpoznaného softwaru** v novém okně.

    Když kliknete na záhlaví příslušných sloupců, jako je třeba **Název**, **Vydavatel** nebo **Kategorie**, můžete sestavu podle těchto sloupců seřadit. Kliknutím na směrovou šipku vedle položky seznamu můžete aktualizace v seznamu rozbalit a zobrazit tak další podrobnosti (třeba počítače, na kterých jsou nainstalované).

#### Aktualizace inventáře počítače, abyste měli jistotu, že je aktuální

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com/) klikněte na **Skupiny** &gt; **Všechna zařízení** (nebo na jinou skupinu obsahující počítač, pro který chcete inventář aktualizovat).

2.  Vyberte počítač. Nebo když stisknete a podržíte **Ctrl**, můžete vybrat víc počítačů.

3.  Na hlavním panelu klikněte na **Vzdálené úlohy** &gt; **Obnovit inventář**.

4.  Pokud chcete zobrazit stav úlohy, klikněte v pravém dolním rohu stránky na **Vzdálené úlohy**.

    V dialogovém okně **Stav úlohy** se zobrazí aktuální vzdálené úlohy, stav úloh, název zařízení, všechny hlášené chyby a odkaz na informace o odstraňování problémů.

## <a name="BKMK_Additional"></a>Další úlohy
Kromě úloh, při kterých se používají zásady, můžete na počítačích dělat taky následující úlohy správy:

#### Vzdálené restartování počítače

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com/) klikněte na **Skupiny** &gt; **Všechna zařízení** (nebo na jinou skupinu obsahující počítač, který chcete restartovat).

2.  Vyberte jeden nebo víc počítačů a pak klikněte na **Vzdálené úlohy** &gt; **Restartovat počítač**.

3.  Pokud chcete zobrazit stav úlohy, klikněte v pravém dolním rohu stránky na **Vzdálené úlohy**.

4.  V dialogovém okně **Stav úlohy** se můžete podívat na aktuální vzdálené úlohy, stav úloh, název zařízení a všechny hlášené chyby.

### <a name="BKMK_Retire"></a>Vyřazení počítače

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com/) klikněte na **Skupiny** &gt; **Všechna zařízení** (nebo na jinou skupinu obsahující počítač, který chcete vyřadit).

2.  Vyberte zařízení, která chcete vyřadit, a pak klikněte na **Vyřadit z provozu či vymazat**.

Když budete chtít počítač do služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] znovu zaregistrovat, přeinstalujte na počítači klientský software, a to podle informací uvedených v tématu [Instalace klienta na počítači s Windows pomocí Microsoft Intune](../Topic/Install_the_Windows_PC_client_with_Microsoft_Intune.md).

Když se nějaký počítač nemůže k [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] připojit, zobrazí se v pracovním prostoru **Řídicí panel** zpráva.

Při vyřazení počítače s stane toto:

-   Počítač se odebere z inventáře [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] a licence, které jsou k němu přiřazené, se uvolní pro nové použití.

-   Jeho stav se už nebude zobrazovat v konzole [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)].

-   [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] odebere z počítače klientský software. Pokud počítač není ke službě [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] připojený, klientský software se odebere, až se počítač zase připojí.

-   Z počítače se odebere služba [!INCLUDE[epshort](../Token/epshort_md.md)]. Pokud je na počítači nainstalovaná jiná aplikace ochrany koncových bodů a je zakázaná, může se tato aplikace po odebrání služby [!INCLUDE[epshort](../Token/epshort_md.md)] zase povolit, aby byla zajištěna ochrana vašich počítačů.

-   Z počítače se odeberou všechny zásady a změní se hodnoty nastavené těmito zásadami.

-   Počítač už nebude od služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] dostávat aktualizace softwaru ani aktualizace definic malwaru.

-   Podle toho, jak jsou vyřazené počítače nakonfigurované, můžou dál dostávat aktualizace pomocí služeb Windows Server Update Services, Windows Update nebo Microsoft Update.

    > [!IMPORTANT]
    > Když byl klientský software nainstalován pomocí objektu zásad skupiny, musíte tento objekt před odebráním klientského softwaru odebrat, abyste zabránili přeinstalaci softwaru.

    Pokud se odinstalace klienta nepovede, přečtěte si další nápovědu v tématu [Řešení potíží se službou Endpoint Protection v Microsoft Intune](../Topic/Troubleshoot_Endpoint_Protection_in_Microsoft_Intune.md).

### <a name="BKMK_UserDeviceLinking"></a>Jak spravovat propojení zařízení s uživatelem
Abyste mohli nasadit software pro uživatele, musíte uživatele propojit s počítačem. Uživatele můžete propojit s několika počítači, ale každý počítač může být propojený jenom s jedním uživatelem. Uživatelé jsou automaticky propojení se všemi počítači, které si přes portál společnosti zaregistrovali v [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

##### Propojení uživatele s počítačem

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com/) klikněte na **Skupiny** &gt; **Všechna zařízení** (nebo na jinou skupinu obsahující počítač, který chcete propojit s uživatelem).

2.  Vyberte počítač, který chcete propojit s uživatelem, a potom klikněte na **Propojit uživatele**.

    V dialogovém okně **Propojit uživatele** se zobrazí seznam dostupných uživatelů včetně jejich zobrazovaného jména, ID a počtu počítačů, se kterými jsou aktuálně propojení. Pokud je s vybraným počítačem už nějaký uživatel propojený, je v části **Aktuální uživatel** zobrazené jeho jméno a ID. Když počítač není propojený s žádným uživatelem, tak se v části **Aktuální uživatel** zobrazuje **Žádný uživatel**.

3.  Udělejte jednu z těchto věcí:

    -   Pokud chcete nechat počítač propojený s aktuálním uživatelem, klikněte na **Storno**.

    -   Pokud chcete propojení s aktuálním uživatelem odebrat, klikněte na **Odebrat odkaz** &gt; **OK**.

    -   Pokud chcete propojit počítač s novým uživatelem, vyberte uživatele v seznamu **Všichni uživatelé**. Potvrďte správnost údajů o uživateli a potom klikněte na **OK**.

> [!TIP]
> Chcete-li koncovým uživatelům omezit schopnosti propojení vlastních účtů s počítači, povolte volbu **Omezit schopnosti uživatelů propojit s počítači vlastní účet** v zásadách **Nastavení agenta Microsoft Intune**.

### Odpověď na žádost o vzdálenou pomoc
Uživatelé můžou požádat o vzdálenou pomoc prostřednictvím nástroje Microsoft Easy Assist, který je na spravovaných počítačích automaticky nainstalovaný. Po odeslání žádosti se v konzole pro správu [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] zobrazí upozornění.

> [!IMPORTANT]
> Vzdálená pomoc není podporovaná na počítačích se systémem Windows 8 nebo novějším.
> 
> Pokud přijmete žádost o vzdálenou pomoc poslanou z počítače, na kterém není nainstalovaný nástroj Microsoft Easy Assist, zobrazí se uživateli výzva k jeho instalaci. Po instalaci se musí počítač restartovat. Abyste se tomuto restartování vyhnuli, je dobré zavést nástroj Microsoft Easy Assist na počítače uživatelů předem.

##### Správa žádosti o vzdálenou pomoc

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com/) klikněte na **Výstrahy** &gt; **Vzdálená pomoc**.

2.  V seznamu **Výstrahy** vyberte žádost o vzdálenou pomoc. Otevře se stránka vlastností této žádosti.

3.  Kliknutím na **Schválit požadavek a spustit vzdálenou pomoc** otevřete dialogové okno, ve kterém budou uvedeny možnosti, jak na žádost reagovat.

4.  Udělejte jednu z těchto věcí:

    -   **Přijměte žádost** – pokud se chcete připojit ke vzdálené relaci, klikněte na **Žádost o vzdálenou pomoc přijměte v případě**.

        Uživateli se zobrazí se zpráva: **Vaše žádost byla přijata. Podle pokynů softwaru Easy Assist nasdílejte program nebo plochu pro správce systému.**.

        > [!IMPORTANT]
        > Žádost o vzdálenou pomoc se nadá přijmout na počítači Mac, na kterém je spuštěná [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)].

    -   **Odmítněte žádost** – zavřete okno **Zobrazit informace o odstraňování potíží** a v okně vlastností výstrahy potom klikněte na **Zavřít tuto výstrahu**.

        Žádost se zavře a uživateli se zobrazí zpráva, že žádost byla odmítnuta. Když bude chtít uživatel požádat o vzdálenou pomoc znova, musí poslat novou žádost o vzdálenou pomoc. Když výstrahu vzdálené pomocí zavřete omylem, kontaktujte uživatele, který žádost o vzdálenou pomoc poslal, a požádejte ho, aby poslal novou žádost.

## <a name="BKMK_Next"></a>Potřebujete další pomoc?
Další nápovědu a podporu najdete v tématu [Řešení potíží se službou Endpoint Protection v Microsoft Intune](../Topic/Troubleshoot_Endpoint_Protection_in_Microsoft_Intune.md).

## Viz také
[Správa počítačů s Windows pomocí Intune](../Topic/Manage_Windows_PCs_with_Microsoft_Intune.md)

