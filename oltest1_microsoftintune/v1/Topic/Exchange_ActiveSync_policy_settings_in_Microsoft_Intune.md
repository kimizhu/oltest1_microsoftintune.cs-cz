---
description: na
keywords: na
title: Exchange ActiveSync policy settings in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e9cbb826-b155-4df6-abf3-60c6f05b2783
---
# Nastaven&#237; z&#225;sad Exchange ActiveSync v Microsoft Intune
Pomocí zásady pro [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Exchange ActiveSync můžete nakonfigurovat nastavení, které vám umožní ovládat řadu funkcí v zařízení spravovaných protokolem Exchange ActiveSync.

## Vytvoření zásady pro Exchange ActiveSync

#### Zadání základního nastavení pro zásadu

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com) klikněte na **Zásady** &gt; **Přehled** &gt; **Přidat zásadu**.

2.  Klikněte na **Obecná nastavení mobilních zařízení** &gt; **Exchange ActiveSync** a potom klikněte na **Vytvořit zásadu**.

    > [!NOTE]
    > Nedaří se vám vytvořit zásadu konfigurace pomocí doporučovaného nastavení. Je potřeba vytvořit vlastní zásadu.

3.  V části **Obecné** stránky **Vytvořit zásadu** zadejte název a popis nové zásady.

4.  Informace v následujících částech vám pomůžou zadat nastavení zásad.

5.  Po dokončení klikněte na **Uložit zásadu**.

Nová zásada se zobrazí v uzlu **Zásady konfigurace** pracovního prostoru **Zásady**.

## <a name="BKMK_Settings"></a>Nastavení zásady pro zařízení spravovaná protokolem Exchange ActiveSync

### <a name="BKMK_sec"></a>Nastavení zabezpečení

|Název nastavení|
|-------------------|
|**Vyžadovat heslo k odemknutí mobilních zařízení**|
|**Vyžadovaný typ hesla**<br /><br />(určuje typ hesla, které se bude vyžadovat, například jenom číslice nebo alfanumerické znaky)|
|**Minimální délka hesla**|
|**Povolit jednoduchá hesla**<br /><br />Příklady jednoduchých hesel :0000 a 1234.|
|**Počet povolených opakovaných neúspěšných přihlášení, než bude zařízení vymazáno**|
|**Vypršení platnosti hesla (dny)**|
|**Pamatovat si historii hesel**|
|**Pamatovat si historii hesel** – **Zabránit opětovnému použití předchozích hesel**|
|**Počet minut nečinnosti před vyžadováním hesla**|

### Nastavení šifrování

|Název nastavení|
|-------------------|
|**Vyžadovat šifrování u mobilního zařízení**<sup>1</sup><br /><br />Pro zařízení s Windows Phone 8 je potřeba nastavit hodnotu **Ano**.<br /><br />Pokud chcete povolit šifrování na zařízeních iOS, povolte nastavení **Vyžadovat heslo k odemknutí mobilních zařízení**.|
|**Vyžadovat šifrování u paměťových karet**|
<sup>1</sup> Další informace pro zařízení s Windows 8.1

-   K vynucení šifrování na zařízeních s Windows 8.1 je potřeba na každé zařízení nainstalovat [aktualizaci MDM klienta pro Windows z prosince 2014](http://support.microsoft.com/kb/3013816).

-   Pokud toto nastavení povolíte pro zařízení s Windows 8.1, všichni uživatelé zařízení musí mít účet Microsoft.

-   Šifrování funguje, jenom když zařízení splňuje hardwarové požadavky certifikace Microsoft [InstantGo](http://blogs.windows.com/bloggingwindows/2014/06/19/instantgo-a-better-way-to-sleep/).

-   Pokud vynutíte šifrování na zařízení, je obnovovací klíč přístupný jenom uživatelům s účtem Microsoft, ke kterému přistupují z účtu na Onedrivu. Tento klíč se nedá obnovit jménem uživatele.

### <a name="BKMK_email"></a>Nastavení e-mailu

|Název nastavení|
|-------------------|
|**Povolit uživatelům stahovat přílohy e-mailů**|
|**Interval synchronizace e-mailu**|
|**Povolit mobilním zařízením, která plně nepodporují nastavení Exchange ActiveSync, synchronizaci se serverem Exchange**|

### <a name="BKMK_browser"></a>Aplikace – Prohlížeč

|Název nastavení|
|-------------------|
|**Povolit webový prohlížeč**|

### <a name="BKMK_hard"></a>Možnosti zařízení – hardware

|Název nastavení|
|-------------------|
|**Povolit fotoaparát**|

## Nasazení zásad konfigurace

1.  Nasaďte zásadu konfigurace do jedné nebo víc skupin uživatelů nebo zařízení ve vaší organizaci.

Další informace o tom, jak nasazovat zásady, najdete v tématu [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

Souhrn stavu a výstrahy v pracovním prostoru **Zásada** určují problémy se zásadou, které vyžadují vaši pozornost. Kromě toho se v pracovním prostoru **Řídicí panel** zobrazí shrnutí stavu.

## Viz také
[Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

