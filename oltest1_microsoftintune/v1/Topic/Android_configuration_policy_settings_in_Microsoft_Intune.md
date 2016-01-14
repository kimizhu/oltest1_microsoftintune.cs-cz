---
description: na
keywords: na
title: Android configuration policy settings in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 71cc39cf-e726-40fd-8d08-78776e099a4b
---
# Nastaven&#237; z&#225;sad konfigurace pro Android v Microsoft Intune
Pomocí **zásady obecné konfigurace pro Android**[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] můžete nakonfigurovat nastavení pro:

-   **Nastavení zabezpečení mobilního zařízení** – Zvolte ze seznamu předdefinovaných nastavení, která umožňují v zařízení ovládat celou řadu funkcí.

-   **Celoobrazovkový režim** (jenom pro zařízení Samsung KNOX) – Umožňuje uzamknout zařízení a povolit fungování jen některých funkcí. Můžete třeba povolit, aby v zařízení běžela jenom jedna vámi určená spravovaná aplikace, nebo můžete zakázat tlačítka hlasitosti na zařízení. Tato nastavení se dají používat pro ukázkový model zařízení nebo zařízení, které může provádět jenom jednu funkci, jako je třeba zařízení POS.

-   **Seznam aplikací dodržujících a nedodržujících předpisy** – Určete seznam aplikací, které splňují nebo nesplňují předpisy ve vaší společnosti. Na zařízeních s Androidem a iOS je možné používat **Sestavu nekompatibilních aplikací** k zobrazení kompatibility aplikací, které jste uvedli v seznamu, s aplikacemi, které nainstalovali uživatelé (ale nemůžete ve skutečnosti zablokovat instalaci aplikace).

> [!TIP]
> Můžete nakonfigurovat podmínky pro uživatele a zajistit tak jejich informovanost o tom, že aplikace na jejich zařízení, včetně osobních aplikací, se budou hodnotit, a nekompatibilní aplikace se zablokují nebo nahlásí jako nevyhovující. Uživatelé musí přijmout tyto podmínky předtím, než můžou zaregistrovat své zařízení a používat firemní portál k získání aplikací. Další informace o podmínkách a ujednáních týkajících se použití najdete v tématu [Práce se zásadami pro pravidla a podmínky v Microsoft Intune](http://msdn.microsoft.com/en-us/library/ce59fb93-01fd-4822-a57d-45ca7d89843d).

## Vytvoření zásady konfigurace pro Android

#### Zadání základního nastavení pro zásadu konfigurace

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com) klikněte na **Zásady** &gt; **Přehled** &gt; **Přidat zásadu**.

2.  Klikněte na tlačítko **Android** &gt; **Obecná konfigurace** a potom klikněte na **Vytvořit zásadu**.

    > [!NOTE]
    > Nedaří se vám vytvořit zásadu konfigurace pomocí doporučovaného nastavení. Je potřeba vytvořit vlastní zásadu.

3.  V části **Obecné** stránky **Vytvořit zásadu** zadejte název a popis nové zásady.

4.  Informace v následujících částech vám pomůžou zadat nastavení zásad.

5.  Po dokončení klikněte na **Uložit zásadu**.

Nová zásada se zobrazí v uzlu **Zásady konfigurace** pracovního prostoru **Zásady**.

## <a name="BKMK_Settings"></a>Nastavení zásady zabezpečení mobilních zařízení pro zařízení se systémem Android
Pokud se v tomto seznamu nezobrazí nastavení, které hledáte, je možné, že ho budete moct vytvořit pomocí vlastních zásad pro Android, které vám k řízení zařízení umožňuje použít nastavení OMA-URI. Další informace naleznete v části [Nastavení vlastních zásad pro Android v Microsoft Intune](../Topic/Android_custom_policy_settings_in_Microsoft_Intune.md).

### <a name="BKMK_sec"></a>Nastavení hesla

|Název nastavení|Android 4.0+|Samsung KNOX|
|-------------------|----------------|----------------|
|**Vyžadovat heslo k odemknutí mobilních zařízení**|Ano|Ano|
|**Minimální délka hesla**|Ano|Ano|
|**Počet povolených opakovaných neúspěšných přihlášení, než bude zařízení vymazáno**|Ano|Ano|
|**Počet minut nečinnosti před vypnutím displeje**|Ano|Ano|
|**Vypršení platnosti hesla (dny)**|Ano|Ano|
|**Pamatovat si historii hesel**|Ano|Ano|
|**Pamatovat si historii hesel** – **Zabránit opětovnému použití předchozích hesel**|Ano|Ano|
|**Kvalita hesla**|Ano|Ano|
|**Povolit odemknutí otiskem prstu**|Ne|Ano|

### Nastavení šifrování

|Název nastavení|Android 4.0+|Samsung KNOX|
|-------------------|----------------|----------------|
|**Vyžadovat šifrování u mobilního zařízení**|Ano|Ano|
|**Vyžadovat šifrování u paměťových karet**|Ne|Ano|

### Nastavení systému

|Název nastavení|Android 4.0+|Samsung KNOX|
|-------------------|----------------|----------------|
|**Povolit snímek obrazovky**|Ne|Ano|
|**Povolit odeslání diagnostických dat**|Ne|Ano|
|**Povolit obnovení továrního nastavení**|Ne|Ano|

### <a name="BKMK_cloud"></a>Nastavení cloudu – dokumenty a data

|Název nastavení|Android a Samsung KNOX|Android 4.0+|
|-------------------|--------------------------|----------------|
|**Povolit zálohování Google**|Ne|Ano|

### Nastavení cloudu – účty a synchronizace

|Název nastavení|Android 4.0+|Samsung KNOX|
|-------------------|----------------|----------------|
|**Povolit automatickou synchronizaci účtu Google**|Ne|Ano|

### <a name="BKMK_browser"></a>Nastavení aplikace – prohlížeč

|Název nastavení|Android 4.0+|Samsung KNOX|
|-------------------|----------------|----------------|
|**Povolit webový prohlížeč**|Ne|Ano|
|**Povolit automatické vyplňování**|Ne|Ano|
|**Povolit blokování automaticky otevíraných oken**|Ne|Ano|
|**Povolit soubory cookie**|Ne|Ano|
|**Povolit aktivní skriptování**|Ne|Ano|

### <a name="BKMK_apps"></a>Nastavení aplikace – aplikace

|Název nastavení|Android 4.0+|Samsung KNOX|
|-------------------|----------------|----------------|
|**Povolit Google Play Store**|Ne|Ano|

### <a name="BKMK_hard"></a>Nastavení možností zařízení – hardware

|Název nastavení|Android 4.0+|Samsung KNOX|
|-------------------|----------------|----------------|
|**Povolit fotoaparát**|Ano|Ano|
|**Povolit vyměnitelné úložiště**|Ne|Ano|
|**Povolit Wi-Fi**|Ne|Ano|
|**Povolit sdílení internetového připojení přes Wi-Fi**|Ne|Ano|
|**Povolit zeměpisnou polohu**<br /><br />(umožňuje zařízením využívat informace o umístění)|Ne|Ano|
|**Povolit komunikaci NFC**<br /><br />(umožňuje operace, které používají bezkontaktní komunikaci)|Ne|Ano|
|**Povolit Bluetooth**|Ne|Ano|
|**Povolit vypnutí napájení**<sup>1</sup>|Ne|Ano|
<sup>1</sup> Pokud je toto nastavení zakázané, nastavení **Počet povolených opakovaných neúspěšných přihlášení, než bude zařízení vymazáno** pro zařízení Samsung KNOX není funkční.

### Nastavení možností zařízení – mobilní

|Název nastavení|Android 4.0+|Samsung KNOX|
|-------------------|----------------|----------------|
|**Povolit hlasový roaming**|Ne|Ano|
|**Povolit datový roaming**|Ne|Ano|
|**Povolit SMS a MMS zprávy**|Ne|Ano|

### Nastavení možností zařízení – funkce

|Název nastavení|Android 4.0+|Samsung KNOX|
|-------------------|----------------|----------------|
|**Povolit hlasového asistenta**|Ne|Ano|
|**Povolit hlasové vytáčení**|Ne|Ano|
|**Povolit kopírování a vkládání**|Ne|Ano|
|**Povolit sdílení schránky mezi aplikacemi**|Ne|Ano|
|**Povolit YouTube**|Ne|Ano|

## Nastavení pro aplikace dodržující a nedodržující předpisy
V seznamu **Kompatibilní a nekompatibilní aplikace** zadejte seznam kompatibilních a nekompatibilních aplikací pomocí následujících informací:

> [!NOTE]
> Jedna zásada může obsahovat seznam jenom kompatibilních, nebo jenom nekompatibilních aplikací. Nejde zadat oba seznamy v jedné zásadě.

|Název nastavení|Další informace|
|-------------------|-------------------|
|**Ohlásit nekompatibilitu, když uživatelé nainstalují aplikace ze seznamu**|Zobrazí seznam aplikací, které Intune nespravuje a které nemají uživatelé dovolené nainstalovat a spustit.|
|**Neoznamovat nekompatibilitu, když uživatel nainstaluje uvedené aplikace**|Zobrazí seznam aplikací, které mají uživatelé dovoleno instalovat. Uživatelé nemůžou instalovat žádné další aplikace. Aplikace, které spravuje Intune, jsou povolené automaticky.|
|**Přidat**|Přidá aplikaci do vybraného seznamu. Zadejte název podle své volby, volitelně vydavatele aplikaci a adresu URL aplikace v úložišti aplikací.<br /><br />[Určení adres URL na obchody s aplikacemi](../Topic/iOS_configuration_policy_settings_in_Microsoft_Intune.md#BKMK_URL)|
|**Importovat aplikace**|Importuje seznam aplikací, které jste zadali v souboru hodnot oddělených čárkami. V souboru použijte formát, název aplikace, vydavatele, adresu URL aplikace.|
|**Upravit**|Tady můžete upravit název, vydavatele a adresu URL vybrané aplikace.|
|**Odstranit**|Odstraní vybranou aplikaci ze seznamu.|

## Nastavení celoobrazovkovém režimu
Zadejte pro **zařízení Samsung KNOX** následující nastavení:

|Název nastavení|Další informace|
|-------------------|-------------------|
|**Vyberte spravovanou aplikaci, která se bude moct spustit, když je zařízení v celoobrazovkovém režimu**|Klikněte na **Procházet**, vyberte spravovanou aplikaci nebo aplikaci ze Storu, která se bude moct spouštět, když je zařízení v celoobrazovkovém režimu. Žádné jiné aplikace nebudou mít dovoleno se na zařízení spouštět.<br /><br />[Určení adres URL na obchody s aplikacemi](../Topic/iOS_configuration_policy_settings_in_Microsoft_Intune.md#BKMK_URL)|
|**Povolit tlačítka hlasitosti**|Povolí nebo zakáže použití tlačítek hlasitosti na zařízení.|
|**Povolit tlačítko probuzení z režimu spánku obrazovky**|Povolí nebo zakáže na zařízení tlačítko probuzení z režimu spánku obrazovky.|

## Nasazení zásad konfigurace

1.  Nasaďte zásadu konfigurace do jedné nebo víc skupin uživatelů nebo zařízení ve vaší organizaci.

Další informace o tom, jak nasazovat zásady, najdete v tématu [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

Souhrn stavu a výstrahy v pracovním prostoru **Zásada** určují problémy se zásadou, které vyžadují vaši pozornost. Kromě toho se v pracovním prostoru **Řídicí panel** zobrazí shrnutí stavu.

## Referenční informace pro aplikace nesplňující předpisy

### Monitorování aplikací, které splňují a nesplňují předpisy
Pomocí **sestavy nekompatibilních aplikací** zobrazte kompatibilitu povolených a blokovaných aplikací.

##### Spuštění sestavy nekompatibilních aplikací

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com) klikněte na **Sestavy** &gt; **Sestava nekompatibilních aplikací**.

2.  Vyberte skupiny zařízení, které chcete zkontrolovat, určete, jestli kontrolovat kompatibilní aplikace, nekompatibilní aplikace nebo obojí a pak klikněte na **Zobrazit sestavu**.

### <a name="BKMK_URL"></a>Určení adres URL na obchody s aplikacemi
Pokud chcete zadat adresu URL aplikace do seznamu kompatibilních a nekompatibilních aplikací nebo použít možnost **Vybrat spravovanou aplikaci, která se může spouštět, když je zařízení v celoobrazovkovém režimu** (jenom iOS), použijte následující formát:

V [oddílu Aplikace na Google Play](https://play.google.com/store/apps) najděte aplikaci, kterou chcete použít.

Otevřete instalační stránku aplikace a zkopírujte adresu URL do schránky. Tu teď můžete použít jako adresu URL v seznamu kompatibilních nebo nekompatibilních aplikací.

**Příklad:** Na webu Google Play vyhledejte systém Microsoft Office Mobile. Použijete adresu URL **https://play.google.com/store/apps/details?id=com.microsoft.office.officehub**.

## Další kroky

## Viz také
[Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

