---
description: na
keywords: na
title: Microsoft Intune App SDK Frequently Asked Questions
search: na
ms.date: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 133d81c4-e550-404a-980e-64f6e843c649
---
# Nejčastějš&#237; dotazy k Microsoft Intune App SDK
Zde jsou uvedeny některé časté dotazy ohledně sady Intune App SDK.

## Našel jsem problém se sadou Intune App SDK nebo v dokumentaci. Jak mohu odeslat zpětnou vazbu nebo nahlásit problém?

Zpětná vazba týkající se sady Intune App SDK jde odeslat prostřednictvím webu Microsoft Connect. Tam uvidíte možnost odeslat zpětnou vazbu nebo nahlásit problém. Uveďte prioritu odeslaných problémů a tým Microsoft Intune se jimi bude zabývat při nejbližší možné příležitosti.

![Formulář zpětné vazby aplikace](/Image/App_Feedback_Form.png)

## Jak sada Intune App SDK zachází s aktualizacemi operačního systému a kompatibilitou?

Pokusíme se zajistit, aby existující funkce SDK fungovaly v nových verzích operačních systémů co nejdřív a aby sada SDK nezpůsobovala havárie aplikací nebo neměla významný dopad na koncové uživatele kvůli přístupu k funkcím nového operačního systému v rámci existujících aplikací.

Když prodejci operačních systémů poskytnou dostatečnou dobu realizace, , Intune poskytne podporu beta verzím operačních systémů pro umožnění testování aplikací před vydáním. Nezávislí dodavatelé softwaru by měli předem ohlásit objevené problémy s kompatibilitou nebo plány na vydání verzí aplikace cílených na verze Preview operačních systémů.

Nové funkce přidané do sady SDK nebudou porušovat existující kompatibilitu s operačním systémem bez předchozího upozornění a schválení od Microsoftu. Nechtěné problémy s kompatibilitou budou řešeny jako chyby.

## Jak sada Intune App SDK ovlivní mé mobilní aplikace?

Sada SDK může ovlivnit aplikaci třemi hlavními způsoby.
* **Výkon**: Metody použité k vynucení zásad mohou ovlivnit výkon aplikace. Otestujte výkon a nahlaste všechny problémy jako chyby a zahrňte výsledky výkonu pro scénář se zásadami a bez nich.
* **Volitelné funkce**: Sada SDK podporuje volitelné funkce prostřednictvím plochy rozhraní API (např. uložit jako). Tyto funkce vyžadují k podpoře změny aplikace.
    System_CAPS_noteNote

    Telemetrie je funkce vyžadující souhlas. Sada SDK iOS MAM protokoluje **ve výchozím nastavení** telemetrická data sady SDK o událostech využití. Tato data se odešlou do Microsoft Intune. Pokud se rozhodnete neodesílat telemetrická data sady SDK z vaší aplikace do Microsoft Intune, musíte zakázat přenos telemetrie sady SDK v `IntuneMAMSettings` nastavením vlastnosti `MAMTelemetryDisabled` na hodnotu YES.
* **Vynucení zásad**: Když se zásady MAM použijí na aplikace sady SDK, mohou být ovlivněny funkce aplikace a činnost koncových uživatelů. Týmy aplikací by měly spolupracovat s týmem Intune na testování aplikací a porozumění tomuto vlivu.



