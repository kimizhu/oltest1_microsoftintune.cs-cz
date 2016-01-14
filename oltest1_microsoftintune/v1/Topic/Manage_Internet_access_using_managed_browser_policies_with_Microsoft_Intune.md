---
description: na
keywords: na
title: Manage Internet access using managed browser policies with Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dc946303-e09b-4d73-8bf4-87742299bc54
---
# Spr&#225;va př&#237;stupu k internetu pomoc&#237; z&#225;sad spravovan&#233; prohl&#237;žeče v Microsoft Intune
Spravovaný prohlížeč je aplikace procházení webu, kterou můžete nasadit v organizaci pomocí [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]. Zásady spravovaného prohlížeče konfigurují seznam povolených nebo blokovaných webů. Tyto seznamy omezují weby, které můžou uživatelé spravovaného prohlížeče navštívit.

Vzhledem k tomu, že je tato aplikace spravovaná, můžete u ní použít taky zásady správy mobilních aplikací, jako je třeba řízení použití operací vyjmutí, kopírování a vložení, prevence pořizování snímků obrazovky nebo taky zajištění, že když uživatel klikne na odkaz, otevře se obsah v určených spravovaných aplikacích. Podrobnosti najdete v tématu [Ochrana dat pomocí zásad správy mobilních aplikací v Microsoft Intune](../Topic/Configure_and_deploy_mobile_application_management_policies_in_the_Microsoft_Intune_console.md).

> [!IMPORTANT]
> Pokud uživatelé nainstalují spravovaný prohlížeč sami, nebude spravovaný žádnými zásadami, které definujete. Aby se zajistilo, že bude prohlížeč spravovat služba Intune, musí uživatelé aplikaci nejdřív odinstalovat a potom jim tuto aplikaci můžete nasadit jako spravovanou aplikaci.

Zásady spravovaného prohlížeče můžete vytvořit pro následující typy zařízení:

-   Zařízení se systémem Android 4 nebo novější verzí

-   Zařízení se systémem iOS 7 nebo novější verzí

## Vytvoření zásady spravovaného prohlížeče

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com) klikněte na **Zásady** &gt; **Přidat zásadu**.

2.  Nakonfigurujte jeden z následujících typů zásad pro **Software**:

    -   **Zásady spravovaného prohlížeče (Android 4 a novější)**

    -   **Zásady spravovaného prohlížeče (iOS 7 a novější)**

    Další informace o tom, jak vytvářet a nasazovat zásady, najdete v tématu [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

3.  S konfigurací nastavení zásad spravovaného prohlížeče vám pomůže následující tabulka:

    |Název nastavení|Další informace|
    |-------------------|-------------------|
    |**Název**|Zadejte jedinečný název zásady spravovaného prohlížeče, abyste ji mohli v konzole [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] snadno identifikovat.|
    |**Popis**|Zadejte popis, který bude shrnovat účel zásady spravovaného prohlížeče, a uveďte jakékoli další důležité informace, které vám pomůžou zásadu najít.|
    |**Povolte seznamu povolených nebo blokovaných webů omezovat adresy URL, které půjdou ve spravovaném prohlížeči otevřít.**|Vyberte jednu z následujících možností:<br /><br />-   **Povolit spravovanému prohlížeči otevřít jenom dole uvedené adresy URL** – určí seznam adres URL, které se dají ve spravovaném prohlížeči otevřít.<br />-   **Blokovat otevření dole uvedených adres URL ve spravovaném prohlížeči** – určí seznam adres URL, které nepůjdou ve spravovaném prohlížeči otevřít z důvodu blokování. **Note:** Do jedné zásady spravovaného prohlížeče nemůžete zahrnout seznam povolených i blokovaných adres URL.<br />Další informace o formátech adres URL, které se dají určit, najdete v části [Formát adresy URL pro povolené a blokované adresy URL](../Topic/Manage_Internet_access_using_managed_browser_policies_with_Microsoft_Intune.md#BKMK_URLs) v tomto tématu.|

4.  Po dokončení klikněte na **Uložit zásadu**.

Nová zásada se zobrazí v uzlu **Zásady konfigurace** pracovního prostoru **Zásady**.

## Vytvoření nasazení softwaru pro aplikaci spravovaného prohlížeče
Po vytvoření zásady spravovaného prohlížeče můžete vytvořit nasazení softwaru pro aplikaci spravovaného prohlížeče a přidružit ho k zásadě spravovaného prohlížeče, kterou jste vytvořili.

> [!IMPORTANT]
> Zásady spravovaného prohlížeče se nenasazují stejným způsobem jako ostatní zásady [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Tento typ zásad musí být přidružený k softwarovému balíčku spravovaného prohlížeče.

Nasaďte aplikaci a na stránce **Správa mobilních aplikací** vyberte zásadu spravovaného prohlížeče, kterou chcete k aplikaci přidružit.

Další informace o tom, jak nasazovat aplikace, najdete v tématu [Nasazení aplikací do mobilních zařízení v Microsoft Intune](../Topic/Deploy_apps_to_mobile_devices_in_Microsoft_Intune_-_deleted.md).

## Zabezpečení a ochrana osobních údajů pro spravovaný prohlížeč

-   V zařízeních se systémem iOS se nedají otevřít weby, u kterých vypršela platnost certifikátu nebo které mají nedůvěryhodný certifikát.

-   Nastavení, která uživatelé vytvoří pro prohlížeče integrované na jejich zařízeních, spravovaný prohlížeč používat nebude. Důvodem je to, že spravovaný prohlížeč nemá k těmto nastavením přístup.

-   Pokud v zásadě správy mobilních aplikací přidružené ke spravovanému prohlížeči nakonfigurujete možnost **Požadovat pro přístup jednoduchý kód PIN** nebo **Požadovat pro přístup podnikové přihlašovací údaje** a uživatel klikne na stránce ověřování na odkaz nápovědy, bude moct na internetu přejít na libovolný web, i když bude tento web uvedený v zásadě spravovaného prohlížeče v seznamu blokovaných webů.

-   Spravovaný prohlížeč může blokovat přístup k webům jenom v případě, že se k nim přistupuje přímo. V případě, že se k webu přistupuje přes zprostředkující služby (třeba překladatelské služby), přístup blokovat nemůže.

-   Kvůli povolení ověřování adresa **&#42;.microsoft.com** nefiguruje v nastavených seznamech povolených a blokovaných webů a je vždycky povolená.

## Referenční informace

### <a name="BKMK_URLs"></a>Formát adresy URL pro povolené a blokované adresy URL
V následující části najdete informace o povolených formátech a zástupných znacích, které můžete použít při zadávání adres URL do seznamů povolených a blokovaných webů.

-   V souladu s pravidly uvedenými dole v seznamu povolených vzorů můžete použít zástupný znak **&#42;**.

-   Při zadávání adres URL do seznamu nezapomeňte u všech uvést předponu **http** nebo **https**.

-   V adrese můžete specifikovat čísla portů. Pokud nezadáte číslo portu, použijí se tyto hodnoty:

    -   Port 80 pro protokol HTTP

    -   Port 443 pro protokol HTTPS

    Použití zástupných znaků pro čísla portů se nepodporuje – třeba **http://www.contoso.com:&#42;** nebo **http://www.contoso.com: /&#42;**

-   Informace o povolených vzorech, které můžete použít při zadávání adres URL, najdete v následující tabulce:

    |Adresa URL|Popis|Odpovídá|Neodpovídá|
    |--------------|---------|------------|--------------|
    |http://www.contoso.com|Odpovídá jediné stránce|www.contoso.com|host.contoso.com<br /><br />www.contoso.com/images<br /><br />contoso.com/|
    |http://contoso.com|Odpovídá jediné stránce|contoso.com/|host.contoso.com<br /><br />www.contoso.com/images<br /><br />www.contoso.com|
    |http://www.contoso.com/&#42;|Odpovídá všem adresám URL začínajícím na www.contoso.com|www.contoso.com<br /><br />www.contoso.com/images<br /><br />www.contoso.com/videos/tvshows|host.contoso.com<br /><br />host.contoso.com/images|
    |http://&#42;.contoso.com/&#42;|Odpovídá všem dílčím doménám domény contoso.com|developer.contoso.com/resources<br /><br />news.contoso.com/images<br /><br />news.contoso.com/videos|contoso.host.com|
    |http://www.contoso.com/images|Odpovídá jediné složce|www.contoso.com/images|www.contoso.com/images/dogs|
    |http://www.contoso.com:80|Odpovídá jediné stránce používající číslo portu|http://www.contoso.com:80||
    |https://www.contoso.com|Odpovídá jediné zabezpečené stránce|https://www.contoso.com|http://www.contoso.com|
    |http://www.contoso.com/images/&#42;|Odpovídá jediné složce a všem podsložkám|www.contoso.com/images/dogs<br /><br />www.contoso.com/images/cats|www.contoso.com/videos|

-   Tady jsou uvedené příklady některých vstupních hodnot, které můžete zadat:

    -   &#42;.com

    -   &#42;.contoso/&#42;

    -   www.contoso.com/&#42;images

    -   www.contoso.com/&#42;images&#42;pigs

    -   www.contoso.com/page&#42;

    -   IP adresy

    -   https://&#42;

    -   http://&#42;

    -   http://www.contoso.com:&#42;

    -   http://www.contoso.com: /&#42;

### Řešení konfliktů mezi seznamy povolených a blokovaných webů
Pokud je na zařízení nasazených víc zásad spravovaného prohlížeče a dojde ke konfliktu nastavení, vyhodnotí se konflikty obou režimů (povoleného i blokovaného) a konflikty seznamů adres URL. V případě konfliktu platí následující pravidlo:

-   Pokud je u obou zásad stejný režim, ale liší se seznamy adres URL, příslušné adresy URL se na zařízení neuplatní.

-   Pokud má každá zásada jiný režim, ale seznamy adres URL jsou stejné, příslušné adresy URL se na zařízení neuplatní.

-   Pokud zařízení obdrží zásady spravovaného prohlížeče poprvé a dojde ke konfliktu dvou zásad, příslušné adresy URL se na zařízení neuplatní. K zobrazení konfliktů použijte uzel **Konflikty zásad** pracovního prostoru **Zásady**.

-   Pokud už zařízení zásady spravovaného prohlížeče obdrželo a nasazuje se druhá zásada s konfliktním nastavením, zůstanou na zařízení původní nastavení. K zobrazení konfliktů použijte uzel **Konflikty zásad** pracovního prostoru **Zásady**.

## Viz také
[Povolení přístupu k prostředkům společnosti se službou Microsoft Intune](../Topic/Enable_access_to_company_resources_with_Microsoft_Intune_-_deleted.md)

