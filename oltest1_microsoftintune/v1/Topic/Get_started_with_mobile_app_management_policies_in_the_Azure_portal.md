---
description: na
keywords: na
title: Get started with mobile app management policies in the Azure portal
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7e6a85e7-e007-41b6-9034-64d77f547b87
---
# Zač&#237;n&#225;me se z&#225;sadami spr&#225;vy mobiln&#237;ch aplikac&#237; na port&#225;lu Azure
V tomto tématu naleznete potřebné informace, pokud začínáte s vytvářením zásad správy mobilních aplikací (MAM) na portálu Azure.

**V tomto tématu**

[Podporované aplikace](#bkmk_supportedapps)

[Podporované platformy](#bkmk_supportedplatforms)

[Co potřebujete, abyste mohli začít](#bkmk_Prereqs)

[Nastavení požadavků](#bkmk_prereqshowto)

[Přístup k portálu Azure Preview](#bkmk_azureportal)

[Další kroky](#bkmk_nextsteps)

## <a name="bkmk_supportedplatforms"></a>Podporované platformy

-   iOS 7.1 nebo novější

-   Android 4 nebo novější

## <a name="bkmk_supportedapps"></a>Podporované aplikace
**iOS:** aplikace Microsoft Word, Excel, PowerPoint a OneDrive

**Android:** OneDrive

## <a name="bkmk_Prereqs"></a>Co potřebujete, abyste mohli začít
Než začnete, budete potřebovat následující:

-   Předplatné služby [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)].    Koncoví uživatelé potřebují licence [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] k získání aplikací se zásadami MAM.

-   Předplatné služby Office 365 (O365) a přístup ke službě Azure Active Directory (Azure AD), chcete-li vytvářet uživatele a přiřazovat licence [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].  Služba Azure AD ověřuje uživatele při spuštění aplikace a zadání přihlašovacích údajů.

    > [!NOTE]
    > Pokud nastavujete uživatele pomocí konzoly [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], uvědomte si, že konfigurace zásad MAM se od nynějška přesouvá na portál Azure. Chcete-li používat tento portál, je nutné nastavit skupiny uživatelů Azure AD pomocí portálu Office 365.

## <a name="bkmk_prereqshowto"></a>Nastavení požadavků
V následující tabulce naleznete přehled rolí a oprávnění, které můžete přiřazovat uživatelům.

|||
|-|-|
|**Role**|**Oprávnění**|
|Globální správce (portál O365)|-   Přístup k portálu O365<br />-   Přístup k portálu Azure AD<br />-   Přístup k portálu Azure Preview (může provádět úkoly správy rolí i správy mobilních aplikací).|
|Role Vlastník (portál Azure Preview)|-   Přístup k portálu Azure Preview (může provádět úkoly správy rolí i správy mobilních aplikací).|
|Role Přispěvatel (portál Azure Preview)|-   Přístup k portálu Azure Preview (může provádět jenom úkoly správy mobilních aplikací).|

#### Vytváření uživatelů a přiřazování licencí [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]

1.  Pokud používáte [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] ke správě svých zařízení, již předplatné [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] máte.  Pokud jste zakoupili licenci EMS, předplatné [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] již také máte. Pokud zkoušíte [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], abyste se seznámili s funkcemi MAM, můžete [tady](http://www.microsoft.com/en-us/server-cloud/products/microsoft-intune/) získat zkušební účet.

    Chcete-li ověřit, zda předplatné [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] máte, přejděte na portálu Office na stránku Fakturace.  Předplatné služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] by mělo být označené jako **Aktivní**.

2.  Přihlaste se na [portál Office](http://portal.office.com) pomocí svých přihlašovacích údajů správce.

3.  Chcete-li přidat uživatele a přiřadit licence [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], přejděte na stránku **Aktivní uživatelé**.

    ![](../Image/AppManagement/OfficePortal_AddUsers.png)

4.  Má-li mít uživatel přístup na portály Office, Azure AD a Azure Preview, přiřaďte mu roli **globálního správce**.

    ![](../Image/AppManagement/OfficePortal_AddRoletoUser.png)

5.  Zásady MAM jsou nasazeny na skupiny uživatelů ve službě Azure Active Directory. Chcete-li vytvořit skupiny uživatelů v souladu se zásadami MAM, přejděte na stránku **Skupiny** na **portálu Office** a kliknutím na ikonu **+** vytvořte novou skupinu zabezpečení.  Zadejte název a popis a klikněte na **Vytvořit**. Do vytvořené skupiny můžete přidávat uživatele kliknutím na volbu **Upravit členy** v nově vytvořené skupině zabezpečení. Skupina zabezpečení je vytvořena ve službě Azure Active Directory.

    ![](../Image/AppManagement/OfficePortal_CreateGroups.png)

## <a name="bkmk_azureportal"></a>Přístup k portálu Azure Preview
Portál **Azure Preview** umožňuje vytvářet zásady aplikací, nasazovat je na uživatele a monitorovat stav nasazení.

#### Jak začít používat portál

1.  Přejděte na [portál Azure Preview](https://portal.azure.com) a přihlaste se pomocí svých přihlašovacích údajů služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

    ![](../Image/AppManagement/AzurePortal_MAMSigninPage.png)

2.  Po přihlášeni se vám zobrazí **Uvítací** nebo **Domovská** stránka.**Uvítací** nebo domovská stránka obsahuje sadu výchozích dlaždic. Přidáním nových dlaždic nebo jejich odebráním si stránku můžete přizpůsobit.

    ![](../Image/AppManagement/AzurePortal_MAMStartboard_NoMAM.png)

3.  V nabídce **Procházet** vyberte volbu **Intune**.![](../Image/AppManagement/AzurePortal_MAM_Browse_Intune.png)

4.  Klikněte na **Intune &gt; Správa mobilních aplikací Intune &gt; Nastavení**.

    ![](../Image/AppManagement/AzurePortal_MAM_Mainblade.png)

    > [!TIP]
    > Chcete-li připnout okno na **Uvítací** stránku, použijte volbu **připnout** v okně.  Kliknutím na ikonu připnutí **v okně správy mobilních aplikací Intune** toto okno připnete na **Uvítací** stránku.

    ![](../Image/AppManagement/AzurePortal_MAM_PinBladeAction.png)

    ![](../Image/AppManagement/AzurePortal_MAM_Startboard_withMAM.png)

**Globální správci** mají přístup k portálu Azure.  Chcete-li, aby ostatní správci mohli konfigurovat zásady a provádět i další úkoly správy mobilních aplikací, můžete jim přiřadit **roli přispěvatele** podle pokynů níže:

#### Přiřazení role Přispěvatel uživateli

1.  V okně **Nastavení** klikněte v části **Správa prostředků** na volbu **Uživatelé**.

    ![](../Image/AppManagement/AzurePortal_MAM_AddUsers.png)

2.  Kliknutím na **Přidat** otevřete okno **Přidat přístup**.

3.  Klikněte na **Vybrat roli** a poté na **role Přispěvatel**.

    ![](../Image/AppManagement/AzurePortal_MAM_AddRole.png)

4.  Jakmile vyberete roli, klikněte na volbu **Přidat uživatele** a vyhledejte uživatele pomocí uživatelského jména nebo e-mailové adresy. V tomto seznamu se zobrazí prvních 1000 uživatelů, které jste vytvořili ve službě Azure AD pomocí portálu Office. Kliknutím na **OK** v okně **Přidat přístup** uložíte a přiřadíte uživateli roli.

    ![](../Image/AppManagement/AzurePortal_MAM_AddusertoRole.png)

    > [!IMPORTANT]
    > Pokud vyberete uživatele, který nemá přiřazenou licenci[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], nebude moci získat přístup k portálu.

## <a name="bkmk_nextsteps"></a>Další kroky
[Vytvoření a nasazení zásad správy mobilních aplikací pomocí Microsoft Intune](../Topic/Create_and_deploy_mobile_app_management_policies_with_Microsoft_Intune.md)

## Viz také
[Nakonfigurujte zásady ochrany před únikem informací pomocí Microsoft Intune.](../Topic/Configure_data_loss_prevention_app_policies_with_Microsoft_Intune.md)

