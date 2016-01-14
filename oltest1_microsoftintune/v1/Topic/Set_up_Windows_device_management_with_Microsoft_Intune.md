---
description: na
keywords: na
title: Set up Windows device management with Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9a18c0fe-9f03-4e84-a4d0-b63821bf5d25
---
# Nastaven&#237; spr&#225;vy pro zař&#237;zen&#237; Windows v Microsoft Intune
Službu [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] můžete používat ke správě stolních počítačů, laptopů a dalších zařízení, která spouští Windows jako mobilní zařízení. Můžete také chtít [Nastavení správy pro zařízení Windows Phone v Microsoft Intune](../Topic/Set_up_Windows_Phone_management_with_Microsoft_Intune.md) nebo [spravovat počítače s klientským softwarem Intune](http://technet.microsoft.com/library/dn646959.aspx) pomocí klienta [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

## Příprava na správu zařízení Windows s Intune
Aby mohli uživatelé přistupovat k prostředkům spravovaným službou [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], mohou registrovat své počítače Windows jako mobilní zařízení.  Vytvořením DNS CNAME uživatelům usnadníte připojení k portálu společnosti [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] bez nutnosti zadávat název serveru. Když chcete nasadit portál společnosti pomocí služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], je potřeba povolit zkušební načtení před prodejem pomocí klíče zkušebního načtení před prodejem.   Uživatelé můžou taky stáhnout a nainstalovat Portál společnosti ze Storu nebo použít software obsažený ve Windows. Dokončením následujících kroků provedete nastavení správy pro zařízení Windows pomocí služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

#### Nastavení správy pro zařízení Windows

1.  **Nastavení služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]** 
    Pokud jste to ještě neudělali, [připravte se na správu mobilních zařízení](https://technet.microsoft.com/library/mt346013.aspx) nastavením autority pro správu mobilních zařízení na **[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]**.

2.  **Nastavení aliasu DNS pro adresu serveru registrace (volitelně)**

    Alias DNS (typ záznamu CNAME) uživatelům usnadňuje registraci zařízení tím, že se při registraci automaticky vyplní název serveru.

    ###### Ověření a vytvoření DNS CNAME

    1.  V [konzole pro správu Intune](http://manage.microsoft.com) klikněte na **Správa** &gt; **Správa mobilních zařízení** &gt; **Windows Phone**.

    2.  Zadejte adresu URL ověřené domény webu společnosti do pole **Zadat název ověřené domény** a klikněte na **Test automatického zjištění**.

    3.  Vytvořte záznamy o prostředcích CNAME pro doménu vaší společnosti. Záznamy o prostředcích CNAME musí obsahovat tyto informace:

        |TYP|Název hostitele|Odkazuje na|Hodnota TTL|
        |-------|-------------------|---------------|---------------|
        |CNAME|enterpriseenrollment.doména_společnosti.com|manage.microsoft.com|1 hodina|
        |CNAME|enterpriseregistration.doména_společnosti.com|enterpriseregistration.windows.net|1 hodina|
        Pokud je třeba web vaší společnosti contoso.com, vytvořili byste záznam CNAME ve službě DNS, který přesměruje adresu EnterpriseEnrollment.contoso.com na manage.microsoft.com. Pokud existuje víc než jedna ověřená doména, vytvořte záznam CNAME pro každou doménu.

        -   `manage.microsoft.com` – Podporuje přesměrování na služby Intune s rozpoznáním domény z doménového názvu e-mailu.

        -   `enterpriseregistration.windows.net` – Podporuje připojení pracovního místa pro mobilní zařízení. Mimoto podporuje i podmíněný přístup pro Windows 8.1.

    ![](../Image/Windows_Device_Enrollment.bmp)

3.  **Povolení zkušebního načtení aplikací** (volitelné)
    U zařízení s Windows RT 8.1, Windows 8.1 a Windows 10 se aplikace Portál společnosti dá nainstalovat z Windows Storu. Pokud se aplikace nenainstaluje přímo z Windows Storu, instalace aplikace Firemní portál vyžaduje zkušební načtení klíčů na cílových počítačích. Podrobnosti o tom, jak nasadit klíče pro zkušební načítání, najdete na adrese [http://go.microsoft.com/fwlink/?LinkID=290705](http://go.microsoft.com/fwlink/?LinkID=290705). I když zkušebně načtené aplikace nemusí být certifikované nebo nainstalované z Windows Store, můžou se instalovat jen na zařízeních s podporou zkušebního načtení. Další informace o získávání klíčů pro zkušební načtení najdete v tématu [Multilicence společnosti Microsoft](http://go.microsoft.com/fwlink/?LinkId=264711).

    ###### Aplikace s podepsaným kódem pro zařízení s Windows

    1.  V [konzole pro správu Intune](http://manage.microsoft.com) klikněte na **Správa** &gt; **Správa mobilních zařízení** &gt; **Windows** &gt; **Přidat kód pro zkušební načtení před prodejem**.

    2.  V dialogovém okně **Přidat kód pro zkušební načtení před prodejem** zadejte název, aktivační klíč pro zkušební načtení produktu, celkový počet aktivací a volitelný popis a potom klikněte na **OK**.

    3.  Stáhněte si aplikaci Firemní portál Microsoft Intune pro Windows Phone 8.1 z webu Stažení softwaru [http://go.microsoft.com/fwlink/?LinkId=615800](http://go.microsoft.com/fwlink/?LinkId=615800). Spusťte stáhnutý soubor, aby se extrahoval soubor CompanyPortal.appx, který umístěte do sdílené složky dostupné ze sítě.

    4.  Spusťte **Windows PowerShell** jako správce a zadejte následující rutinu:

        ```
        Powershell add-appxpackage –path '‹path›'
        ```

    5.  Ověřte, že se v seznamu aplikací na cílovém počítači nachází dlaždice **Firemní portál** (na zařízeních s Windows 8.1 nebo Windows RT 8.1 se dlaždice na obrazovce Start vytvoří automaticky).

4.  **Přidání uživatelů Intune** 
    Abyste mohli mobilní zařízení zaregistrovat, musí být jeho vlastník přidaný do portálu účtu. Přihlaste se k [portálu účtu Microsoft Intune](http://go.microsoft.com/fwlink/?LinkId=698854), klikněte na **Přidat uživatele** a vyberte některou možnost:

    -   **Uživatel**: Pokud chcete přidat jednoho uživatele, vyberte **Nový** &gt; **Uživatel** a zadejte informace do polí **Podrobnosti**, **Přiřadit role** a **Nastavení umístění uživatele** a potom v poli **Skupina** přiřaďte uživatele do skupiny.

    -   **Hromadné přidání**: Vytvořte soubor .csv (podívejte se na dodané ukázkové soubory) a importujte ho na portál účtů. Zadejte role, umístění, skupiny a vytvořte účty. Ukázkové i prázdné soubory .csv si můžete stáhnout z portálu účtu.

    Můžete taky povolit synchronizaci s Active Directory nebo s Azure Active Directory. Pokud chcete další informace o integraci jiných uživatelů Azure Active Directory do Intune, přečtěte si téma [Synchronizace adresářů: rozcestník](http://go.microsoft.com/fwlink/?LinkId=511540).

5.  **Vytváření skupin**  (volitelné)
    Skupiny nabízejí flexibilitu při správě zařízení a uživatelů. Můžete je nastavit tak, aby odpovídaly potřebám vaší organizace (třeba podle zeměpisného umístění, oddělení nebo vlastností hardwaru).   Viz [Použití skupin pro správu uživatelů a zařízení s Microsoft Intune](../Topic/Use_groups_to_manage_users_and_devices_with_Microsoft_Intune.md).

6.  **Přidání zásad pro zařízení** (volitelné)
    Zásady jsou skupiny nastavení, které řídí funkce na zařízeních. Většina zásad MDM je specifických pro platformu. Zásady se vytvářejí pomocí šablon, které obsahují doporučená nebo přizpůsobená nastavení. Potom je můžete nasadit do skupin. Viz [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

7.  **Nastavte limit registrovaných zařízení.** (volitelné) 
    Pokud chcete omezit počet mobilních zařízení, která si může uživatel zaregistrovat, přihlaste se ke [konzole pro správu Microsoft Intune](http://manage.microsoft.com), klikněte na **Správce** &gt; **Správa mobilních zařízení** &gt; **Pravidla registrace**. Vyberte maximální počet zařízení, které může uživatel zaregistrovat, a klikněte na **Uložit**.

8.  **Nastavte portál firmy.**
     Portál společnosti Intune můžete přizpůsobit potřebám své firmy. V [konzole pro správu Microsoft Intune](http://manage.microsoft.com) klikněte na **Správce** &gt; **Portál společnosti**. Co můžete nakonfigurovat:

    -   **název společnosti,**

    -   **Jméno kontaktní osoby oddělení IT**

    -   **Telefonní číslo oddělení IT**

    -   **Další informace**

    -   **Adresa URL prohlášení o zásadách ochrany osobních údajů společnosti**

    -   **adresu URL webu podpory (nezobrazuje se),**

    -   **Název webu**

9. [!INCLUDE[CPEnrollmentTermsAndConditions](../Token/CPEnrollmentTermsAndConditions_md.md)]

10. **Sdělte uživatelům, jak získat přístup k prostředkům společnosti pomocí firemního portálu** 
    Uživatelé budou potřebovat vědět, jak mají registrovat svá zařízení a co mají očekávat po začlenění do správy.[Co říct koncovým uživatelům o používání služby Microsoft Intune](../Topic/What_to_tell_your_end_users_about_using_Microsoft_Intune.md)

## Viz také
[Příprava registrace zařízení v Microsoft Intune](../Topic/Get_ready_to_enroll_devices_in_Microsoft_Intune.md)

