---
description: na
keywords: na
title: Fix issues with mobile device enrollment
search: na
ms.date: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7e5979ab-fc4c-4c7b-a60c-15317496dfa2
robots: noindex,nofollow
---
# Fix issues with mobile device enrollment
Pokud máte problémy s mobilním zařízením, můžete odeslat protokoly správci IT, který vám pak podle nich může pomoct s vyřešením vašich problémů.

## Pokud máte zařízení s Androidem
Protokoly, které pošlete, nebudou zahrnovat žádné vaše osobní údaje, pokud nepovolíte tzv. podrobné protokolování. Protokoly pak budou obsahovat vaši e-mailovou adresu, ale žádné jiné osobní údaje v nich nebudou. Protokoly můžete odeslat jedním z následujících způsobů.

> [!IMPORTANT]
> Standardně je v zařízení povolené podrobné protokolování. Pokud podrobné protokolování na zařízení povolíte, protokoly, které od tohoto okamžiku odešlete, budou obsahovat vaši e-mailovou adresu, dokud podrobné protokolování nezakážete.

### Android – možnost 1

1.  Otevřete aplikaci Portál společnosti.

2.  Klepněte na **Nabídka**. V závislosti na zařízení s Androidem to může být buď softwarové, nebo hardwarové tlačítko.

3.  V **Nabídce** klepněte na **Nastavení** &gt; **Odesílat data**.

Vyzve vás to ke zvolení e-mailové aplikace. Aplikace vytvoří předem adresovaný e-mail, ve kterém už budou jako přílohy připojené všechny nezbytné protokoly.

### Android – možnost 2
Pokud při pokusu o registraci zařízení v Intune dojde k chybě, můžete to zkusit znovu klepnutím na **Opakovat** nebo poslat informace o chybě e-mailem správci IT klepnutím na **Poslat informace**. Automaticky se vytvoří e-mail adresovaný vašemu správci IT obsahující protokoly, které správce potřebuje k tomu, aby vám mohl pomoct řešit problémy s vaším zařízením.

### Android – možnost 3

1.  Připojte zařízení k počítači pomocí kabelu USB.

2.  V počítači vyhledejte adresář, který má název vašeho telefonu. V tomto adresáři najděte: &lt;Zařízení s Androidem&gt;\Phone\Android\data\com.microsoft.windowsintune.companyportal\files\.

3.  Všechny soubory připojte k e-mailu a pošlete je IT oddělení.

(**Poznámka pro správce:** Dejte koncovým uživatelům svoji e-mailovou adresu.)

## Pokud máte zařízení Windows Phone 8.1

1.  Nainstalujte z [Windows Phone Storu](http://www.windowsphone.com/en-us/store/app/field-medic/73c58570-d5a7-46f8-b1b2-2a90024fc29c) aplikaci Field Medic.

2.  Otevřete aplikaci Field Medic a klepněte na **Advanced** (Upřesnit).

3.  V části **Categories** (Kategorie) zkontrolujte, že je povolená možnost **Enterprise**.

4.  Pomocí tlačítka Zpět se vraťte na domovskou stránku Field Medic a klepněte na **Start Logging** (Spustit protokolování).

5.  Otevřete nastavení telefonu a klepněte na **Pracoviště** a pak klepněte na **Zaregistrováno**.

6.  Na nové obrazovce klikněte třikrát na **synchronizační** tlačítko.

7.  Přejděte zpět do aplikace Field Medic a klepněte na **Stop Logging** (Ukončit protokolování). Pojmenujte protokol a pak klepněte na ikonu **Uložit**.

8.  Pak pomocí kabelu USB připojte telefon k počítači. V počítači otevřete Průzkumníka souborů a otevřete položky **&lt; Název telefonu &gt;** &gt; **Telefon** &gt; **Dokumenty** &gt; **FieldMedic** &gt; **sestavy**.

9. Vyberte nejnovější složku, zkopírujte ji a připojte ji k e-mailu adresovanému vašemu správci IT. Složky jsou číslované ve formátu WPB_000_rrrrmmdd_xxxxx.

(Poznámka pro správce: Pokud dáváte přednost nějakému konkrétnímu způsobu sdílení této složky, například kopírování na OneDrive, popište ho tady).

## Pokud máte zařízení s iOS

1.  Otevřete aplikaci Portál společnosti.

2.  Zatřeste zařízením a v místní nabídce diagnostiky zvolte **E-mail**. Otevře se nový e-mail s připojenými protokoly. Odešlete tento e-mail IT oddělení.

> [!TIP]
> Pokud zařízení na zatřesení nereaguje, otevřete **Nastavení** &gt; **Portál společnosti** a zkontrolujte, že je zapnutá možnost **Gesto zatřesením**.

