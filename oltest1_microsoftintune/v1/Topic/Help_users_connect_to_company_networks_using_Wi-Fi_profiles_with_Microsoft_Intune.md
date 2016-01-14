---
description: na
keywords: na
title: Help users connect to company networks using Wi-Fi profiles with Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 0b1b86ed-2e80-474d-8437-17dd4bc07b55
---
# Pomoc uživatelům s připojen&#237;m k s&#237;t&#237;m společnosti pomoc&#237; Wi-Fi profilů s Microsoft Intune
Použijte profily Wi-Fi služby [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] k nasazení nastavení bezdrátové sítě uživatelům a na zařízení ve vaší organizaci. Tato nastavení zjednodušují připojení k bezdrátovým sítím pro koncové uživatele.

Například:

-   Instalujete novou síť Wi-Fi s názvem **Contoso Wi-Fi** a chcete ve všech zařízeních s operačním systémem iOS zřídit nastavení požadované k připojení k této síti.

-   Vytvoříte profil Wi-Fi obsahující nastavení požadovaná pro připojení k bezdrátové síti **Contoso Wi-Fi**.

-   Potom nasadíte tento profil všem uživatelům, kteří mají zařízení s iOS.

-   Uživatelé najdou novou síť **Contoso Wi-Fi** v seznamu bezdrátových sítí a můžou se k ní snadno připojit.

Profily Wi-Fi můžete nasadit na následujících platformách:

-   Android 4.0 nebo novější

-   iOS 7.1 nebo novější

-   Mac OS X 10.9 a novější

Kromě toho pro zařízení, na kterých běží Windows 8.1 a vyšší, můžete importovat konfigurační profil Wi-Fi, který jste předtím exportovali do souboru. Podrobnosti najdete v tématu [Import konfiguračního profilu Wi-Fi (Windows 8.1 a vyšší)](../Topic/Help_users_connect_to_company_networks_using_Wi-Fi_profiles_with_Microsoft_Intune.md#BKMK_Import).

## Postup vytvoření a nasazení profilu Wi-Fi

### Krok 1: Vytvoření profilu Wi-Fi a zadání obecných informací

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com) klikněte na **Zásady** &gt; **Přidat zásadu**.

2.  Vyberte jeden z následujících typů zásad a potom klikněte na **Vytvořit zásadu**:

    -   **Profil Wi-Fi (Android 4 a novější)**

    -   **Profil Wi-Fi (iOS 7.1 a novější)**

    -   **Profil Wi-Fi (Mac OS X 10.9 a novější)**

    Pro tento typ zásad nejsou žádná doporučená nastavení. Je potřeba vytvořit vlastní zásadu.

3.  Zadejte tyto obecné hodnoty:

    |Nastavení|Další informace|
    |-------------|-------------------|
    |**Název**|Zadejte jedinečný název profilu Wi-Fi, podle kterého ho poznáte v konzole služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].|
    |**Popis**|Zadejte popis profilu Wi-Fi, který vám pomůže ho najít.|

### Krok 2: Konfigurace nastavení připojení k síti
Zadejte hodnoty **Síťových připojení**:

|Nastavení|Další informace|
|-------------|-------------------|
|**Název sítě**|Zadejte popisný název bezdrátové sítě. Je to název, který se zobrazí v zařízení uživatele, když vybírá bezdrátovou síť.|
|**Identifikátor SSID (Service Set Identifier)**|Zadejte identifikátor SSID bezdrátové sítě, ke které se mají zařízení připojovat. SSID rozlišuje malá a velká písmena a nezobrazuje se uživatelům.|
|**Připojit automaticky, pokud je tato síť v dosahu**|Vyberte tuto možnost, pokud chcete, aby se zařízení automaticky připojovala k bezdrátové síti, pokud je v dosahu.|
|**Připojit, pokud síť nevysílá svůj název (SSID)**|Po zvolení této možnosti se zařízení můžou připojit k síti, když není zobrazená v seznamu sítí (protože je skrytá a nevysílá svůj název).|

### Krok 3: Konfigurace nastavení zabezpečení
Nakonfigurujte **Nastavení zabezpečení** pro vybranou platformu. Dostupná nastavení závisí na typu zabezpečení, které vyberete.

#### Zařízení s Androidem

|Název nastavení|Další informace|Použijte, když:|
|-------------------|-------------------|-------------------|
|**Typ zabezpečení**|Vyberte protokol zabezpečení bezdrátové sítě:<br /><br />-   **WPA-Enterprise/WPA2-Enterprise**<br />-   **Bez ověřování (otevřené)**, pokud síť není zabezpečená.|Vždy|
|**Typ protokolu EAP**|Zvolte typ protokolu EAP pro ověřování zabezpečených bezdrátových připojení:<br /><br />-   **EAP-TLS**<br />-   **PEAP**<br />-   **EAP-TTLS**|Vybrali jste typ zabezpečení **WPA-Enterprise/WPA2-Enterprise**.|
|**Vybrat kořenové certifikáty pro ověření serveru**|Klikněte na **Vybrat**, pak zvolte profil důvěryhodných kořenových certifikátů pro ověření připojení. **Important:** Pokud chcete vytvořit profil důvěryhodných kořenových certifikátů, přečtěte si téma [Povolení přístupu k firemním prostředkům pomocí profilů certifikátů v Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md).|Je vybraný jakýkoliv **typ protokolu EAP**.|
|**Metoda ověření**|Vyberte metodu ověřování připojení:<br /><br />-   **Certifikáty** – pokud chcete zadat klientský certifikát.<br />-   **Uživatelské jméno a heslo** – pokud chcete zadat jinou metodu ověřování|**Typ protokolu EAP** je **PEAP** nebo **EAP-TTLS**.|
|**Vybrat pro ověřování metodu bez protokolu EAP (vnitřní identita)**|Vyberte metodu ověřování připojení:<br /><br />-   **Žádné**<br />-   **Nezašifrované heslo (PAP)**<br />-   **Protokol CHAP (Challenge Handshake Authentication Protocol)**<br />-   **Protokol Microsoft CHAP (MS-CHAP)**<br />-   **Protokol MS-CHAP v2 (Microsoft CHAP verze 2)**<br /><br />Dostupné možnosti závisí na typu EAP, který jste vybrali.|**Metoda ověřování** je **Uživatelské jméno a heslo**.|
|**Povolit ochranu identity (vnější identita)**|Zadejte text odeslaný v odpovědi na požadavek identity EAP. Tento text může být libovolná hodnota. Při ověřování se nejdřív pošle tato anonymní identita a po ní následuje skutečná identifikace poslaná přes zabezpečené tunelové propojení.|**Typ protokolu EAP** je **PEAP** nebo **EAP-TTLS**.|
|**Vybrat klientský certifikát pro ověřování klientů (certifikát identity)**|Klikněte na **Vybrat**, pak zvolte profil certifikátu SCEP pro ověření připojení. **Important:** Pokud chcete vytvořit profil certifikátu SCEP, přečtěte si téma [Povolení přístupu k firemním prostředkům pomocí profilů certifikátů v Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md).|Typ zabezpečení je **WPA-Enterprise/WPA2-Enterprise** a je vybraný jakýkoliv **typ protokolu EAP**.|

#### Pro zařízení iOS a Mac OS X

|Název nastavení|Další informace|Použijte, když:|
|-------------------|-------------------|-------------------|
|**Typ zabezpečení**|Vyberte protokol zabezpečení bezdrátové sítě:<br /><br />-   **WPA-Personal/WPA2-Personal**<br />-   **WPA-Enterprise/WPA2-Enterprise**<br />-   **WEP**<br />-   **Bez ověřování (otevřené)**, pokud síť není zabezpečená.|Vždy|
|**Typ protokolu EAP**|Zvolte typ protokolu EAP pro ověřování zabezpečených bezdrátových připojení:<br /><br />-   **EAP-TLS**<br />-   **PEAP**<br />-   **EAP-TLS**<br />-   **EAP-AST**<br />-   **LEAP**<br />-   **EAP-SIM**|Vybrali jste typ zabezpečení **WPA-Enterprise/WPA2-Enterprise**.|
|**Názvy certifikátů důvěryhodných serverů**|Vyberte profil důvěryhodných kořenových certifikátů pro ověření připojení. **Important:** Pokud chcete vytvořit profil důvěryhodných kořenových certifikátů, přečtěte si téma [Povolení přístupu k firemním prostředkům pomocí profilů certifikátů v Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md).|Vybrali jste typ protokolu EAP **EAP-TLS**, **PEAP**, **EAP-TTLS** nebo **EAP-FAST**.|
|**Použít ověření PAC (Protected Access Credential)**|Toto nastavení vyberte, pokud chcete použít přihlašovací údaje chráněného přístupu k navázání ověřeného tunelového propojení mezi klientem a serverem ověřování. Použije se stávající soubor PAC, pokud je dostupný.|**Typ protokolu EAP** je **EAP-FAST**.|
|**Zřízení PAC**|Zřídí soubor PAC ve vašich zařízeních.<br /><br />Pokud použijete toto nastavení, můžete taky vybrat **Zřídit PAC anonymně**, aby se soubor PAC mohl zřizovat bez ověřování serveru.|Je vybraný typ zabezpečení **Použít ověření PAC (Protected Access Credential)**.|
|**Metoda ověření**|Vyberte metodu ověřování připojení:<br /><br /><ul><li>**Certifikáty** – pokud chcete zadat klientský certifikát.</li><li>**Uživatelské jméno a heslo** – pokud chcete zadat jednu z následujících metod ověřování bez protokolu EAP (označuje se taky jako vnitřní identita):<br /><br /><ul><li>**Žádné**</li><li>**Nezašifrované heslo (PAP)**</li><li>**Protokol CHAP (Challenge Handshake Authentication Protocol)**</li><li>**Protokol Microsoft CHAP (MS-CHAP)**</li><li>**Protokol MS-CHAP v2 (Microsoft CHAP verze 2)**</li><li>**EAP-TLS**</li></ul></li></ul>|**Typ protokolu EAP** je **PEAP** nebo **EAP-TTLS**.|
|**Vybrat klientský certifikát pro ověřování klientů (certifikát identity)**|Vyberte profil certifikátu SCEP použitý k ověření připojení. **Important:** Pokud chcete vytvořit profil certifikátu SCEP, přečtěte si téma [Povolení přístupu k firemním prostředkům pomocí profilů certifikátů v Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md).|Pokud je typ zabezpečení **WPA-Enterprise/WPA2-Enterprise** a **Typ protokolu EAP** je **EAP-TLS**, **protokol PEAP** nebo **EAP-TTLS**.|
|**Povolit ochranu identity (vnější identita)**|Zadejte text odeslaný v odpovědi na požadavek identity EAP. Tento text může být libovolná hodnota.<br /><br />Při ověřování se nejdřív pošle tato anonymní identita a po ní následuje skutečná identifikace poslaná přes zabezpečené tunelové propojení.|Pokud je **typ protokolu EAP** nastavený na **PEAP**, **EAP-TTLS** nebo **EAP-FAST**.|

### Krok 4: Konfigurace nastavení proxy serveru (jenom iOS a MAC OS X)

1.  U profilů Wi-Fi v iOS a Mac OS X nakonfigurujte následující nastavení (pokud zabezpečujete síť pomocí proxy serveru) v části **Nastavení proxy serveru**:

    |Název nastavení|Další informace|Použijte, když:|
    |-------------------|-------------------|-------------------|
    |**Nastavení proxy serveru pro toto připojení Wi-Fi**|Zvolte typ nastavení proxy serveru:<br /><br />-   **Žádný** (výchozí)<br />-   **Ruční** – ručně zadejte adresu URL a číslo portu proxy serveru.<br />-   **Automatické** – nakonfigurujte proxy server pomocí konfiguračního souboru.|Vždy|
    |**Adresa proxy serveru** a **číslo portu**|Zadejte adresu URL a číslo portu proxy serveru.|**Nastavení proxy serveru pro toto připojení Wi-Fi** je nastavené na **Ruční**|
    |**Adresa URL proxy serveru**|Zadejte adresu URL souboru, který obsahuje nastavení proxy serveru.|**Nastavení proxy serveru pro toto připojení Wi-Fi** je nastavené na **Automatické**|

### Krok 5: Uložení profilu Wi-Fi

1.  Po dokončení klikněte na **Uložit zásadu**.

Nová zásada se zobrazí v uzlu **Zásady konfigurace** pracovního prostoru **Zásady**.

### Krok 6: Nasazení profilu Wi-Fi

1.  Nasaďte profil Wi-Fi do jedné nebo víc skupin uživatelů nebo zařízení ve vaší organizaci.

Další informace o tom, jak nasazovat zásady, najdete v tématu [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

Souhrn stavu a upozornění v pracovním prostoru **Zásady** určují problémy se zásadami, které vyžadují vaši pozornost. Kromě toho se v pracovním prostoru **Řídicí panel** zobrazí shrnutí stavu.

Po úspěšném nasazení se zařízení uživatelů můžou automaticky připojit k podnikové bezdrátové síti, kterou jste nakonfigurovali.

## <a name="BKMK_Import"></a>Import konfiguračního profilu Wi-Fi (Windows 8.1 a vyšší)
Pomocí **Zásady importu Wi-Fi pro Windows** importujte sadu nastavení Wi-Fi, kterou pak můžete nasadit do požadovaných skupin uživatelů nebo zařízení.

> [!TIP]
> Ve Windows můžete pomocí nástroje **netsh wlan** exportovat stávající profil Wi-Fi do souboru XML, který může [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] přečíst.
> 
> Pokud budete chtít exportovat do souboru XML třeba připojení Wi-Fi s názvem **MojePripojeni**, napište na příkazové řádku Windows tento příkaz:
> 
> **netsh wlan export profile MyConnection**

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com) klikněte na **Zásady** &gt; **Přidat zásadu**.

2.  Nakonfigurujte zásady zadáním **Windows** &gt; **Zásady importu Wi-Fi pro Windows**.

    Vytvářet a nasazovat můžete jenom vlastní zásady importu Wi-Fi pro Windows. Doporučená nastavení nejsou dostupná.

    Další informace o tom, jak vytvářet a nasazovat zásady, najdete v tématu [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

3.  Zadejte následující obecné hodnoty pro nastavení Zásady importu Wi-Fi pro Windows:

    |Název nastavení|Další informace|
    |-------------------|-------------------|
    |**Název**|Zadejte jedinečný název profilu Wi-Fi, podle kterého ho poznáte v konzole služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].|
    |**Popis**|Zadejte popis profilu Wi-Fi a další důležité informace, které vám pomůžou ho najít.|

4.  Pod nadpisem **Vlastní profil Wi-Fi** zadejte následující hodnoty:

    |Název nastavení|Další informace|
    |-------------------|-------------------|
    |**Soubor konfiguračního profilu**|Klikněte na **Importovat** a vyberte soubor XML, který obsahuje nastavení profilu Wi-Fi, které chcete importovat do [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].|
    |**Vlastní název konfiguračního profilu (zobrazený uživatelům)**|Zobrazí název konfiguračního profil Wi-Fi tak, jak se bude zobrazovat uživatelům na jejich zařízení.|
    |**Podrobnosti konfiguračního profilu**|Zobrazí kód XML pro konfigurační profil, který jste vybrali.|

5.  Po dokončení klikněte na **Uložit zásadu**.

6.  Nová zásada se zobrazí v uzlu **Zásady konfigurace** pracovního prostoru **Zásady**.

Teď můžete pomocí informací v **kroku 6** nahoře nasadit vlastní profil Wi-Fi.

## Viz také
[Povolení přístupu k prostředkům společnosti se službou Microsoft Intune](../Topic/Enable_access_to_company_resources_with_Microsoft_Intune_-_deleted.md)

