---
description: na
keywords: na
title: Manage device compliance policies for Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0775107a-6662-41c8-9404-be14bbb599f3
---
# Spr&#225;va z&#225;sad dodržov&#225;n&#237; předpisů zař&#237;zen&#237;mi pro Microsoft Intune
**Zásady dodržování předpisů** definují pravidla a nastavení, které zařízení musí dodržovat, aby se dalo považovat za zařízení, které dodržuje zásady podmíněného přístupu. Zásady dodržování předpisů můžeme používat i k monitorování a opravám problémů s dodržováním předpisů u zařízení, a to nezávisle na podmíněném přístupu.

Mezi tato pravidla patří:

-   PIN kód a hesla

-   Šifrování

-   Jestli je zařízení s jailbreakem nebo rootem

-   Jestli je e-mail na zařízení spravovaný zásadami služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]

Zásady dodržování předpisů nasazujete uživatelům a zařízením. Když se zásady dodržování předpisů nasadí uživateli, kontroluje se dodržování předpisů u všech zařízení takového uživatele.

Následující tabulka uvádí typy zařízení podporované zásadami dodržování předpisů. Kromě toho je v ní i způsob, jak se spravují nastavení, která předpisy nedodržují, pokud se zásady používají se zásadami podmíněného přístupu.

|Typ zařízení|Konfigurace PIN kódu nebo hesla|Šifrování zařízení|Zařízení s jailbreakem nebo rootem|E-mailový profil|
|----------------|-----------------------------------|----------------------|--------------------------------------|--------------------|
|Windows 8.1 a vyšší|Opravené|Není k dispozici|Není k dispozici|Není k dispozici|
|Windows Phone 8.1 nebo novější|Opravené|Opravené|Není k dispozici|Není k dispozici|
|iOS 6,0 nebo novější|Opravené|Opravené (nastavením PIN kódu)|V karanténě (není nastavení)|V karanténě|
|Android 4.0 nebo novější|V karanténě|V karanténě|V karanténě (není nastavení)|Není k dispozici|
|Zařízení, na kterém běží Samsung KNOX Standard 4.0 nebo novější|V karanténě|V karanténě|V karanténě (není nastavení)|Není k dispozici|
**Opravené** = dodržování předpisů se vynucuje operačním systémem zařízení (například tak, že uživatel musí zadat PIN kód).  To se nikdy nestane, pokud nastavení nedodržuje předpisy.

**V karanténě** = operační systém zařízení nevynucuje dodržování předpisů (například zařízení s Androidem nenutí uživatele šifrovat svoje zařízení).  V takovém případě:

-   Zařízení se zablokuje, pokud se na uživatele zaměřuje zásada podmíněného přístupu.

-   Firemní portál nebo Webový portál oznámí uživateli všechny problémy s dodržováním předpisů.

## <a name="BKMK_Compliance"></a>Krok 1: Vytvoření zásady dodržování předpisů

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com) klikněte na **Zásady** &gt; **Zásady dodržování předpisů** &gt; **Přidat**.

2.  Na stránce **Vytvořit zásadu** nakonfigurujte požadovaná nastavení:

    |Název nastavení|Další informace|Podporované platformy|
    |-------------------|-------------------|-------------------------|
    |**Název**|Zadejte jedinečný název zásady dodržování předpisů.|-   Všechny|
    |**Popis**|Zadejte popis, který poskytne přehled zásady dodržování předpisů.|-   Všechny|
    |**Vyžadovat heslo k odemknutí mobilních zařízení**|Vyžaduje, aby uživatel zadal heslo, než bude moct svoje zařízení používat.|-   Windows Phone 8 nebo novější<br />-   iOS 6 nebo novější<br />-   Android 4.0 nebo novější<br />-   Zařízení, na kterém běží Samsung KNOX Standard 4.0 nebo novější|
    |**Povolit jednoduchá hesla**|Umožní uživatelům vytvářet jednoduchá hesla, jako jsou **1234**nebo **1111**.|-   Windows Phone 8 nebo novější<br />-   iOS 6 nebo novější|
    |**Minimální délka hesla**<sup>1</sup>|Určuje minimální počet číslic nebo znaků, které musí heslo uživatele obsahovat.|-   Windows Phone 8 nebo novější<br />-   Windows 8.1<br />-   iOS 6 nebo novější<br />-   Android 4.0 nebo novější<br />-   Zařízení, na kterém běží Samsung KNOX Standard 4.0 nebo novější|
    |**Vyžadovaný typ hesla**|Určuje, jestli uživatelé musí vytvořit **Alfanumerické** nebo **Číselné** heslo.|-   Windows Phone 8 nebo novější<br />-   Windows RT a Windows RT 8.1<br />-   Windows 8.1<br />-   iOS 6 nebo novější|
    |**Minimální počet znakových sad**<sup>1</sup>|Pokud se **Požadovaný typ hesla** nastaví na **Alfanumerické**, toto nastavení určuje nejmenší počet znakových sad, které musí heslo obsahovat.<br /><br />Jde o tyto čtyři znakové sady:<br /><br />-   Malá písmena<br />-   Velká písmena<br />-   Symboly<br />-   Čísla<br /><br />Pokud se v tomto nastavení nastaví větší číslo, uživatelé budou muset vytvářet složitější hesla.<br /><br />Pro zařízení s iOS toto nastavení znamená počet speciálních znaků (například **!**, **#**, **&amp;**), které musí heslo obsahovat.|-   Windows Phone 8 nebo novější<br />-   Windows RT a Windows RT 8.1<br />-   Windows 8.1<br />-   iOS 6 nebo novější|
    |**Kvalita hesla**|Konfiguruje požadavky na heslo pro zařízení s Androidem. Vybírejte z těchto možností:<br /><br />-   **Biometrika s nízkým zabezpečením**<br />-   **Požadováno**<br />-   **Aspoň číselné**<br />-   **Aspoň abecední**<br />-   **Aspoň alfanumerické**<br />-   **Alfanumerické se symboly**|-   Android 4.0 nebo novější<br />-   Zařízení, na kterém běží Samsung KNOX Standard 4.0 nebo novější|
    |**Počet minut nečinnosti před vyžadováním hesla**|Určuje dobu nečinnosti, po které bude uživatel muset zadat svoje heslo znovu.|-   iOS 6 nebo novější|
    |**Vypršení platnosti hesla (dny)**|Zvolte počet dní, za který uživatelské heslo vyprší a uživatel bude muset vytvořit nové.|-   Windows Phone 8 nebo novější<br />-   Windows RT a Windows RT 8.1<br />-   Windows 8.1<br />-   iOS 6 nebo novější<br />-   Android 4.0 nebo novější<br />-   Zařízení, na kterém běží Samsung KNOX Standard 4.0 nebo novější|
    |**Pamatovat si historii hesel**|Pokud chcete zabránit uživatelům, aby vytvářeli hesla, která používali dřív, použijte toto nastavení spolu s nastavením **Zakázat opakované použití předchozích hesel**.|-   Windows Phone 8 nebo novější<br />-   Windows RT a Windows RT 8.1<br />-   Windows 8.1<br />-   iOS 6 nebo novější<br />-   Android 4.0 nebo novější<br />-   Zařízení, na kterém běží Samsung KNOX Standard 4.0 nebo novější|
    |**Zakázat opakované použití předchozích hesel**|Pokud se zvolila možnost **Pamatovat si historii hesel**, zadejte počet předchozích hesel, která se nesmí znovu použít.|-   Windows Phone 8 nebo novější<br />-   Windows RT a Windows RT 8.1<br />-   Windows 8.1<br />-   iOS 6 nebo novější<br />-   Android 4.0 nebo novější<br />-   Zařízení, na kterém běží Samsung KNOX Standard 4.0 nebo novější|
    |**Vyžadovat šifrování u mobilního zařízení**|Vyžaduje, aby zařízení bylo před připojením k prostředkům šifrované.<br /><br />Zařízení s Windows Phone 8 se šifrují automaticky. **Important:** Zařízení s iOS se šifrují, pokud nakonfigurujete nastavení **Vyžadovat heslo k odemknutí mobilních zařízení**.|-   Windows Phone 8 nebo novější<br />-   Android 4.0 nebo novější<br />-   Zařízení, na kterém běží Samsung KNOX Standard 4.0 nebo novější|
    |**U zařízení nesmí být provedený jailbreak nebo root**|Pokud se povolí, zařízení s jailbreakem (iOS) nebo rootem (Android) nebudou dodržovat předpisy.|-   iOS 6 nebo novější<br />-   Android 4.0 nebo novější<br />-   Zařízení, na kterém běží Samsung KNOX Standard 4.0 nebo novější|
    |**E-mailový účet se musí spravovat přes Intune**|Pokud se zvolí tato možnost, zařízení se ohlásí jako nedodržující předpisy, pokud uživatel na zařízení nastavil e-mailový účet, který se shoduje s e-mailovým profilem Intune nasazeným na zařízení správcem IT. Intune nemůže přepsat uživatelem zřízený profil, a proto ho nemůže ani spravovat.<br /><br />Aby zařízení dodržovalo předpisy, uživatel musí odstranit existující nastavení e-mailu. Pak Intune může nainstalovat spravovaný e-mailový profil.<br /><br />Podrobnosti o e-mailových profilech najdete v [Konfigurace přístupu k podnikovému e-mailu pomocí e-mailových profilů v Microsoft Intune](../Topic/Configure_access_to_corporate_email_using_email_profiles_with_Microsoft_Intune.md).|-   iOS 6 nebo novější|
    |**Vyberte e-mailový profil, který se musí spravovat přes Intune**|Pokud se zvolí **E-mailový účet se musí spravovat přes Intune**, klikněte na **Vybrat** a zvolte e-mailový profil Intune, přes který se musí spravovat zařízení. Tento e-mailový profil musí být na zařízení.|-   iOS 6 nebo novější|
    <sup>1</sup> U zařízení s Windows zabezpečených účtem Microsoft se zásada dodržování předpisů nevyhodnotí správně, pokud je **Minimální délka hesla** větší než 8 znaků nebo pokud **Minimální počet znakových sad** je víc než 2.

3.  Po dokončení klikněte na **Uložit zásadu**.

Nová zásada se zobrazí v uzlu **Zásady dodržování předpisů** pracovního prostoru **Zásady**.

## Nasazení zásady dodržování předpisů
Nasaďte zásadu dodržování předpisů do jedné nebo víc skupin uživatelů nebo zařízení ve vaší organizaci.

Další informace o tom, jak nasazovat zásady, najdete v tématu [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

Pomocí shrnutí stavu a výstrah na stránce **Přehled** v pracovním prostoru **Zásady** můžete identifikovat problémy se zásadami, které vyžadují vaši pozornost. Kromě toho se v pracovním prostoru **Řídicí panel** zobrazí shrnutí stavu.

## Monitorování zásady dodržování předpisů

#### Zobrazení zařízení, která nesplňují zásady dodržování předpisů

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com) klikněte na **Skupiny**.

2.  Otevřete kartu **Zásada** pro kterékoli zařízení, které je kompatibilní se zásadami dodržování předpisů.

3.  V rozevíracím seznamu **Filtry** zvolte **Nevyhovuje zásadám dodržování předpisů**.

## Způsob řešení konfliktů zásad Intune
V případě konfliktů, ke kterým dojde kvůli tomu, že se na zařízení aplikuje více nastavení Intune, platí následující pravidla:

-   Pokud jsou konfliktní nastavení ze zásad konfigurace a dodržování předpisů služby Intune, bude mít nastavení v zásadách kompatibility přednost před nastavením v zásadách konfigurace, a to i v případě, že je nastavení v zásadách konfigurace bezpečnější.

-   Pokud jste nasadili víc zásad dodržování předpisů, použijí se ty nejbezpečnější z nich.

## Další kroky
Teď už můžete používat zásady dodržování předpisů spolu se zásadami podmíněného přístupu, abyste mohli řídit přístup ke službám ve vaší organizaci.

## Viz také
[Správa přístupu k e-mail a SharePointu pomocí Microsoft Intune](../Topic/Manage_access_to_email_and_SharePoint_with_Microsoft_Intune.md)

