---
description: na
keywords: na
title: iOS configuration policy settings in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: ab46be6c-ab73-4c99-8492-66d1dd418293
---
# Nastaven&#237; z&#225;sad konfigurace pro iOS v Microsoft Intune
Pomocí **zásady obecné konfigurace pro iOS**[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] můžete nakonfigurovat nastavení pro:

-   **Nastavení zabezpečení mobilního zařízení** – Zvolte ze seznamu předdefinovaných nastavení, která umožňují v zařízení ovládat celou řadu funkcí.

-   **Celoobrazovkový režim** – Umožňuje uzamknout zařízení a povolit fungování jenom některých funkcí. Můžete třeba povolit, aby v zařízení běžela jenom jedna vámi určená spravovaná aplikace, nebo můžete zakázat tlačítka hlasitosti na zařízení. Tato nastavení se dají používat pro ukázkový model zařízení nebo zařízení, které může provádět jenom jednu funkci, jako je třeba zařízení POS.

-   **Seznam aplikací dodržujících a nedodržujících předpisy** – Určete seznam aplikací, které splňují nebo nesplňují předpisy ve vaší společnosti. Na zařízeních s Androidem a iOS je možné používat **Sestavu nekompatibilních aplikací** k zobrazení kompatibility aplikací, které jste uvedli v seznamu, s aplikacemi, které nainstalovali uživatelé (ale nemůžete ve skutečnosti zablokovat instalaci aplikace).

> [!TIP]
> Můžete nakonfigurovat podmínky pro uživatele a zajistit tak jejich informovanost o tom, že aplikace na jejich zařízení, včetně osobních aplikací, se budou hodnotit, a nekompatibilní aplikace se zablokují nebo nahlásí jako nevyhovující. Uživatelé musí přijmout tyto podmínky předtím, než můžou zaregistrovat své zařízení a používat firemní portál k získání aplikací. Další informace o podmínkách a ujednáních týkajících se použití najdete v tématu [Práce se zásadami pro pravidla a podmínky v Microsoft Intune](http://msdn.microsoft.com/en-us/library/ce59fb93-01fd-4822-a57d-45ca7d89843d).

## Vytvoření zásady konfigurace pro iOS

#### Zadání základního nastavení pro zásadu konfigurace

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com) klikněte na **Zásady** &gt; **Přehled** &gt; **Přidat zásadu**.

2.  Klikněte na **iOS** &gt; **Obecná konfigurace** a potom klikněte na **Vytvořit zásadu**.

    > [!NOTE]
    > Nedaří se vám vytvořit zásadu konfigurace pomocí doporučovaného nastavení. Je potřeba vytvořit vlastní zásadu.

3.  V části **Obecné** stránky **Vytvořit zásadu** zadejte název a popis nové zásady.

4.  Informace v následujících částech vám pomůžou zadat nastavení zásad.

5.  Po dokončení klikněte na **Uložit zásadu**.

Nová zásada se zobrazí v uzlu **Zásady konfigurace** pracovního prostoru **Zásady**.

## <a name="BKMK_Settings"></a>Aplikace pro zařízení s iOS
Pokud se v tomto seznamu nezobrazí nastavení, které hledáte, je možné, že ho budete moct vytvořit pomocí vlastních zásad pro iOS, které vám umožní naimportovat nastavení, které jste vytvořili, pomocí nástroje [Apple Configurator Tool](https://itunes.apple.com/us/app/apple-configurator/id434433123?mt=12). Další informace naleznete v části [Nastavení vlastních zásad pro iOS v Microsoft Intune](../Topic/iOS_custom_policy_settings_in_Microsoft_Intune.md).

### <a name="BKMK_sec"></a>Nastavení zabezpečení

|Název nastavení|iOS|
|-------------------|-------|
|**Vyžadovat heslo k odemknutí mobilních zařízení**|Ano|
|**Vyžadovaný typ hesla**<br /><br />(určuje typ hesla, které se bude vyžadovat, například jenom číslice nebo alfanumerické znaky)|Ano|
|**Vyžadovaný typ hesla – Minimální počet znakových sad**<br /><br />Používají se čtyři znakové sady: malá písmena, velká písmena, číslice a symboly. Toto nastavení určuje, kolik různých znakových sad musí být v hesle zahrnutých). Pro zařízení s iOS ale určuje počet znaků symbolu, které musí být v hesle.)|Ano|
|**Minimální délka hesla**|Ano|
|**Povolit jednoduchá hesla**<br /><br />Příklady jednoduchých hesel :0000 a 1234.|Ano|
|**Počet povolených opakovaných neúspěšných přihlášení, než bude zařízení vymazáno**|Ano|
|**Počet minut nečinnosti před vypnutím displeje**<sup>1</sup>|Ano|
|**Vypršení platnosti hesla (dny)**|Ano|
|**Pamatovat si historii hesel**|Ano|
|**Pamatovat si historii hesel** – **Zabránit opětovnému použití předchozích hesel**|Ano|
|**Počet minut nečinnosti před vyžadováním hesla**<sup>1</sup>|Ano|
|**Povolit odemknutí otiskem prstu**|iOS 7.1 nebo novější|
<sup>1</sup> U zařízení s iOS se v případě, že nakonfigurujete nastavení **Počet minut nečinnosti před vypnutím displeje** a **Počet minut nečinnosti před vyžadováním hesla**, tato nastavení použijí v uvedeném pořadí. Pokud například pro obě nastavení nastavíte hodnotu **5** minut, obrazovka se po 5 minutách automaticky vypne a po dalších 5 minutách se zařízení zamkne. Pokud ale uživatel vypne obrazovku ručně, druhé nastavení se použije okamžitě. V tomto příkladě se zařízení po tom, co uživatel vypne obrazovku, zamkne po 5 minutách.

### Nastavení systému

|Název nastavení|iOS|
|-------------------|-------|
|**Povolit snímek obrazovky**|Ano|
|**Povolit řídicí centrum na zamykací obrazovce**|iOS 7.1 nebo novější|
|**Povolit zobrazení oznámení na zamykací obrazovce**|iOS 7.1 nebo novější|
|**Povolit zobrazení informací o dnešku na zamykací obrazovce**|iOS 7.1 nebo novější|
|**Povolit odeslání diagnostických dat**|Ano|
|**Povolit nedůvěryhodné certifikáty TLS**|Ano|
|**Povolit aplikaci Passbook při uzamčení**|Ano|

### <a name="BKMK_cloud"></a>Nastavení cloudu – dokumenty a data

|Název nastavení|iOS|
|-------------------|-------|
|**Povolit zálohování na iCloud**|Ano|
|**Povolit synchronizaci dokumentů s iCloudem**|Ano|
|**Povolit synchronizaci datového proudu fotografií s iCloudem**|Ano|
|**Vyžadovat šifrované zálohování**|Ano|

### <a name="BKMK_browser"></a>Nastavení aplikace – prohlížeč

|Název nastavení|iOS|
|-------------------|-------|
|**Povolit Safari**|Ano|
|**Povolit automatické vyplňování**|Ano|
|**Povolit blokování automaticky otevíraných oken**|Ano|
|**Povolit soubory cookie**|Ano|
|**Povolit skriptování v Javě**|Ano|
|**Povolit upozornění na podvod**|Ano|

### <a name="BKMK_apps"></a>Nastavení aplikace – aplikace

|Název nastavení|iOS|
|-------------------|-------|
|**Povolit obchod s aplikacemi**|Ano|
|**Vyžadovat heslo pro přístup do obchodu s aplikacemi**|Ano|
|**Povolit nákupy v aplikaci**|Ano|
|**Povolit spravované dokumenty v jiných nespravovaných aplikacích**|iOS 7.1 nebo novější|
|**Povolit nespravované dokumenty v jiných spravovaných aplikacích**|iOS 7.1 nebo novější|
|**Povolit videokonference**|Ano|
|**Povolit obsah pro dospělé v obchodě s mediálním obsahem**|Ano|

### Nastavení aplikace – hry

|Název nastavení|iOS|
|-------------------|-------|
|**Povolit přidávání přátel v herním centru**|Ano|
|**Povolit hru s více hráči**|Ano|

### <a name="BKMK_hard"></a>Nastavení možností zařízení – hardware

|Název nastavení|iOS|
|-------------------|-------|
|**Povolit fotoaparát**|Ano|

### Nastavení možností zařízení – mobilní

|Název nastavení|iOS|
|-------------------|-------|
|**Povolit hlasový roaming**|Ano|
|**Povolit datový roaming**|Ano|
|**Povolit globální načítání na pozadí při roamingu**|Ano|

### Nastavení možností zařízení – funkce

|Název nastavení|iOS|
|-------------------|-------|
|**Povolit Siri**|Ano|
|**Povolit Siri při uzamčení zařízení**|Ano|
|**Povolit hlasové vytáčení**|Ano|
|**Povolit sdílení schránky mezi aplikacemi**|Ne|
|**Povolit YouTube**|Ne|

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
Pro **zařízení iOS** určete následující nastavení:

|Název nastavení|Další informace|
|-------------------|-------------------|
|**Vyberte spravovanou aplikaci, která se bude moct spustit, když je zařízení v celoobrazovkovém režimu**|Klikněte na **Procházet** a zadejte spravovanou aplikaci nebo aplikaci ze Storu, která se bude moct spouštět, když je zařízení v celoobrazovkovém režimu. Žádné jiné aplikace nebudou mít dovoleno se na zařízení spouštět.<br /><br />[Určení adres URL na obchody s aplikacemi](../Topic/iOS_configuration_policy_settings_in_Microsoft_Intune.md#BKMK_URL).|
|**Povolit dotykové ovládání**|Povolí nebo zakáže dotykovou obrazovku na zařízení.|
|**Povolit otočení obrazovky**|Povolí nebo zakáže změnu orientace obrazovky při otočení zařízení.|
|**Povolit tlačítka hlasitosti**|Povolí nebo zakáže použití tlačítek hlasitosti na zařízení.|
|**Povolit přepínač vyzvánění**|Povolí nebo zakáže přepínač vyzvánění (ztlumení) na zařízení.|
|**Povolit tlačítko probuzení z režimu spánku obrazovky**|Povolí nebo zakáže na zařízení tlačítko probuzení z režimu spánku obrazovky.|
|**Povolit automatické uzamčení**|Povolí nebo zakáže automatické uzamykání zařízení.|
|**Povolit mono zvuk**|Povolí nebo zakáže nastavení usnadnění **Mono zvuk**.|
|**Povolit hlasitý přednes**|Povolí nebo zakáže nastavení usnadnění **VoiceOver**, které předčítá text na displeji zařízení.|
|**Povolit úpravy hlasového přednesu**|Povolí nebo zakáže úpravy hlasového přednesu, které umožňují nastavit funkci nástroje VoiceOver (například rychlost čtení textu na obrazovce).|
|**Povolit zvětšení**|Povolí nebo zakáže nastavení usnadnění **Zvětšení**, které vám umožní používat dotykové ovládání pro zvětšení zobrazení zařízení.|
|**Povolit úpravy zvětšení**|Povolí nebo zakáže úpravy zvětšení, které umožňují nastavit funkci zvětšení.|
|**Povolit inverzi barev**|Povolí nebo zakáže nastavení usnadnění **Invertovat barvy**, které upraví displej tak, aby pomáhal uživatelům se zrakovým postižením.|
|**Povolit úpravy inverze barev**|Povolí nebo zakáže úpravy inverze barev, které umožňuje nastavit funkci inverze barev.|
|**Povolit usnadnění dotykového ovládání**|Povolí nebo zakáže nastavení usnadnění **dotykového ovládání**, která uživatelům pomáhá provádět na obrazovce gesta, která by se jim mohla těžko provádět.|
|**Povolit úpravy usnadnění dotykového ovládání**|Povolí nebo zakáže úpravy usnadnění dotykového ovládání, které umožňují upravit funkce usnadnění dotykového ovládání.|
|**Povolit výběr řeči**|Povolí nebo zakáže nastavení usnadnění **Výběr řeči**, které může nahlas přečíst vybraný text.|
> [!NOTE]
> Následující poznámky platí pro nastavení celoobrazovkového režimu na zařízeních iOS:
> 
> -   Než budete moct nakonfigurovat nastavení zařízení iOS pro celoobrazovkový režim, musíte převést zařízení do režimu dohledu pomocí [nástroje Apple Configurator](https://itunes.apple.com/us/app/apple-configurator/id434433123?mt=12) nebo manažera registrace zařízení. Další informace o nástroji Apple Configurator získáte v dokumentaci Apple.
> -   Pokud je určená aplikace pro iOS nainstalovaná až po nasazení zásad konfigurace, zařízení nepřejde do celoobrazovkového, dokud ho nerestartujete.

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

Pomocí vyhledávacího modulu najděte aplikaci, kterou chcete použít v iTunes App Storu, a otevřete stránku pro aplikaci.

Zkopírujte adresu URL stránky a použijte ji jako URL ke konfiguraci seznamu kompatibilních nebo nekompatibilních aplikací nebo aplikace, kterou chcete spustit v celoobrazovkovém režimu.

**Příklad:** Vyhledejte **Microsoft Word for iPad**. Použitá adresa URL bude **https://itunes.apple.com/us/app/microsoft-word-for-ipad/id586447913?mt=8**.

> [!NOTE]
> Pomocí softwaru iTunes taky můžete najít aplikaci a pomocí příkazu **Kopírovat odkaz** získat adresu URL aplikace.

## Viz také
[Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

