---
description: na
keywords: na
title: Update apps using Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: beee6933-876a-4be0-b395-4c24cfbd519b
---
# Aktualizace aplikac&#237; pomoc&#237; služby Microsoft Intune
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] může pomoci při správě aktualizací aplikací. Informace v tomto tématu vám můžou pomoct pochopit, jak můžete aktualizovat aplikace, pokud je vyžadována novější verze.

## Jak aplikace aktualizovat
Po vydání nové verze aplikace, kterou máte nasazenou, vám [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] umožní aktualizovat a nasadit novější verze aplikace. Nasazení můžete nahradit jedině novější verzi stejné aplikace (pomocí stejného identifikátoru). Aktualizace aplikací nejde použít k aktualizaci nasazení s jiným balíčkem aplikace.

> [!IMPORTANT]
> Když nasadíte aplikaci pomocí akce nasazení **Požadovaná instalace** a později změníte akci nasazení na **Dostupná instalace**, nenainstalují se aktualizace aplikace automaticky na zařízení, na která se aplikace nainstalovala ještě před provedením změny nasazení. Pokud budete chtít tento problém vyřešit, můžete udělat toto:
> 
> -   Řekněte uživateli zařízení, aby přešel na portál společnosti, vybral nainstalovanou aplikaci a potom kliknul na **Nainstalovat**.
> -   Změňte akci nasazení na **Odinstalace** a po odinstalaci aplikace aplikaci znovu nasaďte pomocí akce nasazení **Dostupná instalace**.

#### Aktualizace aplikace

1.  V [konzole pro správu Microsoft Intune](https://account.manage.microsoft.com/admin/default.aspx) klikněte na **Aplikace** &gt; **Aplikace**.

2.  Ze seznamu **Aplikace** vyberte aplikaci, kterou chcete aktualizovat, a potom klikněte na **Upravit**.

3.  V průvodci **úpravou softwaru** zadejte jakékoli nového podrobnosti balíčku aplikace.

4.  Až to budete mít, klikněte na **Aktualizovat**.

Až budou zařízení příště zjišťovat dostupnost aplikací, aplikace se automaticky aktualizuje na nejnovější verzi.

## Viz také
[Nasazení a konfigurace aplikací v Microsoft Intune](../Topic/Deploy_and_configure_apps_with_Microsoft_Intune.md)
[Vyřazení aplikací pomocí služby Microsoft Intune](../Topic/Retire_apps_using_Microsoft_Intune.md)

