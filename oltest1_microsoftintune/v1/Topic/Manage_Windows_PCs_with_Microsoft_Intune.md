---
description: na
keywords: na
title: Manage Windows PCs with Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3b8d22fe-c318-4796-b760-44f1ccf34312
---
# Spr&#225;va poč&#237;tačů s Windows pomoc&#237; Intune
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] můžete kromě správy mobilních zařízení použít taky ke správě počítačů s podporovaným operačním systémem pomocí počítačového klientského softwaru [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].[Požadavky na hardware a software](https://technet.microsoft.com/library/dn646975.aspx) pro spuštění počítačového klienta jsou minimální, dá se říct, že je podporovaný libovolný systém schopný spustit Windows Vista nebo novější verzi.  Klientský software se taky dá snadno nainstalovat do počítačů připojených k doméně (v libovolné doméně) i do počítačů, které do žádné domény připojené nejsou.

[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] spravuje počítače pomocí zásad podobně jako objekty zásad skupiny (GPO) služby AD DS (Active Directory Domain Services) Windows Serveru. Pokud budete počítače připojené k doméně Active Directory spravovat pomocí [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], měli byste [ověřit, že zásady Intune nejsou v konfliktu se žádnými objekty zásad skupiny](https://technet.microsoft.com/library/dn646986.aspx), které jsou nastaveny pro vaši organizaci.

> [!NOTE]
> Microsoft Intune jako samostatná služba nabízí tyto funkce pro správu počítačů. Zařízení se systémem Windows 8.1 můžete spravovat pomocí klienta Intune nebo je můžete zaregistrovat jako mobilní zařízení. Níže uvedené informace platí pro počítače, které používají klienta Intune. Informace o možnostech správy mobilních zařízení, najdete v tématu [Možnosti správy mobilních zařízení v Microsoft Intune](https://technet.microsoft.com/library/dn600287(TechNet.10).aspx).

## Instalace počítačového klienta Intune
Prvním krokem při správě počítačů pomocí [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] je instalace klienta. Klientský software se dá nainstalovat, když je počítač zaregistrovaný ve službě [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] jedním z následujících způsobů:

-   Můžete [ručně nasadit klientský software Microsoft Intune](https://technet.microsoft.com/library/dn646969.aspx#BKMK_Manual). U tohoto typu nasazení správce stáhne klientský software Intune a ručně ho nainstaluje do všech počítačů.

    Pokud chcete stáhnout klientský software Intune, otevřete konzolu správy Intune a v části Stažení klientského softwaru stáhněte balíček klientského softwaru. Po dokončení instalace klientského softwaru Intune automaticky nainstaluje další software nezbytný ke správě počítače.

-   Stejné soubory, které jste stáhli pro ruční instalaci klienta Intune, můžete použít pro [nasazení klienta do počítačů připojených k doméně pomocí objektů zásad skupiny Active Directory](https://technet.microsoft.com/library/dn646969.aspx).

-   [Koncoví uživatelé můžou své počítače sami zaregistrovat](https://technet.microsoft.com/library/dn646969.aspx) pomocí portálu společnosti Intune. Každý zaregistrovaný počítač se pak automaticky propojí s uživatelským účtem použitým při instalaci klientského softwaru Intune.

-   Klientský software Intune můžete do počítačů taky nasadit jako součást [nasazení operačního systému](https://technet.microsoft.com/library/dn646969.aspx).

## Správa počítačů pomocí počítačového klienta Intune
Po dokončení instalace klienta Intune klientský software povolí několik funkcí správy počítačů, včetně [správy aplikací](https://technet.microsoft.com/library/dn646961.aspx), Endpoint Protection, inventáře softwaru a hardwaru, vzdáleného řízení (prostřednictvím žádostí o vzdálenou pomoc), aktualizací softwaru a vytváření sestav nastavení dodržování předpisů.

Některé úlohy správy počítačů povolené počítačovým klientem se spravují pomocí zásad Intune, jako třeba:

-   Konfigurace [nastavení brány Windows Firewall](https://technet.microsoft.com/library/mt346040.aspx) ve spravovaných počítačích.

-   Konfigurace [nastavení aktualizací softwaru](https://technet.microsoft.com/library/dn646968.aspx), které mají spravované počítače kontrolovat, a stažení požadovaných aktualizací softwaru.

-   Pomoc při zabezpečení spravovaných počítačů před potenciálními hrozbami a škodlivým softwarem pomocí správy [monitorování v reálném čase a Endpoint Protection](https://technet.microsoft.com/library/dn646970.aspx).

Kromě akcí klientského agenta Intune prováděných lokálně v jednotlivých počítačích je možné konzolu správce Intune využít taky k dalším [běžným úlohám správy](https://technet.microsoft.com/library/dn646989.aspx) u počítačů s nainstalovaným klientem:

-   Zobrazení informací o inventáři hardwaru a softwaru pro spravované počítače

-   Vzdálené restartování počítače

-   Vyřazení počítače pro odinstalaci klientského softwaru a jeho odebrání ze správy pomocí Intune

-   Propojení uživatelů ke konkrétním spravovaným počítačům

-   Odpověď na žádosti o vzdálenou pomoc

Klientský agent Intune obvykle běží tiše na pozadí a nevyžaduje skoro žádnou interakci ze strany uživatele ani řešení potíží. Pokud byste ale potřebovali pomoc při řešení potíží se správou počítačů, je dostupných několik [prostředků, které vám je pomůžou vyřešit](https://technet.microsoft.com/library/dn646987.aspx).

## Viz také
[Konfigurace a správa zařízení přes Microsoft Intune](../Topic/Configure_and_manage_devices_with_Microsoft_Intune.md)

