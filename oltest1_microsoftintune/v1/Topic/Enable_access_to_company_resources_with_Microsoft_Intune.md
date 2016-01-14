---
description: na
keywords: na
title: Enable access to company resources with Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3dd8dd4e-e165-4d0c-97b7-b3e86ebab909
---
# Povolen&#237; př&#237;stupu k prostředkům společnosti se službou Microsoft Intune
**Profily přístupu k prostředkům**[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] společně pomáhají zajistit uživatelům přístup odkudkoli k souborům a prostředkům, které potřebují ke své práci.

[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] poskytuje následující zásady pro mobilní zařízení, které vám k dosažení tohoto cíle pomohou. Kliknutím na libovolnou položku v tabulce získáte podrobné informace o tom, jak danou zásadu konfigurovat:

## Profily přístupu k prostředkům a podporované platformy

|Zásady Intune|Účel|Windows 8.1 a vyšší|Windows Phone 8.1 nebo novější|iOS|Android|Samsung KNOX|
|-----------------|--------|-----------------------|----------------------------------|-------|-----------|----------------|
|[Profily certifikátů](https://technet.microsoft.com/library/dn818904.aspx)|Pomozte zabezpečit přístup k prostředkům společnosti, včetně bezdrátových sítí a připojení VPN.|Ano|Ano|Ano|Ano|Ano|
|[Profily sítě Wi-Fi](https://technet.microsoft.com/library/dn818903.aspx)|Nasaďte uživatelům nastavení bezdrátové sítě. Nasazením těchto nastavení minimalizujete úsilí koncových uživatelů potřebné k připojení k firemní síti.|Ano (můžete naimportovat profil sítě Wi-Fi systému Windows)|Ano (můžete nakonfigurovat OMA URI) <sup>1</sup>|Ano|Ano|Ano|
|[Profily sítě VPN](https://technet.microsoft.com/library/dn818905.aspx)|Nasaďte uživatelům nastavení virtuální privátní sítě (VPN). Nasazením těchto nastavení zjednodušíte koncovým uživatelům připojování k prostředkům v podnikové síti.|Ano|Ano|Ano|Ano|Ano|
|[E-mailové profily](https://technet.microsoft.com/library/dn800672.aspx)|Vytváření, nasazování a sledování nastavení e-mailů Exchange ActiveSync na zařízeních ve vaší organizaci.|Ne|Ano|Ano|Ne|Ano|
<sup>1</sup> Informace o tom, jak nakonfigurovat profil sítě Wi-Fi systému Windows Phone 8.1 pomocí OMA URI, najdete [v tomto příspěvku blogu](http://blogs.technet.com/b/microsoftintune/archive/2015/02/23/using-oma-uri-to-create-custom-wi-fi-profiles-for-windows-phone-8-1.aspx).

## Viz také
[Konfigurace a správa zařízení přes Microsoft Intune](../Topic/Configure_and_manage_devices_with_Microsoft_Intune.md)

