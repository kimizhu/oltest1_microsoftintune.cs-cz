---
description: na
keywords: na
title: Protect Windows devices with multi-factor authentication
search: na
ms.date: na
ms.prod: configuration-manager
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9b4f197d-bc10-4bee-91c9-19bcc8287d36
---
# Ochrana zař&#237;zen&#237; s Windows pomoc&#237; v&#237;cefaktorov&#233;ho ověřov&#225;n&#237; ve službě Microsoft Intune
[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] zahrnuje vícefaktorové ověřování (MFA), které umožňuje lépe zabezpečit podnikové prostředky tím, že vyžaduje od uživatelů další ověření nad rámec uživatelských jmen a hesel (třeba pomocí telefonátu nebo textové zprávy).[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] podporuje použití vícefaktorového ověřování během registrace zařízení se systémem Windows 8.1 nebo novějším, Windows Phone 8.1 nebo Windows 10 Mobile (a na server ADFS se dá požadavek na vícefaktorové ověřování přiřadit jednotlivým uživatelům nebo skupinám). Pokud má vaše organizace místní infrastrukturu IT, která zahrnuje doménu Active Directory s nakonfigurovanou službou Active Directory Federation Services (ADFS), můžete nakonfigurovat MFA na federačním serveru a potom povolit přihlašování pomocí MFA na [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Když vícefaktorové ověřování nakonfigurujete na federačním serveru, ale nepovolíte přihlašování pomocí tohoto ověřování na [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], budou uživatelé muset toto přihlašování používat při každém přístupu k podnikovým prostředkům.

Můžete taky použít službu AAD MFA, která bude požadovat vícefaktorové ověřování při každém přístupu uživatele k podnikovým prostředkům. Tento požadavek se dá nastavit pro jednotlivé uživatele zvlášť. AAD MFA je cloudová služba, která nevyžaduje žádnou místní infrastrukturu IT. Pokud se chcete dozvědět, jak službu AAD MFA nastavit, přečtěte si téma [Přidání služby Multi-Factor Authentication do Azure Active Directory Directory.](http://technet.microsoft.com/library/dn249466.aspx)

## <a name="Reqs_MFA"></a>Požadavky místní infrastruktury na ADFS MFA
Pro nastavení vícefaktorového ověřování potřebujete:

-   **Doménu služby Active Directory, ke které je připojený server ADFS.**

-   **Server služby Active Directory Federation Services (ADFS) nakonfigurovaný pro MFA.** Server se systémem Windows Server 2012 R2 nastavený jako server ADFS. Další informace najdete v tomto článku: [Použití vícefaktorového ověřování se službou Windows Server 2012 R2 AD FS](http://msdn.microsoft.com/library/azure/dn807157.aspx).

Všechny výš uvedené servery musí splňovat požadavky na systém, které najdete v části [Požadavky na systém a informace o instalaci pro Windows Server 2012 R2](http://technet.microsoft.com/library/dn303418.aspx).

## Vyžadování vícefaktorového ověřování služby ADFS při registraci zařízení se systémem Windows
Informace o tom, jak zapnout MFA v ADFS najdete v tématu [Přehled řízení rizik pomocí dodatečného vícefaktorového ověřování citlivých aplikací](http://technet.microsoft.com/library/dn280949.aspx).

#### Vyžadování vícefaktorového ověřování při registraci v konzole pro správu služby Intune

1.  V konzole pro správu Intune klikněte na **Správce** &gt; **Správa mobilních zařízení** &gt; **Vícefaktorové ověřování**.

2.  Než budete vícefaktorové ověřování vyžadovat pro registraci zařízení s Windows do služby Intune, povolte vícefaktorové ověřování v klientovi služby Azure AD nebo místním prostředí. Pokud to neuděláte, uživatelům se při pokusu o registraci zařízení s Windows zobrazí chybová zpráva.

    > [!IMPORTANT]
    > Pokud vícefaktorové ověřování nepovolíte nejdřív v klientovi služby Azure AD, než ho budete vyžadovat pro registraci do služby Intune, a je nastavená automatická registrace do správy mobilních zařízení (MDM) při připojení ke službě Azure AD, uživatelům se při pokusu o připojení zařízení s Windows ke službě Azure AD zobrazí chybová zpráva.

3.  Klikněte na **Konfigurace vícefaktorového ověřování** a potom na **Povolit vícefaktorové ověřování**.

## Viz také
[Ochrana dat a zařízení v Microsoft Intune](../Topic/Protect_data_and_devices_with_Microsoft_Intune.md)

