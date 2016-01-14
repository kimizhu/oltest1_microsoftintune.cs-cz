---
description: na
keywords: na
title: Windows configuration policy settings in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 6982a2bc-aafa-475a-9236-4840b709e5a1
---
# Nastaven&#237; z&#225;sad konfigurace pro Windows v Microsoft Intune
Ke konfiguraci nastavení pro registrovaná zařízení s Windows 8 a Windows 8.1 použijte **obecné zásady konfigurace Windows**[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]:

## Vytvoření obecných zásad konfigurace pro Windows

#### Zadání základního nastavení pro zásadu konfigurace

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com) klikněte na **Zásady** &gt; **Přehled** &gt; **Přidat zásadu**.

2.  Klikněte na **Windows** &gt; **Obecná konfigurace (Windows 8.1 a novější)** a potom klikněte na **Vytvořit zásadu**.

    > [!NOTE]
    > Nedaří se vám vytvořit zásadu konfigurace pomocí doporučovaného nastavení. Je potřeba vytvořit vlastní zásadu.

3.  V části **Obecné** stránky **Vytvořit zásadu** zadejte název a popis nové zásady.

4.  Informace v následujících částech vám pomůžou zadat nastavení zásad.

5.  Po dokončení klikněte na **Uložit zásadu**.

Nová zásada se zobrazí v uzlu **Zásady konfigurace** pracovního prostoru **Zásady**.

## <a name="BKMK_Settings"></a>Nastavení pro zaregistrovaná zařízení se systémem Windows

### <a name="BKMK_sec"></a>Nastavení zabezpečení

|Název nastavení|Windows 8.1 a Windows RT 8.1|Windows RT|
|-------------------|--------------------------------|--------------|
|**Vyžadovaný typ hesla**<br /><br />(určuje typ hesla, které se bude vyžadovat, například jenom číslice nebo alfanumerické znaky)|Ano|Ano|
|**Vyžadovaný typ hesla – Minimální počet znakových sad**<br /><br />Používají se čtyři znakové sady: malá písmena, velká písmena, číslice a symboly. Toto nastavení určuje, kolik různých znakových sad musí být v hesle zahrnutých). Pro zařízení s iOS ale určuje počet znaků symbolu, které musí být v hesle.)|Ano|Ano|
|**Minimální délka hesla**<sup>1</sup>|Ano|Ano|
|**Počet povolených opakovaných neúspěšných přihlášení, než bude zařízení vymazáno**|Ano|Ano|
|**Počet minut nečinnosti před vypnutím displeje**|Ano|Ano|
|**Vypršení platnosti hesla (dny)**|Ano|Ano|
|**Pamatovat si historii hesel**|Ano|Ano|
|**Pamatovat si historii hesel** – **Zabránit opětovnému použití předchozích hesel**|Ano|Ano|
|**Povolit obrázkové heslo a PIN**|Ano|Ano|
<sup>1</sup> Když nasadíte zásadu délky hesel na zařízení se systémem Windows RT, budou uživatelé přinucení změnit heslo, i když jejich aktuální heslo odpovídá požadavkům zásady.

### Nastavení šifrování

|Název nastavení|Windows 8.1 a Windows RT 8.1|Windows RT|
|-------------------|--------------------------------|--------------|
|**Vyžadovat šifrování u mobilního zařízení**<sup>1</sup><br /><br />Pro zařízení s Windows Phone 8 je potřeba nastavit hodnotu **Ano**.|Ano|Ne|
<sup>1</sup> Další informace pro zařízení s Windows 8.1

-   K vynucení šifrování na zařízeních s Windows 8.1 je potřeba na každé zařízení nainstalovat [aktualizaci MDM klienta pro Windows z prosince 2014](http://support.microsoft.com/kb/3013816).

-   Pokud toto nastavení povolíte pro zařízení s Windows 8.1, všichni uživatelé zařízení musí mít účet Microsoft.

-   Šifrování funguje, jenom když zařízení splňuje hardwarové požadavky certifikace Microsoft [InstantGo](http://blogs.windows.com/bloggingwindows/2014/06/19/instantgo-a-better-way-to-sleep/).

-   Pokud vynutíte šifrování na zařízení, je obnovovací klíč přístupný jenom uživatelům s účtem Microsoft, ke kterému přistupují z účtu na Onedrivu. Tento klíč se nedá obnovit jménem uživatele.

### Nastavení ochrany proti malwaru

|Název nastavení|Windows 8.1 a Windows RT 8.1|Windows RT|
|-------------------|--------------------------------|--------------|
|**Vyžadovat síťovou bránu firewall**|Ano|Ne|
|**Povolit SmartScreen**|Ano|Ne|

### Nastavení systému

|Název nastavení|Windows 8.1 a Windows RT 8.1|Windows RT|
|-------------------|--------------------------------|--------------|
|**Vyžadovat automatické aktualizace**|Ano|Ne|
|**Vyžadovat automatické aktualizace – automatická instalace minimální klasifikace aktualizací** <sup>1</sup><br /><br />Vyberte klasifikace aktualizací, které se instalují automaticky:<br /><br />-   **Důležité** – nainstaluje všechny aktualizace klasifikované jako důležité.<br />-   **Doporučené** – nainstaluje všechny aktualizace klasifikované jako důležité nebo doporučené.|Ano|Ne|
|**Řízení uživatelských účtů**|Ano|Ne|
|**Povolit odeslání diagnostických dat**|Ano|Ne|
<sup>1</sup> Pro vynucení šifrování v zařízeních s Windows 1 je nutné nainstalovat [aktualizaci klienta z prosince 8.1 MDM pro Windows](http://support.microsoft.com/kb/3013816) na každé zařízení.

### <a name="BKMK_cloud"></a>Nastavení cloudu – dokumenty a data

|Název nastavení|Windows 8.1 a Windows RT 8.1|Windows RT|
|-------------------|--------------------------------|--------------|
|**Adresa URL pracovních složek**<br /><br />(nastaví adresu URL pracovní složky, aby bylo možné synchronizovat dokumenty na všech zařízeních)|Ano|Ne|

### <a name="BKMK_email"></a>Nastavení e-mailu

|Název nastavení|Windows 8.1 a Windows RT 8.1|Windows RT|
|-------------------|--------------------------------|--------------|
|**Nastavit účet Microsoft jako volitelný v aplikaci Windows Pošta**|Ano|Ne|

### <a name="BKMK_browser"></a>Nastavení aplikace – prohlížeč

|Název nastavení|Windows 8.1 a Windows RT 8.1|Windows RT|
|-------------------|--------------------------------|--------------|
|**Povolit automatické vyplňování**|Ano|Ne|
|**Povolit blokování automaticky otevíraných oken**|Ano|Ne|
|**Povolit moduly plug-in**|Ano|Ne|
|**Povolit aktivní skriptování**|Ano|Ne|
|**Povolit upozornění na podvod**|Ano|Ne|
|**Povolit intranetovému serveru zadání jednoslovné položky**<br /><br />(umožňuje použití jednoho slova pro přesměrování Internet Exploreru na web jako třeba Bing)|Ano|Ne|
|**Povolit automatické zjišťování sítě intranet**|Ano|Ne|
|**Úroveň zabezpečení pro internet**|Ano|Ne|
|**Úroveň zabezpečení pro intranet**|Ano|Ne|
|**Úroveň zabezpečení pro důvěryhodné lokality**|Ano|Ne|
|**Úroveň zabezpečení pro lokality s omezeným přístupem**|Ano|Ne|
|**Odesílat hlavičku DNT (Do Not Track)**|Ano|Ne|
|**Povolit přístup nabídky podnikového režimu**|Ano|Ne|
|**Umístění webů podnikového režimu**|Ano|Ne|

### Nastavení možností zařízení – mobilní

|Název nastavení|Windows 8.1 a Windows RT 8.1|Windows RT|
|-------------------|--------------------------------|--------------|
|**Povolit datový roaming**|Ano|Ne|

## Nasazení zásad konfigurace

1.  Nasaďte zásadu konfigurace do jedné nebo víc skupin uživatelů nebo zařízení ve vaší organizaci.

Další informace o tom, jak nasazovat zásady, najdete v tématu [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

Souhrn stavu a upozornění v pracovním prostoru **Zásady** určují problémy se zásadami, které vyžadují vaši pozornost. Kromě toho se v pracovním prostoru **Řídicí panel** zobrazí shrnutí stavu.

## Viz také
[Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

