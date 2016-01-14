---
description: na
keywords: na
title: Using your iOS device with Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3d648819-b866-412b-bd19-ac4505eb5eaf
robots: noindex
---
# Použit&#237; zař&#237;zen&#237; iOS s&#160;Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="cs-CZ">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink">
      <introduction>
        <para>
          <caps:sentence sentenceid="75a37d64ef8c3c83c8e12236a6e20471" id="tgt1" class="tgtSentence">Tyto kroky použijte pro úlohy, které musíte udělat na zařízení s iOS, když vaše společnost používá Microsoft Intune:</caps:sentence>
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
                      <link xlink:href="#BKMK_ios_signin_cp">Install and sign in to the Company Portal app</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_ios_enroll_your_device">Enroll your device in Intune</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_ios_what_happ_enroll">What happens when I install the Company Portal app and enroll my device in Intune?</link>
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
                      <link xlink:href="#BKMK_ios_whatis_cp_website">What is the Company Portal website and what can I do with it?</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_ios_erase_lost_device">Reset (erase) your lost or stolen device</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_ios_data_collect">Turn off Microsoft usage data collection</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_ios_unenroll_device">Unenroll your device from Intune</link>
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
                      <link xlink:href="#BKMK_ios_fix_issues">Fix issues when your device is enrolled in Intune</link>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <maml:section expanded="true" address="BKMK_ios_signin_cp" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence sentenceid="fcc6e39b54334b6698afbc39c70d2d83" id="tgt7" class="tgtSentence">Instalace a přihlášení do aplikace Portál společnosti Intune</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence sentenceid="bcc9ebff81099e0055eecc4f9b04f424" id="tgt8" class="tgtSentence">Portál společnosti je aplikace, která po instalaci do vašeho zařízení umožňuje přístup k podnikovým nebo školním aplikacím, e-mailům a síti.</caps:sentence>
            <caps:sentence sentenceid="c4be065ac83e30901401d1098791a413" id="tgt9" class="tgtSentence">  Než získáte přístup, musíte aplikaci Portál společnosti nainstalovat a pak v ní zaregistrovat své zařízení do služby Microsoft Intune.</caps:sentence>
            <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt10" class="tgtSentence"> Další informace najdete v tématu <maml:link xlink:href="#BKMK_ios_what_happ_enroll">Co se stane, když nainstaluji aplikaci Portál společnosti a zaregistruji zařízení do služby Intune?</maml:link></caps:sentence>
          </maml:para>
          <maml:list class="ordered">
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="84fc780d784220118ceb8b1a4d3c5a7e" id="tgt11" class="tgtSentence">Otevřete <maml:ui>App Store</maml:ui> a vyhledejte řetězec <maml:ui>intune</maml:ui>.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="23bd19fcedd382955bc35818765ace04" id="tgt12" class="tgtSentence">Stáhněte aplikaci <maml:ui>Portál společnosti Microsoft Intune</maml:ui>.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="6d9d1904-1462-4c29-a3e6-daccf5b8ec7e"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="64df2b8e2dde54d36299361d4189328a" id="tgt13" class="tgtSentence">Otevřete aplikaci Portál společnosti, zadejte svůj pracovní nebo školní e-mail a heslo a pak klepněte na <maml:ui>Přihlásit</maml:ui>.</caps:sentence>
              </maml:para>
              <maml:para>
                <caps:sentence sentenceid="266b3e7b012119fb91d6962911283bb6" id="tgt14" class="tgtSentence">Když se do aplikace Portál společnosti přihlašujete poprvé a vaše společnost nebo škola používá Intune, zobrazí se výzva k registraci vašeho zařízení do služby Intune.</caps:sentence>
                <caps:sentence sentenceid="5e948074b31b8a9455d72a9372e2f24d" id="tgt15" class="tgtSentence"> Při registraci použijte postup popsaný v části <maml:link xlink:href="#BKMK_ios_enroll_your_device">Registrace zařízení v Intune</maml:link>.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <maml:section address="BKMK_ios_enroll_your_device" expanded="true" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence sentenceid="77956432d1ee5eec1f0a618647bbc6a4" id="tgt16" class="tgtSentence">Registrace zařízení v Intune</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence sentenceid="f420ae496d933fa61a4e7dbd20f20bf2" id="tgt17" class="tgtSentence">Po registraci zařízení do služby Intune budete moct získat přístup k podnikové síti, pracovním e-mailům a souborům a také instalovat podnikové aplikace.</caps:sentence>
            <caps:sentence sentenceid="e518b87c92ded097371c65588339b8cd" id="tgt18" class="tgtSentence"> Další informace o tom, co se stane, když zaregistrujete své zařízení, najdete v tématu <maml:link xlink:href="#BKMK_ios_what_happ_enroll">Co se stane, když nainstaluji aplikaci Portál společnosti a zaregistruji zařízení do služby Intune?</maml:link></caps:sentence>
          </maml:para>
          <maml:para>
            <caps:sentence sentenceid="94f1492f6d274db2e649a11db5e4d80a" id="tgt19" class="tgtSentence">Registrace zařízení:</caps:sentence>
          </maml:para>
          <maml:list class="ordered">
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="34467dfcfb57ed5e287c4f9586a2a48e" id="tgt20" class="tgtSentence">Postupujte podle návodu v tématu <maml:link xlink:href="#BKMK_ios_signin_cp">Instalace a přihlášení do aplikace Portál společnosti Intune</maml:link>.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt21" class="tgtSentence">Na obrazovce <maml:ui>Registrace zařízení</maml:ui> v aplikaci Portál společnosti klepněte na <maml:ui>Registrovat</maml:ui>.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="0e518c1a-34a8-4b41-bb1d-d178fc7d1b1f"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt22" class="tgtSentence">Na obrazovce <maml:ui>Instalovat profil</maml:ui> klepněte na <maml:ui>Instalovat</maml:ui>, a pokud se zobrazí výzva, zadejte své heslo.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="08071677-4fc9-4f8d-988c-096ad4fc307b"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="4c3e12f452674bf9900d2c3dd5d0ea85" id="tgt23" class="tgtSentence"> Klepněte na <maml:ui>Instalovat</maml:ui>.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="2952ad68-e279-4c29-8276-af6b0d38650b"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="4c3e12f452674bf9900d2c3dd5d0ea85" id="tgt24" class="tgtSentence"> Klepnutím na <maml:ui>Instalovat</maml:ui> dejte najevo, že jste si přečetli upozornění.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="565f3b1a-671a-4b8c-acfe-967d12e6bdcc"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="4c3e12f452674bf9900d2c3dd5d0ea85" id="tgt25" class="tgtSentence"> Klepněte na <maml:ui>Důvěřovat</maml:ui>.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="17627759-2f98-4847-b72d-33b3defd1ef4"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt26" class="tgtSentence">Klepněte na <maml:ui>Hotovo</maml:ui>.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="5e9d1770-83cd-4df0-b0a9-3f24ee7792f7"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="c1a06c115e64c41003f8d3aa60aa7697" id="tgt27" class="tgtSentence">Klepněte na <maml:ui>OK</maml:ui>.</caps:sentence>
                <caps:sentence sentenceid="15afcd6e39bd01b0c0fe0a0b0212d290" id="tgt28" class="tgtSentence"> Právě jste zaregistrovali své zařízení do služby Intune.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="818c0228-bbe4-4760-9590-bc9146820ab5"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <section address="BKMK_ios_what_happ_enroll">
        <title>
          <caps:sentence sentenceid="c7771a0e09cd91e94fb6776ff1223ac3" id="tgt29" class="tgtSentence">Co se stane, když nainstaluji aplikaci Portál společnosti a zaregistruji zařízení do služby Intune?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="f0401535f7b1ac877b8f6af14bd6c40d" id="tgt30" class="tgtSentence">Nejdřív nainstalujete aplikaci Portál společnosti a pak v ní zaregistrujete své zařízení do služby Intune.</caps:sentence>
            <caps:sentence sentenceid="9af3ed7432137e078ac63133e9bdc49a" id="tgt31" class="tgtSentence"> Po registraci svého zařízení můžete v aplikaci Portál společnosti provádět tyto kroky:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="cd1a40a617eb283f621ef494fdaa498f" id="tgt32" class="tgtSentence">Přístup k podnikové síti, e-mailu a dalším pracovním souborům</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="365f2777fae357fc28b1489affab4a54" id="tgt33" class="tgtSentence">Získání aplikací společnosti z Portálu společnosti</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="7c7476a0520e0468f40a091eecb0d594" id="tgt34" class="tgtSentence">Automatická konfigurace e-mailového účtu vaší společnosti</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="66b07c74bf99f92822a9939daafde7d3" id="tgt35" class="tgtSentence">Obnovení továrního nastavení telefonu v případě ztráty nebo odcizení</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="9580373c6a8f78a774ff06c526b5e360" id="tgt36" class="tgtSentence">Když své zařízení zaregistrujete do služby Intune, správci IT tím udělíte oprávnění ke správě vašich zařízení, aby bylo možné lépe chránit informace společnosti na daném zařízení.</caps:sentence>
          </para>
          <table border="1">
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="49b5c06f816b80fa0b53001b7e064dd0" id="tgt37" class="tgtSentence">IT neuvidí</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="919967a6e68fc799764ccfadd49d0d82" id="tgt38" class="tgtSentence">IT uvidí</caps:sentence>
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
                        <caps:sentence sentenceid="7b15a2dc20f223897228983bcb839a0d" id="tgt39" class="tgtSentence">Historie volání</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="b5c1e4334dd619fce44e7a047bd05a8d" id="tgt40" class="tgtSentence">Textové zprávy</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="936249fa98a3357097ff1f12312225b4" id="tgt41" class="tgtSentence">Osobní e-maily, kontakty a kalendář</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="827a82394f446cc4d02c0fd5e61f331b" id="tgt42" class="tgtSentence">Webová historie</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="d5189de027922f81005951e6efe0efd5" id="tgt43" class="tgtSentence">Umístění</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="b99bbccd22c782c7f7019bad4a0628f2" id="tgt44" class="tgtSentence">Z fotoaparátu</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="2c5a2582707f1495992f8b6befe92a6c" id="tgt45" class="tgtSentence">Osobní data</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="72122ce96bfec66e2396d2e25225d70a" id="tgt46" class="tgtSentence">Vlastník</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="712778275c556c187fb77a2b8a2af8c4" id="tgt47" class="tgtSentence">Název zařízení</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c9f4029ce9dcf8ff7f8f1b70edead843" id="tgt48" class="tgtSentence">Sériové číslo</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="c2904bca62b22443d6cf5e9d89cab204" id="tgt49" class="tgtSentence">Výrobce</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="20f35e630daf44dbfa4c3f68f5399d8c" id="tgt50" class="tgtSentence">Model</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="d83f147fd8043b67aa813f44f597b39b" id="tgt51" class="tgtSentence">Operační systém</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="93a4cf66e1c393e83e3c39b8446f1b71" id="tgt52" class="tgtSentence">Firemní aplikace</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="a2da362c93e6fb8f4d57947fe2b2d8fd" id="tgt53" class="tgtSentence">Osobní aplikace</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence sentenceid="87ad91150c1a3f3a735dfa76718c903b" id="tgt54" class="tgtSentence">Po registraci vašeho zařízení může správce IT provádět tyto kroky:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="3b4e79bf899b6aaddd519b0e6a8dfadd" id="tgt55" class="tgtSentence">Obnovit výchozí tovární nastavení v případě ztráty nebo odcizení zařízení.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="0dc37493c4cb02c084f4aa01567938fa" id="tgt56" class="tgtSentence">Odebrat ze zařízení veškerá firemní data a nainstalované obchodní aplikace.</caps:sentence>
                <caps:sentence sentenceid="4764910b571c675b37c4a88b110b1379" id="tgt57" class="tgtSentence"> Vaše osobní údaje a nastavení se při tom neodeberou.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="3dadb4ca038f02975523eaee5a2f3ada" id="tgt58" class="tgtSentence">Vynutit používání hesla nebo PIN kódu v zařízení.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c1aa6cfa75e3c98c83374293c4279f76" id="tgt59" class="tgtSentence">Vyžadovat, abyste přijali smluvní podmínky.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f9877cfa9f701abb70b52dc01c3d35e7" id="tgt60" class="tgtSentence">Povolit nebo zakázat používání fotoaparátu/kamery v zařízení.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c097c9b938d8422cf97d12d1efc19333" id="tgt61" class="tgtSentence">Povolit nebo zakázat procházení webu v zařízení.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="5362d8d186d4d7498f369f45a4547e14" id="tgt62" class="tgtSentence">Povolit nebo zakázat zálohování na serveru služby iCloud.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="c13f97c1c50716363f864c2b1cce7d9e" id="tgt63" class="tgtSentence">Povolit nebo zakázat synchronizaci dokumentů na serveru služby iCloud.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="79bb1f540ce994a1ab04f0803c3f033a" id="tgt64" class="tgtSentence">Povolit nebo zakázat datový proud fotografií na serveru služby iCloud.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="4398056c852a7df9e0825a7d639a7ca5" id="tgt65" class="tgtSentence">Povolit nebo zakázat datový roaming v zařízení.</caps:sentence>
                <caps:sentence sentenceid="49bd0633453334131f4aad248ba87925" id="tgt66" class="tgtSentence"> Pokud je povolen datový roaming, mohou vám za něj být účtovány poplatky.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ba05f106b31276b3e2bf67f2114f974f" id="tgt67" class="tgtSentence">Povolit nebo zakázat hlasový roaming v zařízení.</caps:sentence>
                <caps:sentence sentenceid="98d43910f63da52b360113bdb24faa04" id="tgt68" class="tgtSentence"> Pokud je povolen hlasový roaming, mohou vám za něj být účtovány poplatky.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f1715a111d5a7fc544a6292a3e7c22be" id="tgt69" class="tgtSentence">Povolit nebo zakázat automatickou synchronizaci souborů v režimu roamingu v zařízení.</caps:sentence>
                <caps:sentence sentenceid="9662708499169149cc1ab97ce2053f05" id="tgt70" class="tgtSentence"> Pokud je povolena automatická synchronizace souborů, mohou vám být účtovány poplatky za roaming.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="d25157643cd285dd22c4250eb1198755" id="tgt71" class="tgtSentence">Návod k registraci zařízení najdete v tématu <link xlink:href="#BKMK_ios_enroll_your_device">Enroll your device in Intune</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="true" address="BKMK_ios_whatis_cp_website">
        <title>
          <caps:sentence sentenceid="631be7185536cbfc0dd9092b681d30e8" id="tgt72" class="tgtSentence">Co je web portálu společnosti a k čemu ho můžu použít?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="e3eb16afdbabab150c5da0ade825a14d" id="tgt73" class="tgtSentence">
              <externalLink>
                <linkText>Web portálu společnosti</linkText>
                <linkUri>http://portal.manage.microsoft.com</linkUri>
              </externalLink> je webové rozhraní vaší společnosti, pomocí kterého můžete spravovat pracovní počítače a zařízení a také osobní počítače a zařízení, které chcete použít v práci.</caps:sentence>
            <caps:sentence sentenceid="70037d25cd497b5572e18d1bc35334bc" id="tgt74" class="tgtSentence"> Většinu úloh můžete provést jak na tomto webu, tak v aplikaci Portál společnosti, kterou si nainstalujete do svého zařízení.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="14d658610fe447e446e50ce288d1edc1" id="tgt75" class="tgtSentence">Na webu portál společnosti můžete provádět tyto úlohy:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="3dc0b17542da2ec9d90ff0965d19aef1" id="tgt76" class="tgtSentence">Vyhledat a stáhnout firemní aplikace</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="f82609801e7080daebaa60a46cd06e57" id="tgt77" class="tgtSentence">Přejmenovat zařízení</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="2e254e163be6b2905cf22931f4eb4fe0" id="tgt78" class="tgtSentence">Odebrání zařízení z Intune</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="680b802dd6afc46294bf85411f86cccf" id="tgt79" class="tgtSentence">Obnovení výchozího továrního nastavení v mobilním zařízení</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="ed64c84b76d070c3000586dc8cade916" id="tgt80" class="tgtSentence">Vyhledat kontaktní informace pro správce IT</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section expanded="true" address="BKMK_ios_erase_lost_device">
        <title>
          <caps:sentence sentenceid="c06b6d82e53b630aa8f19483e6047696" id="tgt81" class="tgtSentence">Reset (vymazání) ztraceného nebo odcizeného zařízení</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="245c5877e7e6a3fcf2677b171d1a6d0d" id="tgt82" class="tgtSentence">Pokud se telefon zaregistrovaný v Intune ztratí nebo je odcizený, můžete v něm obnovit výchozí tovární nastavení pomocí aplikace Portál společnosti z jiného zařízení.</caps:sentence>
          </para>
          <alert class="warning">
            <para>
              <caps:sentence sentenceid="dcc73e1b3a07aa18eea2923969792157" id="tgt83" class="tgtSentence">Když zařízení resetujete do výchozího stavu od výrobce, odeberete z něho svoje osobní i pracovní informace.</caps:sentence>
            </para>
          </alert>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence sentenceid="c249a580a5b0e0bb1a4d4d9fbde2c950" id="tgt84" class="tgtSentence">V aplikaci Portál společnosti v části <ui>Moje zařízení</ui> vyberte zařízení, které chcete vymazat.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="298eb8b721760a1ff208e241dcde7e9b" id="tgt85" class="tgtSentence">Klepněte na <ui>Resetovat</ui> &gt; <ui>Resetovat</ui>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="843a6cd618daa054e4a48332cc86acbe" id="tgt86" class="tgtSentence">Pokud se vám ztracené nebo ukradené zařízení nedaří resetovat, požádejte správce IT, aby to udělal za vás.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <maml:section address="BKMK_ios_data_collect" expanded="true" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence sentenceid="b321241f2502b5448f5ba9814524413f" id="tgt87" class="tgtSentence">Vypnutí shromažďování dat Microsoftu o využití</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence sentenceid="613c5729b5d70fe8a98c7d50505d4ea7" id="tgt88" class="tgtSentence">Microsoft automaticky shromažďuje anonymní informace o spolehlivosti, výkonu a použití aplikace Portál společnosti za účelem zlepšení svých produktů a služeb.</caps:sentence>
            <caps:sentence sentenceid="4150fed1487d3933fae6b75759c4e79e" id="tgt89" class="tgtSentence"> Shromažďování těchto dat můžete vypnout pomocí nastavení Údaje o používání v aplikaci Portál společnosti.</caps:sentence>
            <caps:sentence sentenceid="e1193143312e8b74386d45adac2e9d42" id="tgt90" class="tgtSentence"> Správci IT nemají nad shromažďováním údajů žádnou kontrolu a nemůžou u tohoto nastavení změnit vaši volbu.</caps:sentence>
          </maml:para>
        </maml:content>
      </maml:section>
      <section address="BKMK_ios_unenroll_device">
        <title>
          <caps:sentence sentenceid="e7334a6647a4beaf7b7148ac205d9349" id="tgt91" class="tgtSentence">Zrušení registrace zařízení v Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="a0c8593b0b5f285d2c025132d17200c6" id="tgt92" class="tgtSentence">Když zrušíte registraci zařízení v Intune, už nebude mít přístup k prostředkům společnosti a nebude ho spravovat Intune.</caps:sentence>
            <caps:sentence sentenceid="8a58ef3bea6c65abe73ee3e2bc7eb650" id="tgt93" class="tgtSentence"> Další informace o zrušení registrace najdete za návodem.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="33ec116fa4d3a05cebd927de0897af22" id="tgt94" class="tgtSentence">Zrušení registrace zařízení v Intune:</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence sentenceid="c249a580a5b0e0bb1a4d4d9fbde2c950" id="tgt95" class="tgtSentence">V aplikaci Portál společnosti v části <ui>Moje zařízení</ui> vyberte zařízení, u kterého chcete zrušit registraci.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="298eb8b721760a1ff208e241dcde7e9b" id="tgt96" class="tgtSentence">Klepněte na <ui>Odebrat</ui> &gt; <ui>Odebrat</ui>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="715a45f185a63212c320c5ddbe6feb5f" id="tgt97" class="tgtSentence">Jakmile zrušíte registraci zařízení v Intune, stane se toto:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="a30b38d6fe341a32afb8c1fa2ae6f00d" id="tgt98" class="tgtSentence">Vaše zařízení se už nebude zobrazovat v aplikaci Portál společnosti.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="debcc4cc4b3dff0ce773acfc3cba2baa" id="tgt99" class="tgtSentence">Už nebudete moct instalovat aplikace z portálu společnosti.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="8a62e1aa36796068c996249797b79a25" id="tgt100" class="tgtSentence">Nastavení, která se v zařízení změnila od jeho přidání, například zakázání fotoaparátu/kamery nebo vyžadování určité délky hesla, přestanou platit.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="e2e05eddbfd9df781fb51550906d96c8" id="tgt101" class="tgtSentence">Je možné, že již v zařízení nebudete mít přístup k některým prostředkům společnosti, jako jsou sdílené složky nebo interní weby.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="29251bb2bd6e6f53b0484ae712b196d0" id="tgt102" class="tgtSentence">Nebudete již moci v zařízení používat aplikace a data společnosti.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="8e9ba66b81a76d53ce5a21a6475c7517" id="tgt103" class="tgtSentence">Je možné, že se už nebudete moct připojovat k podnikové síti pomocí Wi-Fi nebo virtuální privátní sítě (VPN).</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="7faad2ae257ea90bfa9dde6cb649cd47" id="tgt104" class="tgtSentence">E-mailové profily společnosti jsou ze zařízení odebrané.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="a1e7c55d94cbaa4a92d89ae197836b91" id="tgt105" class="tgtSentence">V aplikaci Portál společnosti a na webu se už nebudou zobrazovat zařízení, která jsou nakonfigurovaná jenom pro použití e-mailu.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section address="BKMK_ios_fix_issues">
        <title>
          <caps:sentence sentenceid="b04d8428c19a919568ee64f356b58ed8" id="tgt106" class="tgtSentence">Oprava problémů se zařízením zaregistrovaným v Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="14d9b1747154aba835a2f168930e2506" id="tgt107" class="tgtSentence">Pokud při použití aplikace Portál společnosti dojde k chybě, můžete odeslat informace o této chybě, abyste svému správci IT pomohli potíže vyřešit.</caps:sentence>
            <caps:sentence sentenceid="41058755961023d4116f03f243580ef1" id="tgt108" class="tgtSentence"> Informace o chybě můžete odeslat různými způsoby:</caps:sentence>
          </para>
          <maml:list class="bullet" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="ee20a7ba889a5cb252dfa456cd075774" id="tgt109" class="tgtSentence">Klepnutím na <maml:ui>Zpráva</maml:ui> v chybové zprávě</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="ee20a7ba889a5cb252dfa456cd075774" id="tgt110" class="tgtSentence">Klepnutím na <maml:ui>Odeslat diagnostickou zprávu</maml:ui> na obrazovce O aplikaci v aplikaci Portál společnosti</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence sentenceid="2856feee4e3cbc9d037d7caa3dc09853" id="tgt111" class="tgtSentence">Tím, že zatřesete zařízením se spuštěnou aplikací Portál společnosti a po zobrazení diagnostické výstrahy klepnete na <maml:ui>E-mail</maml:ui></caps:sentence>
                <caps:sentence sentenceid="a33a5b0675fc3271d2a688ea32558807" id="tgt112" class="tgtSentence"> Pokud zatřesete zařízením, ale žádná výstraha se nezobrazí, otevřete <maml:ui>Nastavení</maml:ui> &gt; <maml:ui>Portál společnosti</maml:ui> a zkontrolujte, jestli je zapnutá možnost <maml:ui>Gesto zatřesením</maml:ui>.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Use these steps for tasks that you need to do on your iOS device when your company is using Microsoft Intune:</caps:sentence>
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
                      <link xlink:href="#BKMK_ios_signin_cp">Install and sign in to the Company Portal app</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_ios_enroll_your_device">Enroll your device in Intune</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_ios_what_happ_enroll">What happens when I install the Company Portal app and enroll my device in Intune?</link>
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
                      <link xlink:href="#BKMK_ios_whatis_cp_website">What is the Company Portal website and what can I do with it?</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_ios_erase_lost_device">Reset (erase) your lost or stolen device</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_ios_data_collect">Turn off Microsoft usage data collection</link>
                    </para>
                  </listItem>
                  <listItem>
                    <para>
                      <link xlink:href="#BKMK_ios_unenroll_device">Unenroll your device from Intune</link>
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
                      <link xlink:href="#BKMK_ios_fix_issues">Fix issues when your device is enrolled in Intune</link>
                    </para>
                  </listItem>
                </list>
              </TD>
            </tr>
          </tbody>
        </table>
      </introduction>
      <maml:section expanded="true" address="BKMK_ios_signin_cp" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence id="src7" class="srcSentence">Install and sign in to the Intune Company Portal app</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence id="src8" class="srcSentence">The Company Portal is an app that you install on your device to give you access to your company or school apps, email, and network.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence">  Before you can get access, you must install the Company Portal app, and then  use the app to enroll your device in Microsoft Intune.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> For more information, see <maml:link xlink:href="#BKMK_ios_what_happ_enroll">What happens when I install the Company Portal app and enroll my device in Intune?</maml:link>.</caps:sentence>
          </maml:para>
          <maml:list class="ordered">
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src11" class="srcSentence">Open the <maml:ui>App Store</maml:ui> and search for <maml:ui>intune</maml:ui>.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src12" class="srcSentence">Download the <maml:ui>Microsoft Intune Company Portal</maml:ui> app.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="6d9d1904-1462-4c29-a3e6-daccf5b8ec7e"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src13" class="srcSentence">Open the Company Portal app, enter your work or school email and password, and then tap <maml:ui>Sign in</maml:ui>.</caps:sentence>
              </maml:para>
              <maml:para>
                <caps:sentence id="src14" class="srcSentence">If you are signing into the Company Portal app for the first time, and your company or school is using Intune, you will be prompted to enroll your device in Intune.</caps:sentence>
                <caps:sentence id="src15" class="srcSentence"> To enroll, follow the steps in <maml:link xlink:href="#BKMK_ios_enroll_your_device">Enroll your device in Intune</maml:link>.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <maml:section address="BKMK_ios_enroll_your_device" expanded="true" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence id="src16" class="srcSentence">Enroll your device in Intune</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence id="src17" class="srcSentence">Enrolling your device in Intune enables you to access the company’s network, your work email and work files, and lets you get company apps.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> For more about what happens when you enroll your device, see <maml:link xlink:href="#BKMK_ios_what_happ_enroll">What happens when I install the Company Portal app and enroll my device in Intune?</maml:link>.</caps:sentence>
          </maml:para>
          <maml:para>
            <caps:sentence id="src19" class="srcSentence">To enroll your device:</caps:sentence>
          </maml:para>
          <maml:list class="ordered">
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src20" class="srcSentence">Follow the steps in  <maml:link xlink:href="#BKMK_ios_signin_cp">Install and sign in to the Intune Company Portal app</maml:link>.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src21" class="srcSentence">On the <maml:ui>Device Enrollment</maml:ui> screen in the Company Portal app, tap <maml:ui>Enroll</maml:ui>.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="0e518c1a-34a8-4b41-bb1d-d178fc7d1b1f"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src22" class="srcSentence">On the <maml:ui>Install Profile</maml:ui> screen, tap <maml:ui>Install</maml:ui>, and enter your passcode, if prompted.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="08071677-4fc9-4f8d-988c-096ad4fc307b"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src23" class="srcSentence"> Tap <maml:ui>Install</maml:ui>.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="2952ad68-e279-4c29-8276-af6b0d38650b"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src24" class="srcSentence"> Tap <maml:ui>Install</maml:ui> to indicate that you've read the warning.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="565f3b1a-671a-4b8c-acfe-967d12e6bdcc"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src25" class="srcSentence"> Tap <maml:ui>Trust</maml:ui>.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="17627759-2f98-4847-b72d-33b3defd1ef4"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src26" class="srcSentence">Tap <maml:ui>Done</maml:ui>.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="5e9d1770-83cd-4df0-b0a9-3f24ee7792f7"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src27" class="srcSentence">Tap <maml:ui>OK</maml:ui>.</caps:sentence>
                <caps:sentence id="src28" class="srcSentence"> Your device is now enrolled in Intune.</caps:sentence>
              </maml:para>
              <maml:mediaLink>
                <maml:image xlink:href="818c0228-bbe4-4760-9590-bc9146820ab5"></maml:image>
              </maml:mediaLink>
            </maml:listItem>
          </maml:list>
        </maml:content>
      </maml:section>
      <section address="BKMK_ios_what_happ_enroll">
        <title>
          <caps:sentence id="src29" class="srcSentence">What happens when I install the Company Portal app and enroll my device in Intune?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src30" class="srcSentence">You start by installing the Company Portal app, and then use the app to enroll your device in Intune.</caps:sentence>
            <caps:sentence id="src31" class="srcSentence"> Once your device is enrolled, you  can use the Company Portal app to:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src32" class="srcSentence">Access the company’s network, and your email and work files</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src33" class="srcSentence">Get company apps from the Company Portal</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src34" class="srcSentence">Automatically configure your company email account</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src35" class="srcSentence">Reset your phone to factory settings if it is lost or stolen</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src36" class="srcSentence">When  you enroll your device in Intune, you are giving your IT administrator permission to manage your device to help protect the company information on the device.</caps:sentence>
          </para>
          <table border="1">
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">IT cannot see</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">IT can see</caps:sentence>
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
                        <caps:sentence id="src39" class="srcSentence">Call history</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src40" class="srcSentence">Text messages</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src41" class="srcSentence">Personal email, contacts, and calendar</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src42" class="srcSentence">Web history</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src43" class="srcSentence">Location</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src44" class="srcSentence">Camera roll</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src45" class="srcSentence">Personal data</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
                <TD>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src46" class="srcSentence">Owner</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src47" class="srcSentence">Device name</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src48" class="srcSentence">Serial number</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src49" class="srcSentence">Manufacturer</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src50" class="srcSentence">Model</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src51" class="srcSentence">Operating system</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src52" class="srcSentence">Company apps</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src53" class="srcSentence">Personal apps</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                </TD>
              </tr>
            </tbody>
          </table>
          <para>
            <caps:sentence id="src54" class="srcSentence">When your device is enrolled, your IT administrator can:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src55" class="srcSentence">Reset your device back to manufacturer’s default settings if the device is lost or stolen.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src56" class="srcSentence">Remove all installed company-related data and business apps.</caps:sentence>
                <caps:sentence id="src57" class="srcSentence"> Your personal data and settings aren’t removed.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src58" class="srcSentence">Require you to have a password or PIN on the device.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src59" class="srcSentence">Require you to accept terms and conditions.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src60" class="srcSentence">Enable or disable the camera on your device.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src61" class="srcSentence">Enable or disable web browsing on your device.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src62" class="srcSentence">Enable or disable backup to iCloud.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src63" class="srcSentence">Enable or disable document sync to iCloud.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src64" class="srcSentence">Enable or disable Photo Stream to iCloud.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src65" class="srcSentence">Enable or disable data roaming on your device.</caps:sentence>
                <caps:sentence id="src66" class="srcSentence"> If data roaming is allowed, roaming charges may be incurred.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src67" class="srcSentence">Enable or disable voice roaming on your device.</caps:sentence>
                <caps:sentence id="src68" class="srcSentence"> If voice roaming is allowed, roaming charges may be incurred.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src69" class="srcSentence">Enable or disable automatic file synchronization while in roaming mode on your device.</caps:sentence>
                <caps:sentence id="src70" class="srcSentence"> If automatic file synchronization is allowed, roaming charges may be incurred.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src71" class="srcSentence">For the steps on how to enroll your device, see <link xlink:href="#BKMK_ios_enroll_your_device">Enroll your device in Intune</link>.</caps:sentence>
          </para>
        </content>
      </section>
      <section expanded="true" address="BKMK_ios_whatis_cp_website">
        <title>
          <caps:sentence id="src72" class="srcSentence">What is the Company Portal website and what can I do with it?</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src73" class="srcSentence">The <externalLink><linkText>Company Portal website</linkText><linkUri>http://portal.manage.microsoft.com</linkUri></externalLink> is your company’s web interface that you use to manage your work computers and devices, and your personal computers and devices that you choose to use at work.</caps:sentence>
            <caps:sentence id="src74" class="srcSentence"> You can do most of the same tasks on this website that you can do by using the Company Portal app that you install on your device.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src75" class="srcSentence">You can do the following tasks from the Company Portal website:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src76" class="srcSentence">Browse for and download company apps</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src77" class="srcSentence">Rename your device</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src78" class="srcSentence">Remove your device from Intune</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src79" class="srcSentence">Reset your mobile device to its factory default settings</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src80" class="srcSentence">Find contact information for your IT administrator</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section expanded="true" address="BKMK_ios_erase_lost_device">
        <title>
          <caps:sentence id="src81" class="srcSentence">Reset (erase) your lost or stolen device</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src82" class="srcSentence">If a phone that has been enrolled in Intune is lost or stolen, you can reset it to factory default settings by using the Company Portal app from a different device.</caps:sentence>
          </para>
          <alert class="warning">
            <para>
              <caps:sentence id="src83" class="srcSentence">Resetting a device to factor defaults removes both your personal and work information from it!</caps:sentence>
            </para>
          </alert>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence id="src84" class="srcSentence">In the Company Portal app, under <ui>My Devices</ui>,  select the device you want to erase.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src85" class="srcSentence">Tap  <ui>Reset</ui> &gt; <ui>Reset</ui>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <alert class="note">
            <para>
              <caps:sentence id="src86" class="srcSentence">If you are unable to reset your lost or stolen device, contact IT to reset it for you.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <maml:section address="BKMK_ios_data_collect" expanded="true" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
        <maml:title>
          <caps:sentence id="src87" class="srcSentence">Turn off Microsoft usage data collection</caps:sentence>
        </maml:title>
        <maml:content>
          <maml:para>
            <caps:sentence id="src88" class="srcSentence">In order to improve its products and services, Microsoft automatically collects anonymous data about the reliability and performance of the Company Portal app and how it is used.</caps:sentence>
            <caps:sentence id="src89" class="srcSentence"> You can turn off the collection of that data by using the Usage Data setting in the Company Portal app.</caps:sentence>
            <caps:sentence id="src90" class="srcSentence"> IT administrators have no control over the collection of the data, and they cannot change your selection for the setting.</caps:sentence>
          </maml:para>
        </maml:content>
      </maml:section>
      <section address="BKMK_ios_unenroll_device">
        <title>
          <caps:sentence id="src91" class="srcSentence">Unenroll your device from Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src92" class="srcSentence">When you unenroll your device from Intune, your device will not longer be able to access company resources and will no longer be managed by Intune.</caps:sentence>
            <caps:sentence id="src93" class="srcSentence"> More information about unenrolling follows the steps.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src94" class="srcSentence">To unenroll your device from Intune:</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence id="src95" class="srcSentence">In the Company Portal app, under <ui>My Devices</ui>,  select the device you want to unenroll.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src96" class="srcSentence">Tap  <ui>Remove</ui> &gt; <ui>Remove</ui>.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src97" class="srcSentence">When you unenroll your device from Intune, here's what happens:</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src98" class="srcSentence">Your device won’t appear in the Company Portal anymore</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src99" class="srcSentence">You can’t install apps from the Company Portal anymore.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src100" class="srcSentence">Any settings that were changed on your device when you added it (for example, disabling the camera, or requiring a certain password length) will no longer apply.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src101" class="srcSentence">You might not have access to some company resources, such as file shares or internal web sites, on your device anymore.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src102" class="srcSentence">You can’t use company apps and company data on your device anymore.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src103" class="srcSentence">You might not be able to connect to your company network using Wi-Fi or a virtual private network (VPN) anymore.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src104" class="srcSentence">Company email profiles are removed from the device.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src105" class="srcSentence">Devices that are configured for email only won't appear in the Company Portal app or website anymore.</caps:sentence>
              </para>
            </listItem>
          </list>
        </content>
      </section>
      <section address="BKMK_ios_fix_issues">
        <title>
          <caps:sentence id="src106" class="srcSentence">Fix issues when your device is enrolled in Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src107" class="srcSentence">If you get an error while you’re using the Company Portal app, you can send information about the error to help your IT admin troubleshoot the problem.</caps:sentence>
            <caps:sentence id="src108" class="srcSentence"> You can send error information in different ways:</caps:sentence>
          </para>
          <maml:list class="bullet" xmlns:maml="http://ddue.schemas.microsoft.com/authoring/2003/5">
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src109" class="srcSentence">By tapping <maml:ui>Report</maml:ui> on error alert messages.</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src110" class="srcSentence">By tapping <maml:ui>Send Diagnostic Report</maml:ui> on the About screen of the Company Portal app</caps:sentence>
              </maml:para>
            </maml:listItem>
            <maml:listItem>
              <maml:para>
                <caps:sentence id="src111" class="srcSentence">By shaking your device while you’re in the Company Portal app, and then tapping <maml:ui>Email</maml:ui> when the Diagnostics alert appears.</caps:sentence>
                <caps:sentence id="src112" class="srcSentence"> If the alert doesn’t appear when you shake the device, open <maml:ui>Settings</maml:ui> &gt; <maml:ui>Company Portal</maml:ui>, and make sure that the <maml:ui>Shake Gesture</maml:ui> option is on.</caps:sentence>
              </maml:para>
            </maml:listItem>
          </maml:list>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>