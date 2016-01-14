---
description: na
keywords: na
title: Help protect iOS devices with Activation Lock bypass for Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2804b69c-f210-4a11-aaee-b47ecc430d9c
---
# Pomoc při ochraně zař&#237;zen&#237; s iOS pomoc&#237; funkce Vynechat z&#225;mek aktivace pro Microsoft Intune
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] vám může pomoci spravovat zámek aktivace v iOS – funkci aplikace Najít iPhone pro zařízení s iOS 7.1 a novějším. Zámek aktivace se povolí automaticky, když se na zařízení používá aplikace Najít iPhone. Když je tato funkce povolená, musí se zadat Apple ID a heslo uživatele, aby bylo možné:

-   Vypnout aplikaci Můj iPhone

-   Vymazat zařízení

-   Znovu aktivovat zařízení

## Jaký vliv má funkce Zámek aktivace na práci se zařízením
Funkce Zámek aktivace sice pomáhá zabezpečit zařízení s iOS a zvyšuje šance na obnovení zařízení v případě, že dojde k jeho ztrátě nebo odcizení, může ale pro vás, jakožto správce IT, představovat určité problémy. Například:

-   Jeden z vašich uživatelů si na zařízení nastaví zámek aktivace. Tento uživatel pak společnost opustí a zařízení vrátí. Bez Apple ID a hesla uživatele neexistuje způsob, jak zařízení znovu aktivovat.

-   Potřebujete sestavu všech zařízení, která mají povolený zámek aktivace.

-   V rámci obnovování zařízení v organizaci chcete přiřadit některá zařízení jinému oddělení. Můžete to provést jedině se zařízeními, ve kterých není zámek aktivace povolený.

Aby bylo možné tyto problémy vyřešit, společnost Apple vydala v iOS 7.1 funkci vyřazení zámku aktivace. To vám umožní odebrat zámek aktivace z dozorovaných zařízeních i bez Apple ID a hesla uživatele. Dozorovaná zařízení mohou generovat kód pro vyřazení zámku aktivace, který je uložený na aktivačním serveru společnosti Apple.

> [!TIP]
> Dozorový režim pro zařízení s iOS vám umožňuje pomocí nástroje Apple Configurator zařízení zamknout a omezit tak jeho funkčnost jenom na konkrétní firemní účely. Dozorový režim je obecně určený výhradně pro zařízení v majetku podniků.

## Jak Intune pomáhá se správou zámku aktivace
[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] může požádat o stav zámku aktivace jak u dozorovaných, tak i u nedozorovaných zařízení, na kterých běží iOS 7.1 a novější. Pro dozorovaná zařízení může [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] získat kód pro vyřazení zámku aktivace a přímo ho předat zařízení. Pokud bylo zařízení vymazáno, můžete k zařízení získat přístup tak, že jako uživatelské jméno zadáte tento kód a heslo necháte prázdné).

Pro firmy to má tyto výhody:

-   Uživatel získá výhody zabezpečení aplikace Najít iPhone.

-   Dokážete zajistit, aby uživatel mohl zařízení používat ke své práci, a zároveň budete vědět, že když bude nutné zařízení použít k jinému účelu, budete ho schopni vyřadit nebo odemknout.

## Jak používat vyřazení zámku aktivace z konzoly pro správu služby Intune
> [!IMPORTANT]
> Po vyřazení zámku aktivace na zařízení se při otevření aplikace Najít iPhone automaticky použije nový zámek aktivace. Z tohoto důvodu byste měli mít před provedením tohoto postupu zařízení fyzicky u sebe.

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com) klikněte na **Skupiny** &gt; **Všechna zařízení** &gt; **Všechna zařízení ve vlastnictví firmy**.

2.  Vyberte zařízení, jehož zámek aktivace chcete vyřadit, a potom klikněte na **Vynechat zámek aktivace**.

3.  Přečtěte si upozornění a potom pokračujte kliknutím na **Ano**.

Stav požadavku na odemčení můžete zkontrolovat na stránce podrobností pro dané zařízení.

## Jak zjistit, která zařízení zámek aktivace používají
To, která zařízení zámek aktivace používají, můžete zjistit dvěma způsoby:

-   Spustíte **sestavy inventáře mobilních zařízení**. Tato sestava obsahuje sloupec **Stav zámku aktivace** a **Pod dohledem**, ze kterých je možné zjistit stav zařízení. Hodnoty pro sloupec **Pod dohledem** jsou **Ano** nebo **Ne** a hodnoty pro sloupec **Stav zámku aktivace** jsou:

    -   **Povolené s kódem alternativní metody komunikace**

    -   **Povolené bez kódu alternativní metody komunikace (zařízení není pod dohledem)**

    -   **Povolené bez kódu alternativní metody komunikace (zařízení je nedostupné)**

    -   **Nepovolené**

    U zařízení, na kterých neběží iOS 7.1 nebo novější, je pole **Stav zámku aktivace** prázdné.

-   V zobrazení skupin vyberte zařízení. Stav aktivace zámku uvidíte v podokně podrobností o zařízení.

    Pokud vyberete zařízení v uzlu **Všechna zařízení ve vlastnictví firmy** a zámek aktivace je pro zařízení povolený, uvidíte také kód pro vyřazení zámku. Pomocí tohoto kódu je možné ručně vyřadit zámek aktivace.

## Viz také
[Vyřazení dat a zařízení ze správy službou Microsoft Intune](../Topic/Retire_data_and_devices_from_Microsoft_Intune_management.md)

