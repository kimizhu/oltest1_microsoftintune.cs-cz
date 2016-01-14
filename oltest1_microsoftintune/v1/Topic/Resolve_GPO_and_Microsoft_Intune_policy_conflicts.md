---
description: na
keywords: na
title: Resolve GPO and Microsoft Intune policy conflicts
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e76af5b7-e933-442c-a9d3-3b42c5f5868b
---
# Řešen&#237; konfliktů GPO a z&#225;sad Microsoft Intune
[!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] používá zásady, které vám pomůžou spravovat nastavení na počítačích, které spravujete. Pomocí zásad můžete třeba na počítačích řídit nastavení pro bránu Windows Firewall. Hodně nastavení služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] se podobá nastavením, která nejspíš konfigurujete pomocí zásad skupiny Windows. Někdy se ale může stát, že se tyto dvě metody dostanou vzájemně do konfliktu.

V případě konfliktu mají před zásadami [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] přednost zásady skupiny na úrovni domény mimo případů, kdy se počítač nemůže přihlásit do domény. V takovém případě se použijí na klientském počítači zásady [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

## <a name="BKMK_plan"></a>Co je potřeba udělat, když používáte zásady skupiny
Zkontrolujte, že žádné zásady, které používáte, nejsou spravované zásadami skupiny. Abyste líp zabránili konfliktům, můžete využít některé z těchto metod:

-   Před instalací klienta [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] přesuňte počítače do organizační jednotky služby Active Directory, u které se nepoužívá nastavení zásad skupiny. V organizačních jednotkách obsahujících počítače zaregistrované v [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], u kterých nechcete používat nastavení zásad skupiny, můžete taky zablokovat dědičnost zásad skupiny.

-   Pomocí filtru rozhraní WMI nebo filtru zabezpečení omezte objekty zásad skupiny jenom na počítače, které nespravuje [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Příklady a další informace o tom, jak to udělat, najdete v následující části [Jak filtrovat stávající objekty zásad skupiny, aby nedocházelo ke konfliktům se zásadami Microsoft Intune](../Topic/Resolve_GPO_and_Microsoft_Intune_policy_conflicts.md#BKMK_Filter).

-   Zakažte nebo odeberte objekty zásad skupiny, které jsou v konfliktu se zásadami [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

Další informace o službě Active Directory a zásadách skupiny Windows najdete v dokumentaci k Windows Serveru.

### <a name="BKMK_Filter"></a>Jak filtrovat stávající objekty zásad skupiny, aby nedocházelo ke konfliktům se zásadami Microsoft Intune
Pokud jste našli objekty zásad skupiny s nastavením, které je v konfliktu s nastavením zásad [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], můžete použít některou z následujících metod filtrování a omezit tak tyto objekty zásad skupiny jenom na počítače, které nespravuje [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

#### Použití filtrů rozhraní WMI
Filtry rozhraní WMI selektivně používají objekty zásad skupiny jenom u počítačů, které splňují podmínky dotazu. Pokud chcete použít filtr rozhraní WMI, nasaďte před registrací počítačů ve službě [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] na všechny počítače v podnikové síti instanci třídy služby WMI.

##### <a name="BKMK_filters"></a>Použití filtrů rozhraní WMI u objektu zásad skupiny

1.  Vytvořte soubor objektu správy, a to tak, že zkopírujete následující text, vložíte ho do textového souboru a ten uložíte pod názvem **WIT.mof** na vhodné místo. Tento soubor obsahuje instanci třídy služby WMI a tu můžete nasadit na počítače, které chcete zaregistrovat ve službě [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

    ```
    //Beginning of MOF file. #pragma classflags("forceupdate") #pragma namespace ("\\\\.\\Root") instance of __Namespace { Name = "WindowsIntune"; }; #pragma namespace ("\\\\.\\Root\\WindowsIntune") [ Description("This class defines Microsoft Intune common properties") ] class WindowsIntune_ManagedNode { [ read, Description("This defines whether Microsoft Intune Policy is enabled"): DisableOverride ToSubClass ] boolean WindowsIntunePolicyEnabled; [ read, key, Description("This property defines the version." "Example: 1.0"): ToSubClass ] string Version; }; instance of WindowsIntune_ManagedNode { Version = "1.0"; WindowsIntunePolicyEnabled = 1; };
    ```

2.  Použijte spouštěcí skript nebo zásady skupiny a tento soubor nasaďte. Dole je příkaz pro nasazení v případě spouštěcího skriptu. Instanci třídy služby WMI je potřeba nasadit před registrací klientských počítačů ve službě [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

    **C:/Windows/System32/Wbem/MOFCOMP &lt;path to MOF file&gt;\wit.mof**

3.  Spusťte některý z následujících příkazů pro vytvoření filtrů rozhraní WMI, a to podle toho, jestli je objekt zásad skupiny, který chcete filtrovat, použitý u počítačů spravovaných pomocí [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] nebo u počítačů, které pomocí [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] spravované nejsou.

    -   U objektů zásad skupiny použitých u počítačů, které nejsou spravované pomocí [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], použijte tento příkaz:

        ```
        Namespace:root\WindowsIntune Query:  SELECT WindowsIntunePolicyEnabled FROM WindowsIntune_ManagedNode WHERE WindowsIntunePolicyEnabled=0
        ```

    -   U objektů zásad skupiny použitých u počítačů, které jsou spravované pomocí [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], použijte tento příkaz:

        ```
        Namespace:root\WindowsIntune Query:  SELECT WindowsIntunePolicyEnabled FROM WindowsIntune_ManagedNode WHERE WindowsIntunePolicyEnabled=1
        ```

4.  Upravte objekt zásad skupiny v konzole pro správu zásad skupiny tak, aby používal filtr rozhraní WMI, který jste vytvořili v předchozím kroku.

    -   U objektů zásad skupiny, které by se měly používat jenom u počítačů, které chcete spravovat pomocí [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], použijte filtr **WindowsIntunePolicyEnabled=1**.

    -   U objektů zásad skupiny, které by se měly používat jenom u počítačů, které nechcete spravovat pomocí [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], použijte filtr **WindowsIntunePolicyEnabled=0**.

Další informace o tom, jak používat filtry rozhraní WMI v zásadách skupiny, najdete v blogovém příspěvku [Filtrování zabezpečení, filtrování WMI a cílení na úrovni položek v předvolbách zásad skupiny](http://go.microsoft.com/fwlink/?LinkId=177883).

#### Použití filtrů skupin zabezpečení
Zásady skupiny umožňují používat objekty zásad skupiny jenom u skupin zabezpečení, které jsou pro vybraný objekt zásad skupiny zadané v oblasti **Filtrování zabezpečení** konzoly pro správu zásad skupiny. Objekty zásad skupiny se ve výchozím nastavení používají u skupiny **Authenticated Users**.

-   V modulu snap-in **Uživatelé a počítače služby Active Directory** vytvořte novou skupinu zabezpečení obsahující účty počítačů a uživatelské účty, které nechcete spravovat pomocí [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Vaše skupina by třeba mohla mít název **Nespravovat v [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]**.

-   V konzole pro správu zásad skupiny klikněte na kartě **Delegování** pro vybraný objekt zásad skupiny pravým tlačítkem na novou skupinu zabezpečení a udělte uživatelům i počítačům v této skupině zabezpečení příslušná oprávnění **Číst** a **Používat zásady skupiny**. (Oprávnění **Používat zásady skupiny** jsou dostupná v dialogovém okně **Upřesnit**.)

-   Pak u vybraného objektu zásad skupiny použijte nový filtr skupin zabezpečení a odeberte výchozí filtr **Authenticated Users**.

S novou skupinou zabezpečení se musí ve změnách služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] nakládat jako s registrací.

## Viz také
[Správa počítačů s Windows pomocí Intune](../Topic/Manage_Windows_PCs_with_Microsoft_Intune.md)

