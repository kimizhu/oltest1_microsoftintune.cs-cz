---
description: na
keywords: na
title: Configure and manage devices with Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7b938d95-c068-4d71-a580-c1492c4bff27
---
# Konfigurace a spr&#225;va zař&#237;zen&#237; přes Microsoft Intune
![](../Image/Nav_Icons/WIT_Tile_W_Overview.png)![](../Image/Nav_Icons/WIT_Tile_W_GetStarted.png)![](../Image/Nav_Icons/WIT_Tile_W_EnrollDevices.png)![](../Image/Nav_Icons/WIT_Tile_W_ManageDevicesHighlight.png)![](../Image/Nav_Icons/WIT_Tile_W_ManageApps.png)![](../Image/Nav_Icons/WIT_Tile_W_ProtectResources.png)![](../Image/Nav_Icons/WIT_Tile_W_RetireData.png)![](../Image/Nav_Icons/WIT_Tile_W_TechnicalReference.png)![](../Image/Nav_Icons/WIT_Tile_W_Troubleshooting.png)
![](../Image/Nav_Icons/WIT_Banner_ManageDevices.png)

Pomocí profilů sítě VPN, profilů sítě wi-fi a zásad konfigurace můžete zaměstnancům umožnit přístup k síti při současném splnění požadavků zabezpečení vaší společnosti.

Vaši uživatelé chtějí používat e-maily a pracovat ze všech možných zařízení a chtějí mít možnost používat tato zařízení k těmto účelům, kdekoli budou chtít. To sice znamená, že budou moci ve větší míře produktivně pracovat, ale přináší to také problémy z hlediska zabezpečení dat vaší společnosti.

[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] může vyřešit tyto problémy s profily sítě, profily sítě Wi-Fi a zásadami konfigurace.

## Použití profilů sítě VPN nebo profilů sítě wi-fi k umožnění přístupu k prostředkům společnosti
Zaměstnancům můžete usnadnit přístup k e-mailům nebo přístup k prostředkům společnosti pomocí sítě Wi-Fi nebo sítě VPN díky [profilům přístupu k prostředkům](https://technet.microsoft.com/library/dn997277.aspx). Tyto profily umožňují předem nakonfigurovat v zařízeních nastavení přístupu, která se v zařízeních potřebují pro e-maily a soubory společnosti. Spousta lidí například pro práci na dálku používá sítě VPN. Nastavení pro vytvoření připojení VPN (nebo **profilu**) jsou komplexní a běžný koncový uživatel je nemusí umět nakonfigurovat.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] vám umožní tato nastavení předem nakonfigurovat a nasadit do zařízení uživatelů. To znamená, že zaměstnanci nemusí zadávat komplexní nastavení sítě VPN. Stačí, když vyberou profil sítě VPN ze seznamu a automaticky se připojí. Kromě toho můžete k zabezpečení těchto připojení využít výhod zabezpečení, které nabízí používání certifikátů.

## Správa nastavení a funkcí pomocí zásad služby Intune
Představte si, že jste správcem IT společnosti zabývající se designem. Pracujete na novém produktu a nechcete, aby podrobnosti o produktu pronikly na veřejnost. Rozhodnete, že z důvodu maximálního zabezpečení zakážete na mobilních zařízeních zaměstnanců používání fotoaparátu.[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] vám toho umožňuje snadno dosáhnout pomocí **zásad konfigurace**.

I když [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] nabízí pro konfiguraci zařízení [širokou škálu nastavení](https://technet.microsoft.com/library/dn646984.aspx), nemusí být nastavení, které potřebujete, v některých případech dostupné. V řadě případů můžete tento problém vyřešit pomocí vlastní zásady, která vám umožní nakonfigurovat nastavení OMA-URI, což je běžný standard pro konfiguraci mobilních zařízení na požadované hodnoty.

## Správa počítačů
Můžete sice [zaregistrovat počítače se systémem Windows 8.1 a novějším](https://technet.microsoft.com/library/dn764959.aspx) jako mobilní zařízení, v některých případech je ale můžete chtít spravovat tak, že do nich nainstalujete počítačového klienta služby Intune.[Správa počítačů přes Intune](https://technet.microsoft.com/library/dn646959.aspx) vám dává některé možnosti, které nejsou k dispozici, když počítače spravujete jako mobilní zařízení, například správu aktualizací softwaru Windows a nastavení služby EndPoint Protection a brány Windows Firewall.

## Viz také
[Dokumentace pro Microsoft Intune](../Topic/Documentation_for_Microsoft_Intune.md)

