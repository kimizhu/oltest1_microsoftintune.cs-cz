---
description: na
keywords: na
title: Windows PC management capabilities in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 77fa5c66-a87c-47df-964c-800eea509b33
---
# Možnosti spr&#225;vy poč&#237;tačů s Windows v Microsoft Intune
[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] můžete použít ke správě počítačů s Windows a s nainstalovaným klientem Intune. Správa počítačů umožňuje na spravované počítače nasazovat aplikace a software včetně softwarových aktualizací a spravovat službu Endpoint Protection a bránu Firewall systému Windows a další věci.  Dál je uvedený seznam podporovaných konfigurací a možností.

## <a name="BKMK_ClientReqs"></a>Požadavky na správu stolních počítačů
**Operační systémy**: 
Klienta [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] můžete nainstalovat na počítačích, na kterých běží tyto operační systémy (x86 i x64):

-   **Windows Vista** – verze Business, Enterprise a Ultimate

-   **Windows 7** – verze Professional, Enterprise a Ultimate (bez aktualizace Service Pack nebo s aktualizací SP1)

-   **Windows 8** – verze Professional a Enterprise

-   **Windows 8.1** – verze Professional a Enterprise

-   **Windows 10** – verze Professional a Enterprise

**Hardware:**:
Toto jsou minimální požadavky na hardware pro instalaci klienta [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]:

|Požadavek|Další informace|
|-------------|-------------------|
|Síť|Klient vyžaduje, aby byl počítač připojený k Internetu.|
|Procesor a paměť|Viz požadavky na procesor a paměť RAM pro operační systém počítače.|
|Místo na disku|200 MB volného místa na disku před instalací klientského softwaru.|
**Software**: 
Požadavky na software pro instalaci klienta [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]:

|Požadavek|Další informace|
|-------------|-------------------|
|Oprávnění správce|Účet, který instaluje klientský software, musí mít oprávnění místního správce k tomuto počítači.|
|Instalační služba systému Windows verze 3.1|Na počítači musí být Instalační služba systému Windows minimálně verze 3.1.<br /><br />Pokud chcete zobrazit verzi Instalační služby systému Windows na počítači:<br /><br />-   Na počítači klikněte pravým tlačítkem na **%windir%\System32\msiexec.exe** a potom klikněte na **Vlastnosti**.<br /><br />Nejnovější verzi Instalační služby systému Windows můžete stáhnout ze stránky [Windows Installer Redistributables](http://go.microsoft.com/fwlink/?LinkID=234258) na webu Microsoft Developer Network.|
|Odebrání nekompatibilního klientského softwaru|Před instalací klientského softwaru [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] je potřeba odinstalovat z tohoto počítače tento klientský software:<br /><br />-   Všechny verze aplikace [!INCLUDE[cm5short](../Token/cm5short_md.md)]<br />-   Všechny verze aplikace [!INCLUDE[sccmshortname](../Token/sccmshortname_md.md)]<br />-   Všechny verze Systems Management Serveru (SMS)|

## <a name="WIT_Cap"></a>Možnosti správy počítačů s Intune

-   **Správa aktualizací softwaru.** Vaše počítače můžou být pořád aktuální. Můžete určit, kdy se mají aktualizace použít.

-   **Zásady brány Windows Firewall.** Tyto zásady pomáhají zajistit, že v žádném počítači používaném ve vaší společnosti není neaktivní nebo nesprávně nakonfigurovaná brána Windows Firewall.

-   **Ochrana proti malwaru.** Součástí [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] je služba Endpoint Protection, která pomáhá chránit počítače před malwarem.

-   **Vzdálená pomoc.**[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] umožňuje uživatelům kontaktovat pracovníky technické podpory, kteří jim pak můžou pomoci prostřednictvím funkce vzdálené plochy, která je součástí [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

-   **Správa softwarových licencí.** Můžete sledovat, kolik licencí softwaru je dostupných a kolik z nich se právě používá.

## Viz také
[Úvod do Microsoft Intune](../Topic/Introduction_to_Microsoft_Intune.md)
[Správa počítačů s Windows pomocí Intune](../Topic/Manage_Windows_PCs_with_Microsoft_Intune.md)

