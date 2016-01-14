---
description: na
keywords: na
title: Windows 10 configuration policy settings in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 00a602d9-b339-4fd8-ab70-defbf6686855
---
# Nastaven&#237; z&#225;sad konfigurace Windows 10 v Microsoft Intune
Nakonfigurování nastavení pro zaregistrovaná zařízení se systémem Windows 10 Desktop a Windows 10 Mobile pomocí [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]**obecných zásad konfigurace** pro Windows 10:

## Vytvoření obecných zásad konfigurace pro Windows 10

#### Zadání základního nastavení pro zásadu konfigurace

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com) klikněte na **Zásady** &gt; **Přehled** &gt; **Přidat zásadu**.

2.  Klikněte na **Windows** &gt; **Obecná konfigurace (Windows 10 Desktop nebo Mobile a novější)** a potom klikněte na **Vytvořit zásadu**.

    > [!NOTE]
    > Nedaří se vám vytvořit zásadu konfigurace pomocí doporučovaného nastavení. Je potřeba vytvořit vlastní zásadu.

3.  V části **Obecné** stránky **Vytvořit zásadu** zadejte název a popis nové zásady.

4.  Informace v následujících částech vám pomůžou zadat nastavení zásad.

5.  Po dokončení klikněte na **Uložit zásadu**.

Nová zásada se zobrazí v uzlu **Zásady konfigurace** pracovního prostoru **Zásady**.

## Nastavení zabezpečení

### Heslo

|Název nastavení|Windows 10 Desktop|Windows 10 Mobile|
|-------------------|----------------------|---------------------|
|**Vyžadovat heslo k odemknutí zařízení**|Ano|Ano|
|**Vyžadovaný typ hesla**<br /><br />(Určuje typ hesla, které se bude vyžadovat, například pouze číselné nebo alfanumerické.)|Ano|Ano|
|**Vyžadovaný typ hesla** – **Minimální počet znakových sad**<br /><br />(Používají se čtyři znakové sady: malá písmena, velká písmena, číslice a symboly. Toto nastavení určuje, kolik různých znakových sad musí být v hesle zahrnutých).|Ano|Ano|
|**Minimální délka hesla (jenom Windows 10 Desktop)** **Important:** Toto nastavení se už nepodporuje a v budoucnu se odebere. Pro stolní počítače můžete použít nastavení pro Windows 10 Mobile dole.|Ano|Ne|
|**Minimální délka hesla (jenom Windows 10 Mobile)**|Ne|Ano|
|**Počet povolených opakovaných neúspěšných přihlášení, než bude zařízení vymazáno**|Ano|Ano|
|**Počet minut nečinnosti před vypnutím displeje**|Ano|Ano|
|**Vypršení platnosti hesla (dny)**|Ano|Ano|
|**Pamatovat si historii hesel**|Ano|Ano|
|**Pamatovat si historii hesel** – **Zakázat opakované použití předchozích hesel**|Ano|Ano|
|**Povolit obrázkové heslo a PIN**<br /><br />Umožňuje použít pro přihlášení jednoduchá gesta na obrázku nebo jednoduchý PIN kód.|Ano|Ne|
|**Po návratu zařízení ze stavu nečinnosti vyžadovat heslo**|Ne|Ano|

### Šifrování

|Název nastavení|Windows 10 Desktop|Windows 10 Mobile|
|-------------------|----------------------|---------------------|
|**Vyžadovat šifrování u mobilního zařízení**|Ne|Ano|

### Systému

|Název nastavení|Windows 10 Desktop|Windows 10 Mobile|
|-------------------|----------------------|---------------------|
|**Povolit snímek obrazovky**|Ne|Ano|
|**Povolit manuální zrušení zápisu**<br /><br />Umožňuje uživateli ze zařízení ručně odstranit pracovní účet.|Ano|Ano|
|**Umožnit ruční instalaci kořenového certifikátu**<br /><br />Určuje, jestli uživatel může ručně instalovat kořenové certifikáty.|Ne|Ano|
|**Povolit odesílání diagnostických dat a dat o použití do Microsoftu**|Ano|Ano|

## Nastavení cloudu

### Účet a synchronizace

|Název nastavení|Windows 10 Desktop|Windows 10 Mobile|
|-------------------|----------------------|---------------------|
|**Povolit účet Microsoft**|Ano|Ano|
|**Povolit ruční přidávání jiných účtů, než jsou účty Microsoft**|Ano|Ano|
|**Povolit synchronizaci nastavení u účtů Microsoft**|Ano|Ano|

## Nastavení e-mailu

|Název nastavení|Windows 10 Desktop|Windows 10 Mobile|
|-------------------|----------------------|---------------------|
|**Nastavit účet Microsoft jako volitelný v aplikaci Windows Pošta**|Ano|Ne|

## Nastavení aplikací

### Microsoft Edge

|Název nastavení|Windows 10 Desktop|Windows 10 Mobile|
|-------------------|----------------------|---------------------|
|**Povolit webový prohlížeč**|Ne|Ano|
|**Povolit návrhy vyhledávání v panelu Adresa**|Ano|Ano|
|**Povolit odesílání intranetového provozu do Internet Exploreru**|Ano|Ne|
|**Povolit Do Not Track**|Ano|Ano|
|**Povolit SmartScreen**|Ano|Ano|
|**Povolit aktivní skriptování**|Ano|Ano|
|**Povolit automaticky otevíraná okna**|Ano|Ne|
|**Povolit soubory cookie**|Ano|Ano|
|**Povolit automatické vyplňování**|Ano|Ne|
|**Povolit správce hesel**|Ano|Ano|
|**Umístění webů podnikového režimu**<br /><br />Určuje, kde najít seznam webů, které se otevřou v podnikovém režimu. Uživatelé nemohou tento seznam upravovat.|Ano|Ne|

### Aplikace

|Název nastavení|Windows 10 Desktop|Windows 10 Mobile|
|-------------------|----------------------|---------------------|
|**Povolit obchod s aplikacemi**|Ne|Ano|

## Nastavení možností zařízení

### Mobilní služby

|Název nastavení|Windows 10 Desktop|Windows 10 Mobile|
|-------------------|----------------------|---------------------|
|**Povolit datový roaming**|Ano|Ano|
|**Povolit VPN v mobilní síti**|Ano|Ano|
|**Povolit VPN v mobilní síti v roamingu**|Ano|Ano|

### Hardware

|Název nastavení|Windows 10 Desktop|Windows 10 Mobile|
|-------------------|----------------------|---------------------|
|**Povolit fotoaparát**|Ano|Ano|
|**Povolit vyměnitelné úložiště**|Ano|Ano|
|**Povolit Wi-Fi**|Ne|Ano|
|**Povolit sdílení internetu**|Ano|Ano|
|**Povolit ruční konfiguraci připojení Wi-Fi**|Ne|Ano|
|**Povolit automatické připojení k bezplatným Wi-Fi hotspotům**|Ano|Ano|
|**Povolit zeměpisnou polohu**<br /><br />Určuje, jestli zařízení může používat informace služeb určování polohy.|Ano|Ano|
|**Povolit komunikaci NFC**|Ano|Ano|
|**Povolit Bluetooth**|Ano|Ano|
|**Povolit zjistitelný režim Bluetooth**|Ano|Ano|
|**Povolit reklamu přes Bluetooth**<br /><br />Umožňuje zařízení přijímat reklamu přes Bluetooth.|Ano|Ano|
|**Povolit režim umožňující připojení k Bluetooth** **Important:** Toto nastavení už Windows 10 nepodporuje a v budoucnu se odebere.|Ano|Ano|
|**Povolit obnovení továrního nastavení telefonu**|Ano|Ano|
|**Povolit připojení USB**|Ano|Ano|
|**Povolit režim AntiTheft**<br /><br />Umožňuje nakonfigurovat, jestli má být povolený režim Windows Antitheft.|Ano|Ano|

### Funkce:

|Název nastavení|Windows 10 Desktop|Windows 10 Mobile|
|-------------------|----------------------|---------------------|
|**Povolit kopírování a vkládání**|Ne|Ano|
|**Povolit záznam hlasu**|Ne|Ano|
|**Povolit Cortanu**|Ano|Ano|
|**Povolit oznámení centra akcí**|Ne|Ano|

## Nastavení aktualizací

|Název nastavení|Popis|Windows 10 Desktop|Windows 10 Mobile|
|-------------------|---------|----------------------|---------------------|
|**Povolit automatické aktualizace**|Toto nastavení povolte, pokud chcete povolit automatické aktualizace. Pak nakonfigurováním jedno z následujících nastavení můžete řídit chování aktualizací:<br /><br /><ul><li>**Upozornění na stahování**</li><li>**Automaticky nainstalovat v době údržby**</li><li>**Automaticky nainstalovat a restartovat v době údržby**</li><li>**Automaticky nainstalovat a restartovat v plánovaném čase**<br /><br />    Pokud je vybraná tato možnost, můžete také nakonfigurovat následující nastavení:<br /><br /><ul><li>**Potlačit oznámení pro koncového uživatele**</li><li>**Definujte den instalace pro plánované aktualizace**</li></ul></li></ul>|Ano|Ne|

## Nasazení zásad konfigurace

1.  Nasaďte zásadu konfigurace do jedné nebo víc skupin uživatelů nebo zařízení ve vaší organizaci.

Další informace o tom, jak nasazovat zásady, najdete v tématu [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

Souhrn stavu a výstrahy v pracovním prostoru **Zásada** určují problémy se zásadou, které vyžadují vaši pozornost. Kromě toho se v pracovním prostoru **Řídicí panel** zobrazí shrnutí stavu.

## Viz také
[Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

