---
description: na
keywords: na
title: Windows Team configuration policy settings in Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 38194ef3-e26e-4682-958d-14b395fccba1
---
# Nastaven&#237; z&#225;sad konfigurace pro Windows Team v Microsoft Intune
Použijte [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] **Obecné zásady konfigurace pro Windows 10 Team** ke konfiguraci nastavení pro registrovaná zařízení se systémem Windows 10, jako je například Microsoft Surface Hub.

## Vytvoření zásady konfigurace pro Windows 10 Team

#### Zadání základního nastavení pro zásadu konfigurace

1.  V [konzole pro správu Microsoft Intune](https://manage.microsoft.com) klikněte na **Zásady** &gt; **Přehled** &gt; **Přidat zásadu**.

2.  Klikněte na **Windows** &gt; **Obecná konfigurace (Windows 10 Team a novější)** a potom klikněte na **Vytvořit zásadu**.

    > [!NOTE]
    > Nedaří se vám vytvořit zásadu konfigurace pomocí doporučovaného nastavení. Je potřeba vytvořit vlastní zásadu.

3.  V části **Obecné** stránky **Vytvořit zásadu** zadejte název a popis nové zásady.

4.  Informace v následující části vám pomůžou zadat nastavení zásad.

5.  Po dokončení klikněte na **Uložit zásadu**.

Nová zásada se zobrazí v uzlu **Zásady konfigurace** pracovního prostoru **Zásady**.

## <a name="BKMK_Settings"></a>Seznam nastavení pro tuto zásadu

### <a name="BKMK_sec"></a>Nastavení zařízení

|Název nastavení|Podrobnosti|
|-------------------|---------------|
|**Povolit automatické probuzení obrazovky, když je někdo v místnosti**|Umožňuje zařízení automatické probuzení, když jeho senzor zachytí osobu v místnosti.|
|**Vyžadovat kód PIN pro bezdrátovou projekci**|Určuje, jestli před použitím možností bezdrátové projekce zařízení musíte zadat kód PIN.|
|**Nastavit okno údržby**|Konfiguruje okno při provádění aktualizací na zařízení. Můžete nakonfigurovat čas zahájení okna a jeho trvání (1 až 5 hodin).|

## Nasazení zásad konfigurace

1.  Nasaďte zásadu konfigurace do jedné nebo víc skupin uživatelů nebo zařízení ve vaší organizaci.

Další informace o tom, jak nasazovat zásady, najdete v tématu [Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md).

Souhrn stavu a výstrahy v pracovním prostoru **Zásada** určují problémy se zásadou, které vyžadují vaši pozornost. Kromě toho se v pracovním prostoru **Řídicí panel** zobrazí shrnutí stavu.

## Viz také
[Použití zásad ke správě počítačů a mobilních zařízení s Microsoft Intune](../Topic/Use_policies_to_manage_computers_and_mobile_devices_with_Microsoft_Intune.md)

