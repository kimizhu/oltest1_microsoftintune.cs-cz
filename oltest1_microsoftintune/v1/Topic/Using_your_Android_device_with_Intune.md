---
description: na
keywords: na
title: Using your Android device with Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 465763db-b68d-4392-a5a4-732b5b875c2b
---
# Použit&#237; zař&#237;zen&#237; Android s&#160;Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="cs-CZ">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink">
      <introduction>
        <para>
          <caps:sentence sentenceid="8e84352dc3925fd78cdd7f5fef36efa7" id="tgt1" class="tgtSentence">Tyto kroky použijte pro úlohy, které musíte udělat na zařízení s Androidem, když vaše společnost používá Microsoft Intune:</caps:sentence>
        </para>
        <table border="1">
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="54daf68978f49ad4d646edd222e602f1" id="tgt2" class="tgtSentence">Kategorie úloh</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="e86e187e7bbea2eea4ad12ab7734221e" id="tgt3" class="tgtSentence">Úlohy, které můžete provést</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="e6a2a3272b06e3df4f17efdd8970c4a3" id="tgt4" class="tgtSentence">Instalace aplikace Portál společnosti a registrace ve službě Intune</caps:sentence>
                </para>
              </TD>
              <TD>
                <list class="bullet">
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_install_cp_app">Install the Microsoft Intune Company Portal app</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_signin_cp">Sign in to the Company Portal</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_enroll_devc">Enroll your device in Intune</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_what_happs_add">What happens when I install the Company Portal app and enroll my device in Intune?</link>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="f043154e08f9b3476e587eb2d7bdb007" id="tgt5" class="tgtSentence">Kroky, které můžete provést po registraci zařízení do služby Intune</caps:sentence>
                </para>
              </TD>
              <TD>
                <list class="bullet">
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_whatis_cp_website">What is the Company Portal website and what can I do with it?</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_encrypt_your_device">Encrypt your device</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_set_pin">Set your PIN or password</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_install_vpn">Install your company's Virtual Private Network (VPN)</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_unenroll_device">Unenroll your device from Intune</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_erase_lost_device">Reset (erase) your lost or stolen device</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_data_collect">Turn off Microsoft usage data collection</link>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="c6dc0f40f1debc9ce66e6c01a76742f2" id="tgt6" class="tgtSentence">Oprava problémů se zařízením </caps:sentence>
                </para>
              </TD>
              <TD>
                <list class="bullet">
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_fix_issues">Fix issues when your device is enrolled in Intune</link>
                    </para>
                    <list class="bullet">
                      <listItem>
                        <para>
                          <link xlink:href="#BKMK_andr_verboselogging">Use Verbose Logging to help your IT admin fix issues</link>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <link xlink:href="#BKMK_andr_send_diag_logs">Send diagnostic data logs to your IT admin using email</link>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <link xlink:href="#BKMK_andr_send_diag_usbcable">Send diagnostic data logs to your IT admin using a USB cable</link>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <link xlink:href="#BKMK_andr_send_enroll_errors">Send enrollment errors to your IT admin</link>
                        </para>
                      </listItem>
                    </list>
                  </listItem>
                </list>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section expanded="true" address="BKMK_andr_install_cp_app">
        <title>
          <caps:sentence sentenceid="ee6e4eec4eee8a91c4878544868a748a" id="tgt7" class="tgtSentence">Instalace aplikace Portál společnosti služby Microsoft Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="bcc9ebff81099e0055eecc4f9b04f424" id="tgt8" class="tgtSentence">Portál společnosti je aplikace, která po instalaci do vašeho zařízení umožňuje přístup k podnikovým nebo školním aplikacím, e-mailům a síti.</caps:sentence>
            <caps:sentence sentenceid="dda3e2c0b909ad0d8c50a1d863aa82a0" id="tgt9" class="tgtSentence">  Než získáte přístup, musíte aplikaci Portál společnosti nainstalovat a pak v ní zaregistrovat své zařízení do služby Microsoft Intune.</caps:sentence>
            <caps:sentence sentenceid="5d9ec8c42c2995e1314461554a305101" id="tgt10" class="tgtSentence"> Další informace o tom, co registrace znamená, najdete v tématu <link xlink:href="#BKMK_andr_what_happs_add">What happens when I install the Company Portal app and enroll my device in Intune?</link>.</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt11" class="tgtSentence">Klepněte na <ui>Domů</ui> &gt; <ui>Play Store</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt12" class="tgtSentence">Do pole <ui>vyhledávání</ui> napište <ui>portál společnosti</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt13" class="tgtSentence">Klepněte na <ui>Portál společnosti Intune</ui>.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="8fe9ef88-1360-4018-aa94-de83f09cb439"></image>
              </mediaLink>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt14" class="tgtSentence">Klepněte na <ui>INSTALOVAT</ui>.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="e41358ab-3546-48ca-973e-e3988f519676"></image>
              </mediaLink>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt15" class="tgtSentence">Klepněte na <ui>PŘIJMOUT</ui>.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="b9366110-0d9a-4848-8357-395933976720"></image>
              </mediaLink>
            </listItem>
          </list>
        </content>
      </section>
      <section expanded="true" address="BKMK_andr_signin_cp">
        <title>
          <caps:sentence sentenceid="9f7379f0c4fb464834165f34da1a6a7f" id="tgt16" class="tgtSentence">Přihlášení k portálu společnosti</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="2bb5411102d14c4ba5dc662521c32993" id="tgt17" class="tgtSentence">Když je aplikace Portál společnosti nainstalovaná, musíte se přihlásit k aplikaci a zaregistrovat zařízení v Intune.</caps:sentence>
            <caps:sentence sentenceid="21c131ab9d7bb47da9c359ca3dbb1e4a" id="tgt18" class="tgtSentence"> Po dokončení registrace se můžete k aplikaci Portál společnosti kdykoli přihlásit, stáhnout firemní aplikace a dělat další věci.</caps:sentence>
            <caps:sentence sentenceid="40c6475458964e1be627eb195d0a677b" id="tgt19" class="tgtSentence"> Další informace o tom, co můžete dělat dál, najdete v tématu <link xlink:href="#BKMK_andr_what_happs_add">What happens when I install the Company Portal app and enroll my device in Intune?</link>.</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt20" class="tgtSentence">V seznamu aplikací klepněte na <ui>Portál společnosti</ui>.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="fd42b202-1e8d-4dec-b0d9-2bb5025a8685"></image>
              </mediaLink>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt21" class="tgtSentence">Na <ui>úvodní</ui> obrazovce klepněte na <ui>Přihlásit</ui>.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="d1bd8a99-5433-4d86-8678-02bb157b6531"></image>
              </mediaLink>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="af8ca93c727c77483a702f613d65e6cc" id="tgt22" class="tgtSentence">Zadejte svůj pracovní nebo školní e-mail a heslo a pak klepněte na <ui>Přihlásit</ui>.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="5542d597-0ff4-4858-ba2b-eb909052c3c6"></image>
              </mediaLink>
              <para>
                <caps:sentence sentenceid="88f4e8855abbb6dcb06cd5d805fb89d4" id="tgt23" class="tgtSentence">Když se k portálu společnosti přihlašujete poprvé a vaše společnost nebo škola využívá Intune, budete vyzváni k registraci svého zařízení v Intune.</caps:sentence>
                <caps:sentence sentenceid="5e948074b31b8a9455d72a9372e2f24d" id="tgt24" class="tgtSentence"> Při registraci použijte postup v tématu <link xlink:href="#BKMK_andr_enroll_devc"> Enroll your device in Intune</link>.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section expanded="true" address="BKMK_andr_enroll_devc">
        <title>
          <caps:sentence sentenceid="d065e047890c2ebd02738f563a483d28" id="tgt25" class="tgtSentence"> Registrace zařízení v Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="92ec96c905048e2c17c94c973607a519" id="tgt26" class="tgtSentence">Po registraci zařízení do služby Intune můžete získat přístup k podnikové síti a také k pracovním e-mailům, pracovním souborům a firemním aplikacím.</caps:sentence>
            <caps:sentence sentenceid="e0110f9a2b949d7448b9ccf2746029f1" id="tgt27" class="tgtSentence"> Další informace o tom, co všechno můžete po registraci dělat, najdete v tématu <link xlink:href="#BKMK_andr_what_happs_add">What happens when I install the Company Portal app and enroll my device in Intune?</link>.</caps:sentence>
            <caps:sentence sentenceid="ef4da4bff79fb49620cdc2eca640b8c8" id="tgt28" class="tgtSentence"> Pokud při pokusu o registraci narazíte na problémy, projděte si téma <link xlink:href="#BKMK_andr_send_enroll_errors">Send enrollment errors to your IT admin</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="ceba66042f88d32b94366c1376481552" id="tgt29" class="tgtSentence">Při registraci použijte postup odpovídající typu zařízení, které máte:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <link xlink:href="#BKMK_andr_enroll_native">Enroll your native (non-Samsung device in Intune)</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="#BKMK_andr_enroll_knox">Enroll your Samsung Knox device in Intune</link>
              </para>
            </listItem>
          </list>
        </content>
        <sections>
          <section address="BKMK_andr_enroll_native">
            <title>
              <caps:sentence sentenceid="20f534249b00807c2ca547e95761f998" id="tgt30" class="tgtSentence">Registrace nativního zařízení (jiného zařízení než Samsung) do služby Intune</caps:sentence>
            </title>
            <content>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="119edf7313e9135f1531299a00b51371" id="tgt31" class="tgtSentence">Na <ui>úvodní</ui> obrazovce portálu společnosti klepněte na <ui>Přihlásit</ui> a pak se přihlaste pomocí svého pracovního nebo školního účtu.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="d1bd8a99-5433-4d86-8678-02bb157b6531"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="38af4722b5d89342a4d477c21ddb27ab" id="tgt32" class="tgtSentence">Pokud váš správce IT nastavil firemní podmínky a ujednání, přijměte je klepnutím na <ui>PŘIJMOUT</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="930b52ef-2c50-4fe8-b551-624e757781f4"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt33" class="tgtSentence">Klepněte na <ui>REGISTROVAT</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="161a5f87-3d27-43bf-8b0a-8bfea06d61cf"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt34" class="tgtSentence">Klepněte na <ui>Aktivovat</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="71bd0ea7-259a-468c-b312-a3cf820ba956"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="2b1deb508a675f2cf878e281fccf3338" id="tgt35" class="tgtSentence">Podle pokynů zadejte kód PIN nebo heslo.</caps:sentence>
                    <caps:sentence sentenceid="9767dc1ea2848fa19a8e292a3bb6362c" id="tgt36" class="tgtSentence"> Pokud jste už kód PIN nebo heslo v daném zařízení nastavili, tato obrazovka se buď neobjeví, nebo budete muset zadat nový kód PIN a heslo.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="3167bf58-b9f3-4260-9ffd-4ca22f633ec4"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="38c28950a6f94d6d3f4e8733ad9bccff" id="tgt37" class="tgtSentence">Na obrazovce <ui>Název certifikátu</ui> přijměte výchozí certifikát klepnutím na <ui>OK</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="e9c96498-e528-4694-bdcc-80ebc7cbd9e4"></image>
                  </mediaLink>
                  <para>
                    <caps:sentence sentenceid="8168930ae7ae8157d6f688dc187f9f6a" id="tgt38" class="tgtSentence">Právě jste zaregistrovali své zařízení do služby Intune.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="f849a26d081e296a39efd57b2eff545a" id="tgt39" class="tgtSentence">Pokud při pokusu o registraci zařízení do služby Intune dojde k chybě, projděte si téma <link xlink:href="#BKMK_andr_send_enroll_errors">Send enrollment errors to your IT admin</link>.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_andr_enroll_knox">
            <title>
              <caps:sentence sentenceid="bf108b7344f13ecf0abde91c6b70411d" id="tgt40" class="tgtSentence">Registrace zařízení Samsung Knox do služby Intune</caps:sentence>
            </title>
            <content>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="b3feb8aaf4b8cee01e15dad758697df0" id="tgt41" class="tgtSentence">Na úvodní obrazovce portálu společnosti klepněte na Přihlásit a pak se přihlaste pomocí svého pracovního nebo školního účtu.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="d1bd8a99-5433-4d86-8678-02bb157b6531"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="38af4722b5d89342a4d477c21ddb27ab" id="tgt42" class="tgtSentence">Pokud váš správce IT nastavil firemní podmínky a ujednání, přijměte je klepnutím na <ui>PŘIJMOUT</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="930b52ef-2c50-4fe8-b551-624e757781f4"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt43" class="tgtSentence">Klepněte na <ui>REGISTROVAT</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="161a5f87-3d27-43bf-8b0a-8bfea06d61cf"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt44" class="tgtSentence">Klepněte na <ui>AKTIVOVAT</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="c68d1754-e1a7-4906-a3dc-f13673f7c8d3"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="3221064bbc2e7c9caf89313a3d70ccdc" id="tgt45" class="tgtSentence">Přijměte zásady ochrany osobních údajů řešení Samsung Knox a klepněte na <ui>Potvrdit</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="595681eb-d7f3-47a8-a95d-a427d903a241"></image>
                  </mediaLink>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="8168930ae7ae8157d6f688dc187f9f6a" id="tgt46" class="tgtSentence">Právě jste zaregistrovali své zařízení do služby Intune.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section address="BKMK_andr_what_happs_add">
        <title>
          <caps:sentence sentenceid="c7771a0e09cd91e94fb6776ff1223ac3" id="tgt47" class="tgtSentence">Co se stane, když nainstaluji aplikaci Portál společnosti a zaregistruji zařízení do služby Intune?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f0401535f7b1ac877b8f6af14bd6c40d" id="tgt48" class="tgtSentence">Nejdřív nainstalujete aplikaci Portál společnosti a pak v ní zaregistrujete své zařízení do služby Intune.</caps:sentence>
            <caps:sentence sentenceid="9af3ed7432137e078ac63133e9bdc49a" id="tgt49" class="tgtSentence"> Po registraci svého zařízení můžete v aplikaci Portál společnosti provádět tyto kroky:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="cd1a40a617eb283f621ef494fdaa498f" id="tgt50" class="tgtSentence">Přístup k podnikové síti, e-mailu a dalším pracovním souborům</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="365f2777fae357fc28b1489affab4a54" id="tgt51" class="tgtSentence">Získání aplikací společnosti z Portálu společnosti</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="7c7476a0520e0468f40a091eecb0d594" id="tgt52" class="tgtSentence">Automatická konfigurace e-mailového účtu vaší společnosti</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="66b07c74bf99f92822a9939daafde7d3" id="tgt53" class="tgtSentence">Obnovení továrního nastavení telefonu v případě ztráty nebo odcizení</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="9580373c6a8f78a774ff06c526b5e360" id="tgt54" class="tgtSentence">Když své zařízení zaregistrujete do služby Intune, správci IT tím udělíte oprávnění ke správě vašich zařízení, aby bylo možné lépe chránit informace společnosti na daném zařízení.</caps:sentence>
          </para>
          <table border="1">
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="49b5c06f816b80fa0b53001b7e064dd0" id="tgt55" class="tgtSentence">IT neuvidí</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="919967a6e68fc799764ccfadd49d0d82" id="tgt56" class="tgtSentence">IT uvidí</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="7b15a2dc20f223897228983bcb839a0d" id="tgt57" class="tgtSentence">Historie volání</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="b5c1e4334dd619fce44e7a047bd05a8d" id="tgt58" class="tgtSentence">Textové zprávy</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="936249fa98a3357097ff1f12312225b4" id="tgt59" class="tgtSentence">Osobní e-maily, kontakty a kalendář</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="827a82394f446cc4d02c0fd5e61f331b" id="tgt60" class="tgtSentence">Webová historie</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="d5189de027922f81005951e6efe0efd5" id="tgt61" class="tgtSentence">Umístění</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="b99bbccd22c782c7f7019bad4a0628f2" id="tgt62" class="tgtSentence">Z fotoaparátu</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="2c5a2582707f1495992f8b6befe92a6c" id="tgt63" class="tgtSentence">Osobní data</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="72122ce96bfec66e2396d2e25225d70a" id="tgt64" class="tgtSentence">Vlastník</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="712778275c556c187fb77a2b8a2af8c4" id="tgt65" class="tgtSentence">Název zařízení</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c9f4029ce9dcf8ff7f8f1b70edead843" id="tgt66" class="tgtSentence">Sériové číslo</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c2904bca62b22443d6cf5e9d89cab204" id="tgt67" class="tgtSentence">Výrobce</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="20f35e630daf44dbfa4c3f68f5399d8c" id="tgt68" class="tgtSentence">Model</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="d83f147fd8043b67aa813f44f597b39b" id="tgt69" class="tgtSentence">Operační systém</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="93a4cf66e1c393e83e3c39b8446f1b71" id="tgt70" class="tgtSentence">Firemní aplikace</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="a2da362c93e6fb8f4d57947fe2b2d8fd" id="tgt71" class="tgtSentence">Osobní aplikace</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="7a9bb338270201243cf6be9e712925f2" id="tgt72" class="tgtSentence">Když přidáte zařízení se systémem Android, udělujete správci IT oprávnění k přístupu k zařízení.</caps:sentence>
            <caps:sentence sentenceid="c1c2c0f76e506e4c114e45f70033641c" id="tgt73" class="tgtSentence"> Může provádět například následující akce:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="2833d6f47e693959641866661f074157" id="tgt74" class="tgtSentence">Obnovit v zařízení výchozí tovární nastavení.</caps:sentence>
                <caps:sentence sentenceid="ec2b174c8222d31c80eac2abd68f4f60" id="tgt75" class="tgtSentence"> To je užitečné v případě ztráty nebo odcizení zařízení.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="bbad2fb68e3185a447cf6d63dfb15354" id="tgt76" class="tgtSentence">Odebrat veškerá firemní data.</caps:sentence>
                <caps:sentence sentenceid="bebc79fbe14286bcca2d83d606469094" id="tgt77" class="tgtSentence"> Vaše osobní údaje a nastavení se při tom neodeberou.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="9ce5937038a7840eaa9bbba565e419a8" id="tgt78" class="tgtSentence">Požadovat, abyste si v zařízení nastavili heslo nebo PIN kód, přičemž v případě příliš velkého počtu chybných pokusů o zadání hesla může dojít k zablokování zařízení nebo obnovení zařízení do výchozího továrního nastavení.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c1aa6cfa75e3c98c83374293c4279f76" id="tgt79" class="tgtSentence">Vyžadovat, abyste přijali smluvní podmínky.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f9877cfa9f701abb70b52dc01c3d35e7" id="tgt80" class="tgtSentence">Povolit nebo zakázat používání fotoaparátu/kamery v zařízení.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f588fae704de8edfd6f8cdc33793d3f0" id="tgt81" class="tgtSentence">Vynutit šifrování všech dat v zařízení, včetně firemních a osobních údajů.</caps:sentence>
                <caps:sentence sentenceid="069e34665f9e53073d27ad97b440e0ce" id="tgt82" class="tgtSentence"> Tím jsou data chráněna v případě ztráty nebo odcizení zařízení.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="4370aca60d1ad253c0dc1c64f9b54f90" id="tgt83" class="tgtSentence">Po přidání vašeho zařízení na portál společnosti přibližně každých 8 hodin proběhnou tyto kroky:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="5ba4cc4bde2dd286214e46b9c9155365" id="tgt84" class="tgtSentence">Stažení všech zásad nebo aktualizací aplikací, které vám správce IT zpřístupnil.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="e135d12cb140527861d03d871f7d01ec" id="tgt85" class="tgtSentence">Odeslání všech aktualizací inventáře hardwaru (tyto aktualizace neobsahují osobní informace).</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="ea917e0cc0b6f20af749331177b9f8e0" id="tgt86" class="tgtSentence">Odeslání všech aktualizací inventáře aplikací společnosti (tyto aktualizace neobsahují osobní informace).</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
          </list>
        </content>
      </section>
      <section expanded="true" address="BKMK_andr_whatis_cp_website">
        <title>
          <caps:sentence sentenceid="631be7185536cbfc0dd9092b681d30e8" id="tgt87" class="tgtSentence">Co je web portálu společnosti a k čemu ho můžu použít?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e3eb16afdbabab150c5da0ade825a14d" id="tgt88" class="tgtSentence">
              <externalLink>
                <linkText>Web portálu společnosti</linkText>
                <linkUri>http://portal.manage.microsoft.com</linkUri>
              </externalLink> je webové rozhraní vaší společnosti, pomocí kterého můžete spravovat pracovní počítače a zařízení a také osobní počítače a zařízení, které chcete použít v práci.</caps:sentence>
            <caps:sentence sentenceid="70037d25cd497b5572e18d1bc35334bc" id="tgt89" class="tgtSentence"> Většinu úloh můžete provést jak na tomto webu, tak v aplikaci Portál společnosti, kterou si nainstalujete do svého zařízení.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="14d658610fe447e446e50ce288d1edc1" id="tgt90" class="tgtSentence">Na webu portálu společnosti můžete provádět tyto úlohy:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="3dc0b17542da2ec9d90ff0965d19aef1" id="tgt91" class="tgtSentence">Vyhledat a stáhnout firemní aplikace</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f82609801e7080daebaa60a46cd06e57" id="tgt92" class="tgtSentence">Přejmenovat zařízení</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="2e254e163be6b2905cf22931f4eb4fe0" id="tgt93" class="tgtSentence">Odebrat zařízení z Intune</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="680b802dd6afc46294bf85411f86cccf" id="tgt94" class="tgtSentence">Obnovit výchozí tovární nastavení v mobilním zařízení</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ed64c84b76d070c3000586dc8cade916" id="tgt95" class="tgtSentence">Vyhledat kontaktní informace pro správce IT</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section address="BKMK_andr_encrypt_your_device" expanded="true">
        <title>
          <caps:sentence sentenceid="71589dcc021fa7128be6ce02c4bae40c" id="tgt96" class="tgtSentence">Zašifrování zařízení</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="8b4bb28ccfe25f26b5b51ac2d7425762" id="tgt97" class="tgtSentence">Pokud vaše společnost nebo organizace vyžaduje, abyste si před přístupem k firemním souborům, e-mailu nebo datům zašifrovali zařízení, postupujte takto:</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence sentenceid="af593d936fba1e3defe54881968496c1" id="tgt98" class="tgtSentence">Ujistěte se, že je zařízení připojené k nabíječce.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt99" class="tgtSentence">Klepněte na <ui>Hledat</ui>.</caps:sentence>
                <caps:sentence sentenceid="eef65366d19ec7fa1427057a45c472e7" id="tgt100" class="tgtSentence"> Do pole vyhledávání napište <ui>portál společnosti</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="180a0ae508e82e1fe2f0e7ec1957f07a" id="tgt101" class="tgtSentence">Zkontrolujte, že je pro vaše zařízení nastavený kód PIN nebo heslo zamykací obrazovky.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c7ea902a3b53e77ab15b83a98de09a95" id="tgt102" class="tgtSentence">V Nastavení klikněte na <ui>Zabezpečení</ui> &gt; <ui>Šifrovat telefon</ui>.</caps:sentence>
                <caps:sentence sentenceid="e7cd1083a7d14f29c57cfc3f14ea7f3f" id="tgt103" class="tgtSentence"> (Na některých telefonech budete muset kliknout na <ui>Úložiště</ui> &gt; <ui>Šifrovat úložiště</ui>.)</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="48e7a77ebbc375b27095d1424e9ca739" id="tgt104" class="tgtSentence">Postupujte podle pokynů na obrazovce.</caps:sentence>
                <caps:sentence sentenceid="04fb0e693021f54d4d76c5c98ffd6665" id="tgt105" class="tgtSentence"> Během šifrování se zařízení může několikrát restartovat.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="acc3afeae12c8210f39b9c2e3370e615" id="tgt106" class="tgtSentence">Podle pokynů v <link xlink:href="8373c587-b1ad-4c25-93f9-e0148834d495">Enroll your device in Microsoft Intune</link> zkontrolujte, že je zařízení zaregistrované v Microsoft Intune.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <maml:section expanded="true" address="BKMK_andr_set_pin" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence sentenceid="58883bbb934c33d6c14e423ec7876f01" id="tgt107" class="tgtSentence">Nastavení PINu nebo hesla</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:list class="ordered">
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="298eb8b721760a1ff208e241dcde7e9b" id="tgt108" class="tgtSentence">Klepněte na <maml:ui>Nastavení</maml:ui> &gt; <maml:ui>Zabezpečení</maml:ui> &gt; <maml:ui>Zamykací obrazovka</maml:ui> &gt; <maml:ui>Heslo</maml:ui>.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="efcddfbbc5839ce3888c191bec4cde8a" id="tgt109" class="tgtSentence">Zvolte a potvrďte nové heslo.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="acc3afeae12c8210f39b9c2e3370e615" id="tgt110" class="tgtSentence">Podle pokynů v části <maml:link xlink:href="#BKMK_andr_enroll_devc">Registrace zařízení v Intune</maml:link> zkontrolujte, že je zařízení zaregistrované v Microsoft Intune.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt111" class="tgtSentence">Klepněte na <maml:ui>ZÍSKAT</maml:ui> &gt; <maml:ui>NAINSTALOVAT</maml:ui>.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <maml:section expanded="true" address="BKMK_andr_install_vpn" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence sentenceid="177fce649a24942d01315bd8da5e7076" id="tgt112" class="tgtSentence">Instalace firemní virtuální privátní sítě (VPN)</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence sentenceid="e8fa9ec145e597718eb06082fa820b16" id="tgt113" class="tgtSentence">Pokud správce IT nakonfiguroval aplikaci VPN, která vám umožní připojit se k prostředkům vaší společnosti, zobrazí se v zařízení oznámení, že je potřeba nainstalovat aplikaci VPN.</caps:sentence>
            <caps:sentence sentenceid="f9de42cfde03ef98dfc2d6f0a240a551" id="tgt114" class="tgtSentence"> Aplikaci VPN nainstalujete pomocí následujícího postupu:</caps:sentence>
          </maml:para>
          <maml:list class="ordered">
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="f68d8e82a2420b63954d9064aaafbf84" id="tgt115" class="tgtSentence">Otevřete oznámení a klepněte na <maml:ui>Klepnutím nainstalujete tuto požadovanou aplikaci</maml:ui>.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt116" class="tgtSentence">V <maml:ui>Play Store</maml:ui> klepněte na <maml:ui>INSTALL</maml:ui> a při instalaci aplikace postupujte podle pokynů.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt117" class="tgtSentence">Klepněte na <maml:ui>Instalovat profil firemní sítě VPN</maml:ui>, podle pokynů přijměte aplikaci a aktivujte ji.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <maml:section expanded="true" address="BKMK_andr_unenroll_device" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence sentenceid="e7334a6647a4beaf7b7148ac205d9349" id="tgt118" class="tgtSentence">Zrušení registrace zařízení v Intune</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence sentenceid="a0c8593b0b5f285d2c025132d17200c6" id="tgt119" class="tgtSentence">Když zrušíte registraci zařízení v Intune, už nebude mít přístup k prostředkům společnosti a nebude ho spravovat Intune.</caps:sentence>
          </maml:para>
          <maml:para>
            <caps:sentence sentenceid="33ec116fa4d3a05cebd927de0897af22" id="tgt120" class="tgtSentence">Zrušení registrace zařízení v Intune:</caps:sentence>
          </maml:para>
          <maml:list class="ordered">
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="5de362ca355ae82e403db3be928ad9fa" id="tgt121" class="tgtSentence">Stiskněte <maml:ui>MOJE ZAŘÍZENÍ</maml:ui> a vyberte zařízení, jehož registraci chcete zrušit.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="5de362ca355ae82e403db3be928ad9fa" id="tgt122" class="tgtSentence">Stiskněte <maml:ui>Odebrat</maml:ui> &gt; <maml:ui>OK</maml:ui>.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
          <maml:para>
            <caps:sentence sentenceid="715a45f185a63212c320c5ddbe6feb5f" id="tgt123" class="tgtSentence">Jakmile zrušíte registraci zařízení v Intune, stane se toto:</caps:sentence>
          </maml:para>
          <maml:list class="bullet">
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="19ae91384fd35970ba35834af61f01ac" id="tgt124" class="tgtSentence">Vaše zařízení se už nebude zobrazovat na portálu společnosti.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="debcc4cc4b3dff0ce773acfc3cba2baa" id="tgt125" class="tgtSentence">Z portálu společnosti už nebudete moct instalovat aplikace.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="1e73478ca20c90722c6b651b4f099ce6" id="tgt126" class="tgtSentence">Nastavení, která byla v zařízení změněna od jeho přidání, například zakázání fotoaparátu/kamery nebo vyžadování určité délky hesla, již nebudou platit.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="e2e05eddbfd9df781fb51550906d96c8" id="tgt127" class="tgtSentence">Je možné, že již v zařízení nebudete mít přístup k některým prostředkům společnosti, jako jsou sdílené složky nebo interní weby.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="a1e7c55d94cbaa4a92d89ae197836b91" id="tgt128" class="tgtSentence">V aplikaci Portál společnosti a na webu se už nebudou zobrazovat zařízení, která jsou nakonfigurovaná jenom pro použití e-mailu.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <maml:section expanded="true" address="BKMK_andr_erase_lost_device" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence sentenceid="c06b6d82e53b630aa8f19483e6047696" id="tgt129" class="tgtSentence">Reset (vymazání) ztraceného nebo odcizeného zařízení</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence sentenceid="25c5afd9a776dc51030b16195ab0a2bd" id="tgt130" class="tgtSentence">Pokud telefon ztratíte nebo vám ho někdo ukradne, můžete ho resetovat do výchozího stavu od výrobce.</caps:sentence>
          </maml:para>
          <maml:alert class="warning">
            <maml:para>
              <caps:sentence sentenceid="cc052fb10fe9bbbc80b2b6df67c21fb9" id="tgt131" class="tgtSentence">Když zařízení resetujete do výchozího stavu od výrobce, odeberete z něho jak svoje osobní, tak i pracovní informace.</caps:sentence>
            </maml:para>
          </maml:alert>
          <maml:list class="ordered">
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="008ffbf3521115514e18b2a62951487c" id="tgt132" class="tgtSentence">V prohlížeči otevřete <maml:ui>portal.manage.microsoft.com</maml:ui> a přihlaste se ke svému pracovnímu účtu.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt133" class="tgtSentence">Klepněte na <maml:ui>Moje zařízení</maml:ui> a vyberte název ztraceného nebo ukradeného zařízení.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="ccbe2a6c96a5df5e1966988e40064061" id="tgt134" class="tgtSentence">Klikněte na <maml:ui>Resetovat</maml:ui> &gt; <maml:ui>Resetovat</maml:ui>.</caps:sentence>
              </maml:para>
              <maml:alert class="note">
                <maml:para>
                  <caps:sentence sentenceid="a3544f235a5bb1907e3b26a3816dd4fa" id="tgt135" class="tgtSentence">Pokud se vám ztracené nebo ukradené zařízení nedaří resetovat, požádejte IT správce, aby to udělal za vás.</caps:sentence>
                </maml:para>
              </maml:alert>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <section address="BKMK_andr_data_collect" expanded="true">
        <title>
          <caps:sentence sentenceid="b321241f2502b5448f5ba9814524413f" id="tgt136" class="tgtSentence">Vypnutí shromažďování dat Microsoftu o využití</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="613c5729b5d70fe8a98c7d50505d4ea7" id="tgt137" class="tgtSentence">Microsoft automaticky shromažďuje anonymní informace o spolehlivosti, výkonu a použití aplikace Portál společnosti za účelem zlepšení svých produktů a služeb.</caps:sentence>
            <caps:sentence sentenceid="4150fed1487d3933fae6b75759c4e79e" id="tgt138" class="tgtSentence"> Shromažďování těchto dat můžete vypnout pomocí nastavení Údaje o používání v aplikaci Portál společnosti.</caps:sentence>
            <caps:sentence sentenceid="e1193143312e8b74386d45adac2e9d42" id="tgt139" class="tgtSentence"> Správci IT nemají nad shromažďováním údajů žádnou kontrolu a nemůžou u tohoto nastavení změnit vaši volbu.</caps:sentence>
          </para>
        </content>
      </section>
      <maml:section address="BKMK_andr_fix_issues" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence sentenceid="b04d8428c19a919568ee64f356b58ed8" id="tgt140" class="tgtSentence">Oprava problémů se zařízením zaregistrovaným v Intune</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence sentenceid="cda60aa64bc8e2eab24da8e35e678353" id="tgt141" class="tgtSentence">Pomocí těchto informací můžete svému správci IT pomoct opravit problémy s vaším zařízením potom, co nainstalujete aplikaci Portál společnosti a zaregistrujete zařízení do služby Intune.</caps:sentence>
          </maml:para>
        </maml:content>
        <maml:sections>
          <maml:section address="BKMK_andr_verboselogging">
            <maml:title>
              <caps:sentence sentenceid="464b5f790e098fbd41066848f397707c" id="tgt142" class="tgtSentence">Asistence správci IT při opravě problémů pomocí podrobného protokolování</caps:sentence>
            </maml:title>
            <maml:content>
              <maml:para>
                <caps:sentence sentenceid="6a27f3853a4e797560d0da86d27bf5fa" id="tgt143" class="tgtSentence">Pokud je vaše zařízení zaregistrované ve službě Intune, můžete pomocí nastavení <maml:ui>Podrobné protokolování</maml:ui> určit, že má Portál společnosti a aplikace spravované službou Intune zaznamenávat podrobné protokoly aktivit ve vašem zařízení.</caps:sentence>
                <caps:sentence sentenceid="4647d16a1b693bb166f4677550e42a45" id="tgt144" class="tgtSentence"> Tyto protokoly pomůžou vašemu správci IT opravit případné problémy, na které při použití aplikace Portál společnosti nebo aplikace spravované službou Intune narazíte.</caps:sentence>
                <caps:sentence sentenceid="b49b4b5888845bac5e9e9838c5f40a4d" id="tgt145" class="tgtSentence"> Podrobné protokolování je v zařízení ve výchozím nastavení povolené a protokoly odesílané vašemu správci IT zahrnují i vaši e-mailovou adresu.</caps:sentence>
              </maml:para>
              <maml:para>
                <caps:sentence sentenceid="ace4ed7045b3e834cc1dc2e72b40a0ed" id="tgt146" class="tgtSentence">Pokud chcete funkci <maml:ui>Podrobné protokolování</maml:ui> zapnout nebo vypnout, přihlaste se do aplikace Portál společnosti pomocí svých pracovních nebo školních přihlašovacích údajů, klepněte na <maml:ui>Nastavení</maml:ui> a potom klepněte na tlačítko pro zapnutí/vypnutí vedle položky <maml:ui>Podrobné protokolování</maml:ui>.</caps:sentence>
              </maml:para>
            </maml:content>
          </maml:section>
          <maml:section address="BKMK_andr_send_diag_logs">
            <maml:title>
              <caps:sentence sentenceid="54826dafaa3f8f1bcd109fceb9fdb49a" id="tgt147" class="tgtSentence">Odeslání protokolů s diagnostickými daty e-mailem vašemu správci IT</caps:sentence>
            </maml:title>
            <maml:content>
              <maml:para>
                <caps:sentence sentenceid="d6c6972b05cefc1d628b323a67467022" id="tgt148" class="tgtSentence">Pokud při práci se školními nebo podnikovými aplikacemi nebo s aplikací Portál společnosti dojde k chybě, můžete odeslat protokoly s diagnostickými daty, které vašemu správci IT pomůžou chybu pochopit a vyřešit.</caps:sentence>
                <caps:sentence sentenceid="c5dff4ba01265efbc6a07c1ca6060c69" id="tgt149" class="tgtSentence"> Pokud chcete do protokolů zahrnout všechny podrobnosti, které vašemu správci IT pomůžou problém pochopit, zapněte funkci Podrobné protokolování.</caps:sentence>
              </maml:para>
              <maml:list class="ordered">
                <maml:listItem>
                  <maml:para>
                    <caps:sentence sentenceid="d51b26a46aaf963c828838082daa0faa" id="tgt150" class="tgtSentence">Otevřete aplikaci Portál společnosti.</caps:sentence>
                  </maml:para>
                </maml:listItem>
                <maml:listItem>
                  <maml:para>
                    <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt151" class="tgtSentence">Klepněte na <maml:ui>Nabídka</maml:ui> &gt; <maml:ui>Nastavení</maml:ui>.</caps:sentence>
                  </maml:para>
                  <maml:alert class="note">
                    <maml:para>
                      <caps:sentence sentenceid="ff7845375bcca9661b95db848e63d64b" id="tgt152" class="tgtSentence">Podle toho, jaké zařízení se systémem Android máte, může být <maml:ui>Nabídka</maml:ui> buď softwarové, nebo hardwarové tlačítko.</caps:sentence>
                    </maml:para>
                  </maml:alert>
                </maml:listItem>
                <maml:listItem>
                  <maml:para>
                    <caps:sentence sentenceid="3682d80dcf79049a39e47edaf0434bb8" id="tgt153" class="tgtSentence">V části <maml:ui>Diagnostická data</maml:ui> klepněte na <maml:ui>Odeslat data</maml:ui>.</caps:sentence>
                  </maml:para>
                  <maml:mediaLink>
                    <maml:image xlink:href="e689c712-0ce0-461a-bfb2-5dd59e218a7b"></maml:image>
                  </maml:mediaLink>
                </maml:listItem>
                <maml:listItem>
                  <maml:para>
                    <caps:sentence sentenceid="bcebd066e10c9a2776e02c0707ed028c" id="tgt154" class="tgtSentence">Podle pokynů vyberte e-mailovou aplikaci, pomocí které odešlete protokoly správci IT.</caps:sentence>
                    <caps:sentence sentenceid="4746d31faa1b7d55b9d215cc55980dc2" id="tgt155" class="tgtSentence"> Aplikace vytvoří předem adresovaný e-mail, ve kterém už budou jako přílohy připojené všechny protokoly.</caps:sentence>
                  </maml:para>
                </maml:listItem>
              </maml:list>
            </maml:content>
          </maml:section>
          <maml:section address="BKMK_andr_send_diag_usbcable">
            <maml:title>
              <caps:sentence sentenceid="f7c802cd495ec0ef87d2f01dea55d8e0" id="tgt156" class="tgtSentence">Odeslání protokolů s diagnostickými daty správci IT pomocí kabelu USB</caps:sentence>
            </maml:title>
            <maml:content>
              <maml:para>
                <caps:sentence sentenceid="15a2927c1f5b3ed84882b1390f2e9016" id="tgt157" class="tgtSentence">Pokud nepoužíváte mobilní zařízení, ale počítač, a chcete odeslat protokoly s daty, aby mohl váš správce IT pochopit a opravit příslušný problém, postupujte takto:</caps:sentence>
              </maml:para>
              <maml:list class="ordered">
                <maml:listItem>
                  <maml:para>
                    <caps:sentence sentenceid="503fe34670bdd8a830553f6780b668a8" id="tgt158" class="tgtSentence">Než začnete, ujistěte se, že máte e-mailovou adresu správce IT.</caps:sentence>
                    <caps:sentence sentenceid="7980b0aa7e39ce184a2838074875cc7f" id="tgt159" class="tgtSentence"> Tu většinou najdete na webu portálu společnosti nebo v aplikaci Portál společnosti.</caps:sentence>
                  </maml:para>
                </maml:listItem>
                <maml:listItem>
                  <maml:para>
                    <caps:sentence sentenceid="a35b101a804e644f4fd0393ed4bde8a2" id="tgt160" class="tgtSentence">Připojte zařízení k počítači pomocí kabelu USB.</caps:sentence>
                  </maml:para>
                </maml:listItem>
                <maml:listItem>
                  <maml:para>
                    <caps:sentence sentenceid="82b709c93ab8287b560b7395b7b0df72" id="tgt161" class="tgtSentence">V počítači vyhledejte adresář, který má název vašeho telefonu.</caps:sentence>
                    <caps:sentence sentenceid="00cbf78559c6c72f2e70bcf6206d1cd1" id="tgt162" class="tgtSentence"> V tomto adresáři najděte tuto složku: &lt;Zařízení s Androidem&gt;\Phone\Android\data\com.microsoft.windowsintune.companyportal\files\.</caps:sentence>
                  </maml:para>
                </maml:listItem>
                <maml:listItem>
                  <maml:para>
                    <caps:sentence sentenceid="346ebdc57873b0b6cd9ee65dde880284" id="tgt163" class="tgtSentence">Všechny soubory připojte k e-mailu a odešlete je správci IT.</caps:sentence>
                  </maml:para>
                </maml:listItem>
              </maml:list>
            </maml:content>
          </maml:section>
          <maml:section address="BKMK_andr_send_enroll_errors">
            <maml:title>
              <caps:sentence sentenceid="891b8efb4cd4d53df92b65ab29dd0c0f" id="tgt164" class="tgtSentence">Odeslání chyb při registraci správci IT</caps:sentence>
            </maml:title>
            <maml:content>
              <maml:para>
                <caps:sentence sentenceid="8c7be865ad1e18ec222f54b2568b702a" id="tgt165" class="tgtSentence">Pokud při pokusu o registraci zařízení do služby Intune dojde k chybě, můžete to zkusit znovu klepnutím na <maml:ui>Opakovat</maml:ui> nebo poslat informace o chybě e-mailem správci IT klepnutím na <maml:ui>Poslat informace</maml:ui>.</caps:sentence>
                <caps:sentence sentenceid="415afde21455ff4dcd18fe07a31c4ace" id="tgt166" class="tgtSentence"> Automaticky se vytvoří e-mail adresovaný vašemu správci IT a obsahující protokoly, které správce IT potřebuje k tomu, aby vám mohl pomoct řešit problémy s vaším zařízením.</caps:sentence>
              </maml:para>
            </maml:content>
          </maml:section>
        </maml:sections>
      </maml:section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Use these  steps for tasks that you need to do on your Android device when your company is using Microsoft Intune:</caps:sentence>
        </para>
        <table border="1">
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src2" class="srcSentence">Task category</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src3" class="srcSentence">Tasks you can do</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src4" class="srcSentence">Company Portal app installation and Intune enrollment</caps:sentence>
                </para>
              </TD>
              <TD>
                <list class="bullet">
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_install_cp_app">Install the Microsoft Intune Company Portal app</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_signin_cp">Sign in to the Company Portal</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_enroll_devc">Enroll your device in Intune</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_what_happs_add">What happens when I install the Company Portal app and enroll my device in Intune?</link>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src5" class="srcSentence">Things you can do when your device is enrolled in Intune</caps:sentence>
                </para>
              </TD>
              <TD>
                <list class="bullet">
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_whatis_cp_website">What is the Company Portal website and what can I do with it?</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_encrypt_your_device">Encrypt your device</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_set_pin">Set your PIN or password</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_install_vpn">Install your company's Virtual Private Network (VPN)</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_unenroll_device">Unenroll your device from Intune</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_erase_lost_device">Reset (erase) your lost or stolen device</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_data_collect">Turn off Microsoft usage data collection</link>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">Fix issues with your device </caps:sentence>
                </para>
              </TD>
              <TD>
                <list class="bullet">
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_andr_fix_issues">Fix issues when your device is enrolled in Intune</link>
                    </para>
                    <list class="bullet">
                      <listItem>
                        <para>
                          <link xlink:href="#BKMK_andr_verboselogging">Use Verbose Logging to help your IT admin fix issues</link>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <link xlink:href="#BKMK_andr_send_diag_logs">Send diagnostic data logs to your IT admin using email</link>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <link xlink:href="#BKMK_andr_send_diag_usbcable">Send diagnostic data logs to your IT admin using a USB cable</link>
                        </para>
                      </listItem>
                      <listItem>
                        <para>
                          <link xlink:href="#BKMK_andr_send_enroll_errors">Send enrollment errors to your IT admin</link>
                        </para>
                      </listItem>
                    </list>
                  </listItem>
                </list>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <section expanded="true" address="BKMK_andr_install_cp_app">
        <title>
          <caps:sentence id="src7" class="srcSentence">Install the Microsoft Intune Company Portal app</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src8" class="srcSentence">The Company Portal is an app that you install on your device to give you access to your company or school apps, email, and network.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence">  Before you can get access, you have to install the Company Portal app, and then  use the app to enroll your device in Microsoft Intune.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> To find out more about what enrolling means, see <link xlink:href="#BKMK_andr_what_happs_add">What happens when I install the Company Portal app and enroll my device in Intune?</link>.</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence id="src11" class="srcSentence">Tap <ui>Home</ui> &gt; <ui>Play Store</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src12" class="srcSentence">In the <ui>Search</ui> box, type <ui>company portal</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src13" class="srcSentence">Tap <ui>Intune Company Portal</ui>.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="8fe9ef88-1360-4018-aa94-de83f09cb439"></image>
              </mediaLink>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src14" class="srcSentence">Tap <ui>INSTALL</ui>.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="e41358ab-3546-48ca-973e-e3988f519676"></image>
              </mediaLink>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src15" class="srcSentence">Tap <ui>ACCEPT</ui>.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="b9366110-0d9a-4848-8357-395933976720"></image>
              </mediaLink>
            </listItem>
          </list>
        </content>
      </section>
      <section expanded="true" address="BKMK_andr_signin_cp">
        <title>
          <caps:sentence id="src16" class="srcSentence">Sign in to the Company Portal</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src17" class="srcSentence">After you install the Company Portal app, you'll need to sign in to the app to enroll your device in Intune.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> Once you enroll, you can  sign in to the Company Portal anytime to download company apps and do other tasks.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> For more about what you can do, see <link xlink:href="#BKMK_andr_what_happs_add">What happens when I install the Company Portal app and enroll my device in Intune?</link>.</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence id="src20" class="srcSentence">Tap <ui>Company Portal</ui> in your list of apps.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="fd42b202-1e8d-4dec-b0d9-2bb5025a8685"></image>
              </mediaLink>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src21" class="srcSentence">On the <ui>Welcome</ui> screen, tap <ui>Sign in</ui>.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="d1bd8a99-5433-4d86-8678-02bb157b6531"></image>
              </mediaLink>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src22" class="srcSentence">Enter your work or school email and your password, and then Tap <ui>Sign in</ui>.</caps:sentence>
              </para>
              <mediaLink>
                <image xlink:href="5542d597-0ff4-4858-ba2b-eb909052c3c6"></image>
              </mediaLink>
              <para>
                <caps:sentence id="src23" class="srcSentence">If you are signing into the Company Portal for the first time, and your company or school is using Intune, you will be prompted to enroll your device in Intune.</caps:sentence>
                <caps:sentence id="src24" class="srcSentence"> To enroll, follow the steps in <link xlink:href="#BKMK_andr_enroll_devc"> Enroll your device in Intune</link>.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section expanded="true" address="BKMK_andr_enroll_devc">
        <title>
          <caps:sentence id="src25" class="srcSentence"> Enroll your device in Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src26" class="srcSentence">When you enroll your device in Intune, you can access the company’s network, and get your work email,  work files, and company apps.</caps:sentence>
            <caps:sentence id="src27" class="srcSentence"> To find out more about what you can do when you enroll, see <link xlink:href="#BKMK_andr_what_happs_add">What happens when I install the Company Portal app and enroll my device in Intune?</link>.</caps:sentence>
            <caps:sentence id="src28" class="srcSentence"> If you have issues while trying to enroll, see <link xlink:href="#BKMK_andr_send_enroll_errors">Send enrollment errors to your IT admin</link>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src29" class="srcSentence">To enroll, use the steps that match the type of device you have:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <link xlink:href="#BKMK_andr_enroll_native">Enroll your native (non-Samsung device in Intune)</link>
              </para>
            </listItem>
            <listItem>
              <para>
                <link xlink:href="#BKMK_andr_enroll_knox">Enroll your Samsung Knox device in Intune</link>
              </para>
            </listItem>
          </list>
        </content>
        <sections>
          <section address="BKMK_andr_enroll_native">
            <title>
              <caps:sentence id="src30" class="srcSentence">Enroll your native (non-Samsung device in Intune)</caps:sentence>
            </title>
            <content>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src31" class="srcSentence">On the Company Portal <ui>Welcome</ui> screen, tap <ui>Sign in</ui>, and then sign in with your work or school account..</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="d1bd8a99-5433-4d86-8678-02bb157b6531"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src32" class="srcSentence">If your IT admin set up company terms and conditions, tap <ui>ACCEPT</ui> to accept the terms.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="930b52ef-2c50-4fe8-b551-624e757781f4"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">Tap <ui>ENROLL</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="161a5f87-3d27-43bf-8b0a-8bfea06d61cf"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">Tap <ui>Activate</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="71bd0ea7-259a-468c-b312-a3cf820ba956"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">Follow the prompts to enter a PIN or password.</caps:sentence>
                    <caps:sentence id="src36" class="srcSentence"> If you already set up a PIN or password on this device, you won't see this screen or be required to enter a new PIN or password.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="3167bf58-b9f3-4260-9ffd-4ca22f633ec4"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">On the  <ui>Name the certificate</ui> screen, tap <ui>OK</ui> to accept the default certificate.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="e9c96498-e528-4694-bdcc-80ebc7cbd9e4"></image>
                  </mediaLink>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">Your device is now enrolled in Intune.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src39" class="srcSentence">If you get an error while trying to enroll your device in Intune, see <link xlink:href="#BKMK_andr_send_enroll_errors">Send enrollment errors to your IT admin</link>.</caps:sentence>
              </para>
            </content>
          </section>
          <section address="BKMK_andr_enroll_knox">
            <title>
              <caps:sentence id="src40" class="srcSentence">Enroll your Samsung Knox device in Intune</caps:sentence>
            </title>
            <content>
              <list class="ordered">
                <listItem>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">On the Company Portal Welcome screen, tap Sign in, and then sign in with your work or school account.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="d1bd8a99-5433-4d86-8678-02bb157b6531"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">If your IT admin set up company terms and conditions, tap <ui>ACCEPT</ui> to accept the terms.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="930b52ef-2c50-4fe8-b551-624e757781f4"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">Tap <ui>ENROLL</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="161a5f87-3d27-43bf-8b0a-8bfea06d61cf"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src44" class="srcSentence">Tap <ui>ACTIVATE</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="c68d1754-e1a7-4906-a3dc-f13673f7c8d3"></image>
                  </mediaLink>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">Accept the Samsung Knox Privacy Policy and tap <ui>Confirm</ui>.</caps:sentence>
                  </para>
                  <mediaLink>
                    <image xlink:href="595681eb-d7f3-47a8-a95d-a427d903a241"></image>
                  </mediaLink>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src46" class="srcSentence">Your device is now enrolled in Intune.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <section address="BKMK_andr_what_happs_add">
        <title>
          <caps:sentence id="src47" class="srcSentence">What happens when I install the Company Portal app and enroll my device in Intune?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src48" class="srcSentence">You start by installing the Company Portal app, and then use the app to enroll your device in Intune.</caps:sentence>
            <caps:sentence id="src49" class="srcSentence"> Once your device is enrolled, you  can use the Company Portal app to:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src50" class="srcSentence">Access the company’s network, and your email and work files</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src51" class="srcSentence">Get company apps from the Company Portal</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src52" class="srcSentence">Automatically configure your company email account</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src53" class="srcSentence">Reset your phone to factory settings if it is lost or stolen</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src54" class="srcSentence">When  you enroll your device in Intune, you are giving your IT administrator permission to manage your device to help protect the company information on the device.</caps:sentence>
          </para>
          <table border="1">
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src55" class="srcSentence">IT cannot see</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src56" class="srcSentence">IT can see</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src57" class="srcSentence">Call history</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src58" class="srcSentence">Text messages</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src59" class="srcSentence">Personal email, contacts, and calendar</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src60" class="srcSentence">Web history</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src61" class="srcSentence">Location</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src62" class="srcSentence">Camera roll</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src63" class="srcSentence">Personal data</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src64" class="srcSentence">Owner</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src65" class="srcSentence">Device name</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src66" class="srcSentence">Serial number</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src67" class="srcSentence">Manufacturer</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src68" class="srcSentence">Model</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src69" class="srcSentence">Operating system</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src70" class="srcSentence">Company apps</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src71" class="srcSentence">Personal apps</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src72" class="srcSentence">When you add your Android device, you are giving your IT administrator permission to access the device.</caps:sentence>
            <caps:sentence id="src73" class="srcSentence"> They can do things like:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src74" class="srcSentence">Reset your device back to manufacturer’s defaults.</caps:sentence>
                <caps:sentence id="src75" class="srcSentence"> This is helpful if the device is lost or stolen.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src76" class="srcSentence">Remove all company related data.</caps:sentence>
                <caps:sentence id="src77" class="srcSentence"> Your personal data and settings aren’t removed.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src78" class="srcSentence">Force you to have a password or PIN on the device, which may lock you out of the device, or reset your device back to manufacturer’s default settings, which may include the deletion of data, if there are too many incorrect password attempts.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src79" class="srcSentence">Require you to accept terms and conditions.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src80" class="srcSentence">Enable or disable the camera on your device.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src81" class="srcSentence">Force all the data, including corporate and personal data, on the device to be encrypted.</caps:sentence>
                <caps:sentence id="src82" class="srcSentence"> This helps protect the data if the device is lost or stolen.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src83" class="srcSentence">After your device is added to the Company Portal, approximately every 8 hours it will:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src84" class="srcSentence">Download any policy or app updates that your IT administrator has made available.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src85" class="srcSentence">Send any hardware inventory updates (these updates do not contain personal information).</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src86" class="srcSentence">Send any company app inventory updates (these updates do not contain personal information).</caps:sentence>
                  </para>
                </listItem>
              </list>
            </listItem>
          </list>
        </content>
      </section>
      <section expanded="true" address="BKMK_andr_whatis_cp_website">
        <title>
          <caps:sentence id="src87" class="srcSentence">What is the Company Portal website and what can I do with it?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src88" class="srcSentence">The <externalLink><linkText>Company Portal website</linkText><linkUri>http://portal.manage.microsoft.com</linkUri></externalLink> is your company’s web interface that you use to manage your work computers and devices, and your personal computers and devices that you choose to use at work.</caps:sentence>
            <caps:sentence id="src89" class="srcSentence"> You can do most of the same tasks on this website that you can do by using the Company Portal app that you install on your device.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src90" class="srcSentence">You can do the following tasks from the Company Portal website:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src91" class="srcSentence">Browse for and download company apps</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src92" class="srcSentence">Rename your device</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src93" class="srcSentence">Remove your device from Intune</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src94" class="srcSentence">Reset your mobile device to its factory default settings</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src95" class="srcSentence">Find contact information for your IT administrator</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section address="BKMK_andr_encrypt_your_device" expanded="true">
        <title>
          <caps:sentence id="src96" class="srcSentence">Encrypt your device</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src97" class="srcSentence">If your company or organization requires you to encrypt your device before you can access company files, email, or data, follow these steps to encrypt your device:</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence id="src98" class="srcSentence">Ensure that your device is connected to the charger.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src99" class="srcSentence">Tap <ui>Search</ui>.</caps:sentence>
                <caps:sentence id="src100" class="srcSentence"> In the Search box, type <ui>company portal</ui>.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src101" class="srcSentence">Ensure that a screen lock PIN or password has been set for your device.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src102" class="srcSentence">In Settings, click <ui>Security</ui> &gt; <ui>Encrypt Phone</ui>.</caps:sentence>
                <caps:sentence id="src103" class="srcSentence"> (On some phones, you’ll need to click <ui>Storage</ui> &gt; <ui>Storage encryption</ui>).</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src104" class="srcSentence">Follow the on-screen instructions.</caps:sentence>
                <caps:sentence id="src105" class="srcSentence"> During encryption, your device might restart several times.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src106" class="srcSentence">Ensure that your device is enrolled with Microsoft Intune by following the instructions in <link xlink:href="8373c587-b1ad-4c25-93f9-e0148834d495">Enroll your device in Microsoft Intune</link>.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <maml:section expanded="true" address="BKMK_andr_set_pin" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence id="src107" class="srcSentence">Set your PIN or password</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:list class="ordered">
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src108" class="srcSentence">Tap  <maml:ui>Settings</maml:ui> &gt; <maml:ui>Security</maml:ui> &gt; <maml:ui>Screen Lock</maml:ui> &gt; <maml:ui>Password</maml:ui>.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src109" class="srcSentence">Choose and confirm your new password.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src110" class="srcSentence">Ensure that your device is enrolled with Microsoft Intune by following the instructions in <maml:link xlink:href="#BKMK_andr_enroll_devc"> Enroll your device in Intune</maml:link>.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src111" class="srcSentence">Tap <maml:ui>GET</maml:ui> &gt; <maml:ui>INSTALL</maml:ui>.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <maml:section expanded="true" address="BKMK_andr_install_vpn" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence id="src112" class="srcSentence">Install your company's Virtual Private Network (VPN)</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence id="src113" class="srcSentence">If your IT administrator has configured a VPN application to enable you to  connect to your company's resources, you'll see a notification on your device indicating that you need to install a VPN app.</caps:sentence>
            <caps:sentence id="src114" class="srcSentence"> Follow these steps to install the VPN app:</caps:sentence>
          </maml:para>
          <maml:list class="ordered">
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src115" class="srcSentence">Open the notification, and tap <maml:ui>Tap to install this required app</maml:ui>.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src116" class="srcSentence">In the <maml:ui>Play Store</maml:ui>, click <maml:ui>INSTALL</maml:ui> and follow the prompts to install the app.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src117" class="srcSentence">Tap <maml:ui>Install corporate VPN profile</maml:ui> and follow the prompts to accept and activate the app.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <maml:section expanded="true" address="BKMK_andr_unenroll_device" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence id="src118" class="srcSentence">Unenroll your device from Intune</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence id="src119" class="srcSentence">When you unenroll your device from Intune, your device will not longer be able to access company resources and will no longer be managed by Intune.</caps:sentence>
          </maml:para>
          <maml:para>
            <caps:sentence id="src120" class="srcSentence">To unenroll your device from Intune:</caps:sentence>
          </maml:para>
          <maml:list class="ordered">
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src121" class="srcSentence">Press <maml:ui>MY DEVICES</maml:ui> and select the device to unenroll.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src122" class="srcSentence">Press <maml:ui>Remove</maml:ui> &gt; <maml:ui>OK</maml:ui>.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
          <maml:para>
            <caps:sentence id="src123" class="srcSentence">When you unenroll your device from Intune, here's what happens:</caps:sentence>
          </maml:para>
          <maml:list class="bullet">
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src124" class="srcSentence">Your device won’t appear in the Company Portal anymore.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src125" class="srcSentence">You can’t install apps from the Company Portal anymore.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src126" class="srcSentence">Any settings that were changed on your device when you added it, for example disabling the camera, or requiring a certain password length, will no longer apply.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src127" class="srcSentence">You might not have access to some company resources, such as file shares or internal web sites, on your device anymore.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src128" class="srcSentence">Devices that are configured for email only won't appear in the Company Portal app or website anymore.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <maml:section expanded="true" address="BKMK_andr_erase_lost_device" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence id="src129" class="srcSentence">Reset (erase) your lost or stolen device</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence id="src130" class="srcSentence">If your phone is lost or stolen, you can reset it to factory defaults.</caps:sentence>
          </maml:para>
          <maml:alert class="warning">
            <maml:para>
              <caps:sentence id="src131" class="srcSentence">Resetting a device to factor defaults removes both your personal and work information from it.</caps:sentence>
            </maml:para>
          </maml:alert>
          <maml:list class="ordered">
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src132" class="srcSentence">Open <maml:ui>portal.manage.microsoft.com</maml:ui> in your browser, and sign in to your work account.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src133" class="srcSentence">Tap <maml:ui>My Devices</maml:ui> and select the name of the lost of stolen  device.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src134" class="srcSentence">Click <maml:ui>Reset</maml:ui> &gt; <maml:ui>Reset</maml:ui>.</caps:sentence>
              </maml:para>
              <maml:alert class="note">
                <maml:para>
                  <caps:sentence id="src135" class="srcSentence">If you are unable to reset your lost or stolen device, ask your IT administrator to reset it for you.</caps:sentence>
                </maml:para>
              </maml:alert>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <section address="BKMK_andr_data_collect" expanded="true">
        <title>
          <caps:sentence id="src136" class="srcSentence">Turn off Microsoft usage data collection</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src137" class="srcSentence">In order to improve its products and services, Microsoft automatically collects anonymous data about the reliability and performance of the Company Portal app and how it is used.</caps:sentence>
            <caps:sentence id="src138" class="srcSentence"> You can turn off the collection of that data by using the Usage Data setting in the Company Portal app.</caps:sentence>
            <caps:sentence id="src139" class="srcSentence"> IT administrators have no control over the collection of the data, and they cannot change your selection for the setting.</caps:sentence>
          </para>
        </content>
      </section>
      <maml:section address="BKMK_andr_fix_issues" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence id="src140" class="srcSentence">Fix issues when your device is enrolled in Intune</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence id="src141" class="srcSentence">Use this information to help your IT admin fix any issues that you have with your device when you've installed the Company Portal app and enrolled your device in Intune.</caps:sentence>
          </maml:para>
        </maml:content>
        <maml:sections>
          <maml:section address="BKMK_andr_verboselogging">
            <maml:title>
              <caps:sentence id="src142" class="srcSentence">Use Verbose Logging to help your IT admin fix issues</caps:sentence>
            </maml:title>
            <maml:content>
              <maml:para>
                <caps:sentence id="src143" class="srcSentence">When your device is enrolled in Intune, you can use the <maml:ui>Verbose Logging</maml:ui> setting to make the Company Portal app and Intune-managed apps record detailed logs about what's happening on your device.</caps:sentence>
                <caps:sentence id="src144" class="srcSentence"> These logs help your IT admin fix any issues that you might have when you're using the Company Portal or an app that's managed by Intune.</caps:sentence>
                <caps:sentence id="src145" class="srcSentence"> Verbose Logging is enabled on your device  by default, and the  logs that are sent to your IT admin  include your email address.</caps:sentence>
              </maml:para>
              <maml:para>
                <caps:sentence id="src146" class="srcSentence">To turn <maml:ui>Verbose Logging</maml:ui> on or off, sign in to the Company Portal app using your work or school credentials, tap <maml:ui>Settings</maml:ui>, and tap the on/off button next to the <maml:ui>Verbose Logging</maml:ui> setting.</caps:sentence>
              </maml:para>
            </maml:content>
          </maml:section>
          <maml:section address="BKMK_andr_send_diag_logs">
            <maml:title>
              <caps:sentence id="src147" class="srcSentence">Send diagnostic data logs to your IT admin using email</caps:sentence>
            </maml:title>
            <maml:content>
              <maml:para>
                <caps:sentence id="src148" class="srcSentence">If you get an error while you're working with your school or company apps or while you're in the Company Portal app, you can send diagnostic data logs  to help your IT admin figure out and fix the error.</caps:sentence>
                <caps:sentence id="src149" class="srcSentence"> To include all of the details in the logs, which will make it easier for your IT admin to figure out the issue, turn on Verbose Logging.</caps:sentence>
              </maml:para>
              <maml:list class="ordered">
                <maml:listItem>
                  <maml:para>
                    <caps:sentence id="src150" class="srcSentence">Open the Company Portal app.</caps:sentence>
                  </maml:para>
                </maml:listItem>
                <maml:listItem>
                  <maml:para>
                    <caps:sentence id="src151" class="srcSentence">Tap <maml:ui>Menu</maml:ui> &gt;  <maml:ui>Settings</maml:ui>.</caps:sentence>
                  </maml:para>
                  <maml:alert class="note">
                    <maml:para>
                      <caps:sentence id="src152" class="srcSentence">
                        <maml:ui>Menu</maml:ui> could be a software button or a hardware button, depending on the type of Android device you have.</caps:sentence>
                    </maml:para>
                  </maml:alert>
                </maml:listItem>
                <maml:listItem>
                  <maml:para>
                    <caps:sentence id="src153" class="srcSentence">Under <maml:ui>Diagnostic Data</maml:ui>, tap <maml:ui>Send Data</maml:ui>.</caps:sentence>
                  </maml:para>
                  <maml:mediaLink>
                    <maml:image xlink:href="e689c712-0ce0-461a-bfb2-5dd59e218a7b"></maml:image>
                  </maml:mediaLink>
                </maml:listItem>
                <maml:listItem>
                  <maml:para>
                    <caps:sentence id="src154" class="srcSentence">Follow the prompts to choose an email app to use for sending the logs to your IT admin.</caps:sentence>
                    <caps:sentence id="src155" class="srcSentence"> The app will create a pre-addressed email with all the logs attached.</caps:sentence>
                  </maml:para>
                </maml:listItem>
              </maml:list>
            </maml:content>
          </maml:section>
          <maml:section address="BKMK_andr_send_diag_usbcable">
            <maml:title>
              <caps:sentence id="src156" class="srcSentence">Send diagnostic data logs to your IT admin using a USB cable</caps:sentence>
            </maml:title>
            <maml:content>
              <maml:para>
                <caps:sentence id="src157" class="srcSentence">If you're using a computer rather than a mobile device, and you want to send data logs to have your IT admin figure out and fix your issue, use these steps:</caps:sentence>
              </maml:para>
              <maml:list class="ordered">
                <maml:listItem>
                  <maml:para>
                    <caps:sentence id="src158" class="srcSentence">Before you start, make sure that you have your IT admin's email address.</caps:sentence>
                    <caps:sentence id="src159" class="srcSentence"> It is typically listed on your Company Portal website or in your Company Portal app.</caps:sentence>
                  </maml:para>
                </maml:listItem>
                <maml:listItem>
                  <maml:para>
                    <caps:sentence id="src160" class="srcSentence">Use a USB cable to connect your device to a computer.</caps:sentence>
                  </maml:para>
                </maml:listItem>
                <maml:listItem>
                  <maml:para>
                    <caps:sentence id="src161" class="srcSentence">On the computer, look for a directory that has the name of your phone.</caps:sentence>
                    <caps:sentence id="src162" class="srcSentence"> In that directory, find &lt;Android Device&gt;\Phone\Android\data\com.microsoft.windowsintune.companyportal\files\.</caps:sentence>
                  </maml:para>
                </maml:listItem>
                <maml:listItem>
                  <maml:para>
                    <caps:sentence id="src163" class="srcSentence">Attach all of the files to an email and send them to your IT admin.</caps:sentence>
                  </maml:para>
                </maml:listItem>
              </maml:list>
            </maml:content>
          </maml:section>
          <maml:section address="BKMK_andr_send_enroll_errors">
            <maml:title>
              <caps:sentence id="src164" class="srcSentence">Send enrollment errors to your IT admin</caps:sentence>
            </maml:title>
            <maml:content>
              <maml:para>
                <caps:sentence id="src165" class="srcSentence">If you get an error while trying to enroll your device in Intune, you can try enrolling again by tapping <maml:ui>Retry</maml:ui>, or send the error information to your IT admin in an email by tapping <maml:ui>Send info</maml:ui>.</caps:sentence>
                <caps:sentence id="src166" class="srcSentence"> An email, addressed to your IT administrator, is automatically created and contains the logs that your IT admin needs to help troubleshoot your device.</caps:sentence>
              </maml:para>
            </maml:content>
          </maml:section>
        </maml:sections>
      </maml:section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>