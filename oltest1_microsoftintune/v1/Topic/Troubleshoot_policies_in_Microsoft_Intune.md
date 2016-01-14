---
description: na
keywords: na
title: Troubleshoot policies in Microsoft Intune
search: na
ms.date: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 99fb6db6-21c5-46cd-980d-50f063ab8ab8
---
# Řešen&#237; pot&#237;ž&#237; se z&#225;sadami v Microsoft Intune

## problémy se zásadami;
Tady jsou některé problémy, které může způsobit vaše konfigurace zásad služby [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)], a jejich doporučená řešení.

### Používají se v zařízení zásady?
**Problém:** Není jasné, jestli se v určitém zařízení používá určitá zásada, nebo jestli se zařízení chová v rozporu s touto zásadou.

Zkontrolujte informace o zásadách dostupné pro jednotlivá zařízení, abyste zjistili, jak určitá zásada ovlivňuje konkrétní zařízení.

V konzole pro správu služby Intune má každé zařízení v části **Vlastnosti zařízení** vlastní kartu zásad. Pokud ne, u zařízení možná ještě probíhá registrace nebo se v něm nepoužívají žádné zásady. Každá zásada má **určenou hodnotu** a **Stav**. Určená hodnota označuje to, čeho chcete dosáhnout při přiřazování zásady. Stav označuje to, čeho skutečně dosáhnete, když jsou společně zvažovány všechny zásady, které u zařízení použijete, a všechna omezení a požadavky na hardware a operační systém. Možné stavy:

-   **Vyhovuje**: Zařízení přijalo zásady a hlásí službě, že vyhovuje danému nastavení.

-   **Nepoužívá se**: Nastavení zásad se nedá použít. Například nastavení e-mailu pro zařízení se systémem iOS se nedají použít pro zařízení se systémem Android.

-   **Čeká na vyřízení**: Došlo k odeslání zásady do zařízení a to ještě nenahlásilo službě svůj stav. Na vyřízení může čekat třeba šifrování v systému Android, které vyžaduje, aby šifrování povolil koncový uživatel.

Na tomto snímku obrazovky vidíte dva jasné příklady:

-   Možnost **Povolit jednoduchá hesla** je nastavená na **Ano**, jak ukazuje sloupec **Určená hodnota**, ale její **Stav** je **Nepoužívá se**. Důvodem je, že se na zařízeních s Androidem nepodporují jednoduchá hesla.

-   Podobně pak u tohoto zařízení není použitá rozšířená položka zásad **Nastavení e-mailu pro zařízení iOS**, protože to je zařízení s Androidem.

![](../Image/Intune_Device_Policy_v.2.jpg)

> [!NOTE]
> Mějte na paměti, že když použijete dvě zásady s různými úrovněmi omezení na stejné zařízení nebo uživatele, v praxi se uplatní víc omezující zásada.

### Chyba 0x87D1FDE8 v zařízení KNOX
**Problém**: Po vytvoření a nasazení e-mailového profilu Exchange Active Sync pro platformu Samsung KNOX do různých zařízení se systémem Android hlásí zařízení na kartě Vlastnosti &gt; Zásady chybu **0x87D1FDE8** nebo **Náprava se nezdařila**.

Zkontrolujte konfiguraci svého profilu EAS pro zařízení Samsung KNOX a zdroj zásad. Už není dostupná podpora možnosti synchronizace poznámek Samsung a ve vašem profilu by tato možnost neměla být vybraná. Dopřejte zařízením dostatek času na zpracování zásady, a to až 24 hodin.

### Výstraha: Uložení pravidel přístupu do systému Exchange se nezdařilo
**Problém**: V konzole pro správu se objeví výstraha **Uložení pravidel přístupu do systému Exchange se nezdařilo**.

Pokud jste vytvořili zásady v pracovním prostoru Zásady pro místní Exchange v konzole pro správu, ale používáte služby O365, služba Intune nebude nakonfigurované nastavení zásad vynucovat. Poznamenejte si zdroj zásad uvedený ve výstraze.  V pracovním prostoru Zásady pro místní Exchange odstraňte zastaralá pravidla, protože se jedná o globální pravidla Exchange v rámci Intune pro místní Exchange a nevztahují se na služby O365. Pak vytvořte nové zásady pro služby O365.

## Nelze změnit zásady zabezpečení pro různá zařízení MDM
Zařízení se systémy Windows Phone a Windows RT neumožňují snížení zásad zabezpečení nastavených prostřednictvím MDM nebo EAS, jakmile je nastavíte. Nastavíte třeba **Minimální počet znaků hesla** na hodnotu 8 a tu se pak pokusíte snížit na 4. V zařízení se už ale používá více omezující zásada.

Pokud chcete zásadu změnit na méně zabezpečenou hodnotu, v závislosti na platformě zařízení může být potřeba resetovat zásady zabezpečení. Třeba v systému Windows RT potáhněte na ploše prstem zprava. Otevře se panel **Ovládací tlačítka** a v něm klikněte na **Nastavení** &gt; **Ovládací panely**.  Vyberte aplet **Uživatelské účty**. V navigační nabídce vlevo najdete dole odkaz **Resetovat zásady zabezpečení**. Klikněte na něj a potom klikněte na tlačítko **Resetovat zásady**. Jiná zařízení MDM, třeba zařízení se systémy Android, Windows Phone 8.1 (a novějšími) a iOS, může být potřeba vyřadit a znovu zaregistrovat do služby, abyste mohli použít méně omezující zásadu.

## Zařízení se systémem Android nevynucují změny zásad zabezpečení bez přijetí koncovým uživatelem
Zařízení MDM se systémem Android na rozdíl od ostatních platforem nepovolují službě vynucovat v zařízení počáteční změny zásad. Důvodem jsou funkce systému Android, ne služba Intune. Zařízení se systémem Android zobrazí koncovému uživateli okno s upozorněním na výzvu týkající se dané změny zásad (třeba heslo, šifrování atd.).  Koncový uživatel musí na výzvu odpovědět, a až ji přijme, měla by se zásada použít.

## Viz také
[Řešení potíží s aktualizacemi softwaru ve službě Microsoft Intune](../Topic/Troubleshoot_software_updates_in_Microsoft_Intune.md)

