---
description: na
keywords: na
title: Enroll corporate-owned devices with the Device Enrollment Manager in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: a23abc61-69ed-44f1-9b71-b86aefc6ba03
---
# Přihl&#225;šen&#237; firemn&#237;ch zař&#237;zen&#237; pomoc&#237; manažera registrace zař&#237;zen&#237; v Microsoft Intune
Organizace můžou pomocí Intune spravovat velké počty mobilních zařízení s jediným uživatelským účtem. Účet *manažera registrace zařízení* je speciální účet Intune s oprávněním přihlásit víc než pět zařízení. Manažerovi nebo vedoucímu obchodu třeba můžete přidělit uživatelský účet manažera registrace zařízení, který mu pomůže s následujícím:

-   Registrace zařízení v Intune

-   Přihlášení k firemnímu portálu pro získání podnikových aplikací

-   Instalace a odinstalace softwaru

-   Konfigurace přístupu k datům společnosti

Správce obchodu nemůže zařízení obnovit z podnikového portálu.

**Příklady situací se správcem registrace zařízení:** 
Restaurace chce pro své číšníky pořídit tablety POS a monitory na objednávky pro pracovníky kuchyně. Zaměstnanci nikdy nepotřebují přístup k podnikovým datům ani se nemusí přihlašovat jako uživatelé. Správce Intune vytvoří účet manažera registrace zařízení a zaregistruje zařízení vlastněná společností pomocí tohoto účtu. Správce taky může manažerovi registrace zařízení udělit pověření manažera restaurace, které mu umožňuje registrovat a spravovat zařízení.

Správce nebo manažer může do zařízení restaurace nasadit aplikace specifické pro role. Správce taky může vybrat zařízení v konzole služby Intune a vyřadit ho ze správy mobilních zařízení pomocí konzoly pro správu.

## Účty manažera registrace zařízení v Intune
Účty manažera registrace zařízení jsou uživatelské účty s oprávněním registrovat velká množství zařízení vlastněných společností. Manažeři registrace zařízení můžou být jenom uživatelé v konzole Intune.

#### Přidání správce registrace zařízení do služby Intune

1.  Přejděte na [portál účtů Microsoft Intune](http://go.microsoft.com/fwlink/p/?LinkID=329938) a přihlaste se k účtu správce.

2.  Klikněte na **Přidat uživatele**.

3.  Ověřte, že je uvedený uživatelský účet, který bude manažer registrace zařízení. Pokud ne, přidejte uživatele kliknutím na **Nový** a dokončením procesu přidání uživatele. Další informace o přidávání položek najdete v tématu [Task 3: Add users and assign licenses for your subscription](../Topic/Get_started_with_a_paid_subscription_to_Microsoft_Intune.md#Anchor_3). Každý uživatel, který službu používá, potřebuje licenci předplatného a *manažer registrace zařízení* nemůže být správce Intune. Určete, jestli před používáním této funkce budete muset přidat další licence.

4.  Přihlaste se ke [konzole pro správu Microsoft Intune](http://manage.microsoft.com) pomocí přihlašovacích údajů správce.

5.  V navigačním podokně klikněte na **Správce**, přejděte na **Správa správců** a vyberte **Manažer registrace zařízení**. Otevře se stránka manažera registrace zařízení.

6.  Klikněte na **Přidat...**. Otevře se dialog **Přidat manažera registrace zařízení**.

7.  Zadejte **ID uživatele** účtu Intune a klikněte na **OK**. Manažer registrace zařízení nemůže být správce služby Intune.

8.  Manažer registrace zařízení teď může registrovat mobilní zařízení stejným postupem, jaký používá koncový uživatel ve scénáři BYOD na podnikovém portálu. Pokud chcete registrovat zařízení pomocí podnikového portálu, přečtěte si článek [Povolení registrace mobilních zařízení na portálu účtů Microsoft Intune](../Topic/Enable_mobile_device_enrollment_with_the_Microsoft_Intune_Account_Portal.md).

#### Odstranění manažera registrace zařízení ze služby Intune

1.  Přihlaste se na [portál účtů Microsoft Intune](http://manage.microsoft.com) pomocí přihlašovacích údajů správce.

2.  V navigačním podokně klikněte na **Správce**, přejděte na **Správa správců** a vyberte **Manažer registrace zařízení**. Otevře se stránka manažera registrace zařízení.

3.  Vyberte **uživatele** – manažera registrace zařízení, kterého chcete odstranit, a klikněte na **Odstranit**. Uživatel se neodstraní ze služby Intune a zařízení, která spravuje, zůstanou v Intune zaregistrovaná. Odstranění manažera registrace zabrání tomuto uživateli registrovat v Intune víc zařízení.

4.  Kliknutím na **Ano** potvrďte, že chcete odstranit manažera registrace zařízení.

Odstranění manažera registrace zařízení nemá vliv na zaregistrovaná zařízení. Po odstranění manažera registrace zařízení:

-   Nejsou ovlivněná žádná zaregistrovaná zařízení.

-   Zaregistrovaná zařízení jsou dál plně spravovaná.

-   Přihlašovací údaje účtu manažera registrace zařízení jsou dál platné pro přihlašování na podnikový portál pro přístup k aplikacím

-   Přihlašovací údaje účtu manažera registrace zařízení dál nejde používat k mazání nebo vyřazování zařízení

-   Vztah odstraněného účtu manažera registrace zařízení k zaregistrovaným zařízením trvá, ale nebudou se registrovat žádná další zařízení.

## Viz také
[Začněte s placeným předplatným Microsoft Intune](../Topic/Get_started_with_a_paid_subscription_to_Microsoft_Intune.md)
[Příprava registrace zařízení v Microsoft Intune](../Topic/Get_ready_to_enroll_devices_in_Microsoft_Intune.md)
[Povolení registrace mobilních zařízení na portálu účtů Microsoft Intune](../Topic/Enable_mobile_device_enrollment_with_the_Microsoft_Intune_Account_Portal.md)

