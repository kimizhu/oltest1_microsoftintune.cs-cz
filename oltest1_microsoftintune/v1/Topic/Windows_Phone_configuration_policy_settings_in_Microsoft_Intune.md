---
description: na
keywords: na
title: Windows Phone configuration policy settings in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 83f7469c-272e-43f2-8139-b0d7bc34f43f
---
# Nastaven&#237; z&#225;sad konfigurace pro Windows Phone v Microsoft Intune
Ke konfiguraci následujících nastavení pro zařízení Windows Phone 8.1 použijte **Zásadu obecné konfigurace pro Windows Phone** služby [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]:

-   **Nastavení zabezpečení mobilního zařízení** – Zvolte ze seznamu předdefinovaných nastavení, která umožňují v zařízení ovládat celou řadu funkcí.

-   **Seznam aplikací dodržujících a nedodržujících předpisy** – Určete seznam aplikací, které splňují nebo nesplňují předpisy ve vaší společnosti. Zařízení Windows Phone můžou instalaci těchto aplikací blokovat nebo povolit.

## Vytvoření obecných zásad konfigurace pro Windows Phone

#### Zadání základního nastavení pro zásadu konfigurace

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com) klikněte na **Zásady** &gt; **Přehled** &gt; **Přidat zásadu**.

2.  Klikněte na **Windows** &gt; **Obecná konfigurace (Windows Phone 8.1 a novější)** a potom klikněte na **Vytvořit zásadu**.

    > [!NOTE]
    > Nedaří se vám vytvořit zásadu konfigurace pomocí doporučovaného nastavení. Je potřeba vytvořit vlastní zásadu.

3.  V části **Obecné** stránky **Vytvořit zásadu** zadejte název a popis nové zásady.

4.  Informace v následujících částech vám pomůžou zadat nastavení zásad.

5.  Po dokončení klikněte na **Uložit zásadu**.

Nová zásada se zobrazí v uzlu **Zásady konfigurace** pracovního prostoru **Zásady**.

## <a name="BKMK_Settings"></a>Nastavení pro Windows Phone

### <a name="BKMK_sec"></a>Nastavení zabezpečení

|Název nastavení|Windows Phone 8 a Windows Phone 8.1|
|-------------------|---------------------------------------|
|**Vyžadovat heslo k odemknutí mobilních zařízení**|Ano|
|**Vyžadovaný typ hesla**<br /><br />(určuje typ hesla, které se bude vyžadovat, například jenom číslice nebo alfanumerické znaky)|Ano|
|**Vyžadovaný typ hesla – Minimální počet znakových sad**<br /><br />Používají se čtyři znakové sady: malá písmena, velká písmena, číslice a symboly. Toto nastavení určuje, kolik různých znakových sad musí být v hesle zahrnutých). Pro zařízení s iOS ale určuje počet znaků symbolu, které musí být v hesle.)|Ano|
|**Minimální délka hesla**|Ano|
|**Povolit jednoduchá hesla**<br /><br />Příklady jednoduchých hesel :0000 a 1234.|Ano|
|**Počet povolených opakovaných neúspěšných přihlášení, než bude zařízení vymazáno**|Ano|
|**Počet minut nečinnosti před vypnutím displeje**|Ano|
|**Vypršení platnosti hesla (dny)**|Ano|
|**Pamatovat si historii hesel**|Ano|
|**Pamatovat si historii hesel** – **Zabránit opětovnému použití předchozích hesel**|Ano|

### Nastavení šifrování

|Název nastavení|Windows Phone 8 a Windows Phone 8.1|
|-------------------|---------------------------------------|
|**Vyžadovat šifrování u mobilního zařízení**<br /><br />Pro zařízení s Windows Phone 8 je potřeba nastavit hodnotu **Ano**.|Ano|

### Nastavení systému

|Název nastavení|Windows Phone 8 a Windows Phone 8.1|
|-------------------|---------------------------------------|
|**Povolit snímek obrazovky**|Jenom Windows Phone 8.1|
|**Povolit odeslání diagnostických dat**|Jenom Windows Phone 8.1|

### Nastavení cloudu – účty a synchronizace

|Název nastavení|Windows Phone 8 a Windows Phone 8.1|
|-------------------|---------------------------------------|
|**Povolit účet Microsoft**|Jenom Windows Phone 8.1|

### <a name="BKMK_email"></a>Nastavení e-mailu

|Název nastavení|Windows Phone 8 a Windows Phone 8.1|
|-------------------|---------------------------------------|
|**Povolit vlastní e-mailové účty**|Jenom Windows Phone 8.1|

### <a name="BKMK_browser"></a>Nastavení aplikace – prohlížeč

|Název nastavení|Windows Phone 8 a Windows Phone 8.1|
|-------------------|---------------------------------------|
|**Povolit webový prohlížeč**|Jenom Windows Phone 8.1|

### <a name="BKMK_apps"></a>Nastavení aplikace – aplikace

|Název nastavení|Windows Phone 8 a Windows Phone 8.1|
|-------------------|---------------------------------------|
|**Povolit obchod s aplikacemi**|Jenom Windows Phone 8.1|

### <a name="BKMK_hard"></a>Nastavení možností zařízení – hardware

|Název nastavení|Windows Phone 8 a Windows Phone 8.1|
|-------------------|---------------------------------------|
|**Povolit fotoaparát**|Jenom Windows Phone 8.1|
|**Povolit vyměnitelné úložiště**|Ano|
|**Povolit Wi-Fi**|Jenom Windows Phone 8.1|
|**Povolit sdílení internetového připojení přes Wi-Fi**|Jenom Windows Phone 8.1|
|**Povolit automatické připojení k bezplatným Wi-Fi hotspotům**|Jenom Windows Phone 8.1|
|**Povolit oznamování Wi-Fi hotspotů**<br /><br />(odešlete informace o připojení Wi-Fi, abyste pomohli zjišťovat okolní připojení)|Jenom Windows Phone 8.1|
|**Povolit zeměpisnou polohu**<br /><br />(umožňuje zařízením využívat informace o umístění)|Jenom Windows Phone 8.1|
|**Povolit komunikaci NFC**<br /><br />(umožňuje operace, které používají bezkontaktní komunikaci)|Jenom Windows Phone 8.1|
|**Povolit Bluetooth**|Jenom Windows Phone 8.1|

### Nastavení možností zařízení – funkce

|Název nastavení|Windows Phone 8 a Windows Phone 8.1|
|-------------------|---------------------------------------|
|**Povolit kopírování a vkládání**|Jenom Windows Phone 8.1|

## Nastavení pro aplikace dodržující a nedodržující předpisy
V seznamu **Kompatibilní a nekompatibilní aplikace** zadejte seznam kompatibilních a nekompatibilních aplikací pomocí následujících informací:

> [!NOTE]
> Jedna zásada může obsahovat seznam jenom kompatibilních, nebo jenom nekompatibilních aplikací. Nejde zadat oba seznamy v jedné zásadě.

|Název nastavení|Další informace|
|-------------------|-------------------|
|**Blokovat otevření seznamu aplikací na zařízení**|Zobrazí seznam aplikací, které Intune nespravuje a které nemají uživatelé dovolené nainstalovat a spustit.|
|**Povolit zařízením instalovat jenom uvedené aplikace**|Zobrazí seznam aplikací, které mají uživatelé dovoleno instalovat. Uživatelé nemůžou instalovat žádné další aplikace. Aplikace, které spravuje Intune, jsou povolené automaticky.|
|**Přidat**|Přidá aplikaci do vybraného seznamu. Zadejte název podle své volby, volitelně vydavatele aplikaci a adresu URL aplikace v úložišti aplikací.<br /><br />[Určení adres URL na obchody s aplikacemi](../Topic/Windows_Phone_configuration_policy_settings_in_Microsoft_Intune.md#BKMK_URL)|
|**Importovat aplikace**|Importuje seznam aplikací, které jste zadali v souboru hodnot oddělených čárkami. V souboru použijte formát, název aplikace, vydavatele, adresu URL aplikace.|
|**Upravit**|Tady můžete upravit název, vydavatele a adresu URL vybrané aplikace.|
|**Odstranit**|Odstraní vybranou aplikaci ze seznamu.|
> [!IMPORTANT]
> Pokud zadáváte seznam aplikací povolených pro zařízení Windows Phone 8.1, je potřeba přidat do tohoto seznamu aplikaci Portál společnosti, jinak se zablokuje.

## Nasazení zásad konfigurace

1.  Nasaďte zásadu konfigurace do jedné nebo víc skupin uživatelů nebo zařízení ve vaší organizaci.

Další informace o tom, jak nasazovat zásady, najdete v tématu [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

Souhrn stavu a výstrahy v pracovním prostoru **Zásada** určují problémy se zásadou, které vyžadují vaši pozornost. Kromě toho se v pracovním prostoru **Řídicí panel** zobrazí shrnutí stavu.

## Referenční informace pro aplikace nesplňující předpisy

### <a name="BKMK_URL"></a>Určení adres URL na obchody s aplikacemi
Pokud chcete zadat adresu URL aplikace do seznamu kompatibilních a nekompatibilních aplikací, použijte následující formát:

Na [stránce Aplikace a hry pro Windows Phone](http://www.windowsphone.com/en-us/store/overview) najděte aplikaci, kterou chcete použít.

Otevřete stránku aplikace a zkopírujte adresu URL do schránky. Tu teď můžete použít jako adresu URL v seznamu kompatibilních nebo nekompatibilních aplikací.

**Příklad:** Vyhledejte v obchodě aplikaci Skype. Použijete adresu URL **http://www.windowsphone.com/store/app/skype/c3f8e570-68b3-4d6a-bdbb-c0a3f4360a51**.

## Viz také
[Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

