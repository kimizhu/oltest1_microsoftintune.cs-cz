---
description: na
keywords: na
title: Your computer is already enrolled
search: na
ms.date: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 8d3a40f5-99e9-48dc-9706-f7a3a23e5704
---
# V&#225;š poč&#237;tač je už zaregistrovan&#253;
Tato stránka se zobrazuje, protože jste spustili instalační program pro klientský software [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)]. Software je už ale na počítači nainstalovaný a instalační program nemůže pokračovat.

To může mít následující příčiny:

-   Klientský software už byl nainstalovaný a znovu se spustil instalační program.

-   Instalační program byl na počítači spuštěný potom, co správce IT vaše zařízení ze služby [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] vyřadil. Po vyřazení zařízení může trvat několik hodin, než se klientský software z počítače odebere.

-   Instalační program zjistil nedávno neúspěšnou instalaci nebo neúspěšné odebrání klientského softwaru.

## <a name="bkmk_install"></a>Co instalační program nainstaluje do počítače
Instalační program nainstaluje klienta [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Po dokončení instalace zůstane klientský software spuštěný na pozadí, kde nakonfiguruje počítač pro používání se službou [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Dokončení tohoto procesu může nějakou dobu trvat a zahrnuje:

-   Registrace počítače do služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]

-   Odeslání inventáře o hardwaru počítače a nainstalovaném softwaru

-   Konfigurace zásad [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], včetně instalace služby Endpoint Protection (pokud je nakonfigurovaná)

-   Instalace softwaru [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Center

Po instalaci softwaru [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Center můžete jeho prostřednictvím získat přístup k firemnímu portálu, kde můžete své počítače propojit s vaším pracovním účtem.

## <a name="bkmk_center"></a>Microsoft Intune Center
[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Center se na počítači nainstaluje jako aplikace poté, co počítač úspěšně nainstaluje klientský software a zaregistruje počítač do služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]. Pomocí aplikace [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Center můžete:

-   **Získat aplikace z firemního portálu** – najděte a instalujte aplikace, které nasadil váš správce IT. Při prvním přihlášení k firemnímu portálu na nově zaregistrovaném počítači získáte možnost propojit váš pracovní účet s tímto počítačem.

-   **Zjišťovat aktualizace softwaru** – najděte aktualizace softwaru, které jsou nasazené vaším správcem služby [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

-   **Spustit kontrolu počítače službou Endpoint Protection** – můžete spustit kontrolu škodlivého softwaru na vašem počítači.

-   **Požádat o vzdálenou pomoc** – tato možnost je k dispozici jenom v případě, že vzdálenou pomoci podporuje operační systém počítače.

## <a name="bkmk_validate"></a>Ověření, jestli je klientský software nainstalovaný nebo byl odebraný
**Ověření, jestli je klient nainstalovaný:**
Instalace klienta [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] je dokončená, pokud jsou na počítači k dispozici následující aplikace:

-   **[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Center**

-   **[!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Endpoint Protection** (pokud je služba Endpoint Protection povolená vaším správcem IT)

Pokud umíte pracovat se Správcem úloh, můžete vyhledat klientskou službu [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)], která by měl být spuštěná:

-   **OmcSvc**

**Ověření, jestli byl klient odebraný:**
Po odinstalování klienta [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] z počítače se odeberou aplikace, které byly nainstalované při instalaci klienta, včetně aplikace [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] Center.

Klientská služba [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)]**OmcSvc** se odebere.

## <a name="bkmk_remove"></a>Jak klientský software z počítače odebrat
Ve výchozím nastavení se klientský software [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] odinstaluje několik hodin poté, co správce IT váš počítač vyřadí z konzole pro správu [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)].

K ruční odinstalaci klientského softwaru [!INCLUDE[wit_nextref](../Token/wit_nextref_md.md)] z počítače můžete použít následující kroky, které odinstalaci vynutí:

1.  Na počítači otevřete příkazový řádek v režimu správce.

2.  Přejděte do složky **%programfiles%\Microsoft\OnlineManagement\Common**.

3.  Spusťte následující příkaz: **ProvisioningUtil.exe /UninstallAgents /MicrosoftIntune**

Tím se naplánuje odebrání klientského softwaru.

