---
description: na
keywords: na
title: Get notified by Microsoft Intune alerts
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 396ea714-0433-4bd5-a934-8d0b477f28e4
---
# Upozorňov&#225;n&#237; pomoc&#237; v&#253;strah služby Microsoft Intune
Výstrahy umožňují neustále vědět, co se děje v [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)].

Výstrahy vás můžou informovat například o následujících událostech:

-   Potíže se součástí Exchange Connector, které ovlivňují správu mobilních zařízení

-   Malware zjištěný v počítači

-   Zjištění konfliktu mezi dvěma zásadami [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]

-   Nejnovější aktualizace a informace o službě [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] (oznámení).

## Jak výstrahy fungují
Výstrahy jsou generované na základě **typů výstrah**. To je sada předkonfigurovaných pravidel integrovaných do [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Například výstraha typu **Cloudové úložiště má 10 % volného místa nebo méně** upozorňuje na skutečnost, že v cloudu přestáváte mít dost místa pro ukládání aplikací. Jednotlivé typy výstrah můžete povolit nebo zakázat a také můžete nakonfigurovat jejich vlastnosti. Například u výše uvedeného typu výstrahy můžete nakonfigurovat:

-   **Stav:** To, jestli je tento typ výstrahy povolený nebo zakázaný.

-   **Závažnost:** Jak závažná je tato výstraha?

    |||
    |-|-|
    |Závažnost|Popis|
    |![](../Image/Critical_Alert.jpg)|Označuje závažné potíže, které byste měli prozkoumat co nejdřív, například zjištění malwaru v počítači.|
    |![](../Image/Warning_Alert.jpg)|Označuje potíže, které ještě nejsou závažné, ale mohly by se závažnými stát, když jim nebudete věnovat pozornost, například aktualizace zabezpečení čekající na instalaci.|
    |![](../Image/Informational_Alert.jpg)|Označuje informace, které nejsou pro vaši práci nepostradatelné, například dostupnost nové verze součásti Exchange Connector.|

Ostatní typy výstrah můžou obsahovat různé položky, které můžete konfigurovat, například procento zařízení, které musí být konkrétními potížemi ovlivněné, aby byla vygenerovaná výstraha.

**Při splnění kritérií pro typ výstrahy se vygeneruje příslušná výstraha a zobrazí se v konzole správce [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].**

Navíc můžete [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] nakonfigurovat tak, abyste na vytvoření výstrahy byli upozorněni.

## Konfigurace výstrah
V [konzole pro správu Microsoft Intune](https://manage.microsoft.com) klikněte na **Správa** &gt; **Výstrahy a oznámení** a pak vyberte jednu z těchto konfiguračních úloh:

|Úloha|Popis|
|---------|---------|
|**Typy výstrah**|Zvolte typ výstrahy, který chcete nakonfigurovat, a poté proveďte jednu z následujících akcí:<br /><br />-   Klikněte na **Konfigurovat**. V dialogovém okně **Konfigurace typu výstrahy** nakonfigurujte požadované nastavení a pak klikněte na **OK**.<br />-   Výstrahu **povolte** nebo **zakažte**. **Tip:** Rozbalte uzel **Typ výstrahy**. Kliknutím na kategorii zobrazíte jen typy výstrah, které do této kategorie spadají.|
|**Příjemci**|Kliknutím na **Přidat** přidáte novou e-mailovou adresu, která bude dostávat nakonfigurovaná e-mailová oznámení.<br /><br />Můžete taky **upravit** nebo **odstranit** stávající příjemce. **Tip:** Pro příjem oznámení musíte taky přidat tuto e-mailovou adresu jako příjemce v části **Pravidla oznámení**.|
|**Pravidla oznámení**|Nakonfiguruje pravidla, která definují, komu se budou odesílat e-mailové výstrahy. Máte tyto možnosti:<br /><br /><ul><li>**Zvolit existující pravidlo** – Vyberte pravidlo a klikněte na **Vybrat příjemce**. Pak můžete vybrat všechny příjemce, kteří budou obdrží e-mail, když se vygeneruje výstraha splňující toto pravidlo.</li><li>**Vytvořit nové pravidlo** – Klikněte na **vytvořit nové pravidlo** a pak:<br /><br /><ol><li>Zadejte název pravidla a potom vyberte kategorii a závažnost výstrahy, které se na toto pravidlo vztahují.</li><li>Vyberte skupiny zařízení, na které se toto pravidlo vztahuje.</li><li>Vyberte uživatele, kteří dostanou e-mail při vygenerování výstrahy.</li></ol></li><li>Klikněte na **Uložit**.</li></ul>Můžete taky **povolit**, **zakázat**, **upravit** nebo **odstranit** existující pravidlo.|

## Práce s výstrahami
Následující možnosti vám pomohou při práci s výstrahami z konzoly pro správu Intune.

|Možnost|Popis|
|-----------|---------|
|Zobrazení aktivních výstrah|Vyberte jednu z možností:<br /><br />-   **Zobrazit přehled výstrah** – V pracovním prostoru **Řídicí panel** se hlavní chyby zobrazují v podokně Výstrahy. Kliknutím na podokno zobrazíte podrobnější informace.<br />    Souhrn výstrah můžete taky zobrazit na stránce **Přehled** pracovního prostoru **Výstrahy**.<br />-   **Zobrazit všechny výstrahy** – V pracovním prostoru **Výstrahy** klikněte na **Všechny výstrahy**.|
|Zobrazení oznámení|Vyberte jednu z možností:<br /><br />-   V pracovním prostoru **Řídicí panel** klikněte na **Oznámení**.<br />-   V pracovním prostoru **Výstrahy** klikněte na **Všechny výstrahy** &gt;  **Oznámení**.|
|Zavření výstrahy|V seznamu výstrah vyberte výstrahu, kterou chcete zavřít, a klikněte na **Zavřít výstrahu**.<br /><br />Zavřené výstrahy jsou trvale odstraněny po 90 dnech.|
|Znovu aktivovat zavřenou výstrahu|V seznamu výstrah nastavte rozevírací seznam **Filtry** na **Uzavřené**.<br /><br />V seznamu uzavřených výstrah vyberte výstrahu, kterou chcete znovu aktivovat, a pak klikněte na **Znovu aktivovat výstrahu**.|
Výstrahy [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] zůstanou aktivní do doby, než:

-   Problém, který způsobil výstrahu, se vyřeší.

-   Výstrahu ručně zavřete.

-   Od vygenerování výstrahy uplynulo 45 dní.

> [!TIP]
> Pokud je stejná výstraha generovaná zařízeními s různým operačním systémem, je pravděpodobné, že se v seznamu výstrah zobrazí několik verzí téže výstrahy.

## Viz také
[Monitorování a sestavy v Microsoft Intune](../Topic/Monitoring_and_reports_with_Microsoft_Intune.md)

