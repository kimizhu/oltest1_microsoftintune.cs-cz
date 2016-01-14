---
description: na
keywords: na
title: Manage license agreements for Windows PC software in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c59d8635-3f66-40f5-824a-a71c738e0341
---
# Spr&#225;va licenčn&#237;ch smluv pro software poč&#237;tačů s Windows v&#160;Microsoft Intune
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] umožňuje přidávat a spravovat informace o licenčních smlouvách. Informace se týkají softwaru zakoupeného na základě multilicenčních smluv s Microsoftem. Software může nebo nemusí být od Microsoftu, případně může být koupený jiným způsobem. Tyto informace můžete navíc uspořádat do logických skupin.

> [!IMPORTANT]
> Tato funkce slouží pouze ke zvýšení pohodlí. Její přesnost není zaručena. Neměli byste na ni tedy spoléhat při ověřování shody s multilicenční smlouvou s Microsoftem. Microsoft shromážděná data nepoužije k vyšetřování případných přestupků nebo porušení licenčních smluv, které jste s ním uzavřeli.
> 
> Licence, které přidáte do [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], nebudou mít vliv na vaše licenční smlouvy ani na váš nárok na používání softwaru.  Když třeba z [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] odstraníte dvojici licence/smlouva, neodstraní ani nezruší se tím licenční smlouvy, které jste uzavřeli s Microsoftem.

Co můžete dělat v konzole správce služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] v pracovním prostoru **Licence**:

-   Přidávání a úprava multilicenčních smluv uzavřených s Microsoftem

-   Přidávání a úprava licenčních smluv k jinému softwaru

-   Správa licencí a skupin

-   Porovnávání informací o nárocích, které [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] načte z webu Volume Licensing Service Center (VLSC) do inventáře softwaru od Microsoftu, s informacemi, které [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] zjistí na vámi spravovaných počítačích s Windows

Můžete taky generovat sestavy, které u softwarových titulů zobrazují počty instalací a licencí. Sestavy licencí vám můžou pomoct vyhodnotit vaši kompletní licenční pozici pro software Microsoftu a software jiných společností.

> [!TIP]
> Pracovní prostor **Licence** se v konzole správce nezobrazí, pokud nespravujete aspoň jeden počítač s Windows a počítačovým klientem [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

## Přidání multilicenčních smluv uzavřených s Microsoftem
Multilicenční smlouvy [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] poskytují informace o licenci pro software, který je zakoupený prostřednictvím multilicenčních smluv s Microsoftem. Multilicenční smlouvy s Microsoftem můžete přidat do [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] tak, že zadáte odpovídající páry čísel smluv. Čísla smluv nebo autorizační čísla musí odpovídat správným číslům licencí nebo registrací. Páry čísel smluv získáte při nákupu vašich licenčních smluv na webu [Volume Licensing Service Center (VLSC)](http://go.microsoft.com/fwlink/?LinkID=223842).

### <a name="BKMK_AddVLAgreements"></a>Přidání multilicenční smlouvy uzavřené s Microsoftem

1.  V [konzole pro správu Microsoft Intune](https://account.manage.microsoft.com/admin/default.aspx) klikněte na **Licence**.

2.  Na stránce **Přidat smlouvy** v části **Zvolit typ smlouvy** vyberte **Multilicenční smlouva**.

3.  V části **Přidat podrobnosti smlouvy** zvolte jednu z možností:

    -   **Odeslat soubor CSV obsahující podrobnosti o smlouvě** – klikněte na Procházet a vyberte soubor CSV, který chcete odeslat.

        -   Soubor může obsahovat dva nebo tři sloupce. Dva jsou pro samotné páry smluv. Tři sloupce použijte, pokud chcete přidat popisný název pro jednotlivé páry smluv.

        -   Celkový počet znaků v páru čísel smluv nesmí překročit 16 znaků ASCII.

        -   Podporují se jenom znaky ASCII.

        -   V názvu smlouvy nejsou povolené následující znaky: **~ ! @ # $ ^ &amp; &#42; ( ) = + [ ] { } \ | ; : ' " &lt; &gt; /**. Název může obsahovat mezery.

        -   Název souboru nesmí být delší než 128 znaků.

        -   Soubor musí obsahovat aspoň jeden pár smluv a nesmí obsahovat víc než 5 000 párů smluv.

        **Formát souboru**

        Soubor vytvoříte tak, že do obyčejného textového dokumentu přidáte páry smluv. Soubor musí být v některém z následujících formátů podle typu organizace, který jste zaregistrovali na webu VLSC. Na řádku uveďte jednu dvojici čísel smluv.

        -   **Zákazníci s programem Open Value:** *číslo smlouvy*, *opakujte číslo smlouvy*, *název smlouvy*

        -   **Zákazníci s programem Open:** *autorizační číslo*, *číslo související licence*, *název smlouvy*

        -   **Zákazníci s programy Select a Enterprise:** *číslo smlouvy*, *číslo související prováděcí smlouvy*, *název smlouvy*

        Při přidání nové smlouvy zobrazí formulář **Přidat smlouvy** výzvu k vyhledání tohoto souboru.

        Následuje příklad obsahu souboru CSV pro zákazníka s programem Open Value.

        `01-07001, 01-07001, Office agreements`

    -   **Zadat podrobnosti o smlouvě ručně** – vyplňte následující údaje a pak do polí **Autorizační číslo nebo číslo smlouvy** a **Číslo licence, prováděcí smlouvy nebo zákazníka** zadejte páry čísel smluv. Po zadání obou čísel klikněte na ikonu **Přidat pár** a uložte vaše čísla, potom můžete zadat nový pár.

        -   **Název smlouvy** – zadejte jedinečný název smlouvy.

            Název smlouvy může mít maximálně 256 znaků a nesmí obsahovat následující znaky: **~ ! @ # $ ^ &amp; &#42; ( ) = + [ ] { } \ | ; : ' " &lt; &gt; /**. Název může obsahovat mezery.

        -   **Autorizační číslo nebo číslo smlouvy** – zadejte autorizační číslo nebo číslo smlouvy, které odpovídá páru licencí.

        -   **Číslo licence, prováděcí smlouvy nebo zákazníka** – zadejte číslo licence, prováděcí smlouvy nebo zákazníka, které odpovídá páru licencí.

        > [!NOTE]
        > Pokud přidáte několik párů čísel smluv, [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] vytvoří jednu smlouvu s vámi určeným názvem a všechny vámi přidané páry budou součástí této smlouvy.

    Kliknutím na **+** přidáte jinou dvojici čísel smlouvy. Kliknutím na **-** odeberete zadanou dvojici čísel smlouvy.

4.  V oblasti **Vybrat skupinu licencí** proveďte některou z těchto akcí:

    -   Pokud nové smlouvy nechcete přidávat do skupiny, vyberte **Přidat smlouvy do skupiny Nepřiřazené smlouvy**. Pokud se rozhodnete je do skupiny přidat, můžete smlouvu upravit později.

    -   Pokud chcete nové smlouvy přidávat do nové skupiny licencí, vyberte **Přidat smlouvy do nové skupiny licencí**. Zobrazí se výzva k zadání názvu nové skupiny licencí.

    -   Pokud chcete nové smlouvy přidávat do existující skupiny licencí, vyberte **Přidat smlouvy do existující skupiny licencí**. V seznamu **Název skupiny** vyberte skupinu licencí, do které chcete smlouvy přidat.

5.  Klikněte na **OK**.

Zobrazí se seznam **Všechny smlouvy**. Služba [!INCLUDE[sco_dm_2](../Token/sco_dm_2_md.md)] se připojí k centru Microsoft Volume Licensing Service Center, aby ověřila vámi zadané páry čísel smluv.

Pokud chcete po přidání licenčních smluv ve [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] aktualizovat informace o multilicencích, klikněte na stránce **Přehled licencí** na **Aktualizovat**. Tato akce načte aktuální informace o licenci z centra [Microsoft Volume Licensing Service Center (VLSC)](http://go.microsoft.com/fwlink/?LinkId=223842).

> [!IMPORTANT]
> Dokud neaktualizujete informace o multilicencích, můžou se vám v seznamu smluv a informacích o nárocích na stránce **Přehled smluv** zobrazovat rozdílné informace.

Jakmile informace o multilicencích aktualizujete, můžete je v pracovním prostoru **Aplikace** porovnat se zjištěným softwarem od Microsoftu. Můžete taky spustit následující licenční sestavy:

-   **Sestavy zakoupených licencí** – zobrazují licencovaný software ve vybraných skupinách licencí a umožňují najít mezery v pokrytí.

-   **Sestavy nainstalovaných licencí** – pomáhají zjistit, jestli je pokrytí licenčními smlouvami dostatečné.

> [!NOTE]
> **Název produktu** zobrazený pro všechny multilicenční smlouvy s Microsoftem je **Není k dispozici**.

## Přidávání a úprava licenčních smluv k jinému softwaru
Kromě multilicenčních smluv uzavřených s Microsoftem můžete do [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] přidávat i jiné typy licenčních smluv. Tyto smlouvy můžou zahrnovat software jiného výrobce nebo software Microsoftu zakoupený prostřednictvím prodejce.

> [!IMPORTANT]
> Než přidáte smlouvu, musíte mít v [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] zaregistrovaný aspoň jeden počítač s Windows.  Navíc musí aspoň jeden zaregistrovaný počítač odeslat softwarový balíček, který je provozovatelný v licenci a který použijete k přidání licenční smlouvy.

### <a name="BKMK_AddOtherSoftwareAgreement"></a>Přidání jiných smluv na software

1.  V [konzole pro správu Microsoft Intune](https://account.manage.microsoft.com/admin/default.aspx) klikněte na **Licence**.

2.  Klikněte na **Přidat smlouvy** v části **Licenční smlouvy na ostatní software**.

3.  Na stránce **Přidat smlouvy** v části **Zvolit typ smlouvy** vyberte **Licenční smlouva na ostatní software**.

4.  V části **Přidat podrobnosti smlouvy** zadejte toto:

    -   **Název smlouvy** (povinné) Název smlouvy může mít maximálně 256 znaků a nesmí obsahovat následující znaky: **~ ! @ # $ ^ &amp; &#42; ( ) = + [ ] { } \ | ; : ' " &lt; &gt; /**. Název může obsahovat mezery.

    -   **Vydavatel** (povinné) Když začnete psát název vydavatele, služba načte všechny názvy vydavatelů obsahující vámi zadaná písmena. Pokud třeba zadáte „soft“, služba načte všechny vydavatele, kteří mají v názvu řetězec „soft“, například „Microsoft“ a „Microsoft Research“. Názvy vydavatelů se načítají z katalogu Software Asset Catalog. Než budete moct zadat název produktu, musíte vybrat vydavatele.

        > [!IMPORTANT]
        > Společnost, kterou chcete přidat, se v seznamu nemusí zobrazit. Smlouvy na software můžete přidávat jenom pro společnosti, které už figurují v katalogu Software Asset Catalog. Microsoft ale neustále pracuje na přidávání nejoblíbenějších softwarových produktů. Pokud chcete odeslat žádost o přidání určité společnosti do tohoto seznamu, můžete to udělat na webu [Intune Uservoice](https://microsoftintune.uservoice.com/).

    -   **Název produktu** (povinné) Když začnete psát název produktu, služba načte všechny názvy produktů obsahující vámi zadaná písmena. Než budete moct zadat **Název produktu**, musíte určit **Vydavatele**.

    -   **Počet licencí** (povinné) Zadejte počet zakoupených licencí.

    -   **Počáteční datum licence** Zadejte počáteční datum platnosti licence.

    -   **Koncové datum licence** Zadejte koncové datum platnosti licence.

    -   **Podrobnosti smlouvy** Volitelně můžete zadat kontaktní informace, registrační kódy a další informace.

5.  V oblasti **Vybrat skupinu licencí** proveďte některou z těchto akcí:

    -   Pokud nechcete přidávat nové smlouvy do nové nebo existující skupiny licencí, vyberte **Přidat smlouvy do skupiny Nepřiřazené smlouvy**. Smlouvy můžete kdykoli přidat do uživatelem definovaných skupin licencí.

    -   Pokud chcete nové smlouvy přidávat do nové skupiny licencí, vyberte **Přidat smlouvy do nové skupiny licencí**. Zobrazí se výzva k zadání názvu nové skupiny licencí.

    -   Pokud chcete nové smlouvy přidávat do existující skupiny licencí, vyberte **Přidat smlouvy do existující skupiny licencí**. V seznamu **Název skupiny** vyberte skupinu licencí, do které chcete smlouvy přidat.

6.  Klikněte na **OK**.

Zobrazí se zobrazení seznamu **Všechny smlouvy**.

## <a name="BKMK_LicenseGroups"></a>Správa licenčních smluv
Licenční smlouvy na software se dají přidat do skupin licencí. Skupiny licencí můžete použít k uspořádání licenčních smluv v jednotkách vhodných pro vaši organizaci. Můžete taky odstranit licenční smlouvy, které jste vytvořili v minulosti.

|||
|-|-|
|Úloha|Podrobnosti|
|Vytvoření skupiny licencí|V pracovním prostoru **Licence** na stránce **Přehled** klikněte v nabídce **Úlohy** na **Vytvořit skupinu licencí**. **Note:** Celkem můžete vytvořit maximálně 500 skupin licencí.|
|Přejmenování skupiny licencí|V pracovním prostoru **Licence** zvolte skupinu licencí a pak v nabídce **Úlohy** klikněte na **Upravit skupinu licencí**.|
|Odstranění skupiny licencí|V pracovním prostoru **Licence** zvolte skupinu licencí a pak v nabídce **Úlohy** klikněte na **Odstranit skupinu licencí**. **Tip:** Všechny licence se z odstraněné skupiny přesunou do skupiny licencí **Nepřiřazené smlouvy**.|
|Odstranění licenční smlouvy|V pracovním prostoru **Licence** zvolte smlouvu a klikněte na **Odstranit**. **Tip:** Pokud chcete po odstranění multilicenčních smluv aktualizovat informace o licenci, klikněte na **Aktualizovat** na stránce **Přehled licencí** nebo na kartě **Obecné** konkrétní skupiny licencí.|

## Viz také
[Nasazení aplikací do počítačů s Windows v Microsoft Intune](../Topic/Deploy_apps_to_Windows_PCs_in_Microsoft_Intune.md)

