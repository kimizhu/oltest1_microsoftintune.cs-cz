---
description: na
keywords: na
title: Understand your devices with inventory in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 312911fe-b963-4949-9911-ae425e0590b2
---
# Sezn&#225;men&#237; se zař&#237;zen&#237;mi s invent&#225;řem v Microsoft Intune
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] umožňuje zobrazit inventář spravovaných zařízení a počítačů ve vaší organizaci.

## Zobrazení inventáře mobilních zařízení
Pokud chcete zobrazit inventář, který shromažďují mobilní zařízení, spusťte [sestavy inventáře mobilních zařízení](https://technet.microsoft.com/library/dn646977.aspx).[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] shromažďuje z mobilních zařízení tyto inventáře:

|Skupina vlastností|Vlastnost|Exchange ActiveSync|iOS|Windows RT a Windows 8.1|Windows Phone 8 a Windows Phone 8.1|Poznámky|
|----------------------|-------------|-----------------------|-------|----------------------------|---------------------------------------|------------|
|Systému|Název|Ano|Ano|Ano|Ano||
||Jedinečné ID zařízení||Ano|Ano|Ano||
||Sériové číslo||Ano||||
||E-mailová adresa|Ano|||||
|Operační systém|Typ operačního systému|Ano||Ano|Ano||
||Verze operačního systému|Ano|Ano|Ano|Ano||
||Jazyk operačního systému|Ano|||Ano||
|Úložiště|Celkový úložný prostor||Ano|Ano||Zobrazeno v GB|
||Volný úložný prostor||Ano|Ano||Zobrazeno v GB|
|Podrobnosti výměny|Poslední stav výměny|Ano|||||
||Poslední stav aktualizace zásad|Ano|||||
||Stav přístupu|Ano|||||
||Důvod stavu přístupu|Ano|||||
||ID ActiveSync|Ano|||||
|Skříň systému|Skříň|Ano|„Unknown“|„Unknown“|„Unknown“|U zařízení spravovaných v MDM se ve vlastnosti Skříň zobrazí „Unknown“ (Neznámá).|
||IMEI||Ano||||
||MEID||Ano||||
||Výrobce|||Ano|Ano||
||Model|Ano|Ano|Ano|Ano||
||Telefonní číslo||Ano|||S výjimkou 4 posledních číslic je telefonní číslo zakryté hvězdičkami (&#42;).|
|Podrobnosti o síti|Poskytovatel předplatného||Ano||||
||Mobilní technologie||Ano||||
||Wi-Fi MAC||Ano|Ano|||
|Informace o službě|Datum zápisu||Ano|Ano|Ano|Zobrazuje se v místním čase.|
||Poslední spojení|Ano|Ano|Ano|Ano|Zobrazuje se v místním čase.|
||Stav správy|Ano|||||

## Zobrazení inventáře počítačů
Pokud chcete zobrazit inventář, který shromažďují počítače, spusťte [sestavy inventáře počítačů](https://technet.microsoft.com/library/dn646977.aspx).

## Viz také
[Monitorování a sestavy v Microsoft Intune](../Topic/Monitoring_and_reports_with_Microsoft_Intune.md)

