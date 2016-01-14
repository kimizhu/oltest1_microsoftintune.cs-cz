---
description: na
keywords: na
title: Terms and condition policy settings in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6edf0ac1-4f46-4543-a9e5-f484ac37e9a5
---
# Nastaven&#237; z&#225;sad podm&#237;nek a ujedn&#225;n&#237; v Microsoft Intune
Pro skupiny uživatelů můžete nasadit podmínky a ujednání [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] a vysvětlit jim tak, jaký vliv má registrace, přístup k pracovním prostředkům a používání Portálu společnosti na zařízení a uživatele. Uživatelé musí podmínky a ujednání přijmout, aby mohli pomocí Portálu společnosti zaregistrovat svoje zařízení a získat přístup k prostředkům, které potřebují k práci.

## Práce se zásadami podmínek a ujednání v rámci služby Intune
Můžete vytvořit a nasadit různé zásady obsahující různé podmínky a ujednání. Můžete také vytvořit několik verzí stejných podmínek a ujednání v různých jazycích a ty pak implementovat do svých příslušných skupin.

#### Vytvoření zásad podmínek a ujednání

1.  V [konzole pro správu Microsoft Intune](http://manage.microsoft.com) klikněte na **Zásady** &gt; **Podmínky a ujednání**.

2.  Pokud chcete vytvořit novou zásadu podmínek a ujednání, klikněte na **Přidat**.

    Můžete také **upravit** nebo **odstranit** existující zásady.

3.  Na stránce **Vytvořit podmínky a ujednání** zadejte následující informace:

    -   **Název** – jedinečný název zásady zobrazovaný v konzole služby Intune

    -   **Popis** – podrobnosti, které vám pomohou identifikovat zásadu v konzole služby Intune

    -   **Nadpis** – nadpis zobrazovaný uživatelům v aplikaci Portál společnosti

    -   **Text, který vysvětluje význam toho, když uživatel přijme podmínky** – popisek týkající se přijetí podmínek a ujednání, který uživatelé uvidí**Příklad**: Souhlasím s podmínkami a ujednáními.

4.  Po dokončení klikněte na **Uložit**. Nová zásada se zobrazí v uzlu **Podmínky a ujednání** pracovního prostoru **Zásady**.

#### Nasazení zásady podmínek a ujednání

1.  V [konzole pro správu Microsoft Intune](http://manage.microsoft.com) klikněte na **Zásady** &gt; **Podmínky a ujednání**.

2.  V seznamu **Zásady podmínek a ujednání** vyberte zásadu, kterou chcete nasadit, a klikněte na **Spravovat nasazení**.

3.  V dialogovém okně **Spravovat nasazení** vyberte skupiny uživatelů, pro které chcete zásadu nasadit, a potom klikněte na **OK**.

    Když cíloví uživatelé použijí Portál společnosti, zobrazí se jim podmínky a ujednání služby Intune, které jste nasadili. Uživatelé tyto podmínky musí přijmout, aby mohli mít přístup k prostředkům společnosti.

#### Monitorování zásad podmínek a ujednání

1.  V [konzole pro správu Microsoft Intune](http://manage.microsoft.com) klikněte na **Zásady** &gt; **Podmínky a ujednání**.

2.  V okně **Vytvořit novou sestavu** klikněte na **Zobrazit sestavu**. Sestava se otevře s podrobnostmi o tom, kteří uživatelé přijali podmínky a ujednání, které jste nasadili.

### <a name="BKMK_TCVers"></a>Aktualizace a správa verzí pro podmínky a ujednání
Při úpravách existujících zásad podmínek a ujednání můžete zvolit chování při nasazování zásad. Následující postup vám pomůže aktualizovat existující zásady podmínek a ujednání.

##### Jak pracovat s více verzemi podmínek a ujednání

1.  V [konzole pro správu Microsoft Intune](http://manage.microsoft.com) klikněte na **Zásady** &gt; **Podmínky a ujednání**.

2.  Vyberte zásadu podmínek a ujednání, kterou chcete upravit, a potom klikněte na **Upravit**.

3.  Na stránce **Upravit podmínky a ujednání** proveďte veškeré požadované úpravy a pak určete, jestli tato nová verze vyžaduje, aby podmínky a ujednání přijali všichni uživatelé, nebo jestli se nová verze zobrazí jenom novým uživatelům.

    Doporučujeme zvýšit číslo verze a požadovat přijetí podmínek a ujednání vždy, když v podmínkách a ujednáních provedete významné změny. Aktuální verzi zachovejte, pokud například opravujete překlepy nebo měníte formátování.

## Viz také
[Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

