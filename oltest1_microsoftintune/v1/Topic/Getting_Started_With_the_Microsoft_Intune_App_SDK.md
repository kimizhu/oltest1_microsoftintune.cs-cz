---
description: na
keywords: na
title: Getting Started With the Microsoft Intune App SDK
search: na
ms.date: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 38ebd3f5-cfcc-4204-8a75-6e2f162cd7c1
---
# Zač&#237;n&#225;me s Microsoft Intune App SDK
Tato úvodní příručka vám pomůže rychle povolit mobilní aplikace pro správu mobilních aplikací s Microsoft Intune. Může být vhodné si nejdřív přečíst App dokument [Výhody Intune App SDK](Benefits_of_the_Intune_App_SDK.md) a pochopit výhody sady Intune App SDK.

Tento průvodce vás provede důležitými kroky potřebnými k povolení správy mobilních aplikací ve vaší aplikaci s Microsoft Intune. Sada Intune App SDK podporuje podobné scénáře napříč platformami a je určená k vytvoření konzistentní konzistentního prostředí napříč platformami pro správce IT. Existují ale malé rozdíly v podpoře některých funkcí kvůli omezením platforem.

# Getting Started (Začínáme)

## Registrace pro Microsoft Connect

Sada Intune App SDK je aktuálně přístupná prostřednictvím webu Microsoft Connect a vyžaduje přihlášení. Abyste to mohli provést, zaregistrujte si [účet Microsoft](https://connect.microsoft.com/ConfigurationManagervnext/InvitationUse.aspx?ProgramID=8967&InvitationID=8967-YJYJ-8G6X) pomocí podnikového e-mailu.

Registrace bude v nevyřízeném stavu, dokud tým Intune nezkontroluje vaši žádost. Obvyklá doba odezvy se pohybuje do 2 až 3 pracovních dnů. Po schválení obdržíte e-mailem oznámení s odkazy na stažení sady Intune App SDK pro vaše platformy a všechny příslušné průvodce. K těmto průvodcům můžete také přistupovat na webu MSDN.

## Registrace aplikace z App Storu s Microsoft Intune

**Pokud vaše povolená aplikace je interní a nebude zpřístupněna v App Storu Apple nebo Google**: Není nutné aplikaci registrovat. Tyto interní aplikace správce IT načte přímo do konzoly Microsoft Intune pro nasazení, Intune detekuje, že aplikace byla vytvořena pomocí sady SDK, a nabídne správci IT možnost použít na ni zásady MAM. Můžete přeskočit k části s názvem [Povolení mobilní aplikace systému iOS nebo Android pro MAM s SDK](#enableapp).

**Pokud jste nezávislý dodavatel softwaru vyvíjející aplikaci, která bude přístupná zákazníkům prostřednictvím App Storu Apple nebo Google**: Musíte nejprve registrovat aplikaci s Microsoft Intune a přijmout podmínky registrace. V tuto chvíli můžete poskytnout přímý odkaz na aplikaci. Potom může správce IT použít na aplikaci zásady MAM Intune. Do dokončení a potvrzení registrace týmem Microsoft Intune nebude možné na přímý odkaz na vaší aplikaci použít v  konzole správce zásady MAM. Microsoft také udržuje partnerský web Microsoft Intune, kde bude aplikace registrovaná, aby zákazníci věděli, že podporuje zásady MAM Microsoft Intune MAM.

Pokud chcete zahájit proces registrace, **přečtěte si a podepište** partnerskou smlouvu Microsoft Intune. Tato smlouva popisuje podmínky, které vaše společnost musí splnit, než se stane partnerem aplikací Microsoft Intune. Před zobrazením tohoto dokumentu se musíte přihlásit. Smlouvu najdete na webu Microsoft Connect sady Intune App SDK na kartě Průzkumy nebo zde. Také vás požádáme o poskytnutí názvu aplikace, názvu vaší společnosti a přímý odkaz na aplikaci ve storu Google nebo iTunes.

![Microsoft Connect](/Image/Microsoft_Connect.png)

K potvrzení a dokončení procesu registrace použijeme e-mailovou adresu použitou při registraci. Navíc použijeme e-mailovou adresu použitou při registraci, abychom vás v případě nejasností kontaktovali.

**Co očekávat při procesu registrace**: Po odeslání formuláře budete kontaktováni Microsoftem prostřednictvím e-mailové adresy použité při registraci, abyste potvrdili příjem nebo abychom si vyžádali dodatečné informace k dokončení registrace. Budete také kontaktováni, když bude aplikace úspěšně registrovaná s Microsoft Intune a když bude uvedena na partnerském webu Microsoft Intune. Po potvrzení přijetí informací bude přímý odkaz na vaši aplikaci zahrnut v aktualizaci Microsoft Intune pro příští měsíc. Pokud je například proces registrace dokončený v červenci, přímý odkaz na aplikaci bude podporován v polovině srpna. Pokud se v budoucnu přímý odkaz na aplikace ve Storu změní, musíte aplikaci znovu zaregistrovat. Také nás informujte v případě, že aktualizujete aplikaci s novou verzí sady Intune App SDK.

**Poznámka**: Se všemi informacemi shromážděnými prostřednictvím výše uvedeného formuláře a prostřednictvím e-mailové korespondence s týmem Intune se nakládá v souladu s [Prohlášením o zásadách ochrany osobních údajů společnosti Microsoft](https://www.microsoft.com/en-us/privacystatement/default.aspx).

## <a name="enableapp"></a> Povolení mobilní aplikace systému iOS nebo Android pro MAM s SDK

K povolení mobilních aplikací systému iOS musíte provést následující akce:

1. **[Příručka vývojáře sady Intune App SDK pro systém iOS](Microsoft_Intune_App_SDK_for_iOS_Developer_Guide.md)**: Tento dokument vás detailně provede procesem povolování mobilních aplikací pro systém iOS se sadou Intune App SDK. Tento dokument najdete ve složce dokumentace, kterou jste si stáhli jako součást balíčku Intune App SDK.
2. **Intune App SDK pro systém iOS**: Jakou součást balíčku Intune App SDK staženého z Microsoft Intune najdete složku označenou Intune App SDK for iOS. Tato složka obsahuje celou sadu Intune App SDK pro systém iOS.

K povolení mobilních aplikací systému Android se sadou Intune App SDK musíte provést následující akce:

1. **Příručka vývojáře sady Intune App SDK pro systém Android**: Tento dokument vás detailně provede procesem povolování mobilních aplikací pro systém Android se sadou Intune App SDK. Tento dokument najdete ve složce dokumentace, kterou jste si stáhli jako součást balíčku Intune App SDK.
2. **Intune App SDK pro systém Android**: Jakou součást balíčku Intune App SDK staženého z Microsoft Intune najdete složku označenou Intune App SDK for Android. Tato složka obsahuje celou sadu Intune App SDK pro systém Android.

## Vypnutí telemetrie pro aplikaci

**Vývojáři sady SDK iOS MAM**: Sada SDK ve výchozím nastavení protokoluje telemetrická data sady SDK o událostech využití. Tato data se odešlou do Microsoft Intune.

Pokud se rozhodnete neodesílat telemetrická data sady SDK z vaší aplikace do Microsoft Intune, **musíte zakázat** přenos telemetrie sady SDK v `IntuneMAMSettings` nastavením vlastnosti `MAMTelemetryDisabled` na hodnotu YES.

**Vývojáři sady SDK Android MAM**: Telemetrie sady SDK se neprotokoluje prostřednictvím sady SDK.

## Testování aplikace s povoleným MAM s Microsoft Intune

Po dokončení nezbytných kroků k vylepšení (integraci sady Intune App SDK) vaší sady Intune App SDK pro systém iOS nebo Android se musíte ujistit, že všechny zásady správy aplikací jsou povolené a fungují pro koncové uživatele a správce IT. K testování vylepšené aplikace budete potřebovat toto:

1. **Testování aplikace s povoleným MAM s Microsoft Intune**: Tento průvodce vás detailně provede postupem testování vylepšených aplikací pro systém iOS nebo Android s Microsoft Intune. Tento dokument najdete ve složce dokumentace, kterou jste si stáhli jako součást balíčku Intune App SDK.
2. **Účet Microsoft Intune**: To K testování aplikace s povoleným MAM s Microsoft Intune budete potřebovat účet Microsoft Intune. Pokud jste nezávislý dodavatel softwaru povolující MAM pro aplikace z App Storu pro iOS nebo Android, obdržíte po dokončení registrace s Microsoft Intune podle pokynů k registraci propagační kód. Propagační kód vám umožní přihlásit se k 1 roku používání zkušební verze Microsoft Intune navíc. Pokud vyvíjíte podnikovou aplikaci, která nebude odeslaná do Storu, předpokládá se, že máte přístup k Microsoft Intune prostřednictvím vaší organizace. Můžete se také přihlásit k měsíční zkušební verzi zdarma s [Microsoft Intune](https://portal.office.com/Signup/Signup.aspx?OfferId=40BE278A-DFD1-470a-9EF7-9F2596EA7FF9&dl=INTUNE_A&ali=1#0).





