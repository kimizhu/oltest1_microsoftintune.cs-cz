---
description: na
keywords: na
title: Set up Windows Phone management with Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 61e9b6c3-8795-49b0-8ab2-a9a05ee3ea1f
---
# Nastaven&#237; spr&#225;vy pro zař&#237;zen&#237; Windows Phone v Microsoft Intune
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="cs-CZ">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="0a604f324c694ee705db618e2cc994e9" id="tgt1" class="tgtSentence">Předtím, než můžete spravovat mobilní zařízení Windows Phone v <token>wit_nextref</token>, je třeba nastavit požadavky na správu.</caps:sentence>
          <caps:sentence sentenceid="6f851c45e9fe79c5ab6de4130d2b9cbe" id="tgt2" class="tgtSentence"> Vytvořením DNS CNAME uživatelům usnadníte připojení k portálu společnosti <token>wit_nextref</token>.</caps:sentence>
          <caps:sentence sentenceid="5048746af5eac71abe898d904199556e" id="tgt3" class="tgtSentence"> Windows Phone 8.0 vyžaduje certifikát Symantec k navázání šifrovaného připojení IP mezi zařízeními a <token>wit_nextref</token>.</caps:sentence>
          <caps:sentence sentenceid="7596d820b20382b1f595d4fa01fc958a" id="tgt4" class="tgtSentence"> Windows Phone 8.1 může také, v závislosti na tom, jak uživatelé přistupují k firemnímu portálu.</caps:sentence>
          <caps:sentence sentenceid="2d1734cd0fa2c65f906473cecceca448" id="tgt5" class="tgtSentence"> Certifikát je také nutný k podepsání obchodních aplikací.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="2a52668cbd9bfc247e2bf159f9d980ce" id="tgt6" class="tgtSentence">
                <embeddedLabel>Windows Phone 8.1</embeddedLabel> – Certifikát se vyžaduje jenom pokud:</caps:sentence>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <caps:sentence sentenceid="e22b0f840d2e0467c16eb174f11e04f2" id="tgt7" class="tgtSentence">Uživatelé nebudou stahovat portál společnosti ze Storu.</caps:sentence>
                </para>
              </listItem>
              <listItem>
                <para>
                  <caps:sentence sentenceid="f0de3decc6ae84fd99714b0ad425c29d" id="tgt8" class="tgtSentence">Budete nasazovat obchodní (neboli zkušebně načtené) aplikace.</caps:sentence>
                </para>
              </listItem>
            </list>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="323f02ea3fa5ad027c887ea625be0018" id="tgt9" class="tgtSentence">
                <embeddedLabel>Windows Phone 8</embeddedLabel> – Certifikát se vyžaduje. </caps:sentence>
            </para>
          </listItem>
        </list>
        <mediaLink>
          <image xlink:href="b457bc08-2634-4137-86f6-5f7cc330fbd2"></image>
        </mediaLink>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="d4e96b071977754f0ffe26a9bede39c0" id="tgt10" class="tgtSentence">Příprava na správu mobilních zařízení Windows Phone s Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="37424f9fbd3c42659c22e62c71daf0f2" id="tgt11" class="tgtSentence">Nastavení požadavků pro správu mobilních zařízení Windows Phone závisí na tom, jak budete zařízení spravovat.</caps:sentence>
            <caps:sentence sentenceid="42c1899193d3a45f4bb620920c6b9b20" id="tgt12" class="tgtSentence">  Nastavení dvou záznamů CNAME v registraci DNS vaší společnosti usnadňuje uživatelům registraci zařízení.</caps:sentence>
            <caps:sentence sentenceid="f5b7fd6292695d16931124513f401587" id="tgt13" class="tgtSentence"> Pokud vaši uživatelé budou stahovat aplikaci Portál společnosti ze Storu, pak po konfiguraci nastavení DNS bude třeba jen nastavit firemní portál a informovat uživatele o tom, jak se zaregistrovat.</caps:sentence>
            <caps:sentence sentenceid="1ce89ba3e652aab3dc4cbc73697fd68e" id="tgt14" class="tgtSentence">  U Windows Phone 8.0 nebo Windows Phone 8.1, kde nasadíte Portál společnosti, budete pro podepsání kódu aplikace potřebovat certifikát Symantec.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence sentenceid="27a772f8b3aee6a88266de7b2f38dd01" id="tgt15" class="tgtSentence">Nastavení registrace Windows Phone v Intune</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt16" class="tgtSentence">
                      <embeddedLabel>Nastavení<token>wit_nextref</token></embeddedLabel> <br />Pokud jste to ještě neudělali, připravte se na správu mobilních zařízení <externalLink><linkText>nastavením autority pro správu mobilních zařízení</linkText><linkUri>https://technet.microsoft.com/library/mt346013.aspx</linkUri></externalLink> na <embeddedLabel>Microsoft Intune</embeddedLabel>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9781b62d0e687e3d5e772f805a335d75" id="tgt17" class="tgtSentence">
                      <embeddedLabel>Nastavení aliasu DNS pro adresu serveru registrace (volitelně)</embeddedLabel>
                      <br /> </caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="f560aa912f671a18f3703213593be7cb" id="tgt18" class="tgtSentence">Alias DNS (typ záznamu CNAME) uživatelům usnadňuje registraci zařízení tím, že se při registraci automaticky vyplní název serveru.</caps:sentence>
                  </para>
                  <procedure>
                    <title>
                      <caps:sentence sentenceid="749993060a7e3a66e889394faf5c9e22" id="tgt19" class="tgtSentence">Ověření a vytvoření DNS CNAME</caps:sentence>
                    </title>
                    <steps class="ordered">
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt20" class="tgtSentence">V <externalLink target="_blank"><linkText>konzole pro správu Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> klikněte na <ui>Správa</ui> &gt; <ui>Správa mobilních zařízení</ui> &gt; <ui>Windows Phone</ui>.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="5471ca9a49d6463fbc7f3306fe385bd7" id="tgt21" class="tgtSentence">Zadejte adresu URL ověřené domény webu společnosti do pole <ui>Zadat název ověřené domény</ui> a klikněte na <ui>Test automatického zjištění</ui>.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="e7791f265c2e6ed258d1beb636e351c5" id="tgt22" class="tgtSentence">Vytvořte záznamy o prostředcích CNAME pro doménu vaší společnosti.</caps:sentence>
                            <caps:sentence sentenceid="e38c4e5bb6340155dd5172a5b1971886" id="tgt23" class="tgtSentence"> Záznamy o prostředcích CNAME musí obsahovat tyto informace:</caps:sentence>
                          </para>
                          <table border="1">
                            <thead>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="599dcce2998a6b40b1e38e8c6006cb0a" id="tgt24" class="tgtSentence">TYP</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="7bac9dc63b9408f7043a63c902ca5bdf" id="tgt25" class="tgtSentence">Název hostitele</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="9a69c94d460695b849447f29c4698904" id="tgt26" class="tgtSentence">Odkazuje na</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="c431a4425bc56080c868435c8d910f83" id="tgt27" class="tgtSentence">Hodnota TTL</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                            </thead>
                            <tbody>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="056301054c43f8bbea2090debfec16b1" id="tgt28" class="tgtSentence">CNAME</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <caps:sentence sentenceid="8e2237c00eca06c96d1d66c5a5b546c7" id="tgt29" class="tgtSentence">  <para>enterpriseenrollment.doména_společnosti.com</para></caps:sentence>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="103f16169e6c5483d3c3522b5673024d" id="tgt30" class="tgtSentence">manage.microsoft.com
</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="72ab9d0304d3e84c6aa2dd15eda282f2" id="tgt31" class="tgtSentence">1 hodina</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="056301054c43f8bbea2090debfec16b1" id="tgt32" class="tgtSentence">CNAME</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt33" class="tgtSentence"> <para>enterpriseregistration.doména_společnosti.com</para></caps:sentence>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="b8e596718f436b22e7d47c18522a0117" id="tgt34" class="tgtSentence">enterpriseregistration.windows.net
</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence sentenceid="72ab9d0304d3e84c6aa2dd15eda282f2" id="tgt35" class="tgtSentence">1 hodina</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                            </tbody>
                          </table>
                          <para>
                            <caps:sentence sentenceid="0ddb188e0c3d6f753fa556e387c3eedb" id="tgt36" class="tgtSentence">Pokud je třeba web vaší společnosti contoso.com, vytvořili byste záznam CNAME ve službě DNS, který přesměruje adresu EnterpriseEnrollment.contoso.com na manage.microsoft.com.</caps:sentence>
                            <caps:sentence sentenceid="74ebccfb9a34b27966e6e47a30e9a2ac" id="tgt37" class="tgtSentence"> Pokud existuje víc než jedna ověřená doména, vytvořte záznam CNAME pro každou doménu.</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="fc2c4794f88183cd526fc7be558726b6" id="tgt38" class="tgtSentence">
                                  <codeInline>manage.microsoft.com</codeInline> – Podporuje přesměrování na služby Intune s rozpoznáním domény z doménového názvu e-mailu.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="a2983dbe3d567d4058550acda540ca05" id="tgt39" class="tgtSentence">
                                  <codeInline>enterpriseregistration.windows.net</codeInline> – Podporuje připojení pracovního místa pro mobilní zařízení.</caps:sentence>
                                <caps:sentence sentenceid="99fde62d77c6759ad6803da7822eab47" id="tgt40" class="tgtSentence"> Mimoto podporuje i podmíněný přístup pro Windows 8.1.</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </content>
                      </step>
                    </steps>
                  </procedure>
                  <mediaLink>
                    <image xlink:href="33622fc8-d7ad-4f20-a4ec-c50de6a158bc"></image>
                  </mediaLink>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="a596843407babf6e4c25e584affedd4b" id="tgt41" class="tgtSentence">
                      <embeddedLabel>Správa certifikátů pro podporu podepisování aplikací</embeddedLabel>
                      <br />[Vyžaduje se pro Windows Phone 8.0 a Windows Phone 8.1, které nemají přístup k Windows Phone Storu nebo potřebují obchodní aplikace.]</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="1ea59c51f5e88f231ce3342443a35380" id="tgt42" class="tgtSentence">Aby šlo podporovat aplikaci Portál společnosti pro Windows Phone 8.0 a nasazovat firemní aplikace na Windows Phone 8.1, musíte získat certifikát <embeddedLabel>Symantec Enterprise Mobile Code Signing Certificate</embeddedLabel>.</caps:sentence>
                    <caps:sentence sentenceid="1973c953a5aedfde14cbef8d3a7448e3" id="tgt43" class="tgtSentence"> Nejde použít certifikát vydaný vlastní certifikační autoritou, protože pro zařízení Windows Phone je důvěryhodný jen certifikát Symantec.</caps:sentence>
                    <caps:sentence sentenceid="2ff6639b8ad24df47cc02757d66f1c8a" id="tgt44" class="tgtSentence"> Tento certifikát se vyžaduje, aby se dalo:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="eed648e5bed91d657e01816fdb7be98c" id="tgt45" class="tgtSentence">Podepsat aplikaci Portál společnosti pro nasazení do <token>winphone8_client_1</token> za účelem registrace a správy telefonu.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="a4104207177adb1ac885342c9c759d74" id="tgt46" class="tgtSentence">Podepsat firemní aplikace tak, aby je <token>wit_nextref</token> mohl nasadit do telefonů Windows Phone.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="d1aee644e17abda9397214172b7615de" id="tgt47" class="tgtSentence">Další informace najdete v tématu <externalLink><linkText>Nejčastější dotazy ke správě mobilních zařízení Windows Phone</linkText><linkUri>https://technet.microsoft.com/en-us/library/dn764959.aspx#BKMK_FAQ</linkUri></externalLink>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="37e3d99e42a049de76e0dfebd9dfb8f9" id="tgt48" class="tgtSentence">Následující postup vám pomůže získat požadované certifikáty a podepsat aplikace firemního portálu.</caps:sentence>
                    <caps:sentence sentenceid="28646b41405959e87441d471b331ff11" id="tgt49" class="tgtSentence"> Budete potřebovat účet Centrum vývojářů pro Windows Phone a pak budete muset zakoupit certifikát Symantec.</caps:sentence>
                  </para>
                  <procedure expanded="false" address="BKMK_CodeSign">
                    <title>
                      <caps:sentence sentenceid="ff3c52f78f7a2aa39610b4221277e835" id="tgt50" class="tgtSentence">Získání certifikátu a podepsání kódu Portálu společnosti</caps:sentence>
                    </title>
                    <steps class="ordered">
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt51" class="tgtSentence">
                              <embeddedLabel>Připojení k centru vývojářů pro Windows Phone</embeddedLabel> <br />Až se budete přihlašovat k zakoupení firemního účtu, připojte se k <externalLink target="_blank"><linkText>Centru vývojářů pro Windows Phone</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268442</linkUri></externalLink> pomocí informací o firemním účtu.</caps:sentence>
                            <caps:sentence sentenceid="a261c9138f990d03116c76f848cafd13" id="tgt52" class="tgtSentence"> Certifikát pro podepisování kódu obdržíte až po schválení žádosti vedoucím pracovníkem společnosti.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt53" class="tgtSentence">
                              <embeddedLabel>Získejte pro společnost certifikát Symantec</embeddedLabel>
                              <br />Pomocí ID společnosti Symantec zakupte certifikát z <externalLink target="_blank"><linkText>webu společnosti Symantec</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268441</linkUri></externalLink>.</caps:sentence>
                            <caps:sentence sentenceid="c139bb5145d959ef2cde38b0e3628817" id="tgt54" class="tgtSentence"> Po zakoupení certifikátu obdrží schvalovatel, kterého jste uvedli v účtu Windows Phone Dev Center, e-mail požadující schválení žádosti o certifikát.</caps:sentence>
                            <caps:sentence sentenceid="25dd18ac503217d095e40e9383a2e9c3" id="tgt55" class="tgtSentence"> Další informace o požadavku na certifikát Symantec najdete v tématu <externalLink><linkText>Proč Windows Phone vyžaduje certifikát Symantec?</linkText><linkUri>https://technet.microsoft.com/en-us/library/dn764959.aspx#BKMK_Symantec</linkUri></externalLink> Nejčastější dotazy k registraci zařízení Windows</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt56" class="tgtSentence">
                              <embeddedLabel>Import certifikátů</embeddedLabel>
                              <br />Jakmile se žádost schválí, obdržíte e-mail s pokyny k importování certifikátů.</caps:sentence>
                            <caps:sentence sentenceid="203edf623515d6f2eae34af754786d57" id="tgt57" class="tgtSentence"> Postupujte podle pokynů v e-mailu pro import certifikátů.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt58" class="tgtSentence">
                              <embeddedLabel>Ověření importovaných certifikátů</embeddedLabel>
                              <br />Abyste se přesvědčili, že se certifikáty importovaly správně, přejděte do modulu snap-in <ui>Certifikáty</ui>, klikněte pravým tlačítkem na <ui>Certifikáty</ui> a vyberte <ui>Hledat certifikáty</ui>.</caps:sentence>
                            <caps:sentence sentenceid="4f4f145aafdf6ea8a38164ebe7706661" id="tgt59" class="tgtSentence"> Do pole <ui>Obsahuje</ui> zadejte „Symantec“ a klikněte na <ui>Najít</ui>.</caps:sentence>
                            <caps:sentence sentenceid="4f457d2e2b9d837831a16cf2dafd91fe" id="tgt60" class="tgtSentence"> Importované certifikáty by se měly zobrazit ve výsledcích.</caps:sentence>
                          </para>
                          <para>
                            <mediaLinkInline>
                              <image xlink:href="52f7f33c-987f-48ad-b661-d826489044cd"></image>
                            </mediaLinkInline>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt61" class="tgtSentence">
                              <embeddedLabel>Export podpisového certifikátu</embeddedLabel>
                              <br />Jakmile ověříte, že jsou certifikáty dostupné, můžete exportovat soubor .pfx a podepsat Portál společnosti.</caps:sentence>
                            <caps:sentence sentenceid="95b28e0eac464de8a1ea35219cdc8fd6" id="tgt62" class="tgtSentence"> Vyberte certifikát Symantec se <ui>zamýšleným účelem</ui> „podepisování kódu”.</caps:sentence>
                            <caps:sentence sentenceid="9df574524024f4ac803c969217c4c6b1" id="tgt63" class="tgtSentence"> Klikněte pravým tlačítkem na certifikát pro podpis kódu a vyberte <ui>Exportovat</ui>.</caps:sentence>
                          </para>
                          <para>
                            <mediaLinkInline>
                              <image xlink:href="a5e198a5-7d2b-4797-bdfa-853a8e664b3c"></image>
                            </mediaLinkInline>
                          </para>
                          <para>
                            <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt64" class="tgtSentence">V <ui>Průvodci exportem certifikátu</ui> vyberte <ui>Ano, exportovat soukromý klíč</ui> a klikněte na <ui>Další</ui>.</caps:sentence>
                            <caps:sentence sentenceid="7215ee9c7d9dc229d2921a40e899ec5f" id="tgt65" class="tgtSentence"> Vyberte <ui>Personal Information Exchange –PKCS #12 (.PFX)</ui> a zaškrtněte políčko <ui>Zahrnout všechny certifikáty do cesty certifikátu (pokud je to možné)</ui>.</caps:sentence>
                            <caps:sentence sentenceid="476c3dffb6ddcfdd6308dcf7ac393bb6" id="tgt66" class="tgtSentence"> Dokončete průvodce.</caps:sentence>
                            <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt67" class="tgtSentence"> Další informace naleznete v tématu <externalLink><linkText>Exportování certifikátu se soukromým klíčem</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=203031</linkUri></externalLink>.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <embeddedLabel>
                              <caps:sentence sentenceid="09b777d4b84b7ca37eca8d47cb17a4f7" id="tgt68" class="tgtSentence">Stažení a podepsání aplikace Portál společnosti</caps:sentence>
                            </embeddedLabel>
                            <br />
                          </para>
                          <para>
                            <caps:sentence sentenceid="2fb11af53d6b4d40a30c696b128fe5fa" id="tgt69" class="tgtSentence">Podpora pro registraci zařízení s Windows Phone vyžaduje podepsanou a na Intune nahranou aplikaci Portál společnosti Windows Phone 8.0.</caps:sentence>
                          </para>
                          <procedure expanded="true">
                            <title>
                              <caps:sentence sentenceid="5df8bc8d708ed06a1927b3b6dcff7f22" id="tgt70" class="tgtSentence">Windows Phone 8.0: Stažení a podepsání aplikace Portál společnosti </caps:sentence>
                            </title>
                            <steps class="ordered">
                              <step>
                                <content>
                                  <para>
                                    <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt71" class="tgtSentence">
                                      <embeddedLabel>Stažení firemního portálu</embeddedLabel> <br />Stáhněte <externalLink target="_blank"><linkText>Portál společnosti Intune pro Windows Phone</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268440</linkUri></externalLink> ze služby Stažení softwaru.</caps:sentence>
                                    <caps:sentence sentenceid="66a94af7ea41447f1131ef2d9f973fd4" id="tgt72" class="tgtSentence"> Výchozí umístění instalace je <codeInline>C:\Program Files (x86)\Microsoft Corporation\Windows Intune Company Portal for Windows Phone</codeInline>.</caps:sentence>
                                  </para>
                                </content>
                              </step>
                              <step>
                                <content>
                                  <para>
                                    <caps:sentence sentenceid="23bd19fcedd382955bc35818765ace04" id="tgt73" class="tgtSentence">
                                      <embeddedLabel>Stažení sady Windows Phone 8.0 SDK</embeddedLabel>
                                      <br />Stáhněte sadu <externalLink target="_blank"><linkText>Windows Phone SDK</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615570</linkUri></externalLink>.</caps:sentence>
                                  </para>
                                </content>
                              </step>
                              <step>
                                <content>
                                  <para>
                                    <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt74" class="tgtSentence">
                                      <embeddedLabel>Podepsání kódu aplikace Portál společnosti</embeddedLabel>
                                      <br />Pomocí aplikace XAPSignTool stažené společně se sadou SDK podepište firemní portál souborem .pfx, který jste vytvořili z certifikátu Symantec.</caps:sentence>
                                    <caps:sentence sentenceid="1070f425823a6e05a98eb2d747f0c53d" id="tgt75" class="tgtSentence"> Další informace najdete v tématu <externalLink target="_blank"><linkText>Podepsání firemní aplikace pomocí XapSignTool</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=280195</linkUri></externalLink>.</caps:sentence>
                                  </para>
                                </content>
                              </step>
                            </steps>
                          </procedure>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt76" class="tgtSentence">
                              <embeddedLabel>Nahrání aplikace Portál společnosti do služby <token>wit_nextref</token></embeddedLabel>
                              <br />Nahráním podepsaného souboru aplikace firemního portálu a svého certifikátu pro podpis kódu zpřístupníte aplikaci vašim koncovým uživatelům.</caps:sentence>
                          </para>
                          <list class="ordered">
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="004dc0ceb5e9b2247446dc0a40f7a169" id="tgt77" class="tgtSentence">V <externalLink target="_blank"><linkText>konzole pro správu Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> klikněte na <ui>Správa</ui> &gt; <ui>Windows Phone</ui>.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="41ad10da17628099ea69f30e0bc238ba" id="tgt78" class="tgtSentence">Klikněte na <ui>Nahrát podepsaný soubor aplikace</ui> a přihlaste se svým ID správce pro <token>wit_nextref</token>.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt79" class="tgtSentence">Na stránce <ui>Instalace softwaru</ui> přejděte v části <ui>Zadejte umístění instalačních souborů softwaru</ui> na umístění aplikace Portál společnosti (.xap pro Windows Phone 8.0 nebo .appx pro Windows Phone 8.1) s podepsaným kódem.</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence sentenceid="a3dd3999c7c2f2311b445428e3279147" id="tgt80" class="tgtSentence">Pokud hodnotíte <token>wit_nextref</token> a nahráváte soubor aplikace s podepsaným kódem ve zkušební verzi účtu <token>wit_nextref</token>, zrušte zaškrtnutí políčka <ui>Použijte soubor aplikace z portálu společnosti podepsaný ukázkovým certifikátem pro podepisování kódu od společnosti Symantec</ui>.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="699e0486160e2a34fb947dc0d669fb82" id="tgt81" class="tgtSentence">Přidejte soubor certifikátu (.pfx), který jste exportovali do <ui>certifikátu pro podpis kódu</ui> a vytvořte pro tento certifikát heslo.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="87c942eae0180b2f79691fe9cf6c988f" id="tgt82" class="tgtSentence">Na stránce <ui>Popis softwaru</ui> vyplňte příslušná pole. Nezapomeňte, že uživatelé při zobrazení podrobností o aplikaci na firemním portálu uvidí tyto informace na svých zařízeních.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence sentenceid="2267545103c9e1387bf304a0df2c06f5" id="tgt83" class="tgtSentence">Dokončete průvodce.</caps:sentence>
                                <caps:sentence sentenceid="fa2ac8e896b35eb1e96d789e6f67fffc" id="tgt84" class="tgtSentence"> Uživatelé, kteří si zaregistrovali zařízení Windows Phone 8.0, teď získají během registrace na svá zařízení aplikaci firemního portálu.</caps:sentence>
                                <caps:sentence sentenceid="ba525c5963210483a84bfef0dd02203d" id="tgt85" class="tgtSentence"> Uživatelé Windows Phone 8.1 můžou nainstalovat aplikaci Portál společnosti z Windows Storu.</caps:sentence>
                                <caps:sentence sentenceid="d56409e2c2ed2fbf8715df89e747e428" id="tgt86" class="tgtSentence">  Pokud se zařízení s Windows Phone 8.1 na Windows Phone Storu blokují nebo pokud chcete nasadit aplikaci Portál společnosti přes Intune, musíte si stáhnout a podepsat aplikaci Portál společnosti Windows Phone 8.1 (SSP.appx).</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </content>
                      </step>
                    </steps>
                  </procedure>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt87" class="tgtSentence">
                      <embeddedLabel>Přidejte uživatele Intune.</embeddedLabel> <br />Abyste mohli mobilní zařízení zaregistrovat, musí být jeho vlastník přidaný do portálu účtu Microsoft Intune.</caps:sentence>
                    <caps:sentence sentenceid="4ad3f37ced51ee31a6023786a31e0a36" id="tgt88" class="tgtSentence"> Přihlaste se k <externalLink><linkText>portálu účtu Microsoft Intune</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=698854</linkUri></externalLink>, klikněte na <ui>Přidat uživatele</ui> a vyberte některou možnost:</caps:sentence>
                  </para>
                  <para></para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="18c21fa550c6e43924af228a0679d742" id="tgt89" class="tgtSentence">
                          <embeddedLabel>Uživatel</embeddedLabel>: Pokud chcete přidat jednoho uživatele, vyberte <ui>Nový</ui> &gt; <ui>Uživatel</ui> a zadejte <ui>Podrobnosti</ui>, <ui>Přiřazení rolí</ui>, <ui>Nastavit umístění uživatele</ui> a zařaďte uživatele do <ui>skupiny</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence sentenceid="a2f878d4f238f251d1ca75147c9c0fbf" id="tgt90" class="tgtSentence">
                          <embeddedLabel>Hromadné přidání</embeddedLabel>: Vytvořte soubor .csv (podívejte se na dodané ukázkové soubory) a importujte ho do portálu účtu Intune.</caps:sentence>
                        <caps:sentence sentenceid="c1b650589e7e36a0c106e31a527a915b" id="tgt91" class="tgtSentence"> Zadejte role, umístění, skupiny a vytvořte účty.</caps:sentence>
                        <caps:sentence sentenceid="310c151380683e4137bd81b5c16379fa" id="tgt92" class="tgtSentence"> Ukázkové i prázdné soubory .csv si můžete stáhnout z portálu účtu Microsoft Intune.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence sentenceid="665358b9ae967c6584e5f22475cbb77e" id="tgt93" class="tgtSentence">Můžete taky povolit synchronizaci s Active Directory nebo s Azure Active Directory.</caps:sentence>
                    <caps:sentence sentenceid="ccabfe774f8edea6ef04ff48472298c4" id="tgt94" class="tgtSentence"> Pokud chcete další informace o integraci jiných uživatelů Azure Active Directory do Intune, přečtěte si téma <externalLink><linkText>Synchronizace adresářů: rozcestník</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=511540</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9781b62d0e687e3d5e772f805a335d75" id="tgt95" class="tgtSentence">
                      <embeddedLabel>Vytváření skupin </embeddedLabel> (volitelné)<br />Skupiny nabízejí flexibilitu při správě zařízení a uživatelů.</caps:sentence>
                    <caps:sentence sentenceid="507c76716449010dc59f1483e3964cd5" id="tgt96" class="tgtSentence"> Můžete je nastavit tak, aby odpovídaly potřebám vaší organizace (třeba podle zeměpisného umístění, oddělení nebo vlastností hardwaru).</caps:sentence>
                    <caps:sentence sentenceid="e3d2410d4aed3acc53c4e7d50a0202e7" id="tgt97" class="tgtSentence">   Viz <link xlink:href="eb9b01ce-9b9b-4c2a-bf99-3879c0bdaba5">Use groups to manage users and devices with Microsoft Intune</link>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt98" class="tgtSentence">
                    <para>
                      <embeddedLabel>Přidání zásad pro zařízení</embeddedLabel> (volitelné)<br />Zásady jsou skupiny nastavení, které řídí funkce na zařízeních. Většina zásad MDM je specifických pro platformu. Zásady se vytvářejí pomocí šablon, které obsahují doporučená nebo přizpůsobená nastavení. Potom je můžete nasadit do skupin. Viz <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</para> </caps:sentence>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="ebc4e07b040da274fbcd0bc615d552aa" id="tgt99" class="tgtSentence">
                      <embeddedLabel>Nastavte limit registrovaných zařízení.</embeddedLabel> (volitelné) <br />Pokud chcete omezit počet mobilních zařízení, která si může uživatel zaregistrovat, přihlaste se ke <externalLink><linkText>konzole pro správu Microsoft Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, klikněte na <ui>Správce</ui> &gt; <ui>Správa mobilních zařízení</ui> &gt; <ui>Pravidla registrace</ui>.</caps:sentence>
                    <caps:sentence sentenceid="81896f17af8e74876e83bdcbfb84232d" id="tgt100" class="tgtSentence"> Vyberte maximální počet zařízení, které může uživatel zaregistrovat, a klikněte na <ui>Uložit</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="486bbd9b1c2d83f16fd091ae8a3e3110" id="tgt101" class="tgtSentence">
                      <embeddedLabel>Nastavte portál firmy.</embeddedLabel>
                      <br /> Portál společnosti Intune můžete přizpůsobit potřebám své firmy.</caps:sentence>
                    <caps:sentence sentenceid="4f4f145aafdf6ea8a38164ebe7706661" id="tgt102" class="tgtSentence"> V <externalLink><linkText>konzole pro správu Microsoft Intune</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> klikněte na <ui>Správce</ui> &gt; <ui>Portál společnosti</ui>.</caps:sentence>
                    <caps:sentence sentenceid="625a8686dac7b5297d90d5266d7fcd78" id="tgt103" class="tgtSentence"> Co můžete nakonfigurovat:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="9bb4c85dfbafa8c61f627241bb21358c" id="tgt104" class="tgtSentence">název společnosti,</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="16576d71cb733d359db3b6e40b97b228" id="tgt105" class="tgtSentence">Jméno kontaktní osoby oddělení IT</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="965d8e507652fcc1b19d4b13823cf800" id="tgt106" class="tgtSentence">Telefonní číslo oddělení IT</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="4eec452dee7d15acfb78a023b487bf19" id="tgt107" class="tgtSentence">Další informace</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="2ddf6ec5ba19603e0bbf4dd9dd16b1c5" id="tgt108" class="tgtSentence">Adresa URL prohlášení o zásadách ochrany osobních údajů společnosti</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="07c657dc49d79de1aa99cc410449492d" id="tgt109" class="tgtSentence">adresu URL webu podpory (nezobrazuje se),</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence sentenceid="ca75dc95767c2d020aba7b02bb2837c8" id="tgt110" class="tgtSentence">Název webu</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step address="BKMK_Terms">
                <content>
                  <tokenBlock>CPEnrollmentTermsAndConditions</tokenBlock>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt111" class="tgtSentence">
                      <embeddedLabel>Sdělte uživatelům, jak získat přístup k prostředkům společnosti pomocí firemního portálu</embeddedLabel> <br />Uživatelé budou potřebovat vědět, jak mají registrovat svá zařízení a co mají očekávat po začlenění do správy.</caps:sentence>
                    <caps:sentence sentenceid="7215ee9c7d9dc229d2921a40e899ec5f" id="tgt112" class="tgtSentence">
                      <link xlink:href="48914533-f138-4dc0-8b93-4cea3ac61f7b">What to tell your end users about using Intune</link>
                    </caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="58f2e45a7f16fb7d9bb18f3e983eebf2" id="tgt113" class="tgtSentence">Nasazení aplikace Portál společnosti Windows Phone 8.1.</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="a40f9fafcca406b45bc874831dbb4b58" id="tgt114" class="tgtSentence">Aplikaci Portál společnosti můžete místo instalace z Windows Phone Store nasadit do zařízení Windows Phone 8.1 v <token>wit_nextref</token>.</caps:sentence>
                <caps:sentence sentenceid="60e7e9dcd9deab69d4aefb99d1eb669f" id="tgt115" class="tgtSentence"> Stále bude třeba podle postupu nahoře povolit registraci zařízení Windows Phone pomocí certifikátu společnosti Symantec.</caps:sentence>
                <caps:sentence sentenceid="f2855d100c99c8677c7ce473fb8bb0fe" id="tgt116" class="tgtSentence"> Pak je nutné stáhnout aplikaci Portál společnosti Windows Phone 8.1 a podepsat ji certifikátem společnosti Symantec.</caps:sentence>
                <caps:sentence sentenceid="38239abcf1644ec61ea21beda72d8faa" id="tgt117" class="tgtSentence">  To je nutné pouze v případě, že uživatelé nebudou používat Store společnosti a chcete nasadit firemní portál na zařízení Windows Phone 8.1.</caps:sentence>
              </para>
              <procedure expanded="false" address="BKMK_WP81appx">
                <title>
                  <caps:sentence sentenceid="593063f388f896f2b7939233bc0b76d1" id="tgt118" class="tgtSentence">Postup stáhnutí a podepsání aplikace Portál společnosti Windows Phone 8.1 pro nasazení s Intune</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="9af7c117d9de9a06fba7a5f1ea5fcc2d" id="tgt119" class="tgtSentence">
                          <embeddedLabel>Stáhněte Portál společnosti</embeddedLabel> <br /></caps:sentence>
                      </para>
                      <para>
                        <caps:sentence sentenceid="23bd19fcedd382955bc35818765ace04" id="tgt120" class="tgtSentence">Stáhněte si <externalLink target="_blank"><linkText>Aplikaci Portál společnosti Microsoft Intune pro Windows Phone 8.1</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615799</linkUri></externalLink> z webu Stažení softwaru a spusťte samorozbalovací (.exe) soubor.</caps:sentence>
                        <caps:sentence sentenceid="915293ff28ecd13258a5c246d8ff93e6" id="tgt121" class="tgtSentence"> Tento soubor obsahuje dva soubory:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="d3b17b87a0f03614ef445ef6e1871e7e" id="tgt122" class="tgtSentence">CompanyPortal.appx – instalační aplikace Portálu společnosti pro Windows Phone 8.1</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="9b70becfcf3be271def18686c811a1d5" id="tgt123" class="tgtSentence">WinPhoneCompanyPortal.ps1 – Powershellový skript, který můžete použít k podepsání aplikace Portál společnosti, aby se dala nasadit na zařízení s Windows Phone 8.1</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para></para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="23bd19fcedd382955bc35818765ace04" id="tgt124" class="tgtSentence">
                          <embeddedLabel>Stažení sady Windows Phone SDK</embeddedLabel>
                          <br />Stáhněte si <externalLink target="_blank"><linkText>sadu Windows Phone SDK 8.0</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615570</linkUri></externalLink> (http://go.microsoft.com/fwlink/?LinkId=268439) a nainstalujte ji na svůj počítač.</caps:sentence>
                        <caps:sentence sentenceid="7c37c9028d2f59387e2b9f2db1452021" id="tgt125" class="tgtSentence"> Potřebujete ji k vygenerování tokenu pro registraci aplikace.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="def41a67e2ddf550a1efd2f9dcbec355" id="tgt126" class="tgtSentence">
                          <embeddedLabel>Generování souboru AETX</embeddedLabel>
                          <br />Pomocí programu AETGenerator.exe, který je součástí sady Windows Phone SDK 8.0, vygenerujte soubor tokenu pro registraci aplikace (.aetx) ze souboru Symantec PFX.</caps:sentence>
                        <caps:sentence sentenceid="ad2cb60a6fa7c1facec37cfb7a9c337b" id="tgt127" class="tgtSentence"> Pokyny, jak vytvořit soubor AETX, najdete v tématu <externalLink><linkText>Jak vygenerovat token pro registraci aplikace pro Windows Phone</linkText><linkUri>https://msdn.microsoft.com/library/windows/apps/jj735576.aspx</linkUri></externalLink>.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="599f968755b3fd6fb4191c3386a799f0" id="tgt128" class="tgtSentence">
                          <embeddedLabel>Stažení sady Windows SDK pro Windows 8.1</embeddedLabel>
                          <br />Stáhněte a nainstalujte si sadu <externalLink target="_blank"><linkText>Windows Phone SDK</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=613525</linkUri></externalLink> (http://go.microsoft.com/fwlink/?LinkId=613525).</caps:sentence>
                        <caps:sentence sentenceid="e052a473d1029072cf5b45d0ecd3934d" id="tgt129" class="tgtSentence"> Všimněte si, že powershellový skript dodaný spolu s aplikací Portál společnosti používá výchozí umístění instalace <codeInline>${env:ProgramFiles(x86)}\Windows Kits\8.1</codeInline>.</caps:sentence>
                        <caps:sentence sentenceid="2b4b5bf4ef49b31264c4644aca27912f" id="tgt130" class="tgtSentence"> Pokud máte instalaci jinde, musíte její umístění zahrnout jako parametr rutiny.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="c5aa190bef9dfa4cf52860037fb9a409" id="tgt131" class="tgtSentence">
                          <embeddedLabel>Podepsání kódu aplikace pomocí PowerShellu</embeddedLabel>
                          <br />Otevřete na hostitelském počítači, na kterém je nainstalovaná sada Windows SDK a certifikát Symantec Enterprise Mobile Code Signing Certificate, <ui>Windows PowerShell</ui> jako správce, přejděte na soubor Sign-WinPhoneCompanyPortal.ps1 a spusťte skript.</caps:sentence>
                      </para>
                      <para>
                        <embeddedLabel>
                          <caps:sentence sentenceid="e93b3fa481be3932aa08bd68c3deee70" id="tgt132" class="tgtSentence">Příklad 1</caps:sentence>
                        </embeddedLabel>
                      </para>
                      <code>.\Sign-WinPhoneCompanyPortal.ps1 -InputAppx 'C:\temp\CompanyPortal.appx' -OutputAppx 'C:\temp\CompanyPortalEnterpriseSigned.appx' -PfxFilePath 'C:\signing\cert.pfx' -PfxPassword '1234' -AetxPath 'C:\signing\cert.aetx'</code>
                      <para>
                        <caps:sentence sentenceid="99b6b6e0e44a19e34c86098e5979a3f0" id="tgt133" class="tgtSentence">Tento příklad podepíše CompanyPortal.appx ve složce C:\temp\ a vytvoří soubor CompanyPortalEnterpriseSigned.appx.</caps:sentence>
                        <caps:sentence sentenceid="e0571817898d04af0c95c719456cf5f3" id="tgt134" class="tgtSentence"> Použije heslo PFX 1234 a přečte ID vydavatele ze souboru PFX.</caps:sentence>
                        <caps:sentence sentenceid="0c83a38d77d189b78d21a6f71153363e" id="tgt135" class="tgtSentence"> Kromě toho přečte i ID organizace ze souboru cert.aetx.</caps:sentence>
                      </para>
                      <para>
                        <embeddedLabel>
                          <caps:sentence sentenceid="a6b23ee7f9c084154997ea3bf5b4c1e3" id="tgt136" class="tgtSentence">Příklad 2</caps:sentence>
                        </embeddedLabel>
                      </para>
                      <code>.\Sign-WinPhoneCompanyPortal.ps1 -InputAppx 'C:\temp\CompanyPortal.appx' -OutputAppx 'C:\temp\CompanyPortalEnterpriseSigned.appx' -PfxFilePath 'C:\signing\cert.pfx' -PfxPassword '1234' -PublisherId 'OID.0.9.2342.19200300.100.1.1=1000000001, CN="Test, Inc.", OU=Test 1' -EnterpriseId 1000000001</code>
                      <para>
                        <caps:sentence sentenceid="99b6b6e0e44a19e34c86098e5979a3f0" id="tgt137" class="tgtSentence">Tento příklad podepíše CompanyPortal.appx ve složce C:\temp\ a vytvoří soubor CompanyPortalEnterpriseSigned.appx.</caps:sentence>
                        <caps:sentence sentenceid="b38e6ecb4a008c1d5ae7bcddb70adb6d" id="tgt138" class="tgtSentence"> Použije heslo PFX 1234 a zadané ID vydavatele.</caps:sentence>
                      </para>
                      <para>
                        <embeddedLabel>
                          <caps:sentence sentenceid="bf987f0415d3fefd8fbfbb5a6ab3a60a" id="tgt139" class="tgtSentence">Parametry:</caps:sentence>
                        </embeddedLabel>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="2154f1323d71cabff7d84e69486cbb99" id="tgt140" class="tgtSentence">
                              <codeInline>-InputAppx</codeInline> – Místní cesta k souboru CompanyPortal.appx v jednoduchých uvozovkách</caps:sentence>
                            <caps:sentence sentenceid="8e7c82dcb51ef0a29f4c91c6d48afda8" id="tgt141" class="tgtSentence"> Například 'C:\temp\CompanyPortal.appx'.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="db0f98a70046962795dda19d1353f7d7" id="tgt142" class="tgtSentence">
                              <codeInline>-OutputAppx</codeInline> – Místní cesta a název souboru podepsané aplikace Portál společnosti v jednoduchých uvozovkách</caps:sentence>
                            <caps:sentence sentenceid="0403882cb14e21a75053b8fe46e4660f" id="tgt143" class="tgtSentence"> Například 'C:\temp\CompanyPortalEnterpriseSigned.appx'.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="37406b23da0c95feeadffe0ed2f2e2f2" id="tgt144" class="tgtSentence">
                              <codeInline>-PfxFilePath</codeInline> – Místní cesta a název souboru pro exportovaný soubor PFX certifikátu Symantec.</caps:sentence>
                            <caps:sentence sentenceid="cb7e1c17fd7fbccdfee34f6ec3517046" id="tgt145" class="tgtSentence"> Například 'C:\signing\cert.pfx'.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="608a28ced851bec9f91fd064f5951e1a" id="tgt146" class="tgtSentence">
                              <codeInline>-PfxPassword</codeInline> – Heslo použité k podepsání souboru PFX v jednoduchých uvozovkách.</caps:sentence>
                            <caps:sentence sentenceid="a1c69f54fcc3343fbe05ee9e1b639a7b" id="tgt147" class="tgtSentence"> Například '1234'.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="a2ae2bbf3241fcd3cbad4e21210007ae" id="tgt148" class="tgtSentence">
                              <codeInline>-AetxPath</codeInline> – Místní cesta k souboru .aetx, který se používá k přečtení ID organizace, pokud se nedefinuje argument EnterpriseId.</caps:sentence>
                            <caps:sentence sentenceid="8026272ac081154b279b2ec9d1f56295" id="tgt149" class="tgtSentence"> Zadat se musí buď tento argument, nebo EnterpriseId.</caps:sentence>
                            <caps:sentence sentenceid="92ed377af9bc50371ea5446337c47cdb" id="tgt150" class="tgtSentence"> Například 'C:\signing\cert.aetx'.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="0054ce9e0acf26959d5f7755005669f8" id="tgt151" class="tgtSentence">
                              <codeInline>-PublisherId</codeInline> – ID vydavatele dané organizace.</caps:sentence>
                            <caps:sentence sentenceid="e57c41ca30767da4088e84d285ebea57" id="tgt152" class="tgtSentence"> Pokud chybí, použije se pole Subject certifikátu Symantec Enterprise Mobile Code Signing Certificate.</caps:sentence>
                            <caps:sentence sentenceid="447aa2f9d4781de497f6fe66f1dd35af" id="tgt153" class="tgtSentence"> Například OID.0.9.2342.19200300.100.1.1=1000000001, CN="Test, Inc.", OU=Test 1</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="0eaa511e60ba861b2b429991814e3b4e" id="tgt154" class="tgtSentence">
                              <codeInline>-SdkPath</codeInline> – Cesta ke kořenové složce sady Windows SDK pro Windows 8.1</caps:sentence>
                            <caps:sentence sentenceid="4e16b4deaf8c428580187b116de8d533" id="tgt155" class="tgtSentence"> Tento argument je volitelný a jeho výchozí hodnota je ${env:ProgramFiles(x86)}\Windows Kits\8.1.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence sentenceid="72598cc79faa20a87ad1c8e33e9d7214" id="tgt156" class="tgtSentence">
                              <codeInline>-EnterpriseId</codeInline> – ID organizace</caps:sentence>
                            <caps:sentence sentenceid="07968656625d1c14a856a4e62db43118" id="tgt157" class="tgtSentence"> Musí se zadat buď tento argument, nebo AetxPath.</caps:sentence>
                            <caps:sentence sentenceid="4180f108ac1f3ae2e8d9735c058f6773" id="tgt158" class="tgtSentence"> Pokud se tento argument nezadá, ID organizace se přečte ze souboru AETX.</caps:sentence>
                            <caps:sentence sentenceid="1ff4112e83e346066d3e4ba0d4c33bc1" id="tgt159" class="tgtSentence"> Například 1000000001.</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para></para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence sentenceid="78ed0e740ca082d18b5b55d5445d1cda" id="tgt160" class="tgtSentence">Nasazení aplikace Portál společnosti Windows Phone 8.1 (SSP.appx)</caps:sentence>
                      </para>
                      <alert class="important">
                        <para>
                          <caps:sentence sentenceid="660dbabe465935d074e99c94422cbe4e" id="tgt161" class="tgtSentence">Soubor ssp.xap i firemní portál z Windows Store se dají nainstalovat zároveň, což může uživatele mást.</caps:sentence>
                          <caps:sentence sentenceid="7b153146551f60db93bc0d7b4ee78bf9" id="tgt162" class="tgtSentence"> Pokud chcete, aby všichni uživatelé používali ssp.xap, vytvořte blokovanou aplikaci pro verzi firemního portálu z Windows Store.</caps:sentence>
                          <caps:sentence sentenceid="42234178a8dc0432f4f0234ce726c309" id="tgt163" class="tgtSentence"> Pokud chcete, aby všechna zařízení Windows Phone 8.1 používala jen verzi firemního portálu z Windows Store, máte tři možnosti:</caps:sentence>
                        </para>
                        <list class="bullet">
                          <listItem>
                            <para>
                              <caps:sentence sentenceid="d21d43181a8ebfa6f82099e6abbea447" id="tgt164" class="tgtSentence">Pokud nebude zkušebně načítat aplikace a nepotřebujete podporovat Windows Phone 8.0, nenahrávejte podepsaný soubor ssp.xap.</caps:sentence>
                            </para>
                          </listItem>
                          <listItem>
                            <para>
                              <caps:sentence sentenceid="11fc13be9f3cde7c629ce0337906461a" id="tgt165" class="tgtSentence">Pokud potřebujete zkušebně načtené aplikace a neregistrují se žádná zařízení Windows Phone 8, změňte automaticky vytvořené nasazení souboru ssp.xap z „dostupný“ na „odinstalovat“.</caps:sentence>
                            </para>
                          </listItem>
                          <listItem>
                            <para>
                              <caps:sentence sentenceid="14c0fdbc4a0ce4ce8ddfbda28f481f4e" id="tgt166" class="tgtSentence">Pokud musíte nainstalovat zkušebně načtené aplikace a zařízení Windows Phone 8.0 musí zaregistrovat a přijmout soubor ssp.xap, vytvořte nové nasazení softwaru ze souboru ssp.xap a nasaďte je akcí <ui>odinstalace</ui>.</caps:sentence>
                              <caps:sentence sentenceid="2ceab1c373f1181739ed568303dc2ba4" id="tgt167" class="tgtSentence"> Zařízení Windows Phone 8.0 nepodporují vynucené instalace nebo odinstalace aplikací, takže budou nasazení ignorovat.</caps:sentence>
                              <caps:sentence sentenceid="3af88cba174c19fa141be3b55f0598c5" id="tgt168" class="tgtSentence"> Zařízení Windows Phone 8.1 podporují akci odinstalace a odeberou soubor ssp.xap.</caps:sentence>
                            </para>
                          </listItem>
                        </list>
                      </alert>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="0ae8e358ce25de11f47161cfaf786819" id="tgt169" class="tgtSentence">Obnovit svůj certifikát Symantec Enterprise pro podpis kódu pro zařízení s Windows</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="51bfdd2c469f2f32f7ee1784438cc90c" id="tgt170" class="tgtSentence">Certifikát od Symantecu použitý ke správě určitých mobilních zařízení s Windows a Windows Phone se musí pravidelně obnovovat.</caps:sentence>
            <caps:sentence sentenceid="326cb7aa260d149bc539350181b33bac" id="tgt171" class="tgtSentence"> Pro zařízení Windows Phone 8.0 se pro registraci zařízení potřebuje podepsaná aplikace Portál společnosti a certifikát pro podpis kódu.</caps:sentence>
            <caps:sentence sentenceid="80ae8b75cfe475eff3037cedfc65ee80" id="tgt172" class="tgtSentence"> Novější zařízení Windows Phone může používat aplikaci firemního portálu staženou z Windows Store.</caps:sentence>
            <caps:sentence sentenceid="0e1f6a8e9350b2b4e355406fb6b90232" id="tgt173" class="tgtSentence"> Certifikát pro podpis kódu se vyžaduje i pro nasazení obchodních aplikací.</caps:sentence>
          </para>
          <procedure expanded="false">
            <title>
              <caps:sentence sentenceid="779e8425c55023567c0632d6ab4473af" id="tgt174" class="tgtSentence">Jak obnovit certifikát Symantec Enterprise pro podpis kódu</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="02971f9aca16d5e2a7ce66fb3ca89d07" id="tgt175" class="tgtSentence">Najděte e-mail s informacemi o obnovení, který vám Symantec poslal přibližně 14 dnů před vypršením platnosti certifikátu.</caps:sentence>
                    <caps:sentence sentenceid="ea9c74b6105f1c78a125f30f5ae444a1" id="tgt176" class="tgtSentence"> V tomto e-mailu jsou pokyny od Symantecu o obnovení vašeho podnikového certifikátu.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="bb5af1c3a6d60b4947f070de9780726c" id="tgt177" class="tgtSentence">Další informace o certifikátech Symantec získáte na webu <externalLink><linkText>www.symantec.com</linkText><linkUri>http://www.symantec.com</linkUri></externalLink> nebo telefonním čísle 1-877-438-8776 nebo 1-650-426-3400.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="8a20404fb2a9dceb5dc3641a00eb463b" id="tgt178" class="tgtSentence">Přejděte na web (příklad: <externalLink><linkText>https://products.websecurity.symantec.com/orders/enrollment/microsoftCert.do</linkText><linkUri>https://products.websecurity.symantec.com/orders/enrollment/microsoftCert.do</linkUri></externalLink>) a přihlaste se s ID vydavatele od Symantecu a e-mailovou adresou spojenou s certifikátem.</caps:sentence>
                    <caps:sentence sentenceid="a9387d7047bd71af5ca17dc633e94791" id="tgt179" class="tgtSentence"> Ke spuštění obnovení musíte použít stejný počítač, který použijete ke stažení certifikátu.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="d4099a7d6380929b7b5c6b5a6623ae09" id="tgt180" class="tgtSentence">Po schválení a zaplacení obnovení si stáhněte certifikát.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
          <procedure expanded="false">
            <title>
              <caps:sentence sentenceid="b922e0fb4a86449b6aff176e41af7e88" id="tgt181" class="tgtSentence">Jak nainstalovat aktualizovaný certifikát pro Windows Phone 8.0</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="444257c164a32b232b9ede0412edc362" id="tgt182" class="tgtSentence">Stáhněte si a podepište nejnovější Portál společnosti Windows Phone, který najdete tady: <externalLink><linkText>http://www.microsoft.com/cs-cz/download/details.aspx?id=36060</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=36060</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="84f8df8e69faaf38b6a258b5e17b3926" id="tgt183" class="tgtSentence">Otevřete konzolu pro správu Intune (<externalLink><linkText>https://admin.manage.microsoft.com</linkText><linkUri>https://admin.manage.microsoft.com</linkUri></externalLink>), přejděte na <ui>Správce</ui>, <ui>Správa mobilních zařízení</ui> &gt; <ui>Windows Phone</ui> a klikněte na <ui>Nahrát podepsanou aplikaci</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="fd66cd717e159db47ce295d4bcd12623" id="tgt184" class="tgtSentence">Nahrajte nově podepsaný firemní portál.</caps:sentence>
                    <caps:sentence sentenceid="6f3395584021182930fb87574e71da98" id="tgt185" class="tgtSentence"> Budete potřebovat nově podepsaný soubor SSP.xap a nový soubor .PFX, který jste dostali od Symantecu, nebo token pro zápis aplikace vytvořený pomocí tohoto nového souboru .PFX.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="5101a1da5de5102b696fa683c6c7c620" id="tgt186" class="tgtSentence">Až se nahrávání dokončí, odeberte předchozí verzi aplikace Portál společnosti v pracovní prostoru <ui>Software</ui> v konzole pro správu Intune.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="1d2af3b8610e8640021243c7527825f7" id="tgt187" class="tgtSentence">Podepište znovu všechny podnikové a firemní aplikace stejným certifikátem a nahrajte a nahraďte stávající aplikace.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence sentenceid="c1cf3e547f3444db486cda0bccd743ad" id="tgt188" class="tgtSentence">Poskytnutí podepsaného souboru SSP.xap je aktuálně jedinou možností, jak poskytnout aktualizovaný certifikát pro podepisování kódu.</caps:sentence>
                  <caps:sentence sentenceid="615a79d1519ef0e08e059151c7c938f3" id="tgt189" class="tgtSentence"> Aby byla zajištěná podpora podepsaných obchodních aplikací, je nutné podepsat a nahrát aplikaci Portál společnosti i v případě, že si uživatelé nainstalují aplikaci Portál společnosti ze Storu.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure expanded="false">
            <title>
              <caps:sentence sentenceid="3761619c03e867047963ca0a54e469c8" id="tgt190" class="tgtSentence">Jak nainstalovat aktualizovaný certifikát pro zařízení s Windows Phone 8.1 a novějším systémem</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="b524d5abe0e85f658b0662dc161112b8" id="tgt191" class="tgtSentence">Stáhněte si a podepište nejnovější Portál společnosti Windows Phone z webu Stažení softwaru, který najdete tady: <externalLink><linkText>http://www.microsoft.com/cs-cz/download/details.aspx?id=36060</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=36060</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="41ab81aedec29d904a088b53214e2e6b" id="tgt192" class="tgtSentence">Otevřete konzolu pro správu Intune (<externalLink><linkText>https://admin.manage.microsoft.com</linkText><linkUri>https://admin.manage.microsoft.com</linkUri></externalLink>), přejděte na <ui>Správce</ui> &gt; <ui>Správa mobilních zařízení</ui> &gt; <ui>Windows Phone</ui> a klikněte na <ui>Nahrát podepsanou aplikaci</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="fd66cd717e159db47ce295d4bcd12623" id="tgt193" class="tgtSentence">Nahrajte nově podepsaný firemní portál.</caps:sentence>
                    <caps:sentence sentenceid="6f3395584021182930fb87574e71da98" id="tgt194" class="tgtSentence"> Budete potřebovat nově podepsaný soubor SSP.xap a nový soubor .PFX, který jste dostali od Symantecu, nebo token pro zápis aplikace vytvořený pomocí tohoto nového souboru .PFX.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="5101a1da5de5102b696fa683c6c7c620" id="tgt195" class="tgtSentence">Po dokončení nahrávání odeberte předchozí verzi aplikace Portál společnosti v pracovním prostoru <ui>Software</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="1ab4bf40c46f0ac064fb574c89e0f60e" id="tgt196" class="tgtSentence">Zaregistrujte všechny nové a aktualizované podnikové aplikace pomocí nového certifikátu.</caps:sentence>
                    <caps:sentence sentenceid="135e5abbaa26e9cd47fdb5b9fbaf2c5e" id="tgt197" class="tgtSentence"> Stávající aplikace není nutné znovu podepisovat a nasazovat.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section address="BKMK_FAQ">
        <title>
          <caps:sentence sentenceid="a8473d2d445d6121c874811a283e6f1e" id="tgt198" class="tgtSentence">Nejčastější dotazy ke správě mobilních zařízení pro Microsoft Intune, včetně správy přes Configuration Manager 2012</caps:sentence>
        </title>
        <content>
          <para></para>
        </content>
        <sections>
          <section expanded="false" address="BKMK_Symantec">
            <title>
              <caps:sentence sentenceid="0acc04a99923ff487f1e62cc62ac9283" id="tgt199" class="tgtSentence">Proč Windows Phone vyžaduje certifikát Symantecu pro správu?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="bca5bdf78a9a87711a6a2f3191e339a6" id="tgt200" class="tgtSentence">Windows Phone určuje, jak můžete instalovat aplikace.</caps:sentence>
                <caps:sentence sentenceid="aeca71661d91b31dd20f037d310b34d6" id="tgt201" class="tgtSentence"> Každý uživatel s účtem Microsoft může instalovat aplikace z Windows Phone Storu nebo si společnost může nainstalovat nebo zkušebně načíst svoje interně vyvinuté obchodní (LOB) aplikace během speciálního procesu popsaného v dokumentaci k Windows Phone.</caps:sentence>
                <caps:sentence sentenceid="63c52d556e83a21fa24b077fe618d2ba" id="tgt202" class="tgtSentence"> Při instalaci obchodních aplikací zařízení s Windows Phone důvěřují jenom jednomu speciálnímu typu certifikátu, který vydal Symantec.</caps:sentence>
                <caps:sentence sentenceid="f967bb0d3d96cb9455c59003bf2f1a63" id="tgt203" class="tgtSentence"> Nejde použít žádný jiný komerčně nebo soukromě vygenerovaný certifikát.</caps:sentence>
                <caps:sentence sentenceid="09cd94f170cf68ec7afe6f8b3f228614" id="tgt204" class="tgtSentence"> Tento požadavek neplatí jen pro Intune, ale pro všechna řešení pro správu mobilních zařízení.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="4486bedaf2aad8fbd8ce6308c36365dc" id="tgt205" class="tgtSentence">Certifikát Symantec vytvoří token zápisu aplikace (AET).</caps:sentence>
                <caps:sentence sentenceid="cd7946b0d209a2874b077a3e4b85958c" id="tgt206" class="tgtSentence"> AET se může instalovat na zařízení, které je registrované pro správu mobilních zařízení, nebo se může instalovat vzdáleně ze zabezpečeného webu nebo z přílohy e-mailu.</caps:sentence>
                <caps:sentence sentenceid="e23ee43b117aa2f05f7ce0678c65031b" id="tgt207" class="tgtSentence"> Správci musí podepsat každou obchodní aplikaci certifikátem Symantec pomocí nástrojů sady <externalLink target="_blank"><linkText>Windows Phone SDK</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268439</linkUri></externalLink>.</caps:sentence>
                <caps:sentence sentenceid="d9f30d299b5c3971eac4739d37396740" id="tgt208" class="tgtSentence"> Když se uživatelé pokusí instalovat obchodní aplikace, operační systém Windows Phone ověří podpis v AET s podpisem na aplikaci.</caps:sentence>
                <caps:sentence sentenceid="8a269fe729dc7c14c459805ff817eef8" id="tgt209" class="tgtSentence"> Pokud se podpisů shodují, může instalace pokračovat.</caps:sentence>
                <caps:sentence sentenceid="e72acee76aeaa6415d939c088ceb8f84" id="tgt210" class="tgtSentence"> Pokud se AET nedá ověřit, instalace se nezdaří.</caps:sentence>
                <caps:sentence sentenceid="a4d47b612e312de7101ea5ec01510e5b" id="tgt211" class="tgtSentence"> Tady je několik důvodů, proč nemusí dojít k ověření AET:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="fd645953ed631257d19883615b793f22" id="tgt212" class="tgtSentence">AET nebyl nikdy na zařízení nainstalovaný.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="16368cf359f2911f56f6321b92beef47" id="tgt213" class="tgtSentence">Vypršela platnost AET.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="71a1e04f27919212d81bb91fbcc26f01" id="tgt214" class="tgtSentence">AET nebyl vytvořený stejným certifikátem Symantec použitým k podepsání aplikace.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="a6aef39c4d509b2213305476b24cd130" id="tgt215" class="tgtSentence">Windows Phone nevyžaduje, aby byl AET dostupný při registraci MDM. Před vydáním verze v listopadu 2014 ale Intune vyžadovalo AET a podepsaný soubor ssp.xap, protože kromě registrace nebyl jiný způsob, jak AET a ssp.xap nainstalovat.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="c5579fc500647b65bf98f37f19979c94" id="tgt216" class="tgtSentence">Jak se vytváří AET pro uživatele Intune?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="5ae84604a7e2d71341406f67047c6ca3" id="tgt217" class="tgtSentence">Pokud správci nahrají pro svůj certifikát Symantec soubor .pfx, Intune automaticky vytvoří AET a nasadí ho na registrovaná zařízení Windows Phone.</caps:sentence>
                <caps:sentence sentenceid="3673950fa30fb4a5b214efc6c1ece8c8" id="tgt218" class="tgtSentence"> Správce Intune nemusí používat nástroj AET Generator v sadě Windows Phone SDK.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence sentenceid="77fefb917a7ab6999763d45d4eab2972" id="tgt219" class="tgtSentence">Intune nepodporuje ruční vytvoření AET a jeho vzdálené nasazení.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="06f29a6979696756b4ca89ca6e4655c3" id="tgt220" class="tgtSentence">Jaké změny přispěly ke snížení požadavku na certifikát Symantec?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="16a954d50815f14c2eaae99c548348e0" id="tgt221" class="tgtSentence">U verze Intune z listopadu 2014 jsou změny, které umožní použít scénáře, kdy společnosti nemají certifikát Symantec.</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="8e5785e0f2a407289b2b448597ee4ed2" id="tgt222" class="tgtSentence">Firemní portál pro Windows Phone 8.1 se dá instalovat z Windows Store, takže se nemusí podepisovat certifikátem Symantec a ověřovat s AET.</caps:sentence>
                    <caps:sentence sentenceid="870b721c9c385fe3b369476a0ccb4c5e" id="tgt223" class="tgtSentence"> Místo toho se aplikace ověřuje jako součást procesu publikování na Windows Store.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="3fd9c84ead013cd036b409c5f6b4e687" id="tgt224" class="tgtSentence">Zařízení Windows Phone 8.1 můžete zaregistrovat s nebo bez AET v telefonu.</caps:sentence>
                    <caps:sentence sentenceid="17e8f2f82c4f4daa47f60466d31857ab" id="tgt225" class="tgtSentence"> Pokud je AET dostupný, nainstaluje se při první synchronizaci zařízení s Intune.</caps:sentence>
                    <caps:sentence sentenceid="ab1784c5d6cb3c52abf66f14a2a0352a" id="tgt226" class="tgtSentence"> Pokud není dostupný žádný AET, zařízení můžete dál spravovat přes Intune a uživatelé můžou instalovat firemní portál z Windows Store a používat k podepisování aplikací většinu funkcí firemního portálu bez certifikátu Symantec.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="f9bff7cb4f98158765d890ba47c27592" id="tgt227" class="tgtSentence">Požadavek Symantecu pro zařízení Windows Phone 8 se nemění.</caps:sentence>
                <caps:sentence sentenceid="968858e5bbf674e1176a63319dd99275" id="tgt228" class="tgtSentence"> Zařízení Windows Phone 8 musí mít podepsaný soubor ssp.xap a při registraci musí použít AET, jinak se jejich registrace zablokuje.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="27f38a368b320d3bbda10e828f5db6a2" id="tgt229" class="tgtSentence">Jaké funkce jsou podporované, když se registruje zařízení Windows Phone 8.1 bez certifikátu Symantec?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="d37d81db57a8768a88d00a5b32137827" id="tgt230" class="tgtSentence">Pokud registrujete zařízení Windows Phone 8.1, ale nemáte žádný certifikát Symantec, můžete udělat tohle:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="a6eff3471ecee6ba66f3a757e9dc7857" id="tgt231" class="tgtSentence">Vytvořit zásady a vložit je na zařízení</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="617b7bebf9b5e89394b404b407e3d5e9" id="tgt232" class="tgtSentence">Nakonfigurovat kontaktní informace oddělení IT, které se zobrazí na firemním portálu</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="878fb2365222c016787648a0d3ef3001" id="tgt233" class="tgtSentence">Vytvořit přímé odkazy na Windows Store a nasadit je na firemní portál</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="ed637eb5906e5ebdc91f81d3053198a7" id="tgt234" class="tgtSentence">Vytvořit odkazy na webové stránky a nasadit je na firemní portál</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="e95d654aba16b07959b72d850e5f12b7" id="tgt235" class="tgtSentence">Vytvořit podmínky, které musí uživatelé před používáním firemního portálu přijmout</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="80ada9528124e15df4dd26935aa605ae" id="tgt236" class="tgtSentence">Bez certifikátu Symantec ale nejdou nasazovat obchodní aplikace.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence sentenceid="a81bff7622c8e73171ad3e2b93dc1ca4" id="tgt237" class="tgtSentence">Intune Software Publisher neověřuje, jestli jsou aplikace při nahrávání podepsané.</caps:sentence>
                  <caps:sentence sentenceid="46660005128f53bc64e6c7bceceb2bcd" id="tgt238" class="tgtSentence"> Pokud nasazujete nepodepsané aplikace a uživatelé se je pokusí nainstalovat, bude instalace neúspěšná.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="d959623c7541516bd9a781d53b0c4d3e" id="tgt239" class="tgtSentence">Co můžou uživatelé dělat, když firemní mají portál bez certifikátu Symantec?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="552f4dae42c6b84b79e6bebb5d79ec29" id="tgt240" class="tgtSentence">Zařízení Windows Phone 8.1 se můžou registrovat až potom, co si uživatelé nainstalují firemní portál z Windows Store.</caps:sentence>
                <caps:sentence sentenceid="275b38084299a98feb7e0a323b5dd812" id="tgt241" class="tgtSentence"> Pokud není zařízení zaregistrované, zobrazí se uživatelům výzva k registraci.</caps:sentence>
                <caps:sentence sentenceid="a65d8c8ad714514177dfcd664bc69b9c" id="tgt242" class="tgtSentence"> Když uživatelé klepnou na tuto výzvu na firemním portálu, přesměruje je to přímo na <ui>Nastavení / Pracovní plocha</ui>, kde si můžou svoje zařízení zaregistrovat.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="a47ea5cf9d9625766c7477800cd6d202" id="tgt243" class="tgtSentence">I bez registrace zařízení můžou uživatelé na firemním portálu nainstalovaném z Windows Store dělat tohle:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="86a130c9193962978650feab26546162" id="tgt244" class="tgtSentence">Přijmout nebo odmítnout podmínky nakonfigurované správcem.</caps:sentence>
                    <caps:sentence sentenceid="aedd567dbc376df8e6e4b11fb43e7996" id="tgt245" class="tgtSentence"> Pokud uživatelé tyhle podmínky odmítnou, firemní portál se ukončí.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="5b8adf835d42ecf17a11dcab8a95fa7d" id="tgt246" class="tgtSentence">Zobrazit kontaktní informace oddělení IT</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="425b6b3da98781c5b55f481080080d5d" id="tgt247" class="tgtSentence">Zobrazit zaregistrovaná zařízení, včetně zařízení s iOS, Androidem a Windows</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="bf4492432aa4d31374f36fe6cb0db216" id="tgt248" class="tgtSentence">Používat přímé odkazy na aplikace ve Windows Store</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="5245e8a94087a5a2082528f421784aae" id="tgt249" class="tgtSentence">Používat webové odkazy k otevírání webových stránek</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="681cef1de549baba59faf4f773c29f5e" id="tgt250" class="tgtSentence">Zaregistrované zařízení můžou uživatelé vidět v seznamu <ui>Moje zařízení</ui>.</caps:sentence>
                <caps:sentence sentenceid="453ba15b346c9557a686cb0db7a346e4" id="tgt251" class="tgtSentence"> Po registraci se na zařízení vztahují všechny nasazené zásady Intune.</caps:sentence>
                <caps:sentence sentenceid="2b3bf3125ff7527a76fc76a2a4982d6f" id="tgt252" class="tgtSentence"> Abyste mohli získat AET a instalovat obchodní aplikace, musí být zařízení registrované.</caps:sentence>
                <caps:sentence sentenceid="274077dccf96d6b4d7e6e2ff6be0b8a9" id="tgt253" class="tgtSentence"> Když se pokusíte na nezaregistrovaném zařízení o instalaci obchodní aplikace, přesměruje vás to na registraci.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="44fc05b4e45d60fc7658f2f7bb9f722e" id="tgt254" class="tgtSentence">Pokud nemá společnost certifikát Symantec, může jen instalovat obchodní aplikace nasazené správcem.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="8908a0afb06ed65c1edef45b122baa65" id="tgt255" class="tgtSentence">Naše společnost už má certifikát a registruje zařízení Windows Phone 8.1.</caps:sentence>
              <caps:sentence sentenceid="cdd7ef49ee7488b490b74a567305aa8f" id="tgt256" class="tgtSentence"> Musím udělat něco jinak, když je teď ve Windows Store dostupný firemní portál?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="cdb72a02b423f4db13f9914d497fedf6" id="tgt257" class="tgtSentence">Na zařízeních Windows Phone 8.1 pořád funguje aktuální soubor ssp.xap z webu Stažení softwaru.</caps:sentence>
                <caps:sentence sentenceid="635f418afd05eff3c5a8c22f835f6426" id="tgt258" class="tgtSentence"> Můžete dál navádět uživatele, aby se zaregistrovali a získali během instalace firemní portál.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="5c9f54b558a579c725d95fa79d038f6c" id="tgt259" class="tgtSentence">Jaké výhody a nevýhody přinese uživatelům stažení firemního portálu z Windows Store?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="b028aaa3d7589d6f1a8f4dcc51bc5886" id="tgt260" class="tgtSentence">Výhody:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="44b59bd5003a52759f5badd8abe57c0c" id="tgt261" class="tgtSentence">Uživatelé získají přímé a webové odkazy, i když nebudou mít zaregistrované zařízení Windows Phone 8.1.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="930a4f8505ad69bd7f0d04a1e85b6a8f" id="tgt262" class="tgtSentence">Když Microsoft aktualizuje firemní portál, aplikace z Windows Store se automaticky aktualizuje, aniž byste museli stahovat, podepisovat a znovu nasazovat soubor ssp.xap</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="f59020828d42d1f89021c34991e5fb27" id="tgt263" class="tgtSentence">Dokumentace je pro uživatele Windows Phone 8.1, iOS, Androidu a Windows konzistentní: „Přejděte na Windows Store a nainstalujte si Portál společnosti.“</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="a8b1fc65f186cd804791e0063b4822e6" id="tgt264" class="tgtSentence">Uživatelé vidí aplikaci, když se instaluje, a po jejím otevření získají pokyny k registraci.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="c5e9cbdfd23494eade05650d2e315736" id="tgt265" class="tgtSentence">Nevýhody:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="67b0cdf5eb7cc1353e29dc9091eeda50" id="tgt266" class="tgtSentence">Uživatelé vidí zaškrtávací políčko pro instalaci <ui>firemního centra</ui>, ale v seznamu aplikací v zařízení není nic, co by je odkazovalo na firemní portál.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="527369e8b7bcd296bf39deeb7102bccf" id="tgt267" class="tgtSentence">Uživatelé můžou přijmout vlastní podmínky až po otevření firemního portálu.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="e0670c64da4d7a389e3edc4f98074a3d" id="tgt268" class="tgtSentence">V následujících případech můžete dál odkazovat uživatele na registraci a během ní instalovat soubor ssp.xap:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="2e775f1961bb6cf07c5a85ae329a4f14" id="tgt269" class="tgtSentence">Pokud společnost blokuje ze zařízení Windows Phone přístup k Windows Store, musíte si při registraci nainstalovat soubor ssp.xap.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="c549b0bfebbc3da38fcb01ac665be91c" id="tgt270" class="tgtSentence">Pokud uživatelé nemají na svých zařízeních Windows Phone nakonfigurovaný účet Microsoft, nebudou moct z Windows Store instalovat firemní portál.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="21b30a7e587b3dbe09fdec247f457275" id="tgt271" class="tgtSentence">Pokud se ve stávající dokumentaci pro registraci Windows Phone uvádí, aby uživatelé nejdřív přešli na Nastavení &gt; Pracovní plocha, může chvíli trvat, než se aktualizují dokumenty a uživatelé budou moct přejít do Windows Store.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="fe8f3c69642c11e2b9ea6d84f0371765" id="tgt272" class="tgtSentence">Jaký je rozdíl mezi ssp.xap na webu Stažení softwaru a aplikací ve Windows Store?</caps:sentence>
            </title>
            <content>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="9158d571d0ffe116fdd82a094e7beab5" id="tgt273" class="tgtSentence">K instalaci firemního portálu z Windows Store ho nemusíte podepisovat certifikátem Symantec.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="ff8c41c93a55cc70906a725b57770f47" id="tgt274" class="tgtSentence">Firemní portál ve Windows Store zobrazí uživateli podmínky, ale ssp.xap na webu Stažení softwaru ne.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="47295996a58c02577f305efe2c34562e" id="tgt275" class="tgtSentence">Firemní portál ve Windows Store je souborem .appx, nikoli .xap.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="b2e4b482c2464ea642f30472708b0fd4" id="tgt276" class="tgtSentence">Můžu si stáhnout soubor aplikace Portál společnosti a poslat ho přímo svým uživatelům a neodkazovat je na Windows Store?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="4f7b50bec76bcf2b862eeb2140701427" id="tgt277" class="tgtSentence">Ano.</caps:sentence>
                <caps:sentence sentenceid="863d73f5079173aed48a39a775f609f7" id="tgt278" class="tgtSentence"> Aplikace Portál společnosti se dá na webu Stažení softwaru stáhnout pro tyto operační systémy:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="80ca961f21952f878b8688c0b28b72d1" id="tgt279" class="tgtSentence">Windows Phone 8.1: <externalLink><linkText>http://go.microsoft.com/fwlink/?LinkId=615799</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615799</linkUri></externalLink></caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="132a42035119c4b6819173ebaefee335" id="tgt280" class="tgtSentence">Windows Phone 8.0 : <externalLink><linkText>http://go.microsoft.com/fwlink/?LinkId=268440</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268440</linkUri></externalLink></caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="4e458d4908dd91d3612a8e39fd1b9903" id="tgt281" class="tgtSentence">Windows 8.1: <externalLink><linkText>http://go.microsoft.com/fwlink/?LinkId=615800</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615800</linkUri></externalLink></caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="07a844f479ec1aa2a83c1de9c238a276" id="tgt282" class="tgtSentence">Můžou společnosti i nadále používat nástroj podpory pro správu zkušební verze Windows Phone ve Windows Intune, i když nemají certifikát Symantec a jejich uživatelé si chtějí nainstalovat firemní portál z Windows Store?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="4f7b50bec76bcf2b862eeb2140701427" id="tgt283" class="tgtSentence">Ano.</caps:sentence>
                <caps:sentence sentenceid="8c24975691fabd85fb3ead253d3c9451" id="tgt284" class="tgtSentence"> Pokud musíte udělat testování konceptu, které zahrnuje instalaci obchodních aplikací, bude nástroj pro správu zkušební verze fungovat s verzí firemního portálu z Windows Store.</caps:sentence>
                <caps:sentence sentenceid="6b9cdd25078fdd8f3f3544de94cb24e6" id="tgt285" class="tgtSentence"> I když už k registraci zařízení Windows Phone 8.1 nepotřebujete AET z certifikátu Symantec, společnosti můžou otestovat instalaci aplikace přímými odkazy na aplikace ve Windows Store.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="e0b94b3beb8578f9a74f62aa274e8de8" id="tgt286" class="tgtSentence">Nástroj podpory pro správu zkušební verze Windows Phone ve Windows Intune slouží jen pro zkušební předplatné Intune.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence sentenceid="b423f1f2cd0cd14a02d5a88c115ce89e" id="tgt287" class="tgtSentence">K testování používejte jen nástroj pro správu zkušební verze.</caps:sentence>
                  <caps:sentence sentenceid="a10570b481f6494ad67cbda562791b19" id="tgt288" class="tgtSentence"> Pokud už není pro nástroj pro správu zkušební verze dostupný certifikát Symantec nebo pokud společnost získá svůj vlastní certifikát Symantec pro podepisování aplikací, musí se zařízení zaregistrovaná přes AET z nástroje pro správu zkušební verze znova zaregistrovat.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence sentenceid="9b2d8eef1c442aab1669ce98878685c9" id="tgt289" class="tgtSentence">Můžou společnosti začít s instalací bez certifikátu Symantec a později ho přidat, i když už budou zařízení Windows Phone 8.1 zaregistrovaná?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="4f7b50bec76bcf2b862eeb2140701427" id="tgt290" class="tgtSentence">Ano.</caps:sentence>
                <caps:sentence sentenceid="c542071594b3362f2e3a769ea372178b" id="tgt291" class="tgtSentence"> I když jsou už zařízení Windows Phone 8.1 zaregistrovaná, můžete získat certifikát Symantec, podepsat soubor ssp.xap a nahrát ho spolu se souborem .pfx.</caps:sentence>
                <caps:sentence sentenceid="8e37b1ff45265fcef519fe877434c54e" id="tgt292" class="tgtSentence"> Intune pak vygeneruje AET.</caps:sentence>
                <caps:sentence sentenceid="0366852c1413d4a083ea32d99992e9dc" id="tgt293" class="tgtSentence"> Zařízení Windows Phone 8.1 získají AET při své další synchronizaci během osmi hodin.</caps:sentence>
                <caps:sentence sentenceid="fee18265465e2efd8f40eba170049879" id="tgt294" class="tgtSentence"> Mezi nahráním souborů .xap a .pfx a nasazením obchodních aplikací nechte aspoň osm hodin.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="44fd4af0-f9b0-493a-b590-7825139d9d40">Manage mobile devices with Microsoft Intune</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Before you can manage Windows Phone mobile devices with <token>wit_nextref</token>, you have to set up management requirements.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Creating a DNS CNAME helps users connect to the <token>wit_nextref</token> company portal.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Windows Phone 8.0 requires a Symantec certificate to establish an encrypted IP connection between devices and <token>wit_nextref</token>.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> Depending upon how users access the company portal, Windows Phone 8.1 might also.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> A certificate is also required to sign line-of-business apps.</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">
                <embeddedLabel>Windows Phone 8.1</embeddedLabel> - Requires a certificate only if:</caps:sentence>
            </para>
            <list class="bullet">
              <listItem>
                <para>
                  <caps:sentence id="src7" class="srcSentence">Users won't download the company portal from the Store</caps:sentence>
                </para>
              </listItem>
              <listItem>
                <para>
                  <caps:sentence id="src8" class="srcSentence">You'll deploy  line-of-business (AKA "sideloaded") apps</caps:sentence>
                </para>
              </listItem>
            </list>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">
                <embeddedLabel>Windows Phone 8</embeddedLabel> - Required </caps:sentence>
            </para>
          </listItem>
        </list>
        <mediaLink>
          <image xlink:href="b457bc08-2634-4137-86f6-5f7cc330fbd2"></image>
        </mediaLink>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src10" class="srcSentence">Prepare to manage Windows Phone mobile devices with Intune</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src11" class="srcSentence">Setup requirements for Window Phone mobile device management depend upon how you'll manage devices.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence">  Setting two CNAMEs in your company's DNS registration makes enrollment easier for uses.</caps:sentence>
            <caps:sentence id="src13" class="srcSentence"> If your users will download the Company Portal app from the Store, then once you've configured DNS settings you just need to set up the Company Portal and inform users how to enroll.</caps:sentence>
            <caps:sentence id="src14" class="srcSentence">  For Windows Phone 8.0, or Windows Phone 8.1 where you'll deploy the Company Portal, you'll need a Symntec certificate to code-sign the app.</caps:sentence>
          </para>
          <procedure>
            <title>
              <caps:sentence id="src15" class="srcSentence">Set up Windows Phone enrollment with Intune</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">
                      <embeddedLabel>Set up <token>wit_nextref</token></embeddedLabel> <br />If you haven’t already, prepare for mobile device management by  <externalLink><linkText>setting the mobile device management authority</linkText><linkUri>https://technet.microsoft.com/library/mt346013.aspx</linkUri></externalLink> as <embeddedLabel>Microsoft Intune</embeddedLabel>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">
                      <embeddedLabel>Set a DNS alias for the enrollment server address</embeddedLabel> (optional)<br /> </caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">A DNS alias (CNAME record type) makes it easier users to enroll their devices by automatically populating the server name during enrollment.</caps:sentence>
                  </para>
                  <procedure>
                    <title>
                      <caps:sentence id="src19" class="srcSentence">Verify and create DNS CNAME</caps:sentence>
                    </title>
                    <steps class="ordered">
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src20" class="srcSentence">In the <externalLink target="_blank"><linkText>Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, click <ui>Administration</ui> &gt; <ui>Mobile Device Management</ui> &gt; <ui>Windows Phone</ui>.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src21" class="srcSentence">Type the URL of the verified domain of the company website in the <ui>Specify a verified domain name</ui> box and then click <ui>Test Auto-Detection</ui>.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src22" class="srcSentence">Create CNAME resource records for your company’s domain.</caps:sentence>
                            <caps:sentence id="src23" class="srcSentence"> The CNAME resource records must contain the following information:</caps:sentence>
                          </para>
                          <table border="1">
                            <thead>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence id="src24" class="srcSentence">TYPE</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src25" class="srcSentence">Host Hame</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src26" class="srcSentence">Points to</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src27" class="srcSentence">TTL</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                            </thead>
                            <tbody>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence id="src28" class="srcSentence">CNAME</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <caps:sentence id="src29" class="srcSentence">  <para>enterpriseenrollment.company_domain.com </para></caps:sentence>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src30" class="srcSentence">manage.microsoft.com
</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src31" class="srcSentence">1 Hour</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                              <tr>
                                <TD>
                                  <para>
                                    <caps:sentence id="src32" class="srcSentence">CNAME</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <caps:sentence id="src33" class="srcSentence"> <para>enterpriseregistration.company_domain.com </para></caps:sentence>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src34" class="srcSentence">enterpriseregistration.windows.net
</caps:sentence>
                                  </para>
                                </TD>
                                <TD>
                                  <para>
                                    <caps:sentence id="src35" class="srcSentence">1 Hour</caps:sentence>
                                  </para>
                                </TD>
                              </tr>
                            </tbody>
                          </table>
                          <para>
                            <caps:sentence id="src36" class="srcSentence">For example, if your company’s website is contoso.com, you would create a CNAME in DNS that redirects EnterpriseEnrollment.contoso.com to manage.microsoft.com.</caps:sentence>
                            <caps:sentence id="src37" class="srcSentence"> If there is more than one verified domain, create a CNAME record for each domain.</caps:sentence>
                          </para>
                          <list class="bullet">
                            <listItem>
                              <para>
                                <caps:sentence id="src38" class="srcSentence">
                                  <codeInline>manage.microsoft.com</codeInline> – Supports a redirect to the Intune service with domain recognition from the email’s domain name</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src39" class="srcSentence">
                                  <codeInline>enterpriseregistration.windows.net</codeInline> – Supports workplace join for mobile devices.</caps:sentence>
                                <caps:sentence id="src40" class="srcSentence"> It also supports conditional access for Windows 8.1</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </content>
                      </step>
                    </steps>
                  </procedure>
                  <mediaLink>
                    <image xlink:href="33622fc8-d7ad-4f20-a4ec-c50de6a158bc"></image>
                  </mediaLink>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">
                      <embeddedLabel>Certificate management to support app signing</embeddedLabel>
                      <br />[Required for Windows Phone 8.0 and Windows Phone 8.1 that won’t access the Windows Phone Store and/or need line-of-business apps.]</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">To support the Company Portal app for Windows Phone 8.0 and to deploy company apps to Windows Phone 8.1 you must get a <embeddedLabel>Symantec Enterprise Mobile Code Signing Certificate</embeddedLabel>.</caps:sentence>
                    <caps:sentence id="src43" class="srcSentence"> You cannot use a certificate issued by your own certification authority because only the Symantec certificate is trusted by Windows Phone devices.</caps:sentence>
                    <caps:sentence id="src44" class="srcSentence"> This certificate is required in order to:</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src45" class="srcSentence">Sign the Company Portal app for deployment to <token>winphone8_client_1</token> for enrollment and phone management</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src46" class="srcSentence">Sign company line-of-business apps so <token>wit_nextref</token> can deploy them to Windows Phones</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src47" class="srcSentence">For more information, see <externalLink><linkText>Frequently Asked Questions about Windows Phone Mobile Device Management</linkText><linkUri>https://technet.microsoft.com/en-us/library/dn764959.aspx#BKMK_FAQ</linkUri></externalLink>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">The steps below will help you get the required certificates and sign the company portal app.</caps:sentence>
                    <caps:sentence id="src49" class="srcSentence"> You will need a Windows Phone Dev Center account and then you will need to purchase a Symantec certificate.</caps:sentence>
                  </para>
                  <procedure expanded="false" address="BKMK_CodeSign">
                    <title>
                      <caps:sentence id="src50" class="srcSentence">To get a certificate and code-sign the Company Portal</caps:sentence>
                    </title>
                    <steps class="ordered">
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src51" class="srcSentence">
                              <embeddedLabel>Join the Windows Phone Dev Center</embeddedLabel> <br />Join the <externalLink target="_blank"><linkText>Windows Phone Dev Center</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268442</linkUri></externalLink> using corporate account information when logging in to purchase your company account.</caps:sentence>
                            <caps:sentence id="src52" class="srcSentence"> This request will need to be authorized by a company officer before you receive a code-signing certificate.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src53" class="srcSentence">
                              <embeddedLabel>Get a company Symantec certificate</embeddedLabel> <br />Purchase a certificate from the <externalLink target="_blank"><linkText>Symantec website</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268441</linkUri></externalLink> using your Symantec ID.</caps:sentence>
                            <caps:sentence id="src54" class="srcSentence"> After you purchase the certificate, the corporate approver whom you designated in your Windows Phone Dev Center account will receive an email asking for approval of the certificate request.</caps:sentence>
                            <caps:sentence id="src55" class="srcSentence"> For more information about the Symantec certificate requirement, see the <externalLink><linkText>Why Windows Phone requires a Symantec certificate?</linkText><linkUri>https://technet.microsoft.com/en-us/library/dn764959.aspx#BKMK_Symantec</linkUri></externalLink> Windows device enrollment FAQ.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src56" class="srcSentence">
                              <embeddedLabel>Import certificates</embeddedLabel> <br />Once the request has been approved, you will receive an email containing instructions for importing certificates.</caps:sentence>
                            <caps:sentence id="src57" class="srcSentence"> Follow the instructions in the email to import the certificates.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src58" class="srcSentence">
                              <embeddedLabel>Verify certificates imported</embeddedLabel> <br />To verify that the certificates have been imported correctly, go to the <ui>Certificates</ui> snap-in, right-click <ui>Certificates</ui>, and select <ui>Find Certificates</ui>.</caps:sentence>
                            <caps:sentence id="src59" class="srcSentence"> In the <ui>Contains</ui> field, enter “Symantec”, and click <ui>Find Now</ui>.</caps:sentence>
                            <caps:sentence id="src60" class="srcSentence"> The certificates you imported should appear in the results.</caps:sentence>
                          </para>
                          <para>
                            <mediaLinkInline>
                              <image xlink:href="52f7f33c-987f-48ad-b661-d826489044cd"></image>
                            </mediaLinkInline>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src61" class="srcSentence">
                              <embeddedLabel>Export a signing certificate</embeddedLabel> <br />Having verified that the certificates are present, you can export the .pfx file to sign the company portal.</caps:sentence>
                            <caps:sentence id="src62" class="srcSentence"> Select the Symantec certificate with <ui>Intended purpose</ui> “code-signing.”</caps:sentence>
                            <caps:sentence id="src63" class="srcSentence"> Right-click the code-signing certificate and select <ui>Export</ui>.</caps:sentence>
                          </para>
                          <para>
                            <mediaLinkInline>
                              <image xlink:href="a5e198a5-7d2b-4797-bdfa-853a8e664b3c"></image>
                            </mediaLinkInline>
                          </para>
                          <para>
                            <caps:sentence id="src64" class="srcSentence">In the <ui>Certificate Export Wizard</ui>, select <ui>Yes, export the private key</ui> and then click <ui>Next</ui>.</caps:sentence>
                            <caps:sentence id="src65" class="srcSentence">
                              <ui>Select Personal Information Exchange –PKCS #12 (.PFX)</ui> and check <ui>Include all the certificates in the certification path if possible</ui>.</caps:sentence>
                            <caps:sentence id="src66" class="srcSentence"> Complete the wizard.</caps:sentence>
                            <caps:sentence id="src67" class="srcSentence"> For more information, see <externalLink><linkText>How to Export a Certificate with the Private Key</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=203031</linkUri></externalLink>.</caps:sentence>
                          </para>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <embeddedLabel>
                              <caps:sentence id="src68" class="srcSentence">Download and sign the Company Portal app</caps:sentence>
                            </embeddedLabel>
                            <br />
                          </para>
                          <para>
                            <caps:sentence id="src69" class="srcSentence">Support for Windows Phone enrollment requires the Windows Phone 8.0 Company Portal app be signed and uploaded to Intune.</caps:sentence>
                          </para>
                          <procedure expanded="true">
                            <title>
                              <caps:sentence id="src70" class="srcSentence">Windows Phone 8.0: Download and sign the Company Portal app </caps:sentence>
                            </title>
                            <steps class="ordered">
                              <step>
                                <content>
                                  <para>
                                    <caps:sentence id="src71" class="srcSentence">
                                      <embeddedLabel>Download the Company Portal</embeddedLabel> <br />Download the <externalLink target="_blank"><linkText>Intune Company Portal for Windows Phone</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268440</linkUri></externalLink> from the Download Center.</caps:sentence>
                                    <caps:sentence id="src72" class="srcSentence"> The default installation location is <codeInline>C:\Program Files (x86)\Microsoft Corporation\Windows Intune Company Portal for Windows Phone</codeInline>.</caps:sentence>
                                  </para>
                                </content>
                              </step>
                              <step>
                                <content>
                                  <para>
                                    <caps:sentence id="src73" class="srcSentence">
                                      <embeddedLabel>Download the Windows Phone 8.0 SDK</embeddedLabel>
                                      <br />Download the <externalLink target="_blank"><linkText>Windows Phone SDK</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615570</linkUri></externalLink>.</caps:sentence>
                                  </para>
                                </content>
                              </step>
                              <step>
                                <content>
                                  <para>
                                    <caps:sentence id="src74" class="srcSentence">
                                      <embeddedLabel>Code-sign the Company Portal app</embeddedLabel> <br />Use the XAPSignTool app downloaded with the SDK to sign the company portal with the .pfx file you created from the Symantec certificate.</caps:sentence>
                                    <caps:sentence id="src75" class="srcSentence"> For more information, see <externalLink target="_blank"><linkText>How to sign a company app by using XapSignTool</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkID=280195</linkUri></externalLink>.</caps:sentence>
                                  </para>
                                </content>
                              </step>
                            </steps>
                          </procedure>
                        </content>
                      </step>
                      <step>
                        <content>
                          <para>
                            <caps:sentence id="src76" class="srcSentence">
                              <embeddedLabel>Upload the Company Portal app to <token>wit_nextref</token></embeddedLabel> <br />Upload the signed Company Portal app file and your code-signing certificate to make the app available to your end users.</caps:sentence>
                          </para>
                          <list class="ordered">
                            <listItem>
                              <para>
                                <caps:sentence id="src77" class="srcSentence">In the <externalLink target="_blank"><linkText>Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> click <ui>Administration</ui> &gt; <ui>Windows Phone</ui>.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src78" class="srcSentence">Click the <ui>Upload Signed App File</ui> and sign in with your <token>wit_nextref</token> Administrator ID.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src79" class="srcSentence">On the <ui>Software setup</ui> page for <ui>Specify the location of the software setup files</ui>, browse to the code-signed Company Portal app location (.xap for Windows Phone 8.0 or .appx for Windows Phone 8.1).</caps:sentence>
                              </para>
                              <para>
                                <caps:sentence id="src80" class="srcSentence">If you are evaluating <token>wit_nextref</token> and uploading a code-signed app file in a trial <token>wit_nextref</token> account, uncheck the <ui>Use the Company Portal App file signed by the sample Symantec code-signed certificate</ui> checkbox.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src81" class="srcSentence">Add the certificate (.pfx) file that you exported to <ui>Code-signing certificate</ui> and create a password for the certificate.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src82" class="srcSentence">On the <ui>Software description</ui> page, complete the fields remembering that users see this information on their devices when viewing details about the app in the Company Portal.</caps:sentence>
                              </para>
                            </listItem>
                            <listItem>
                              <para>
                                <caps:sentence id="src83" class="srcSentence">Complete the wizard.</caps:sentence>
                                <caps:sentence id="src84" class="srcSentence"> Users who enroll a Windows Phone 8.0 device will now get the Company Portal app on their devices during enrollment.</caps:sentence>
                                <caps:sentence id="src85" class="srcSentence"> Windows Phone 8.1 users can install the Company Portal app from the store version of the Company Portal.</caps:sentence>
                                <caps:sentence id="src86" class="srcSentence">  If Windows Phone 8.1 devices are blocked from the Windows Phone Store or you want to deploy the Company Portal app using Intune, you must download and sign the Windows Phone 8.1 Company Portal (SSP.appx) app.</caps:sentence>
                              </para>
                            </listItem>
                          </list>
                        </content>
                      </step>
                    </steps>
                  </procedure>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src87" class="srcSentence">
                      <embeddedLabel>Add Intune users</embeddedLabel> <br />The mobile device owner must be added to the Microsoft Intune Account Portal before devices can be enrolled.</caps:sentence>
                    <caps:sentence id="src88" class="srcSentence"> Log in to the <externalLink><linkText>Microsoft Intune Account Portal</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=698854</linkUri></externalLink>, click <ui>Add users</ui>, and select an option:</caps:sentence>
                  </para>
                  <para></para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <caps:sentence id="src89" class="srcSentence">
                          <embeddedLabel>User</embeddedLabel>: To add a single user select <ui>New</ui> &gt; <ui>User</ui> and enter <ui>Details</ui>, <ui>Assign roles</ui>, <ui>Set user location</ui>, and then assign the user to a <ui>Group</ui>.</caps:sentence>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <caps:sentence id="src90" class="srcSentence">
                          <embeddedLabel>Bulk add</embeddedLabel>: Create a .csv file (see samples files provided) and import it into the Intune Account Portal.</caps:sentence>
                        <caps:sentence id="src91" class="srcSentence"> Specify roles, location, and group, and then create the accounts.</caps:sentence>
                        <caps:sentence id="src92" class="srcSentence"> Sample and blank .csv files can be downloaded from the Microsoft Intune Account Portal.</caps:sentence>
                      </para>
                    </listItem>
                  </list>
                  <para>
                    <caps:sentence id="src93" class="srcSentence">You can also enable Active Directory or Azure Active Directory synchronization.</caps:sentence>
                    <caps:sentence id="src94" class="srcSentence"> For more information about integrating other Azure Active Directory users with Intune, see <externalLink><linkText>Directory synchronization roadmap</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=511540</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src95" class="srcSentence">
                      <embeddedLabel>Create groups </embeddedLabel> (Optional)<br />Groups give flexibility for managing devices and users.</caps:sentence>
                    <caps:sentence id="src96" class="srcSentence"> You can set up groups to suit your organizational needs by geographic location, department, or hardware characteristics, for example.</caps:sentence>
                    <caps:sentence id="src97" class="srcSentence">   See <link xlink:href="eb9b01ce-9b9b-4c2a-bf99-3879c0bdaba5">Use groups to manage users and devices with Microsoft Intune</link>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <caps:sentence id="src98" class="srcSentence">
                    <para>
                      <embeddedLabel>Add policies for devices</embeddedLabel> (Optional)<br />Policies are groups of settings that control features on devices. Most MDM policies are platform specific. You create policies using templates  containing recommended or customized settings, and then deploy them to groups. See <link xlink:href="efb4dcd6-56ea-44a8-8fe2-6f1542fc75ec">Use policies to manage computers and mobile devices with Microsoft Intune</link>.</para> </caps:sentence>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src99" class="srcSentence">
                      <embeddedLabel>Set device enrollment limit</embeddedLabel> (Optional) <br />To limit the number of mobile devices a user can enroll, log in to the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink>, click <ui>Admin</ui> &gt; <ui>Mobile Device Management</ui> &gt; <ui>Enrollment rules</ui>.</caps:sentence>
                    <caps:sentence id="src100" class="srcSentence"> Select the maximum number of devices a user can enroll and then click <ui>Save</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src101" class="srcSentence">
                      <embeddedLabel>Set Company Portal settings </embeddedLabel>
                      <br /> You can customize the Intune Company Portal for your company.</caps:sentence>
                    <caps:sentence id="src102" class="srcSentence"> In the <externalLink><linkText>Microsoft Intune administration console</linkText><linkUri>http://manage.microsoft.com</linkUri></externalLink> click <ui>Admin</ui> &gt; <ui>Company Portal</ui>.</caps:sentence>
                    <caps:sentence id="src103" class="srcSentence"> Configure the following</caps:sentence>
                  </para>
                  <list class="bullet">
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src104" class="srcSentence">Company Name</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src105" class="srcSentence">IT department contact name</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src106" class="srcSentence">IT department phone number</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src107" class="srcSentence">Additional information</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src108" class="srcSentence">Company privacy statement URL</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src109" class="srcSentence">Support website URL (not displayed)</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                    <listItem>
                      <para>
                        <ui>
                          <caps:sentence id="src110" class="srcSentence">Website name</caps:sentence>
                        </ui>
                      </para>
                    </listItem>
                  </list>
                </content>
              </step>
              <step address="BKMK_Terms">
                <content>
                  <tokenBlock>CPEnrollmentTermsAndConditions</tokenBlock>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src111" class="srcSentence">
                      <embeddedLabel>Tell users how to get access to company resources with the company portal</embeddedLabel> <br />Your users will need to know how to enroll their devices and what to expect once they're brought into management.</caps:sentence>
                    <caps:sentence id="src112" class="srcSentence">
                      <link xlink:href="48914533-f138-4dc0-8b93-4cea3ac61f7b">What to tell your end users about using Intune</link>
                    </caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src113" class="srcSentence">Deploy the Windows Phone 8.1 Company Portal app</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src114" class="srcSentence">You can deploy the Company Portal app to Windows Phone 8.1 devices with <token>wit_nextref</token> instead of installing from the Windows Phone Store.</caps:sentence>
                <caps:sentence id="src115" class="srcSentence"> You must still enable Windows Phone device enrollment with the steps above using the Symantec certificate.</caps:sentence>
                <caps:sentence id="src116" class="srcSentence"> You must then download the Windows Phone 8.1 Company Portal app and sign it with your Symantec certificate.</caps:sentence>
                <caps:sentence id="src117" class="srcSentence">  This is only necessary if your users won't use the Company Store and you want to deploy the Company Portal to Windows Phone 8.1 devices.</caps:sentence>
              </para>
              <procedure expanded="false" address="BKMK_WP81appx">
                <title>
                  <caps:sentence id="src118" class="srcSentence">Steps to download and sign the Windows Phone 8.1 Company Portal app for deployment with Intune</caps:sentence>
                </title>
                <steps class="ordered">
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src119" class="srcSentence">
                          <embeddedLabel>Download the Company Portal</embeddedLabel> <br /></caps:sentence>
                      </para>
                      <para>
                        <caps:sentence id="src120" class="srcSentence">Download the <externalLink target="_blank"><linkText>Microsoft Intune Company Portal App for Windows Phone 8.1</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615799</linkUri></externalLink> from the Download Center and run the self-extracting (.exe) file.</caps:sentence>
                        <caps:sentence id="src121" class="srcSentence"> This file contains two files:</caps:sentence>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src122" class="srcSentence">CompanyPortal.appx– The Company Portal installation app for Windows Phone 8.1</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src123" class="srcSentence">WinPhoneCompanyPortal.ps1 – A PowerShell script you can use to sign the Company Portal app file so it can be deployed to Windows Phone 8.1 devices</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para></para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src124" class="srcSentence">
                          <embeddedLabel>Download the Windows Phone SDK</embeddedLabel>
                          <br />Download the <externalLink target="_blank"><linkText>Windows Phone SDK 8.0</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615570</linkUri></externalLink> (http://go.microsoft.com/fwlink/?LinkId=268439) and install the SDK to your computer.</caps:sentence>
                        <caps:sentence id="src125" class="srcSentence"> This SDK is needed to generate an application enrollment token.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src126" class="srcSentence">
                          <embeddedLabel>Generate an AETX file</embeddedLabel>
                          <br />Generate an application enrollment token (.aetx) file from the Symantec PFX file using AETGenerator.exe, part of Windows Phone SDK 8.0.</caps:sentence>
                        <caps:sentence id="src127" class="srcSentence"> For instructions on how to create an AETX file, see <externalLink><linkText>How to generate an application enrollment token for Windows Phone</linkText><linkUri>https://msdn.microsoft.com/library/windows/apps/jj735576.aspx</linkUri></externalLink></caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src128" class="srcSentence">
                          <embeddedLabel>Download the Windows SDK for Windows 8.1</embeddedLabel>
                          <br />Download and install the <externalLink target="_blank"><linkText>Windows Phone SDK</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=613525</linkUri></externalLink> (http://go.microsoft.com/fwlink/?LinkId=613525).</caps:sentence>
                        <caps:sentence id="src129" class="srcSentence"> Note that the PowerShell script included with the Company Portal app uses the default install location, <codeInline>${env:ProgramFiles(x86)}\Windows Kits\8.1</codeInline>.</caps:sentence>
                        <caps:sentence id="src130" class="srcSentence"> If you install elsewhere, you must include the location in a cmdlet parameter.</caps:sentence>
                      </para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src131" class="srcSentence">
                          <embeddedLabel>Code-sign the app using PowerShell</embeddedLabel>
                          <br />As an administrator, open <ui>Windows PowerShell</ui> on the host computer installed with the Windows SDK, the Symantec Enterprise Mobile Code Signing Certificate, navigate to the Sign-WinPhoneCompanyPortal.ps1 file and run the script.</caps:sentence>
                      </para>
                      <para>
                        <embeddedLabel>
                          <caps:sentence id="src132" class="srcSentence">Example 1</caps:sentence>
                        </embeddedLabel>
                      </para>
                      <code>.\Sign-WinPhoneCompanyPortal.ps1 -InputAppx 'C:\temp\CompanyPortal.appx' -OutputAppx 'C:\temp\CompanyPortalEnterpriseSigned.appx' -PfxFilePath 'C:\signing\cert.pfx' -PfxPassword '1234' -AetxPath 'C:\signing\cert.aetx'</code>
                      <para>
                        <caps:sentence id="src133" class="srcSentence">This example signs the CompanyPortal.appx at C:\temp\ and produces the CompanyPortalEnterpriseSigned.appx.</caps:sentence>
                        <caps:sentence id="src134" class="srcSentence"> It would use PFX password 1234 and read the publisher ID from the PFX file.</caps:sentence>
                        <caps:sentence id="src135" class="srcSentence"> It reads the enterprise ID from the cert.aetx file as well.</caps:sentence>
                      </para>
                      <para>
                        <embeddedLabel>
                          <caps:sentence id="src136" class="srcSentence">Example 2</caps:sentence>
                        </embeddedLabel>
                      </para>
                      <code>.\Sign-WinPhoneCompanyPortal.ps1 -InputAppx 'C:\temp\CompanyPortal.appx' -OutputAppx 'C:\temp\CompanyPortalEnterpriseSigned.appx' -PfxFilePath 'C:\signing\cert.pfx' -PfxPassword '1234' -PublisherId 'OID.0.9.2342.19200300.100.1.1=1000000001, CN="Test, Inc.", OU=Test 1' -EnterpriseId 1000000001</code>
                      <para>
                        <caps:sentence id="src137" class="srcSentence">This example signs the CompanyPortal.appx at C:\temp\ and produces the CompanyPortalEnterpriseSigned.appx.</caps:sentence>
                        <caps:sentence id="src138" class="srcSentence"> It would use PFX password 1234 and use the publisher ID specified.</caps:sentence>
                      </para>
                      <para>
                        <embeddedLabel>
                          <caps:sentence id="src139" class="srcSentence">Parameters:</caps:sentence>
                        </embeddedLabel>
                      </para>
                      <list class="bullet">
                        <listItem>
                          <para>
                            <caps:sentence id="src140" class="srcSentence">
                              <codeInline>-InputAppx</codeInline> – The local path to the CompanyPortal.appx file in single quotes.</caps:sentence>
                            <caps:sentence id="src141" class="srcSentence"> For example 'C:\temp\CompanyPortal.appx'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src142" class="srcSentence">
                              <codeInline>-OutputAppx</codeInline> – The local path and file name for the signed Company Portal app in single quotes.</caps:sentence>
                            <caps:sentence id="src143" class="srcSentence"> For example, 'C:\temp\CompanyPortalEnterpriseSigned.appx'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src144" class="srcSentence">
                              <codeInline>-PfxFilePath</codeInline> – The local path and file name for the exported PFX file of the Symantec certificate.</caps:sentence>
                            <caps:sentence id="src145" class="srcSentence"> For example, 'C:\signing\cert.pfx'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src146" class="srcSentence">
                              <codeInline>-PfxPassword</codeInline> – The password used to sign the PFX file in single quotes.</caps:sentence>
                            <caps:sentence id="src147" class="srcSentence"> For example '1234'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src148" class="srcSentence">
                              <codeInline>-AetxPath</codeInline> – The local path to the .aetx file which is used for reading the enterprise ID if the 'EnterpriseId' argument is not defined.</caps:sentence>
                            <caps:sentence id="src149" class="srcSentence"> Either this argument or EnterpriseId must be provided.</caps:sentence>
                            <caps:sentence id="src150" class="srcSentence"> For example 'C:\signing\cert.aetx'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src151" class="srcSentence">
                              <codeInline>-PublisherId</codeInline> - The Publisher ID of the enterprise.</caps:sentence>
                            <caps:sentence id="src152" class="srcSentence"> If absent, the 'Subject' field of the Symantec Enterprise Mobile Code Signing Certificate is used.</caps:sentence>
                            <caps:sentence id="src153" class="srcSentence"> For example, 'OID.0.9.2342.19200300.100.1.1=1000000001, CN="Test, Inc.", OU=Test 1'</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src154" class="srcSentence">
                              <codeInline>-SdkPath</codeInline> - The path to the root folder of the Windows SDK for Windows 8.1.</caps:sentence>
                            <caps:sentence id="src155" class="srcSentence"> This argument is optional and defaults to ${env:ProgramFiles(x86)}\Windows Kits\8.1.</caps:sentence>
                          </para>
                        </listItem>
                        <listItem>
                          <para>
                            <caps:sentence id="src156" class="srcSentence">
                              <codeInline>-EnterpriseId</codeInline> - The enterprise ID.</caps:sentence>
                            <caps:sentence id="src157" class="srcSentence"> Either this argument or 'AetxPath' must be provided.</caps:sentence>
                            <caps:sentence id="src158" class="srcSentence"> If this argument is not provided, the enterprise ID is read from the AETX file.</caps:sentence>
                            <caps:sentence id="src159" class="srcSentence"> For example, 1000000001</caps:sentence>
                          </para>
                        </listItem>
                      </list>
                      <para></para>
                    </content>
                  </step>
                  <step>
                    <content>
                      <para>
                        <caps:sentence id="src160" class="srcSentence">Deploy the Windows Phone 8.1 Company Portal (SSP.appx) app.</caps:sentence>
                      </para>
                      <alert class="important">
                        <para>
                          <caps:sentence id="src161" class="srcSentence">The ssp.xap and the Company Portal from the store can both be installed at the same time, which can be confusing for users.</caps:sentence>
                          <caps:sentence id="src162" class="srcSentence"> To have all users using the ssp.xap, create a blocked app for the store version of the Company Portal.</caps:sentence>
                          <caps:sentence id="src163" class="srcSentence"> To have all Windows Phone 8.1 devices to use only the store version of the Company Portal, you have three choices:</caps:sentence>
                        </para>
                        <list class="bullet">
                          <listItem>
                            <para>
                              <caps:sentence id="src164" class="srcSentence">If you won’t sideload apps and don’t need to support Windows Phone 8.0, don’t upload the signed ssp.xap.</caps:sentence>
                            </para>
                          </listItem>
                          <listItem>
                            <para>
                              <caps:sentence id="src165" class="srcSentence">If sideloaded apps are needed, and if there are no Windows Phone 8 devices enrolling, change the automatically created ssp.xap deployment from “available” to “uninstall.”</caps:sentence>
                            </para>
                          </listItem>
                          <listItem>
                            <para>
                              <caps:sentence id="src166" class="srcSentence">If sideloaded apps need to be installed and Windows Phone 8.0 devices need to enroll and receive the ssp.xap, create a new software deployment of the ssp.xap and deploy it with the <ui>uninstall</ui> action.</caps:sentence>
                              <caps:sentence id="src167" class="srcSentence"> Windows Phone 8.0 devices don’t support forced install or uninstall of apps, so they will ignore the deployment.</caps:sentence>
                              <caps:sentence id="src168" class="srcSentence"> Windows Phone 8.1 devices support the uninstall action and will remove the ssp.xap.</caps:sentence>
                            </para>
                          </listItem>
                        </list>
                      </alert>
                    </content>
                  </step>
                </steps>
              </procedure>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src169" class="srcSentence">Renew your Symantec enterprise code-signing certificate for Windows devices</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src170" class="srcSentence">The Symantec certificate used to manage certain Windows and Windows Phone mobile devices must be renewed periodically.</caps:sentence>
            <caps:sentence id="src171" class="srcSentence"> For Windows Phone 8.0 devices, a signed Company Portal app and the code-signing certificate are needed for device enrollment.</caps:sentence>
            <caps:sentence id="src172" class="srcSentence"> Later Windows Phone devices can use the company portal app downloaded from the store.</caps:sentence>
            <caps:sentence id="src173" class="srcSentence"> A code-signing certificate is also be required for deploying line-of-business apps.</caps:sentence>
          </para>
          <procedure expanded="false">
            <title>
              <caps:sentence id="src174" class="srcSentence">How to renew the Symantec enterprise code-signing certificate</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src175" class="srcSentence">Look for a renewal email sent from Symantec approximately 14 days prior to certificate expiration.</caps:sentence>
                    <caps:sentence id="src176" class="srcSentence"> This email contains directions from Symantec about renewing your enterprise certificate.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src177" class="srcSentence">For additional information about Symantec certificates, visit <externalLink><linkText>www.symantec.com</linkText><linkUri>http://www.symantec.com</linkUri></externalLink> or call 1-877-438-8776 or 1-650-426-3400.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src178" class="srcSentence">Go to the website (example: <externalLink><linkText>https://products.websecurity.symantec.com/orders/enrollment/microsoftCert.do</linkText><linkUri>https://products.websecurity.symantec.com/orders/enrollment/microsoftCert.do</linkUri></externalLink>) and login with the Symantec Publisher ID and email addressed associated with the certificate.</caps:sentence>
                    <caps:sentence id="src179" class="srcSentence"> Remember to use the same machine for starting the renewal that you’ll use to download the certificate.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src180" class="srcSentence">Once the renewal is approved and paid for, download the certificate.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
          <procedure expanded="false">
            <title>
              <caps:sentence id="src181" class="srcSentence">How to install the updated certificate for Windows Phone 8.0</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src182" class="srcSentence">Download and sign the latest Windows Phone Company Portal located here: <externalLink><linkText>http://www.microsoft.com/en-us/download/details.aspx?id=36060</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=36060</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src183" class="srcSentence">Open your Intune Administration Console (<externalLink><linkText>https://admin.manage.microsoft.com</linkText><linkUri>https://admin.manage.microsoft.com</linkUri></externalLink>) and go to <ui>Admin</ui>, <ui>Mobile Device Management</ui> &gt; <ui>Windows Phone</ui> and click <ui>Upload Signed App</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src184" class="srcSentence">Upload the newly signed Company Portal.</caps:sentence>
                    <caps:sentence id="src185" class="srcSentence"> You’ll need the newly signed SSP.xap and the new .PFX file you received from Symantec or the application enrollment token that was created with this new .PFX file.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src186" class="srcSentence">When the upload is complete, remove the old Company Portal version in the <ui>Software</ui> workspace in the Intune Management Console.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src187" class="srcSentence">Sign all enterprise line-of-business apps again using the same certificate and upload and replace existing applications.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
            <conclusion>
              <content>
                <para>
                  <caps:sentence id="src188" class="srcSentence">Providing a signed SSP.xap file is currently the only way to provide the updated code signing certificate.</caps:sentence>
                  <caps:sentence id="src189" class="srcSentence"> To support signed line-of-business apps, you must sign and upload a Company Portal app even though your users will install the Company Portal app from the store.</caps:sentence>
                </para>
              </content>
            </conclusion>
          </procedure>
          <procedure expanded="false">
            <title>
              <caps:sentence id="src190" class="srcSentence">How to install the updated certificate for Windows Phone 8.1 and later devices</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src191" class="srcSentence">Download and sign the latest Windows Phone Company Portal from the Download Center located here: <externalLink><linkText>http://www.microsoft.com/en-us/download/details.aspx?id=36060</linkText><linkUri>http://www.microsoft.com/en-us/download/details.aspx?id=36060</linkUri></externalLink>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src192" class="srcSentence">Open your <externalLink><linkText>Intune Administration Console</linkText><linkUri>https://admin.manage.microsoft.com</linkUri></externalLink> (https://admin.manage.microsoft.com) and go to <ui>Admin</ui> &gt; <ui>Mobile Device Management</ui> &gt; <ui>Windows Phone</ui> and click <ui>Upload Signed App</ui>.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src193" class="srcSentence">Upload the newly signed Company Portal.</caps:sentence>
                    <caps:sentence id="src194" class="srcSentence"> You’ll need the newly signed SSP.xap and the new .PFX file you received from Symantec or the Application enrollment token that was created with this new .PFX file.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src195" class="srcSentence">When the upload is complete, remove the old Company Portal version in the <ui>Software </ui> workspace.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src196" class="srcSentence">Sign all new and any updated enterprise line-of-business apps using the new certificate.</caps:sentence>
                    <caps:sentence id="src197" class="srcSentence"> Existing applications do not need to be resigned and redeployed.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <section address="BKMK_FAQ">
        <title>
          <caps:sentence id="src198" class="srcSentence">Frequently asked questions about mobile device management for Microsoft Intune including management with Configuration Manager 2012</caps:sentence>
        </title>
        <content>
          <para></para>
        </content>
        <sections>
          <section expanded="false" address="BKMK_Symantec">
            <title>
              <caps:sentence id="src199" class="srcSentence">Why does Windows Phone require a Symantec certificate for management?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src200" class="srcSentence">Windows Phone controls how you can install apps.</caps:sentence>
                <caps:sentence id="src201" class="srcSentence"> Any user with a Microsoft account can install apps from the Windows Phone store, or companies can install or sideload their internally developed line of business (LOB) apps using a special process described in the Windows Phone documentation.</caps:sentence>
                <caps:sentence id="src202" class="srcSentence"> When installing LOB apps, Windows Phones trust only one special type of certificate issued by Symantec.</caps:sentence>
                <caps:sentence id="src203" class="srcSentence"> You cannot use any other commercially or privately generated certificate.</caps:sentence>
                <caps:sentence id="src204" class="srcSentence"> This requirement is true for all mobile device management solutions, not just Intune.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src205" class="srcSentence">The Symantec certificate creates an application enrollment token (AET).</caps:sentence>
                <caps:sentence id="src206" class="srcSentence"> The AET can be installed on a device when the device enrolls for mobile device management, or it can be installed out-of-band from a secure website or from an email attachment.</caps:sentence>
                <caps:sentence id="src207" class="srcSentence"> Administrators must sign every LOB app with the Symantec certificate, using the tools provided in the <externalLink target="_blank"><linkText>Windows Phone SDK</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268439</linkUri></externalLink>.</caps:sentence>
                <caps:sentence id="src208" class="srcSentence"> When users attempt to install LOB apps, the Windows Phone operating system checks the signature in the AET against the signature on the app.</caps:sentence>
                <caps:sentence id="src209" class="srcSentence"> If the signatures match, the installation is allowed to proceed.</caps:sentence>
                <caps:sentence id="src210" class="srcSentence"> If the AET cannot be verified, installation fails.</caps:sentence>
                <caps:sentence id="src211" class="srcSentence"> There are several reasons the AET might not be verified:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src212" class="srcSentence">The AET was never installed on the device</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src213" class="srcSentence">The AET has expired</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src214" class="srcSentence">The AET was not created using the same Symantec certificate used to sign the app</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src215" class="srcSentence">Windows Phone does not require that the AET be present during MDM enrollment, but prior to the November 2014 release, Intune required the AET and a signed ssp.xap because there was no other way to install the AET and ssp.xap except during enrollment.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src216" class="srcSentence">How is the AET created for Intune users?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src217" class="srcSentence">When administrators upload the .pfx file for their Symantec certificate, Intune automatically creates the AET and deploys it to enrolled Windows Phones.</caps:sentence>
                <caps:sentence id="src218" class="srcSentence"> It is not necessary for Intune admins to use the AET Generator tool in the Windows Phone SDK.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence id="src219" class="srcSentence">Intune does not support manually creating the AET and deploying it out-of-band.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src220" class="srcSentence">What changes happened to reduce the requirement for a Symantec certificate?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src221" class="srcSentence">For the November 2014 release, Intune made changes to allow for scenarios where companies do not have a Symantec certificate.</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src222" class="srcSentence">The Company Portal for Windows Phone 8.1 is available to install from the store, so it needn’t be signed with a Symantec certificate and validated against an AET.</caps:sentence>
                    <caps:sentence id="src223" class="srcSentence"> Instead, the app is validated as part of the store publishing process.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src224" class="srcSentence">Windows Phone 8.1 devices can enroll with or without an AET on the phone.</caps:sentence>
                    <caps:sentence id="src225" class="srcSentence"> If an AET is available, it will be installed the first time the device synchronizes with Intune.</caps:sentence>
                    <caps:sentence id="src226" class="srcSentence"> If there is no AET, the device can still be managed by Intune, and users can install the Company Portal from the store and use most features of the Company Portal without a Symantec certificate to sign apps.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src227" class="srcSentence">There are no changes to the Symantec requirement for Windows Phone 8 devices.</caps:sentence>
                <caps:sentence id="src228" class="srcSentence"> Windows Phone 8 devices must have the signed ssp.xap and the AET present during enrollment or they will be blocked from enrolling.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src229" class="srcSentence">What functionality is supported if a Windows Phone 8.1 device is enrolled but there is no Symantec certificate?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src230" class="srcSentence">If a Windows Phone 8.1 device is enrolled but there’s no Symantec certificate, you can:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src231" class="srcSentence">Create policies and push them to the device</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src232" class="srcSentence">Configure contact information for the IT department that will shows in the Company Portal</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src233" class="srcSentence">Create deep links to the store and deploy them to the Company Portal</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src234" class="srcSentence">Create links to web pages and deploy them to the Company Portal</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src235" class="srcSentence">Create terms and conditions that must be accepted by users before they can use the Company Portal</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src236" class="srcSentence">The one thing you cannot do without a Symantec certificate is deploy LOB apps.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence id="src237" class="srcSentence">The Intune Software Publisher does not verify that apps are signed when you upload them.</caps:sentence>
                  <caps:sentence id="src238" class="srcSentence"> If you deploy unsigned apps, they will fail when users try to install them.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src239" class="srcSentence">What can users do if they have the Company Portal but there is no Symantec certificate?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src240" class="srcSentence">Windows Phone 8.1 devices don’t have to be enrolled before users install the Company Portal from the store.</caps:sentence>
                <caps:sentence id="src241" class="srcSentence"> If the device is not enrolled, users are prompted to enroll.</caps:sentence>
                <caps:sentence id="src242" class="srcSentence"> Touching the prompt in the Company Portal takes users directly to <ui>Settings / Workplace</ui> where they can enroll their devices.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src243" class="srcSentence">Even without enrolling the device, uses can perform the following actions with the Company Portal installed from the store:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src244" class="srcSentence">Accept or decline any terms and conditions configured by the admin.</caps:sentence>
                    <caps:sentence id="src245" class="srcSentence"> If users decline the terms and conditions, the Company Portal closes.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src246" class="srcSentence">View the contact information for the IT department</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src247" class="srcSentence">View any enrolled devices including iOS, Android, and Windows devices</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src248" class="srcSentence">Use deep links to apps in the store</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src249" class="srcSentence">Use web links to open web pages</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src250" class="srcSentence">With the device enrolled, users can view the device in the <ui>My Devices</ui> list.</caps:sentence>
                <caps:sentence id="src251" class="srcSentence"> Once enrolled, the device is subject to any deployed Intune policies.</caps:sentence>
                <caps:sentence id="src252" class="srcSentence"> Devices must be enrolled to get the AET and install LOB apps.</caps:sentence>
                <caps:sentence id="src253" class="srcSentence"> An unenrolled device trying to install an LOB app will be directed to enroll.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src254" class="srcSentence">The only thing users cannot do if the company does not have a Symantec certificate is install LOB apps deployed by the admin.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src255" class="srcSentence">Our company already has a certificate and has been enrolling Windows Phone 8.1 devices.</caps:sentence>
              <caps:sentence id="src256" class="srcSentence"> Do I have to do anything different now that the Company Portal is available in the store?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src257" class="srcSentence">The current ssp.xap from the Download Center still works on Windows Phone 8.1 devices.</caps:sentence>
                <caps:sentence id="src258" class="srcSentence"> You can continue to direct users to enroll and get the company portal during installation.</caps:sentence>
              </para>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src259" class="srcSentence">What are the advantages and disadvantages of users getting the Company Portal from the store?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src260" class="srcSentence">Advantages:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src261" class="srcSentence">Users get deep links and web links, even if the Windows Phone 8.1 device isn’t enrolled</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src262" class="srcSentence">When Microsoft updates the Company Portal, the store app updates automatically without your downloading, signing, and redeploying the ssp.xap</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src263" class="srcSentence">Documentation for Windows Phone 8.1, iOS, Android, and Windows users is consistent: “Go to the store and install the Company Portal.”</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src264" class="srcSentence">Users see the app as it installs and get enrollment instructions when it opens</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src265" class="srcSentence">Disadvantages:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src266" class="srcSentence">Users see a checkbox to install a “<ui>company hub</ui>” but nothing directs them to the Company Portal in the device’s app list</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src267" class="srcSentence">Users aren’t required to accept custom terms and conditions until they open the Company Portal</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src268" class="srcSentence">In the following circumstances, you can continue directing users to enroll and have the ssp.xap installed during enrollment:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src269" class="srcSentence">If the company blocks access to the store from Windows Phones, users must get the ssp.xap installed during enrollment.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src270" class="srcSentence">If users do not have Microsoft accounts configured on their Windows Phones, they will not be able to install the Company Portal from the store.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src271" class="srcSentence">If the existing documentation for Windows Phone enrollment tells them to go to Settings, Workplace first, it may take a while to update the docs and direct users to the store.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src272" class="srcSentence">What’s the difference between the ssp.xap on the Download Center and the app in the store?</caps:sentence>
            </title>
            <content>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src273" class="srcSentence">The Company Portal in the store does not have to be signed by a Symantec certificate to be installed</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src274" class="srcSentence">The Company Portal in the store presents the terms and conditions to the user but the ssp.xap on the Download Center doesn’t</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src275" class="srcSentence">The Company Portal in the store is an .appx instead of a .xap</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src276" class="srcSentence">Can I get the Company Portal file and push it to my users instead of sending them to the store?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src277" class="srcSentence">Yes.</caps:sentence>
                <caps:sentence id="src278" class="srcSentence"> The Company Portal app can be downloaded for the following operating systems from the Download Center:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src279" class="srcSentence">Windows Phone 8.1: <externalLink><linkText>http://go.microsoft.com/fwlink/?LinkId=615799</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615799</linkUri></externalLink></caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src280" class="srcSentence">Windows Phone 8.0 : <externalLink><linkText>http://go.microsoft.com/fwlink/?LinkId=268440</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=268440</linkUri></externalLink></caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src281" class="srcSentence">Windows 8.1: <externalLink><linkText>http://go.microsoft.com/fwlink/?LinkId=615800</linkText><linkUri>http://go.microsoft.com/fwlink/?LinkId=615800</linkUri></externalLink></caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src282" class="srcSentence">Can companies still use the Support Tool for Windows Intune Trial Management of Windows Phone if they don’t have a Symantec certificate, and still have users install the Company Portal from the store?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src283" class="srcSentence">Yes.</caps:sentence>
                <caps:sentence id="src284" class="srcSentence"> If you need to do a proof of concept that includes installation of LOB apps, the trial management tool works with the store version of the company portal.</caps:sentence>
                <caps:sentence id="src285" class="srcSentence"> Because the AET from the Symantec certificate is no longer required to enroll Windows Phone 8.1 devices, however, companies can test app installation using deep links to apps in the store.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src286" class="srcSentence">The Support Tool for Windows Intune Trial Management of Windows Phone is only for trial subscriptions of Intune.</caps:sentence>
              </para>
              <alert class="important">
                <para>
                  <caps:sentence id="src287" class="srcSentence">Only use the trial management tool testing.</caps:sentence>
                  <caps:sentence id="src288" class="srcSentence"> Devices enrolled with the AET from the trial management tool must unenroll and reenroll if the Symantec certificate for the trial management tool is no longer available, or if the company obtains its own Symantec certificate for signing apps.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section expanded="false">
            <title>
              <caps:sentence id="src289" class="srcSentence">Can companies start without any Symantec certificate and then add one later, even after Windows Phone 8.1 devices have enrolled?</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src290" class="srcSentence">Yes.</caps:sentence>
                <caps:sentence id="src291" class="srcSentence"> Even if Windows Phone 8.1 devices have already enrolled, you can get a Symantec certificate, sign the ssp.xap, and upload it and the pfx file.</caps:sentence>
                <caps:sentence id="src292" class="srcSentence"> Intune will then generate the AET.</caps:sentence>
                <caps:sentence id="src293" class="srcSentence"> Windows Phone 8.1 devices will get the AET the next time they sync, up to eight hours.</caps:sentence>
                <caps:sentence id="src294" class="srcSentence"> Allow at least eight hours before deploying line of business apps after uploading the xap and pfx.</caps:sentence>
              </para>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="44fd4af0-f9b0-493a-b590-7825139d9d40">Manage mobile devices with Microsoft Intune</link>
      </relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>