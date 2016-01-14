---
description: na
keywords: na
title: Set up Android management with Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: dbe5cad1-3e0d-41a9-966b-738156089700
---
# Nastaven&#237; spr&#225;vy syst&#233;mu Android pomoc&#237; Microsoft Intune
Mobilní zařízení se systémem Android umožňují uživatelům registraci pomocí aplikace Portál společnosti dostupné na webu Google Play. Pokud chcete, aby mohli uživatelé registrovat svá zařízení ve službě [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], proveďte následující kroky.

## Nastavení mobilních zařízení se systémem Android v Microsoft Intune

1.  **Nastavení[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]** 
    Pokud jste to ještě neudělali, připravte se na správu mobilních zařízení [nastavením autority pro správu mobilních zařízení](https://technet.microsoft.com/library/mt346013.aspx) na **Microsoft Intune**.

2.  **Přidání uživatelů Intune** 
    Abyste mohli mobilní zařízení zaregistrovat, musí být jeho vlastník přidaný do portálu účtu. Přihlaste se k [portálu účtu Microsoft Intune](http://go.microsoft.com/fwlink/?LinkId=698854), klikněte na **Přidat uživatele** a vyberte některou možnost:

    -   **Uživatel**: Pokud chcete přidat jednoho uživatele, vyberte **Nový** &gt; **Uživatel** a zadejte informace do polí **Podrobnosti**, **Přiřadit role** a **Nastavení umístění uživatele** a potom v poli **Skupina** přiřaďte uživatele do skupiny.

    -   **Hromadné přidání**: Vytvořte soubor .csv (podívejte se na dodané ukázkové soubory) a importujte ho na portál účtů. Zadejte role, umístění, skupiny a vytvořte účty. Ukázkové i prázdné soubory .csv si můžete stáhnout z portálu účtu.

    Můžete taky povolit synchronizaci s Active Directory nebo s Azure Active Directory. Pokud chcete další informace o integraci jiných uživatelů Azure Active Directory do Intune, přečtěte si téma [Synchronizace adresářů: rozcestník](http://go.microsoft.com/fwlink/?LinkId=511540) nebo na portálu účtu klikněte na **Další způsoby přidávání uživatelů**.

3.  **Vytváření skupin**  (volitelné)
    Skupiny nabízejí flexibilitu při správě zařízení a uživatelů. Můžete je nastavit tak, aby odpovídaly potřebám vaší organizace (třeba podle zeměpisného umístění, oddělení nebo vlastností hardwaru).   Viz [Použití skupin pro správu uživatelů a zařízení s Microsoft Intune](../Topic/Use_groups_to_manage_users_and_devices_with_Microsoft_Intune.md).

4.  **Přidání zásad pro zařízení** (volitelné)
    Zásady jsou skupiny nastavení, které řídí funkce na zařízeních. Většina zásad MDM je specifických pro platformu. Zásady se vytvářejí pomocí šablon, které obsahují doporučená nebo přizpůsobená nastavení. Potom je můžete nasadit do skupin. Viz [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

5.  **Nastavte limit registrovaných zařízení.** (volitelné) 
    Pokud chcete omezit počet mobilních zařízení, která si může uživatel zaregistrovat, přihlaste se ke [konzole pro správu Microsoft Intune](http://manage.microsoft.com), klikněte na **Správce** &gt; **Správa mobilních zařízení** &gt; **Pravidla registrace**. Vyberte maximální počet zařízení, které může uživatel zaregistrovat, a klikněte na **Uložit**.

6.  **Nastavte portál firmy.**
     Portál společnosti Intune můžete přizpůsobit potřebám své firmy. V [konzole pro správu Microsoft Intune](http://manage.microsoft.com) klikněte na **Správce** &gt; **Portál společnosti**. Co můžete nakonfigurovat:

    -   **název společnosti,**

    -   **Jméno kontaktní osoby oddělení IT**

    -   **Telefonní číslo oddělení IT**

    -   **Další informace**

    -   **Adresa URL prohlášení o zásadách ochrany osobních údajů společnosti**

    -   **adresu URL webu podpory (nezobrazuje se),**

    -   **Název webu**

7.  [!INCLUDE[CPEnrollmentTermsAndConditions](../Token/CPEnrollmentTermsAndConditions_md.md)]

8.  **Sdělte uživatelům, jak získat přístup k prostředkům společnosti pomocí firemního portálu** 
    Uživatelé budou potřebovat vědět, jak mají registrovat svá zařízení a co mají očekávat po začlenění do správy.[Co říct koncovým uživatelům o používání služby Microsoft Intune](../Topic/What_to_tell_your_end_users_about_using_Microsoft_Intune.md)

## Viz také
[Příprava registrace zařízení v Microsoft Intune](../Topic/Get_ready_to_enroll_devices_in_Microsoft_Intune.md)

