---
description: na
keywords: na
title: Use policies to manage computers and mobile devices with Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec
---
# Použit&#237; z&#225;sad ke spr&#225;vě poč&#237;tačů a mobiln&#237;ch zař&#237;zen&#237; s Microsoft Intune
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] **Zásady** jsou skupiny nastavení, které řídí funkce pro mobilní zařízení a počítače. Zásady můžete vytvořit pomocí šablon, které obsahují doporučená nebo přizpůsobená nastavení, a pak je můžete nasadit na skupiny zařízení nebo uživatelů.

## Vytvoření zásad konfigurace
Způsob vytváření zásad se liší podle typu zásady, kterou vytváříte.

Tyto postupy popisují vytváření zásad konfigurace.

-   Pomoc při výběru vhodné zásady podle toho, co potřebujete, najdete v tématu [Správa nastavení a funkcí v zařízeních pomocí zásad Microsoft Intune](../Topic/Manage_settings_and_features_on_your_devices_with_Microsoft_Intune_policies.md).

-   Informace o vytváření zásad dodržování předpisů najdete v tématu [Správa zásad dodržování předpisů zařízeními pro Microsoft Intune](../Topic/Manage_device_compliance_policies_for_Microsoft_Intune.md).

-   Informace o vytváření zásad podmíněného přístupu najdete v tématu [Správa přístupu k e-mail a SharePointu pomocí Microsoft Intune](../Topic/Manage_access_to_email_and_SharePoint_with_Microsoft_Intune.md).

-   Informace o vytváření zásad registrace firemních zařízení najdete v tématu [Nastavení správy iOS pomocí Microsoft Intune](../Topic/Set_up_iOS_and_Mac_management_with_Microsoft_Intune.md).

#### Vytvoření sestavy

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com/) klikněte na **Zásady** &gt; **Zásady konfigurace** &gt; **Přidat**.

2.  Zvolte požadovanou zásadu a vyberte doporučené nastavení pro tuto zásady (pokud je dostupné; toto nastavení pak můžete později změnit), nebo vytvořte vlastní zásadu s vlastním nastavením.

    > [!TIP]
    > Pomoc při výběru vhodné zásady najdete v tématu [Správa nastavení a funkcí v zařízeních pomocí zásad Microsoft Intune](../Topic/Manage_settings_and_features_on_your_devices_with_Microsoft_Intune_policies.md).

3.  Až budete připravení, klikněte na **Vytvořit zásadu**.

4.  Na obrazovce **Vytvořit zásadu** nakonfigurujte název a volitelný popis zásady.

5.  Nakonfigurujte požadovaná nastavení a pak klikněte na **Uložit zásadu**.

6.  Kliknutím na tlačítko **Ano** v potvrzovacím dialogovém okně zásadu hned nasadíte, kliknutím na **Ne** zásadu vytvoříte, ale nenasadíte ji.

Novou zásadu můžete zobrazit a upravit tak, že si projdete oddíly pro každý typ zásad v pracovním prostoru **Zásady**.

Když vytvoříte zásadu, která používá doporučená nastavení, je název nové zásady kombinací názvu šablony, data a času. Když zásadu upravujete, název se aktualizuje pomocí data a času úpravy.

Teď když je zásada vytvořená, budete ji obvykle chtít nasadit do jedné nebo víc skupin uživatelů nebo zařízení.

> [!TIP]
> Nenasazujete všechny typy zásad. Třeba zásada správy mobilních aplikací se nenasadila. Tento typ zásad se místo toho přidruží aplikaci a teprve ta se pak nasadí.

#### Nasazení zásady

1.  V pracovním prostoru **Zásady** vyberte zásadu, kterou chcete nasadit, a pak klikněte na **Spravovat nasazení**.

2.  V dialogovém okně **Spravovat nasazení**:

    -   **Pokud chcete zásadu nasadit** – Vyberte jednu nebo víc skupin, do kterých chcete zásady nasadit, a pak klikněte na **Přidat** &gt; **OK**.

    -   **Pokud chcete dialogové okno zavřít bez nasazení zásady** – klikněte na **Zrušit**.

Když vyberete nasazenou zásadu, zobrazí se v dolní části seznamu zásad další informace o tomto nasazení.

#### Správa už vytvořených zásad

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com/) klikněte na **Zásady** a vyhledejte a vyberte zásadu, kterou chcete spravovat.

2.  Vyberte jednu z akcí v následující tabulce:

    |Akce|Další informace|
    |--------|-------------------|
    |**Upravit**|Otevře vlastnosti vybrané zásady a umožní vám provádět změny.|
    |**Odstranit**|Odstraní vybranou zásadu.<br /><br />Pokud zásadu odstraníte, odebere se ze všech skupin, ve kterých byla nasazená.<br /><br />[Co se stane, když se zásada odstraní nebo už není platná?](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md#BKMK_What)|
    |**Spravovat nasazení**|V dialogovém okně **Spravovat nasazení** vyberte skupinu, na kterou chcete zásadu nasadit, a klikněte na **Přidat**.|

## Úlohy pro zásady Intune

### <a name="BKMK_Refresh"></a>Aktualizace zásad na zařízení k zajištění jejich aktuálnosti (platí jenom pro počítače)

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com/) klikněte na **Skupiny** a pak vyberte skupinu zařízení.

2.  Vyberte zařízení, na kterých chcete zásady aktualizovat, a pak klikněte na **Vzdálené úlohy** &gt; **Obnovit zásady**.

3.  V pravém dolním rohu okna [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)] klikněte na **Vzdálené úlohy** a zkontrolujte stav úlohy.

## Další informace o zásadách Intune

### Jak dlouho trvá mobilnímu zařízení, než získá zásadu nebo aplikaci potom, co byly nasazené?
Po nasazení zásady nebo aplikace **[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] se hned začne pokoušet upozornit zařízení, že se mělo ohlásit službě [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].** To obvykle trvá méně než 5 minut.

Pokud se zařízení neohlásí po odeslání prvního oznámení, následují 3 další pokusy.  Když je zařízení offline (je třeba vypnuté nebo není připojené k síti), nemusí oznámení vůbec dostat.

V takovém případě zařízení získá zásadu při dalším plánovaném ohlášení své přítomnosti ve službě [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]:

|Platforma|Četnost ohlašování po počátečním oznámení|
|-------------|---------------------------------------------|
|iOS|Každých 6 hodin|
|Android|Každých 8 hodin|
|Windows Phone|Každých 8 hodin|
|Počítače s Windows zaregistrované jako zařízení|Každých 24 hodin|
Pokud se zařízení právě zaregistrovalo, četnost ohlašování bude vyšší:

|Platforma|Četnost|
|-------------|-----------|
|iOS|Prvních 6 hodin každých 15 minut a pak každých 6 hodin|
|Android|Prvních 15 minut každé 3 minuty, další 2 hodiny každých 15 minut a pak každých 8 hodin|
|Windows Phone|Prvních 15 minut každých 5 minut, další 2 hodiny každých 15 minut a pak každých 8 hodin|
|Počítače s Windows zaregistrované jako zařízení|Prvních 30 minut každé 3 minuty a pak každých 24 hodin|
Uživatelé můžou taky spustit aplikaci Portál společnosti a synchronizovat zařízení. Zásady se tak zkontrolují hned.

### Jaké akce způsobí, že Intune hned zařízení odešle oznámení?
Zařízení se ohlašují službě [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] buď když dostanou oznámení, že se mají ohlásit, nebo při pravidelném plánovaném ohlašování, jak je uvedené v tabulkách výš.  Když akce, jako je vymazání, zamknutí, resetování hesla, nasazení aplikace, nasazení profilu (WiFi, VPN, e-mail atd.) nebo nasazení zásad, cílí na konkrétního uživatele nebo zařízení,  [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] se hned pokusí zařízení upozornit, že by se mělo ohlásit službě Intune a získat tyto aktualizace.

Ostatní změny, jako je třeba úprava kontaktních informací na portálu společnosti, nezpůsobí okamžité odeslání oznámení.

### Pokud se pro stejné zařízení nebo uživatele nasadí víc zásad, jak poznám, které nastavení se použije?
Je důležité vědět, že pokud se pro stejného uživatele nebo zařízení nasadí dvě nebo víc zásad, vyhodnocení toho, které nastavení se použije, se provádí na úrovni jednotlivých nastavení.

-   Nastavení zásad dodržování předpisů mají vždycky přednost před nastaveními zásad konfigurace.

-   Nejvíc omezující nastavení zásad dodržování předpisů se použije při vyhodnocení proti stejnému nastavení v jiné zásadě dodržování předpisů.

-   Nejvíc omezující nastavení zásad konfigurace se použije při vyhodnocení proti stejnému nastavení v jiné zásadě konfigurace.

### Co se stane, když jsou zásady správy mobilních aplikací (MAM) ve vzájemném konfliktu? Která se použije pro příslušnou aplikaci?
Nejvíc omezující nastavení v zásadách správy mobilních aplikací jsou konfliktní hodnoty, s výjimkou polí s počtem zadání (jako jsou pokusy o zadání PINu před resetováním).  Pole s počtem zadání se nastaví na stejnou hodnotu, jako když zásadu MAM vytvoříte v konzole pomocí možnosti doporučeného nastavení.

Konflikt nastane, když je nastavení dvou zásad stejné.  Představte si třeba, že jste nakonfigurovali dvě zásady MAM, které jsou stejné až na nastavení kopírování/vkládání.  V tomto scénáři se nastavení kopírování/vkládání nastaví na nejvíc omezující hodnotu, ale ostatní nastavení se použijí tak, jak se nakonfigurovala.

Pokud se jedna zásada nasadí do aplikace a uplatní se a pak se nasadí druhá zásada, bude mít první nasazená zásada přednost a zůstane nasazená, a u druhé se zobrazí konflikt. Když se ale obě nasadí současně, to znamená, že nebude žádná předchozí zásada, budou v konfliktu obě a všechna konfliktní nastavení se nastaví na nejvíc omezující hodnoty.

### Co se stane při konfliktu vlastních zásad iOS?
Intune nevyhodnocuje datovou část konfiguračních souborů Apple nebo vlastní zásady OMA-URI, slouží jenom jako mechanismus doručování.

Proto když nasadíte vlastní zásadu, zkontrolujte, jestli nakonfigurované nastavení není v konfliktu se zásadami dodržování předpisů, konfiguračními zásadami nebo jinými vlastními zásadami. Při konfliktu mezi nastavením a vlastní zásadou je pořadí použití nastavení náhodné.

### <a name="BKMK_What"></a>Co se stane, když se zásada odstraní nebo už není platná?
Pokud odstraníte zásadu nebo odeberete zařízení ze skupiny, na kterou byla zásada nasazená, zásada a nastavení se ze zařízení odeberou podle následujících tabulek:

#### Mobilní zařízení

|Typ zásad|Windows|Android|Windows Phone (jenom 8.1)|iOS|
|-------------|-----------|-----------|-----------------------------|-------|
|Profily Wi-Fi, VPN, certifikátu a e-mailu|Odebrané|Odebrané|Odebrané|Odebrané|
|Všechny ostatní typy zásad|Neodebrané|Neodebrané|Následující nastavení jsou odebraná:<br /><br />-   Vyžadovat heslo k odemknutí mobilních zařízení<br />-   Povolit jednoduchá hesla<br />-   Minimální délka hesla<br />-   Vyžadovaný typ hesla<br />-   Vypršení platnosti hesla (dny)<br />-   Pamatovat si historii hesel<br />-   Počet povolených opakovaných neúspěšných přihlášení, než bude zařízení vymazáno<br />-   Počet minut nečinnosti před vyžadováním hesla<br />-   Typ požadovaného hesla – minimální počet znaků<br />-   Povolit fotoaparát<br />-   Vyžadovat šifrování u mobilního zařízení<br />-   Povolit vyměnitelné úložiště<br />-   Povolit webový prohlížeč<br />-   Povolit obchod s aplikacemi<br />-   Povolit snímek obrazovky<br />-   Povolit zeměpisnou polohu<br />-   Povolit účet Microsoft<br />-   Povolit kopírování a vkládání<br />-   Povolit sdílení internetového připojení přes Wi-Fi<br />-   Povolit automatické připojení k bezplatným Wi-Fi hotspotům<br />-   Povolit oznamování Wi-Fi hotspotů<br />-   Povolit obnovení továrního nastavení<br />-   Povolit Bluetooth<br />-   Povolit komunikaci NFC<br />-   Povolit Wi-Fi|Odebrané s **výjimkou**:<br /><br />-   Povolit hlasový roaming<br />-   Povolit datový roaming<br />-   Povolit automatickou synchronizaci při roamingu|

#### Počítače

|Typ zásad|Akce|
|-------------|--------|
|**Nastavení služby Endpoint Protection**|Nastavení se obnoví na doporučené hodnoty. Jedinou výjimkou je nastavení **Připojit ke službě Microsoft Active Protection Service**, pro které je výchozí hodnota **Ne**. Podrobnosti najdete v tématu [Pomoc se zabezpečením počítačů s Windows pomocí služby Endpoint Protection pro Microsoft Intune](../Topic/Help_secure_Windows_PCs_with_Endpoint_Protection_for_Microsoft_Intune.md).|
|**Nastavení aktualizací softwaru**|Nastavení se obnoví do výchozího stavu pro operační systém. Podrobnosti najdete v tématu [Udržování počítačů s Windows v aktuálním stavu díky softwarovým aktualizacím v Microsoft Intune](../Topic/Keep_Windows_PCs_up_to_date_with_software_updates_in_Microsoft_Intune.md).|
|**Nastavení [!INCLUDE[wit_tools](../Token/wit_tools_md.md)]**|Veškeré kontaktní informace podpory, které zásady nakonfigurovaly, se z počítače odstraní.|
|**Nastavení brány Windows Firewall**|Nastavení se obnoví na výchozí hodnoty pro operační systém počítače. Podrobnosti najdete v tématu [Pomoc se zabezpečením počítačů s Windows pomocí služby Endpoint Protection pro Microsoft Intune](../Topic/Help_secure_Windows_PCs_with_Endpoint_Protection_for_Microsoft_Intune.md).|

## Viz také
[Technické reference pro Microsoft Intune](../Topic/Technical_reference_for_Microsoft_Intune.md)
[Správa nastavení a funkcí v zařízeních pomocí zásad Microsoft Intune](../Topic/Manage_settings_and_features_on_your_devices_with_Microsoft_Intune_policies.md)

