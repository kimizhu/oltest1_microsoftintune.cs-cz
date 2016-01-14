---
description: na
keywords: na
title: Release notes for Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: db9479b2-582d-4a1a-9fbc-fbfc6c680e6f
---
# Pozn&#225;mky k verzi Microsoft Intune
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] je integrované cloudové řešení pro správu klienta, které poskytuje nástroje, sestavy a licence na upgrade na nejnovější verzi Windows a pomáhá udržovat počítač aktualizovaný a zabezpečený. Kromě toho [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] umožňuje spravovat mobilní zařízení v síti, a to buď prostřednictvím protokolu Exchange ActiveSync, nebo přímo přes [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Následující poznámky k verzi popisují důležité informace a známé problémy ve [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)].

-   [Instalace, nasazení a registrace](../Topic/Release_notes_for_Microsoft_Intune.md#BKMK_WitRelnoteInstall)

-   [Výstrahy](../Topic/Release_notes_for_Microsoft_Intune.md#BKMK_WitRelnoteAlerts)

## <a name="BKMK_WitRelnoteInstall"></a>Instalace, nasazení a registrace
Následující problémy se můžou objevit během nasazení softwaru klienta, přípravy zařízení klienta na [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] nebo registraci zařízení.

### Při registraci zařízení se systémem Windows 8.1, které se musí ověřit na proxy serveru, proces registrace selže, aniž by se ukázala jakákoli příčina selhání.
**Problém:** Když registrujete zařízení [!INCLUDE[winblue_client_2](../Token/winblue_client_2_md.md)], které se musí během procesu registrace ověřit na proxy serveru, tak v případě, že toto zařízení nemá v mezipaměti uložené přihlašovací údaje proxy serveru, registrace selže. Pokud přihlašovací údaje k proxy serveru nejsou uložené v mezipaměti zařízení, musí proces registrace čekat, až tyto přihlašovací údaje uživatel zadá. Výzva k zadání přihlašovacích údajů k proxy serveru se ale během procesu registrace nezobrazí. Výsledkem je, že proces registrace nemůže ověřit proxy server, ale uživateli se žádná informace o tomto selhání nezobrazí.

**Alternativní řešení:** U zařízení [!INCLUDE[winblue_client_2](../Token/winblue_client_2_md.md)], která se musí registrovat v síti vyžadující použití ověřeného proxy serveru, nakonfigurujte a uložte přihlašovací údaje k proxy serveru ještě před jejich registrací. Konfigurace a uložení přihlašovacích údajů na zařízení [!INCLUDE[winblue_client_2](../Token/winblue_client_2_md.md)]:

1.  Na zařízení [!INCLUDE[winblue_client_2](../Token/winblue_client_2_md.md)] otevřete **Internet Explorer**.

2.  Když se zobrazí výzva k zadání přihlašovacích údajů k proxy serveru, zadejte přihlašovací údaje a potom vyberte možnost **Zapamatovat pověření**.

3.  Registrace zařízení

### Zařízení se systémem Windows Phone 8.1 nejde zaregistrovat do Microsoft Intune, pokud je ve službě AD FS povolené ověřování zařízení.
**Problém:** Při registraci zařízení Windows Phone 8.1 registrace selže, pokud je povolené volitelné nastavení pro ověřování zařízení v rámci globální zásady ověřování ve službě Active Directory Federated Services (AD FS).

**Alternativní řešení:** Zakažte ověřování zařízení na serveru služby AD FS zrušením zaškrtnutí políčka **Povolit ověřování zařízení** v nastavení **Upravit globální zásady ověřování**. Další informace najdete v tématu [Konfigurace zásad ověřování](http://technet.microsoft.com/library/dn486781.aspx).

### Konfigurace nastavení Povolit obsah pro dospělé v obchodě s médii může mít vliv na způsob zobrazení nastavení zařízení.
**Problém:** Pokud má zásada mobilního zařízení nakonfigurované nastavení **Povolit obsah pro dospělé v obchodě s médii** a používá se pro zařízení se systémem iOS 5 nebo iOS 6, může se stav všech nastavení pro toto zařízení zobrazit jako **Vyhovuje**.

**Alternativní řešení:** Pokud chcete zobrazit správný stav nastavení zařízení, odeberte ze zásady nastavení **Povolit obsah pro dospělé v obchodě s médii** a znovu zásadu použijte.

### Při přidání zásad nebo aplikací do skupin Microsoft Intune zařízení, která jsou členy skupiny Neseskupená zařízení, tyto zásady nebo aplikace neobdrží.
**Problém:** [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] nepoužije správně zásady a aplikace na zařízení, které zůstává ve skupině **Neseskupená zařízení**. K tomu dojde i v případě, že je zásada nebo aplikace zadaná u jiné skupiny než **Neseskupená zařízení**. U tohoto problému se nezobrazují žádné chyby.

**Alternativní řešení:** Odeberte zařízení ze skupiny **Neseskupená zařízení** a ověřte, jestli tato zařízení zůstala aspoň v jedné další skupině, která zásady a aplikace obdrží.

### Nástroj Microsoft Intune App Wrapping Tool pro Android nemá žádnou integrovanou možnost odinstalace.
**Problém:** Nástroj **Microsoft App Wrapping Tool for Android** nemá vestavěnou funkci odinstalace.

**Alternativní řešení:** Přejděte do umístění, kam jste nástroj nainstalovali, a adresář odstraňte. Výchozí instalační umístění: **C:\Program Files (x86)\Microsoft Intune Mobile Application Management\Android\App Wrapping Tool**. Další informace o nástroji pro zabalení aplikace najdete v tématu [Příprava aplikací pro Android na správu mobilních aplikací](http://technet.microsoft.com/library/mt147413.aspx).

## <a name="BKMK_WitRelnoteAlerts"></a>Výstrahy
Následující seznam uvádí známé problémy s výstrahami v této verzi [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

### Vzdálená pomoc není dostupná na počítačích se systémem Windows 8 nebo Windows 8.1.
**Problém:** V této verzi není na počítačích se systémem Windows 8 nebo Windows 8.1 dostupná funkce Vzdálená pomoc.

**Alternativní řešení:** Žádné.

### Oznámení výstrah pro příjemce, kteří jsou přidaní automaticky, nemusí fungovat.
**Problém:** Pokud je příjemce k oznámení výstrahy přidaný automaticky, nemusí vždycky dostat oznámení.

**Alternativní řešení:** Pokud chcete mít jistotu, že příjemci dostanou oznámení, měli byste tyto příjemce k oznámením výstrah přidat ručně.

## Viz také
[Technické reference pro Microsoft Intune](../Topic/Technical_reference_for_Microsoft_Intune.md)

