---
description: na
keywords: na
title: Configure access to corporate email using email profiles with Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 10f0cd61-e514-4e44-b13e-aeb85a8e53ae
---
# Konfigurace př&#237;stupu k podnikov&#233;mu e-mailu pomoc&#237; e-mailov&#253;ch profilů v Microsoft Intune
E-mailové profily v [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] vám pomůžou vytvořit, nasadit a sledovat nastavení e-mailů Exchange ActiveSync na zařízeních. Díky tomu mají uživatelé na svých osobních zařízeních přístup k podnikovému e-mailu, bez nutnosti něco nastavovat.

E-mailové profily můžete použít ke konfiguraci následujících typů zařízení:

-   Zařízení s Windows Phone 8 nebo novějším

-   Zařízení se iOS 5 nebo novějším

-   Zařízení, na kterém běží Samsung KNOX Standard (4.0 nebo novější)

Kromě nakonfigurování e-mailového účtu na zařízení můžete taky nakonfigurovat nastavení synchronizace, jako třeba kolik e-mailů se má synchronizovat, a v závislosti na typu zařízení i typy synchronizovaného obsahu.

> [!IMPORTANT]
> Pokaždé, když je to možné, vyberte nejbezpečnější možnosti, které vaše e-mailová infrastruktura a klientské operační systémy můžou podporovat. Pomocí e-mailových profilů můžete pohodlně centrálně distribuovat a spravovat nastavení e-mailu, která už vaše zařízení podporuje. [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] nepřidává žádné další e-mailové funkce.

## Jak jsou e-mailové profily zabezpečené
E-mailové profily se dají zabezpečit jedním ze dvou způsobů:

### Certifikáty
Když vytváříte e-mailový profil, vybíráte profil certifikátu SCEP, který jste předtím vytvořili v [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Je známý jako certifikát identity a slouží k ověřování na základě důvěryhodného profilu certifikátu (neboli kořenového certifikátu), který jste vytvořili, aby se zařízení uživatele mohlo připojovat. Důvěryhodný certifikát je nasazený na počítači, který ověřuje e-mailové připojení, většinou na serveru Exchange.

Další informace o vytváření a používání profilů certifikátů v [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] najdete v části [Povolení přístupu k firemním prostředkům pomocí profilů certifikátů v Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md).

### Uživatelské jméno a heslo
Uživatel se ověřuje na serveru Exchange zadáním uživatelského jména a hesla.

Heslo není součástí e-mailového profilu, uživatel ho tedy musí zadat při připojování k e-mailu.

### Vytvoření e-mailového profilu

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com) klikněte na **Zásady** &gt; **Přidat zásadu**.

2.  Nakonfigurujte jeden z následujících typů zásad:

    -   **E-mailový profil pro standard Samsung KNOX (4.0 nebo novější)**

    -   **E-mailový profil (iOS 5 a novější)**

    -   **E-mailový profil (Windows Phone 8 a novější)**

    Můžete vytvořit a nasadit jenom vlastní zásadu e-mailového profilu. Doporučená nastavení nejsou dostupná.

    Další informace o tom, jak vytvářet a nasazovat zásady, najdete v tématu [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

3.  S konfigurací nastavení e-mailového profilu Samsung KNOX vám pomůže následující tabulka:

    |Název nastavení|Další informace|
    |-------------------|-------------------|
    |**Název**|Zadejte jedinečný název emailového profilu.|
    |**Popis**|Zadejte popis, který bude shrnovat účel e-mailového profilu, a uveďte jakékoliv další důležité informace, které vám pomůžou ho najít.|
    |**Hostitel**|Zadejte název hostitele vašeho podnikového Exchange Serveru, který hostuje služby Exchange ActiveSync.|
    |**Název účtu**|Zadejte zobrazovaný název e-mailového účtu tak, jak ho uvidí uživatelé na svých zařízeních.|
    |**Uživatelské jméno**|Vyberte způsob získání uživatelského jména pro e-mailový účet:<br /><br />-   Pokud máte místní server Exchange server, vyberte **Uživatelské jméno**.<br />-   V případě Office 365 vyberte **Hlavní název uživatele**|
    |**E-mailová adresa**|Vyberte způsob generování e-mailové adresy uživatele na každém zařízení:<br /><br />-   **Primární adresa SMTP:** Použije se primární adresa SMTP, kterou se uživatel přihlašuje k serveru Exchange.<br />-   **Hlavní název uživatele:** Jako e-mailová adresa se použije celý hlavní název uživatele.|
    |**Metoda ověření**|Vyberte metodu ověřování používanou pro e-mailový profil:<br /><br />-   **Uživatelské jméno a heslo**<br />-   **Certifikáty**|
    |**Vybrat klientský certifikát pro ověřování klientů (certifikát identity)**|Vyberte certifikát klienta SCEP, který jste dříve vytvořili a který se použije k ověření připojení Exchange. Další informace o používání profilů certifikátů v [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] najdete v části [Povolení přístupu k firemním prostředkům pomocí profilů certifikátů v Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md). **Note:** Tato možnost se zobrazí jenom v případě, že je metoda ověřování **Certifikáty**.|
    |**Použít S/MIME**|Posílá odchozí poštu s šifrováním S/MIME.|
    |**Podpisový certifikát**|Vyberte podpisový certifikát, který se bude používat k podepsání odchozích e-mailů. **Note:** Tato možnost se zobrazí jenom v případě, že jste vybrali **Použít S/MIME**.|
    |**Počet dnů, za které se mají e-maily synchronizovat**|Z rozevíracího seznamu vyberte počet dní, za které se mají e-maily synchronizovat, nebo vyberte **Neomezený**, pokud chcete synchronizovat všechny dostupné e-maily.|
    |**Plán synchronizace**|Vyberte plán, podle kterého budou zařízení synchronizovat data z Exchange Serveru. Můžete taky vybrat **Při doručování zpráv**, kdy se data synchronizují hned po doručení, nebo **Ruční**, kdy musí synchronizaci inicializovat uživatel zařízení.|
    |**Použít protokol SSL**|Při posílání a přijímání e-mailů a komunikaci se Exchange Serverem použijte komunikaci SSL (Secure Sockets Layer). **Note:** U zařízení, na kterých běží Samsung KNOX 4.0 nebo novější, musíte exportovat certifikát SSL Exchange Serveru a v [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] ho nasadit jako Profil důvěryhodného certifikátu Androidu. [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] nepodporuje přístup k tomuto certifikátu, pokud je na Exchange Server nainstalovaný jiným způsobem.|
    |**Typ obsahu, který se má synchronizovat**|Vyberte typy obsahu, které se mají na zařízeních synchronizovat. Vybírejte z těchto možností:<br /><br />-   **E-mail**<br />-   **Kontakty**<br />-   **Kalendář**<br />-   **Úkoly**<br />-   **Poznámky**|
    S konfigurací nastavení e-mailového profilu iOS vám pomůže následující tabulka:

    |Název nastavení|Další informace|
    |-------------------|-------------------|
    |**Název**|Zadejte jedinečný název emailového profilu.|
    |**Popis**|Zadejte popis, který bude shrnovat účel e-mailového profilu, a uveďte jakékoliv další důležité informace, které vám pomůžou ho najít.|
    |**Hostitel**|Zadejte název hostitele vašeho podnikového Exchange Serveru, který hostuje služby Exchange ActiveSync.|
    |**Název účtu**|Zadejte zobrazovaný název e-mailového účtu tak, jak ho uvidí uživatelé na svých zařízeních.|
    |**Uživatelské jméno**|Vyberte způsob generování uživatelského jména e-mailové adresy na každém zařízení. Z rozevíracího seznamu si můžete vybrat jednu z těchto možností:<br /><br />-   **Primární adresa SMTP:** Použije se primární adresa SMTP, kterou se uživatel přihlašuje k serveru Exchange.<br />-   **Hlavní název uživatele:** Použije se celý hlavní název, kterým se uživatel přihlašuje k serveru Exchange.|
    |**E-mailová adresa**|Vyberte způsob generování e-mailové adresy uživatele na každém zařízení. Z rozevíracího seznamu si můžete vybrat jednu z těchto možností:<br /><br />-   **Primární adresa SMTP:** Použije se primární adresa SMTP, kterou se uživatel přihlašuje k serveru Exchange.<br />-   **Hlavní název uživatele:** Jako e-mailová adresa se použije celý hlavní název uživatele.|
    |**Metoda ověření**|Vyberte metodu ověřování používanou pro e-mailový profil:<br /><br />-   **Uživatelské jméno a heslo**<br />-   **Certifikáty**|
    |**Vybrat klientský certifikát pro ověřování klientů (certifikát identity)**|Vyberte certifikát klienta SCEP, který jste dříve vytvořili a který se použije k ověření připojení Exchange. Další informace o používání profilů certifikátů v [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] najdete v části [Povolení přístupu k firemním prostředkům pomocí profilů certifikátů v Microsoft Intune](../Topic/Enable_access_to_company_resources_using_certificate_profiles_with_Microsoft_Intune.md). **Note:** Tato možnost se zobrazí jenom v případě, že je metoda ověřování **Certifikáty**.|
    |**Použít S/MIME**|Posílá odchozí poštu s šifrováním S/MIME.|
    |**Podpisový certifikát**|Volitelně vyberte podpisový certifikát, který se bude používat k podepsání odchozích e-mailů. **Note:** Tato možnost se zobrazí jenom v případě, že jste vybrali **Použít S/MIME**.|
    |**Počet dnů, za které se mají e-maily synchronizovat**|Z rozevíracího seznamu vyberte počet dní, za které se mají e-maily synchronizovat, nebo vyberte **Neomezený**, pokud chcete synchronizovat všechny dostupné e-maily.|
    |**Použít protokol SSL**|Při posílání a přijímání e-mailů a komunikaci se Exchange Serverem použijte komunikaci SSL (Secure Sockets Layer).|
    |**Povolit přesunování zpráv na jiné e-mailové účty**|Povolí uživatelům přesunovat e-mailové zprávy mezi různými účty, které si na svých zařízeních nakonfigurovali.|
    |**Povolit odesílání e-mailů z aplikací třetí strany**|Povolí uživatelům posílat e-maily z jiných aplikací, než je výchozí e-mailová aplikace.|
    |**Synchronizovat naposledy použité e-mailové adresy**|Povolí synchronizaci seznamu e-mailových adres, které se na zařízení naposledy používaly.|
    S konfigurací nastavení e-mailového profilu Windows Phonu vám pomůže následující tabulka:

    |Název nastavení|Další informace|
    |-------------------|-------------------|
    |**Název**|Zadejte jedinečný název emailového profilu.|
    |**Popis**|Zadejte popis, který bude shrnovat účel e-mailového profilu, a uveďte jakékoliv další důležité informace, které vám pomůžou ho najít.|
    |**Hostitel**|Zadejte název hostitele vašeho podnikového Exchange Serveru, který hostuje služby Exchange ActiveSync.|
    |**Název účtu**|Zadejte zobrazovaný název e-mailového účtu tak, jak ho uvidí uživatelé na svých zařízeních.|
    |**Uživatelské jméno**|Vyberte způsob generování uživatelského jména e-mailové adresy na každém zařízení. Z rozevíracího seznamu si můžete vybrat jednu z těchto možností:<br /><br />-   **Primární adresa SMTP:** Použije se primární adresa SMTP, kterou se uživatel přihlašuje k serveru Exchange.<br />-   **Hlavní název uživatele:** Použije se celý hlavní název, kterým se uživatel přihlašuje k serveru Exchange.|
    |**E-mailová adresa**|Vyberte způsob generování e-mailové adresy uživatele na každém klientském počítači. Z rozevíracího seznamu si můžete vybrat jednu z těchto možností:<br /><br />-   **Primární adresa SMTP:** Použije se primární adresa SMTP, kterou se uživatel přihlašuje k serveru Exchange.<br />-   **Hlavní název uživatele:** Jako e-mailová adresa se použije celý hlavní název uživatele.|
    |**Počet dnů, za které se mají e-maily synchronizovat**|Z rozevíracího seznamu vyberte počet dní, za které se mají e-maily synchronizovat, nebo vyberte **Neomezený**, pokud chcete synchronizovat všechny dostupné e-maily.|
    |**Plán synchronizace**|Vyberte plán, podle kterého budou zařízení synchronizovat data z Exchange Serveru. Můžete taky vybrat **Při doručování zpráv**, kdy se data synchronizují hned po doručení, nebo **Ruční**, kdy musí synchronizaci inicializovat uživatel zařízení.|
    |**Použít protokol SSL**|Při posílání a přijímání e-mailů a komunikaci se Exchange Serverem použijte komunikaci SSL (Secure Sockets Layer).|
    |**Typ obsahu, který se má synchronizovat**|Vyberte typy obsahu, které se mají na zařízeních synchronizovat. Vybírejte z těchto možností:<br /><br />-   **E-mail**<br />-   **Kontakty**<br />-   **Kalendář**<br />-   **Úkoly**|
    > [!IMPORTANT]
    > Pokud jste nasadili e-mailový profil a pak chcete změnit hodnoty pro **hostitele Exchange ActiveSync** nebo **e-mailovou adresu**, je potřeba odstranit stávající e-mailový profil a vytvořit nový s požadovanými hodnotami.

4.  Po dokončení klikněte na **Uložit zásadu**.

Nová zásada se zobrazí v uzlu **Zásady konfigurace** pracovního prostoru **Zásady**.

### Nasazení e-mailového profilu

1.  Nasaďte e-mailový profil do jedné nebo víc skupin uživatelů nebo zařízení ve vaší organizaci.

Další informace o tom, jak nasazovat zásady, najdete v tématu [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

Shrnutí stavu a upozornění na stránce **Přehled** v pracovním prostoru **Zásady** identifikují problémy se zásadami, které vyžadují vaši pozornost. Kromě toho se v pracovním prostoru **Řídicí panel** zobrazí shrnutí stavu.

> [!NOTE]
> Pokud byste chtěli e-mailový profil ze zařízení odebrat, upravte nasazení a odeberte všechny skupiny, ve kterých je zařízení členem.

## Další kroky
Po úspěšném nasazení se na zařízeních uživatelů zřídí správná nastavení pro přístup k podnikovému e-mailu.

## Viz také
[Povolení přístupu k prostředkům společnosti se službou Microsoft Intune](../Topic/Enable_access_to_company_resources_with_Microsoft_Intune_-_deleted.md)

