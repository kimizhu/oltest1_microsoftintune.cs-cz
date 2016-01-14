---
description: na
keywords: na
title: Use groups to manage users and devices with Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: eb9b01ce-9b9b-4c2a-bf99-3879c0bdaba5
---
# Použit&#237; skupin pro spr&#225;vu uživatelů a zař&#237;zen&#237; s Microsoft Intune
**Skupiny** ve [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] poskytují flexibilitu pro správu zařízení a uživatelů. Skupiny můžete nastavit tak, aby odpovídaly potřebám vaší organizace (třeba podle zeměpisného umístění, oddělení nebo vlastností hardwaru).

Skupiny navíc můžete filtrovat a povolit, aby oprávnění správců IT umožňovala provádět operace pouze na vámi zadaných skupinách. Další informace najdete v části [Použití filtrovaných zobrazení skupiny k zabezpečení a správě uživatelů a zařízení](../Topic/Use_groups_to_manage_users_and_devices_with_Microsoft_Intune.md#BKMK_Filter) tohoto tématu.

Pokud chcete vytvořit a spravovat skupiny, použijte pracovní prostor **Skupiny** v konzole [!INCLUDE[wit_adminconsole](../Token/wit_adminconsole_md.md)]. Stránka **Přehled skupin** obsahuje souhrny stavů, které vám pomůžou identifikovat problémy vyžadující vaši pozornost a určit jejich prioritu:

-   Výstrahy

-   Aktualizace softwaru

-   [!INCLUDE[epshort](../Token/epshort_md.md)]

-   Zásady

-   Správa softwaru

Kromě toho se zobrazuje i hierarchické zobrazení vašich skupin, které vám umožní prohlédnout si souhrny stavu a identifikovat a vyřešit problémy členů vybrané skupiny.

[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] poskytuje devět předdefinovaných skupin, které se nedají upravit ani odstranit:

-   **Všichni uživatelé**

    -   **Neseskupení uživatelé**

-   **Všechna zařízení**

    -   **Všechny počítače**

    -   **Všechna mobilní zařízení**

        -   **Všechna přímo spravovaná zařízení**

        -   **Všechna zařízení spravovaná prostřednictvím protokolu Exchange ActiveSync**

    -   **Všechna zařízení vlastněná společností**

    -   **Neseskupená zařízení**

## Členství ve skupinách

-   Skupina může obsahovat uživatele nebo zařízení, nemůže obsahovat oboje.

    -   **Skupiny zařízení:** Sem patří počítače a mobilní zařízení. Před přidáním počítače do skupiny je potřeba ho zapsat. Než budete moct přidat mobilní zařízení do skupiny, musíte nakonfigurovat prostředí tak, aby podporovalo mobilní zařízení. Zařízení musí navíc být zapsaná nebo zjištěná protokolem Exchange ActiveSync.

    -   **Skupiny uživatelů:** Skupina může obsahovat uživatele ze skupin zabezpečení. To jsou skupiny, které se synchronizují ze služby Active Directory. Pokud synchronizaci Active Directory nepoužíváte, můžete tyto skupiny vytvořit ručně.

-   Zařízení nebo uživatel může patřit do víc než jedné skupiny.

-   Skupina může zahrnout a vyloučit členy na základě následujících pravidel členství:

    -   **Členství na základě kritérií:** Jedná se o dynamická pravidla, která [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] používá pro zahrnutí nebo vyloučení členů.  Tato kritéria používají skupiny zabezpečení a další informace synchronizované z vaší místní služby Active Directory. Pokud se změní skupina zabezpečení nebo synchronizovaná data, může se změnit členství ve skupině.

    -   **Přímé členství:** Jedná se o statická pravidla, která členy explicitně přidávají nebo vylučují. Seznam členství je statický.

-   K vytvoření skupin uživatelů nebo skupin zařízení obsahujících uživatele nebo počítače se služba Active Directory Domain Services (AD DS) nevyžaduje. Pokud ale mají skupiny zařízení obsahovat mobilní zařízení, musí být prostředí nakonfigurované pro podporu mobilních zařízení.

    Zařízení navíc musí být zjištěná a přidaná do [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

## Vztahy skupiny

-   Každá vytvořená skupina musí mít nadřazenou skupinu. Po vytvoření skupiny už nemůžete její nadřazenou skupinu změnit.

-   Přidávání uživatelů nebo zařízení do podřízené skupiny:

    -   Podřízené skupiny jsou vždycky podskupinami nadřazené skupiny.

    -   Noví členové přidaní do podřízené skupiny se automaticky přidají do příslušné nadřazené skupiny.

    -   Pokud je člen vyloučený z nadřazené skupiny, nemůžete ho přidat do podřízené skupiny.

-   Členství v nadřazené skupině definuje dostupné členy pro podřízenou skupinu.

-   Pokud odstraníte nadřazenou skupinu, odstraní se všechny podřízené skupiny.

-   Obsah a zásady můžete nasadit na nadřazenou skupinu, i když je nasazení na podřízené skupiny vyloučené.

-   Do podřízené skupiny, která není členem nadřazené skupiny, můžete přidat konkrétního uživatele nebo zařízení. V takovém případě se nový člen skupiny přidá do nadřazené skupiny.

    Člena ale nemůžete přidat do podřízené skupiny, která je z nadřazené skupiny vyloučená.

-   Členství ve skupině je rekurzivní. Například:

    -   **Jan** je členem jenom jedné skupiny, skupiny zabezpečení **Uživatelé přenosných počítačů**.

    -   Skupina **Uživatelé přenosných počítačů** je členem skupiny zabezpečení **Schválení uživatelé**.

    -   Vytvoříte skupinu ve [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], která používá dynamický dotaz na členství obsahující členy skupiny **Schválení uživatelé**. Důsledkem toho pak bude vaše skupina uživatelů [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] zahrnovat **Jana**.

> [!TIP]
> Při vytváření skupin vezměte v úvahu, jak použijete zásady. Můžete mít třeba zásady specifické pro operační systémy zařízení a zásady specifické pro různé role ve vaší organizaci nebo pro organizační jednotky, které jste už v Active Directory definovali. Někdo považuje za užitečné používat skupiny zařízení specifické pro iOS, Android a Windows a skupiny uživatelů pro každou organizační roli.
> 
> Budete chtít nejspíš vytvořit výchozí zásadu, která platí pro všechny skupiny a zařízení, pro zajištění základních požadavků na dodržování předpisů ve vaší společnosti. Potom vytvořte konkrétnější zásady pro nejširší kategorie uživatele a zařízení, například zásady e-mailu pro každý operační systém zařízení.
> 
> Pečlivě zásady pojmenujte, abyste je později mohli snadno identifikovat. Dobrý název zásady je třeba **Zásada e-mailů WP pro celou firmu**.
> 
> Při každém vytvoření omezující zásady budete chtít tuto zásadu sdělit uživatelům, takže doporučujeme, abyste po vytvoření obecnějších skupin a zásad věnovali pozornost tomu, jak vytváříte menší skupiny, aby se redukovala zbytečná komunikace.

## Jak vytvořit skupiny Microsoft Intune

### <a name="BKMK_CreateDevGroup"></a>Vytvoření skupiny zařízení

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com/) klikněte na **Skupiny** &gt; **Přehled** &gt; **Vytvořit skupinu**.

2.  Zadejte název skupiny a její nepovinný popis, vyberte skupinu zařízení jako nadřazenou skupinu a klikněte na **Další**.

3.  Na stránce **Definovat kritéria členství** vyberte typ zařízení, který bude skupina obsahovat. Další možnosti konfigurace skupiny závisí na vybraném typu zařízení:

    -   **Počítač:** Určete, jestli se mají zahrnout všichni členové nadřazené skupiny, a organizační jednotky a domény, které chcete zahrnout nebo vyloučit. Informace o organizačních jednotkách a doménách počítače se získávají z inventáře.

    -   **Mobilní:** Určete, jestli se mají zahrnout jenom mobilní zařízení spravovaná [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], zařízení spravovaná Exchange ActiveSync, nebo obojí.

    -   **Všechna zařízení:** Tato možnost zahrne všechna zařízení, bez vyloučení na základě kritérií.

4.  Na stránce **Definovat přímé členství** zahrňte nebo vylučte jednotlivá zařízení, která určíte kliknutím na **Procházet**. Pokud použijete možnost pro výběr zařízení, která nejsou ve vámi určené nadřazené skupině, přidají se tato zařízení do nadřazené skupiny automaticky.

5.  Na stránce **Souhrn** si prohlédněte akce, které se provedou, a pak klikněte na **Dokončit**.

Nově vytvořenou skupinu najdete v seznamu **Skupiny**, v pracovním prostoru **Skupiny**, v rámci nadřazené skupiny. Tady můžete skupinu i upravit nebo odstranit.

#### Vytvoření skupiny uživatelů

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com/) klikněte na **Skupiny** &gt; **Přehled** &gt; **Vytvořit skupinu**.

2.  Zadejte název skupiny a její nepovinný popis, vyberte skupinu uživatelů jako nadřazenou skupinu a klikněte na **Další**.

3.  Na stránce **Definovat kritéria členství** určete, jestli se mají zahrnout všichni členové nadřazené skupiny, nebo jestli se má začít s prázdnou skupinou.  Potom můžete zahrnout nebo vyloučit členy na základě nastavení **Skupiny uživatelů**, které ručně nakonfigurujete na portálu účtů nebo které se synchronizuje z vaší místní služby Active Directory. Pokud se změní členství ve skupině zabezpečení, může se změnit i členství ve skupinách uživatelů založených na této skupině zabezpečení.

    > [!IMPORTANT]
    > Teď platí, že pokud vaše skupina obsahuje členy z konkrétní skupiny zabezpečení nebo manažera a zároveň vyloučíte členy z konkrétních skupin, dojde k odebrání členů, které jste na začátku zahrnuli. Pokud chcete vytvořit skupinu, která má zahrnuté i vyloučené členy, doporučujeme nejdřív vytvořit nadřazenou skupinu se zahrnutými členy a pak k této skupině vytvořit podřízenou skupinu, ve které uvedete vyloučené členy. Podřízenou skupinu pak můžete podle potřeby využít pro zásady Intune, profily a distribuci aplikací.

    > [!NOTE]
    > Na portálu pro správu Azure můžete vytvořit skupinu podle manažera, kterému uživatelé podléhají. Skupina se bude dynamicky měnit podle toho, jak se do týmu daného manažera ve službě Azure Active Directory přidávají zaměstnanci nebo se z něj naopak odebírají. Postup pro vytvoření skupiny Azure podle manažera najdete v článku [Vytváření rozšířených pravidel pomocí atributů](https://azure.microsoft.com/en-us/documentation/articles/active-directory-accessmanagement-groups-with-advanced-rules/) v části **Konfigurace skupiny manažera**.

4.  Na stránce **Definovat přímé členství** zahrňte nebo vylučte jednotlivé uživatele, které určíte kliknutím na **Procházet**. Pokud použijete možnost pro výběr uživatelů, kteří nejsou ve vámi určené nadřazené skupině, přidají se tito uživatelé do nadřazené skupiny automaticky.

5.  Na stránce **Souhrn** si prohlédněte akce, které se provedou, a pak klikněte na **Dokončit**.

Nově vytvořenou skupinu najdete v seznamu **Skupiny**, v pracovním prostoru **Skupiny**, v rámci nadřazené skupiny. Tady můžete skupinu i upravit nebo odstranit.

> [!TIP]
> Skupiny zabezpečení jsou skvělým zdrojem pro naplnění skupin uživatelů. Protože vaše skupiny zabezpečení definují, kdo má k jakým prostředkům přístup, jsou srozumitelné pro skupiny uživatelů [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Skupiny zabezpečení, které jsou synchronizované z Active Directory do Azure Active Directory nebo které jsou vytvořené přímo v Azure Active Directory pomocí portálu účtu [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], portálu pro správu O365 nebo portálu pro správu Azure, jsou všechny dostupné pro vytváření skupin uživatelů ve službě [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

## Správa skupin
Po vytvoření vlastních skupin je budete moct dále spravovat podle potřeb vaší organizace.

### <a name="BKMK_Filter"></a>Použití filtrovaných zobrazení skupiny k zabezpečení a správě uživatelů a zařízení
Zobrazení filtrované skupiny vám umožní omezit, které skupiny můžou jednotliví správci IT spravovat. To může být užitečné, když:

-   Vaši správci IT mají možnost nasadit položky jenom u konkrétních uživatelů a zařízení.

-   Chcete pro každého správce IT zobrazit jenom relevantní skupiny.

Filtrovaná zobrazení skupiny pro správce služeb můžete nakonfigurovat v konzole pro správu [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Podrobnosti najdete v tématu [Co potřebujete vědět před nastavením Microsoft Intune](../Topic/What_to_know_before_setting_up_Microsoft_Intune.md).

Po dokončení konfigurace filtrovaných zobrazení skupiny pro správce služby tento správce:

-   Může zobrazit a vybrat jenom skupiny, které jste při nasazení softwaru nebo zásad nebo pomocí sestav zadali.

-   Neobdrží informace o stavu na následujících stránkách konzoly pro správu:

    -   **Přehled systému**

    -   **Přehled skupin**

    -   **Přehled služby Endpoint Protection**

    -   **Přehled výstrah**

    -   **Přehled softwaru**

    -   **Přehled zásad**

##### Konfigurace filtrovaných zobrazení skupiny

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com) klikněte na **Správce** &gt; **Správa správců** &gt; **Správci služeb**.

2.  Vyberte správce služeb, pro kterého chcete filtrovat skupiny, a pak klikněte na **Spravovat skupiny**.

3.  V dialogovém okně **Vyberte skupiny, které budou pro tohoto správce služeb viditelné** přidejte skupiny, ke kterým bude moct vybraný správce služeb přistupovat, a pak klikněte na **OK**.

Po dokončení konfigurace filtrovaných zobrazení skupiny, bude správce IT moct zobrazit a vybrat jenom vámi zvolené skupiny.

## Další úlohy správy pro skupiny
Skupinu můžete upravit tak, aby se změnil její název a popis a také členové, které obsahuje.

Skupinu, která už neslouží potřebám vaší organizace, můžete odstranit. Odstraněním skupiny nedojde k odstranění uživatelů, kteří do této skupiny patří.

## Skupiny a zásady
Po nastavení skupin a zásad budete chtít ověřit praktický dopad vytvořeného designu. Tady jsou některé užitečné tipy a informace o skupinách a zásadách.

Je možné načíst spousty informací o jednotlivých zařízeních, která [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] spravuje. Vyberte jakákoli zařízení ze skupiny zařízení a procházejte kategorie informací v horní části obrazovky. Vyberte **Zásada**. Zobrazí se snímek obrazovky nastavení zásady zařízení Android podobný následujícímu.

![](../Image/Intune_Device_Policy_v.2.jpg)

Každá zásada má **určenou hodnotu** a **Stav**. Určená hodnota označuje to, čeho chcete dosáhnout při přiřazování zásady. Stav označuje to, čeho skutečně dosáhnete, když jsou společně zvažovány všechny zásady, které u zařízení použijete, a všechna omezení a požadavky na hardware a operační systém.  Na snímku obrazovky vidíte dva jasné příklady:

-   Možnost **Povolit jednoduchá hesla** je nastavená na **Ano**, jak ukazuje sloupec **Určená hodnota**, ale její **Stav** je **Nepoužívá se**. Důvodem je, že se na zařízeních s Androidem nepodporují jednoduchá hesla.

-   Podobně pak u tohoto zařízení není použitá rozšířená položka zásad **Nastavení e-mailu pro zařízení iOS**, protože to je zařízení s Androidem.

> [!NOTE]
> Mějte na paměti, že když použijete dvě zásady s různými úrovněmi omezení na stejné zařízení nebo uživatele, v praxi se uplatní víc omezující zásada.

## Viz také
[Začněte s placeným předplatným Microsoft Intune](../Topic/Get_started_with_a_paid_subscription_to_Microsoft_Intune.md)
[Jak koupit Intune](http://technet.microsoft.com/en-us/library/dn646949.aspx)

