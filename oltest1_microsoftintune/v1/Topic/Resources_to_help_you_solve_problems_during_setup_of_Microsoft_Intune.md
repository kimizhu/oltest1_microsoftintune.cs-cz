---
description: na
keywords: na
title: Resources to help you solve problems during setup of Microsoft Intune
search: na
ms.date: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6865f1fb-c2c1-47af-83f5-5704e7210a49
robots: noindex,nofollow
---
# Materi&#225;ly, kter&#233; v&#225;m pomůžou při řešen&#237; pot&#237;ž&#237; během instalace Microsoft Intune
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] je cloudová služba, proto by nemělo být moc potřeba opravovat nebo odstraňovat provozní potíže. Pokud se při přístupu ke službě setkáte s problémy, v následujících částech můžete zjistit, jaké další kroky je potřeba provést.

## <a name="BKMK_ResolveSetupProblems"></a>Tipy pro řešení problémů s instalací a konfigurací Microsoft Intune
[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] negeneruje instalační nebo provozní protokoly, které byste mohli využít k řešení problémů.

Vaše akce správy využívají webový prohlížeč pro připojení ke cloudové službě. Problémy s přístupem ke službě mají obvykle některou z těchto příčin:

|Problém|Podrobnosti|
|-----------|---------------|
|Nedostatečná oprávnění pro [!INCLUDE[wit_icp_1](../Token/wit_icp_1_md.md)]|Pokud chcete používat [!INCLUDE[wit_icp_1](../Token/wit_icp_1_md.md)] ke správě více než vlastního profilu uživatele, musí váš účet:<br /><br />-   mít licenci pro používání [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)],<br />-   mít pro přihlášení stav přihlašování **Povoleno**,<br />-   být správcem klienta [!INCLUDE[wit_icp_1](../Token/wit_icp_1_md.md)].<br /><br />Informace naleznete v tématu [Účty správce Intune a zvláštní oprávnění](../Topic/What_to_know_before_setting_up_Microsoft_Intune.md#BKMK_AdminAccounts).|
|Přístup k síti včetně:<br /><br />-   Domény používané službou [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]<br />-   Provoz v síti<br />-   Podpora webového prohlížeče|Pokud se chcete připojit k [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], musíte:<br /><br />-   použít podporovaný webový prohlížeč,<br />-   mít přístup v síti přes brány firewall nebo proxy servery k různým doménám, které služba [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] používá.<br /><br />Informace o požadavcích a konfiguracích nezbytných k používání služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] najdete v tématech:<br /><br />-   [Infrastructure requirements](../Topic/Network_infrastructure_requirements_for_Microsoft_Intune.md#BKMK_InfrastructureReqs)<br />-   [Web browsers supported by Microsoft Intune](../Topic/Network_infrastructure_requirements_for_Microsoft_Intune.md#BKMK_SupportedBrowsers)|
|Dostupnost služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]|Pokud vás zajímají podrobnosti (nebo pokud se chcete přihlásit k odběru informačních kanálů RSS) o stavu služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], podívejte se sem:<br /><br />-   [Služba Microsoft Intune](http://status.manage.microsoft.com/)|

## Viz také
[Úvod do Microsoft Intune](../Topic/Introduction_to_Microsoft_Intune.md)

