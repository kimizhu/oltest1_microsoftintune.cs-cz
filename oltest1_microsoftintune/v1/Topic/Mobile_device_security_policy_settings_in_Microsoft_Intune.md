---
description: na
keywords: na
title: Mobile device security policy settings in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e5ab3b76-08af-4893-b294-fb6627fdc4c6
---
# Nastaven&#237; z&#225;sad zabezpečen&#237; mobiln&#237;ho zař&#237;zen&#237; v Microsoft Intune
> [!IMPORTANT]
> [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] teď nabízí oddělené zásady konfigurace pro každou platformu zařízení a tyto zásady obsahují nejaktuálnější nastavení, které můžete použít. Můžete dál používat zásady zabezpečení mobilních zařízení a všechna existující nasazení budou i nadále fungovat. Měli byste si ale v nejbližší době naplánovat migraci na nové zásady konfigurace, protože zásady zabezpečení mobilních zařízení se v budoucnu odeberou.

Zásady zabezpečení mobilních zařízení [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] můžete použít ke konfiguraci široké škály nastavení, která se dají nasadit na spravovaných zařízeních v organizaci. Tato nastavení se dají použít k řízení funkcí a zabezpečení vašich zařízení.

Zásady zabezpečení mobilních zařízení můžete vytvořit a nasadit u následujících typů zařízení:

-   Windows RT 8.1 a zaregistrovaná zařízení se systémem Windows 8.1

-   Windows RT

-   Windows Phone 8 a Windows Phone 8.1

-   iOS

-   Android a Samsung KNOX

> [!NOTE]
> Některá nastavení se u některých zařízení nedají použít. Úplný seznam nastavení, která můžete nakonfigurovat, najdete v následující tabulce.

## Vytvoření zásady zabezpečení mobilních zařízení

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com) klikněte na **Zásady** &gt; **Přidat zásadu**.

2.  Klikněte na **Společná nastavení mobilních zařízení** &gt; **Zabezpečení mobilních zařízení**.

3.  Vyberte, jestli chcete vytvořit zásadu obsahující doporučená nastavení, nebo vlastní zásadu, a potom klikněte na **Vytvořit zásadu**.

    > [!TIP]
    > Když kliknete na informační ikonu u kteréhokoli nastavení, zobrazí se jeho doporučená hodnota.

    Další informace o tom, jak vytvářet a nasazovat zásady, najdete v tématu [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

4.  Informace o nastaveních, která můžete konfigurovat, najdete v části [Policy settings for mobile devices](../Topic/Mobile_device_security_policy_settings_in_Microsoft_Intune.md#BKMK_Settings) v tomto tématu.

5.  Po dokončení klikněte na **Uložit zásadu**.

Nová zásada se zobrazí v uzlu **Zásady konfigurace** pracovního prostoru **Zásady**.

## Nasazení zásady zabezpečení mobilních zařízení

1.  Nasaďte zásadu zabezpečení mobilních zařízení v jedné nebo více skupinách uživatelů nebo zařízení ve vaší organizaci.

Další informace o tom, jak nasazovat zásady, najdete v tématu [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

Shrnutí stavu a výstrahy na stránce **Přehled** v pracovním prostoru **Zásady** identifikují problémy se zásadami, které vyžadují vaši pozornost. Kromě toho se v pracovním prostoru **Řídicí panel** zobrazí shrnutí stavu.

> [!IMPORTANT]
> Může trvat až 24 hodin, než se informace o stavu zobrazí v konzole pro správu [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

## <a name="BKMK_Settings"></a>Nastavení zásad pro mobilní zařízení

### <a name="BKMK_sec"></a>Nastavení zabezpečení

|Název nastavení|Windows 8.1 a Windows RT 8.1|Windows RT|Windows Phone 8 a Windows Phone 8.1|iOS|Android a Samsung KNOX|
|-------------------|--------------------------------|--------------|---------------------------------------|-------|--------------------------|
|**Vyžadovat heslo k odemknutí mobilních zařízení**|Ne|Ne|Ano|Ano|Ano|
|**Vyžadovaný typ hesla**<br /><br />(určuje typ hesla, které se bude vyžadovat, například jenom číslice nebo alfanumerické znaky)|Ano|Ano|Ano|Ano|Ne|
|**Vyžadovaný typ hesla – Minimální počet znakových sad**<br /><br />Používají se čtyři znakové sady: malá písmena, velká písmena, číslice a symboly. Toto nastavení určuje, kolik různých znakových sad musí být v hesle zahrnutých). Pro zařízení s iOS ale určuje počet znaků symbolu, které musí být v hesle.)|Ano<sup>2</sup>|Ano|Ano|Ano|Ne|
|**Minimální délka hesla**|Ano|Ano|Ano|Ano|Ano|
|**Povolit jednoduchá hesla**<br /><br />Příklady jednoduchých hesel :0000 a 1234.|Ne|Ne|Ano|Ano|Ne|
|**Počet povolených opakovaných neúspěšných přihlášení, než bude zařízení vymazáno**|Ano|Ano|Ano|Ano|Ano|
|**Počet minut nečinnosti před vypnutím displeje**<sup>1</sup>|Ano|Ano|Ano|Ano|Ano|
|**Vypršení platnosti hesla (dny)**|Ano|Ano|Ano|Ano|Ano|
|**Pamatovat si historii hesel**|Ano|Ano|Ano|Ano|Ano|
|**Pamatovat si historii hesel** – **Zabránit opětovnému použití předchozích hesel**|Ano|Ano|Ano|Ano|Ano|
|**Kvalita hesla**|Ne|Ne|Ne|Ne|Ano|
|**Povolit obrázkové heslo a PIN**|Ano|Ano|Ne|Ne|Ne|
|**Počet minut nečinnosti před vyžadováním hesla**<sup>1</sup>|Ne|Ne|Ne|Ano|Ne|
|**Povolit odemknutí otiskem prstu**|Ne|Ne|Ne|iOS 7 nebo novější|Ne|
<sup>1</sup> U zařízení s iOS se v případě, že nakonfigurujete nastavení **Počet minut nečinnosti před vypnutím displeje** a **Počet minut nečinnosti před vyžadováním hesla**, tato nastavení použijí v uvedeném pořadí. Pokud například pro obě nastavení nastavíte hodnotu **5** minut, obrazovka se po 5 minutách automaticky vypne a po dalších 5 minutách se zařízení zamkne. Pokud ale uživatel vypne obrazovku ručně, druhé nastavení se použije okamžitě. V tomto příkladě se zařízení po tom, co uživatel vypne obrazovku, zamkne po 5 minutách.

<sup>2</sup> Když nasadíte zásadu délky hesel na zařízení se systémem Windows RT, budou uživatelé přinucení změnit heslo, i když jejich aktuální heslo odpovídá požadavkům zásady.

### Nastavení šifrování

|Název nastavení|Windows 8.1 a Windows RT 8.1|Windows RT|Windows Phone 8 a Windows Phone 8.1|iOS|Android a Samsung KNOX|
|-------------------|--------------------------------|--------------|---------------------------------------|-------|--------------------------|
|**Vyžadovat šifrování u mobilního zařízení**<sup>1</sup><br /><br />Pro zařízení s Windows Phone 8 je potřeba nastavit hodnotu **Ano**.<br /><br />Pokud chcete povolit šifrování na zařízeních iOS, povolte nastavení **Vyžadovat heslo k odemknutí mobilních zařízení**.|Ano|Ne|Ano|Ne|Ano|
|**Vyžadovat šifrování u paměťových karet** <sup>2</sup>|není k dispozici|není k dispozici|není k dispozici (aplikace a související data se šifrují automaticky)|není k dispozici|Ano|
<sup>1</sup> Další informace pro zařízení s Windows 8.1

-   K vynucení šifrování na zařízeních s Windows 8.1 je potřeba na každé zařízení nainstalovat [aktualizaci MDM klienta pro Windows z prosince 2014](http://support.microsoft.com/kb/3013816).

-   Pokud toto nastavení povolíte pro zařízení s Windows 8.1, všichni uživatelé zařízení musí mít účet Microsoft.

-   Šifrování funguje, jenom když zařízení splňuje hardwarové požadavky certifikace Microsoft [InstantGo](http://blogs.windows.com/bloggingwindows/2014/06/19/instantgo-a-better-way-to-sleep/).

-   Pokud vynutíte šifrování na zařízení, je obnovovací klíč přístupný jenom uživatelům s účtem Microsoft, ke kterému přistupují z účtu na Onedrivu. Tento klíč se nedá obnovit jménem uživatele.

<sup>2</sup> platí taky pro zařízení, která spravuje Exchange ActiveSync.

### Nastavení ochrany proti malwaru

|Název nastavení|Windows 8.1 a Windows RT 8.1|Windows RT|Windows Phone 8 a Windows Phone 8.1|iOS|Android a Samsung KNOX|
|-------------------|--------------------------------|--------------|---------------------------------------|-------|--------------------------|
|**Vyžadovat síťovou bránu firewall**|Ano|Ne|Ne|Ne|Ne|
|**Povolit SmartScreen**|Ano|Ne|Ne|Ne|Ne|

### Nastavení systému

|Název nastavení|Windows 8.1 a Windows RT 8.1|Windows RT|Windows Phone 8 a Windows Phone 8.1|iOS|Android a Samsung KNOX|
|-------------------|--------------------------------|--------------|---------------------------------------|-------|--------------------------|
|**Vyžadovat automatické aktualizace**|Ano|Ne|Ne|Ne|Ne|
|**Vyžadovat automatické aktualizace – automatická instalace minimální klasifikace aktualizací** <sup>1</sup><br /><br />Vyberte klasifikace aktualizací, které se instalují automaticky:<br /><br />-   **Důležité** – nainstaluje všechny aktualizace klasifikované jako důležité.<br />-   **Doporučené** – nainstaluje všechny aktualizace klasifikované jako důležité nebo doporučené.|Ano|Ne|Ne|Ne|Ne|
|**Povolit snímek obrazovky**|Ne|Ne|Jenom Windows Phone 8.1|Ano|Ano (jenom Samsung KNOX)|
|**Povolit řídicí centrum na zamykací obrazovce**|Ne|Ne|Ne|iOS 7 nebo novější|Ne|
|**Povolit zobrazení oznámení na zamykací obrazovce**|Ne|Ne|Ne|iOS 7 nebo novější|Ne|
|**Povolit zobrazení informací o dnešku na zamykací obrazovce**|Ne|Ne|Ne|iOS 7 nebo novější|Ne|
|**Řízení uživatelských účtů**|Ano|Ne|Ne|Ne|Ne|
|**Povolit odeslání diagnostických dat**|Ano|Ne|Jenom Windows Phone 8.1|Ano|Ano (jenom Samsung KNOX)|
|**Povolit nedůvěryhodné certifikáty TLS**|Ne|Ne|Ne|Ano|Ne|
|**Povolit software osobní Peněženka při uzamčení**|Ne|Ne|Ne|Ano|Ne|
|**Povolit obnovení továrního nastavení**|Ne|Ne|Ne|Ne|Ano (jenom Samsung KNOX)|
<sup>1</sup> Pro vynucení šifrování v zařízeních s Windows 1 je nutné nainstalovat [aktualizaci klienta z prosince 8.1 MDM pro Windows](http://support.microsoft.com/kb/3013816) na každé zařízení.

### <a name="BKMK_cloud"></a>Nastavení cloudu – dokumenty a data

|Název nastavení|Windows 8.1 a Windows RT 8.1|Windows RT|Windows Phone 8 a Windows Phone 8.1|iOS|Android a Samsung KNOX|
|-------------------|--------------------------------|--------------|---------------------------------------|-------|--------------------------|
|**Povolit zálohování na iCloud**|Ne|Ne|Ne|Ano|Ne|
|**Povolit synchronizaci dokumentů s iCloudem**|Ne|Ne|Ne|Ano|Ne|
|**Povolit synchronizaci datového proudu fotografií s iCloudem**|Ne|Ne|Ne|Ano|Ne|
|**Vyžadovat šifrované zálohování**|Ne|Ne|Ne|Ano|Ne|
|**Adresa URL pracovních složek**<br /><br />(nastaví adresu URL pracovní složky, aby bylo možné synchronizovat dokumenty na všech zařízeních)|Ano|Ne|Ne|Ne|Ne|
|**Povolit zálohování Google**|Ne|Ne|Ne|Ne|Ano (jenom Samsung KNOX)|

### Nastavení cloudu – účty a synchronizace

|Název nastavení|Windows 8.1 a Windows RT 8.1|Windows RT|Windows Phone 8 a Windows Phone 8.1|iOS|Android a Samsung KNOX|
|-------------------|--------------------------------|--------------|---------------------------------------|-------|--------------------------|
|**Povolit účet Microsoft**|Ne|Ne|Jenom Windows Phone 8.1|Ne|Ne|
|**Povolit automatickou synchronizaci účtu Google**|Ne|Ne|Ne|Ne|Ano (jenom Samsung KNOX)|

### <a name="BKMK_email"></a>Nastavení e-mailu

|Název nastavení|Windows 8.1 a Windows RT 8.1|Windows RT|Windows Phone 8 a Windows Phone 8.1|iOS|Android a Samsung KNOX|
|-------------------|--------------------------------|--------------|---------------------------------------|-------|--------------------------|
|**Povolit uživatelům stahovat přílohy e-mailů**<sup>1</sup>|není k dispozici|není k dispozici|není k dispozici|není k dispozici|není k dispozici|
|**Interval synchronizace e-mailu**<sup>1</sup>|není k dispozici|není k dispozici|není k dispozici|není k dispozici|není k dispozici|
|**Povolit mobilní zařízení, která tato nastavení pro synchronizaci se serverem Exchange (Exchange ActiveSync) plně nepodporují** <sup>1</sup>|není k dispozici|není k dispozici|není k dispozici|není k dispozici|není k dispozici|
|**Nastavit účet Microsoft jako volitelný v aplikaci Windows Pošta**|Ano|Ne|Ne|Ne|Ne|
|**Povolit vlastní e-mailové účty**|Ne|Ne|Jenom Windows Phone 8.1|Ne|Ne|
<sup>1</sup> platí taky pro zařízení, která spravuje Exchange ActiveSync.

### <a name="BKMK_browser"></a>Nastavení aplikace – prohlížeč

|Název nastavení|Windows 8.1 a Windows RT 8.1|Windows RT|Windows Phone 8 a Windows Phone 8.1|iOS|Android a Samsung KNOX|
|-------------------|--------------------------------|--------------|---------------------------------------|-------|--------------------------|
|**Povolit webový prohlížeč**|Ne|Ne|Jenom Windows Phone 8.1|Ano|Ano (jenom Samsung KNOX)|
|**Povolit automatické vyplňování**|Ano|Ne|Ne|Ano|Ano (jenom Samsung KNOX)|
|**Povolit blokování automaticky otevíraných oken**|Ano|Ne|Ne|Ano|Ano (jenom Samsung KNOX)|
|**Povolit soubory cookie**|Ne|Ne|Ne|Ano|Ano (jenom Samsung KNOX)|
|**Povolit moduly plug-in**|Ano|Ne|Ne|Ne|Ne|
|**Povolit aktivní skriptování**|Ano|Ne|Ne|Ano|Ano (jenom Samsung KNOX)|
|**Povolit upozornění na podvod**|Ano|Ne|Ne|Ano|Ne|
|**Povolit intranetovému serveru zadání jednoslovné položky**<br /><br />(umožňuje použití jednoho slova pro přesměrování Internet Exploreru na web jako třeba Bing)|Ano|Ne|Ne|Ne|Ne|
|**Povolit automatické zjišťování sítě intranet**|Ano|Ne|Ne|Ne|Ne|
|**Úroveň zabezpečení pro internet**|Ano|Ne|Ne|Ne|Ne|
|**Úroveň zabezpečení pro intranet**|Ano|Ne|Ne|Ne|Ne|
|**Úroveň zabezpečení pro důvěryhodné lokality**|Ano|Ne|Ne|Ne|Ne|
|**Úroveň zabezpečení pro lokality s omezeným přístupem**|Ano|Ne|Ne|Ne|Ne|
|**Odesílat hlavičku DNT (Do Not Track)**|Ano|Ne|Ne|Ne|Ne|
|**Povolit přístup nabídky podnikového režimu**|Ano|Ne|Ne|Ne|Ne|
|**Umístění webů podnikového režimu**|Ano|Ne|Ne|Ne|Ne|

### <a name="BKMK_apps"></a>Nastavení aplikace – aplikace

|Název nastavení|Windows 8.1 a Windows RT 8.1|Windows RT|Windows Phone 8 a Windows Phone 8.1|iOS|Android a Samsung KNOX|
|-------------------|--------------------------------|--------------|---------------------------------------|-------|--------------------------|
|**Povolit obchod s aplikacemi**|Ne|Ne|Jenom Windows Phone 8.1|Ano|Ano (jenom Samsung KNOX)|
|**Vyžadovat heslo pro přístup do obchodu s aplikacemi**|Ne|Ne|Ne|Ano|Ne|
|**Povolit nákupy v aplikaci**|Ne|Ne|Ne|Ano|Ne|
|**Povolit spravované dokumenty v jiných nespravovaných aplikacích**|Ne|Ne|Ne|iOS 7 nebo novější|Ne|
|**Povolit nespravované dokumenty v jiných spravovaných aplikacích**|Ne|Ne|Ne|iOS 7 nebo novější|Ne|
|**Povolit videokonference**|Ne|Ne|Ne|Ano|Ne|
|**Povolit obsah pro dospělé v obchodě s mediálním obsahem**|Ne|Ne|Ne|Ano|Ne|
|**Povolit instalace aplikací**|Ne|Ne|Ne|iOS 6 nebo novější|Ne|

### Nastavení aplikace – hry

|Název nastavení|Windows 8.1 a Windows RT 8.1|Windows RT|Windows Phone 8 a Windows Phone 8.1|iOS|Android a Samsung KNOX|
|-------------------|--------------------------------|--------------|---------------------------------------|-------|--------------------------|
|**Povolit přátele z herního centra**|Ne|Ne|Ne|Ano|Ne|
|**Povolit hru s více hráči**|Ne|Ne|Ne|Ano|Ne|

### <a name="BKMK_hard"></a>Nastavení možností zařízení – hardware

|Název nastavení|Windows 8.1 a Windows RT 8.1|Windows RT|Windows Phone 8 a Windows Phone 8.1|iOS|Android a Samsung KNOX|
|-------------------|--------------------------------|--------------|---------------------------------------|-------|--------------------------|
|**Povolit fotoaparát**|Ne|Ne|Jenom Windows Phone 8.1|Ano|Ano|
|**Povolit vyměnitelné úložiště**|Ne|Ne|Ano|Ne|Ano (jenom Samsung KNOX)|
|**Povolit Wi-Fi**|Ne|Ne|Jenom Windows Phone 8.1|Ne|Ano (jenom Samsung KNOX)|
|**Povolit sdílení internetového připojení přes Wi-Fi**|Ne|Ne|Jenom Windows Phone 8.1|Ne|Ano (jenom Samsung KNOX)|
|**Povolit automatické připojení k bezplatným Wi-Fi hotspotům**|Ne|Ne|Jenom Windows Phone 8.1|Ne|Ne|
|**Povolit oznamování Wi-Fi hotspotů**<br /><br />(odešlete informace o připojení Wi-Fi, abyste pomohli zjišťovat okolní připojení)|Ne|Ne|Jenom Windows Phone 8.1|Ne|Ne|
|**Povolit zeměpisnou polohu**<br /><br />(umožňuje zařízením využívat informace o umístění)|Ne|Ne|Jenom Windows Phone 8.1|Ne|Ano (jenom Samsung KNOX)|
|**Povolit komunikaci NFC**<br /><br />(umožňuje operace, které používají bezkontaktní komunikaci)|Ne|Ne|Jenom Windows Phone 8.1|Ne|Ano (jenom Samsung KNOX)|
|**Povolit Bluetooth**|Ne|Ne|Jenom Windows Phone 8.1|Ne|Ano (jenom Samsung KNOX)|
|**Povolit vypnutí napájení**<sup>1</sup>|Ne|Ne|Ne|Ne|Ano (jenom Samsung KNOX)|
<sup>1</sup> Pokud je toto nastavení zakázané, nastavení **Počet povolených opakovaných neúspěšných přihlášení, než bude zařízení vymazáno** pro zařízení Samsung KNOX není funkční.

### Nastavení možností zařízení – mobilní

|Název nastavení|Windows 8.1 a Windows RT 8.1|Windows RT|Windows Phone 8 a Windows Phone 8.1|iOS|Android a Samsung KNOX|
|-------------------|--------------------------------|--------------|---------------------------------------|-------|--------------------------|
|**Povolit hlasový roaming**|Ne|Ne|Ne|Ano|Ano (jenom Samsung KNOX)|
|**Povolit datový roaming**|Ano|Ne|Ne|Ano|Ano (jenom Samsung KNOX)|
|**Povolit automatickou synchronizaci při roamingu**|Ne|Ne|Ne|Ano|Ne|
|**Povolit SMS a MMS zprávy**|Ne|Ne|Ne|Ne|Ano (jenom Samsung KNOX)|

### Nastavení možností zařízení – funkce

|Název nastavení|Windows 8.1 a Windows RT 8.1|Windows RT|Windows Phone 8 a Windows Phone 8.1|iOS|Android a Samsung KNOX|
|-------------------|--------------------------------|--------------|---------------------------------------|-------|--------------------------|
|**Povolit hlasového asistenta**|Ne|Ne|Ne|Ano|Ano (jenom Samsung KNOX)|
|**Povolit hlasového asistenta při uzamknutém zařízení**|Ne|Ne|Ne|Ano|Ne|
|**Povolit hlasové vytáčení**|Ne|Ne|Ne|Ano|Ano (jenom Samsung KNOX)|
|**Povolit kopírování a vkládání**|Ne|Ne|Jenom Windows Phone 8.1|Ne|Ano (jenom Samsung KNOX)|
|**Povolit sdílení schránky mezi aplikacemi**|Ne|Ne|Ne|Ne|Ano (jenom Samsung KNOX)|
|**Povolit YouTube**|Ne|Ne|Ne|Ne|Ano (jenom Samsung KNOX)|

## Viz také
[Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

