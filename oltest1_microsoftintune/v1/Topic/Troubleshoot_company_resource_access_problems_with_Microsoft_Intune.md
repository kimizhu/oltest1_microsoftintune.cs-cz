---
description: na
keywords: na
title: Troubleshoot company resource access problems with Microsoft Intune
search: na
ms.date: na
ms.service: microsoft-intune
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 40622ced-6029-4abf-873e-b51d2b51934c
---
# Řešen&#237; probl&#233;mů s př&#237;stupem k prostředkům společnosti ve službě Microsoft Intune
Informace z tohoto tématu použijte k vyřešení problémů, když akce [!INCLUDE[wit_firstref](../Token/wit_firstref_md.md)] vrátí kód chyby.

Pokud tyto informace váš problém nevyřeší, přečtěte si článek [Jak získat podporu pro Microsoft Intune](../Topic/How_to_get_support_for_Microsoft_Intune.md), kde najdete další nápovědu.

## Kódy chyb související s přístupem k podnikovým prostředkům

### Stavové kódy pro zařízení s Windows spravovaná systémem MDM

|Stavový kód|Chybová zpráva|Co dělat|
|---------------|------------------|------------|
|10 (APP_CI_ENFORCEMENT_IN_PROGRESS)|Probíhá instalace||
|20 (APP_CI_ENFORCEMENT_IN_PROGRESS_WAITING_CONTENT)|Čeká se na obsah||
|30 (APP_CI_ENFORCEMENT_ERROR_RETRIEVING_CONTENT)|Načítá se obsah|Pravděpodobná příčina: Stav úlohy 30 označuje, že se uživateli nepodařilo stáhnout aplikaci.<br /><br />Toto jsou pravděpodobné příčiny:<br /><br />V průběhu stahování zařízení ztratilo připojení k internetu.<br /><br />Mohlo dojít k vypršení platnosti certifikátu vydaného pro zařízení v době registrace.<br /><br />Snížení rizika:<br /><br />Spuštěním Aplikací společnosti z ovládacích panelů na zařízení potvrďte, že platnost certifikátu zařízení nevypršela. Pokud platnost vypršela, bude nutné zařízení znovu zaregistrovat.<br /><br />Potvrďte, že zařízení je připojené k internetu , a zkuste znovu požádat o aplikaci.|
|40 (APP_CI_ENFORCEMENT_IN_PROGRESS_CONTENT_DOWNLOADED)|Stahování obsahu se dokončilo||
|50 (APP_CI_ENFORCEMENT_IN_PROGRESS_INSTALLING)|Probíhá instalace||
|60 (APP_CI_ENFORCEMENT_ERROR_INSTALLING)|Instalace Došlo k chybě|Aplikaci se po stažení nepodařilo nainstalovat.<br /><br />Certifikát pro podpis kódu, kterým je aplikace podepsaná, se v zařízení nenachází.<br /><br />Závislost architektury, na které je aplikace závislá, není na zařízení nainstalovaná.<br /><br />Ujistěte se, že certifikát pro podpis kódu, se kterým je aplikace podepsaná, v zařízení existuje, a u správce ověřte, že tento certifikát je určený pro všechna zapsaná podniková zařízení s Windows RT.<br /><br />V případě, že je chyba instalace způsobená chybějící závislostí architektury, bude muset správce aplikaci znovu publikovat v balíčku společně s aplikací.<br /><br />Stažený balíček aplikace není platným balíčkem, je poškozený, nebo není kompatibilní s verzí operačního systému zařízení.|
|70 (APP_CI_ENFORCEMENT_SUCCEEDED)|Instalace byla úspěšná||
|80 (APP_CI_ENFORCEMENT_IN_PROGRESS)|Probíhá odinstalace||
|90 (APP_CI_ENFORCEMENT_ERROR)|Došlo k chybě odinstalace||
|100 (APP_CI_ENFORCEMENT_SUCCEEDED)|Odinstalace byla úspěšná||
|110 (APP_CI_ENFORCEMENT_ERROR)|Neshoda algoritmu hash obsahu||
|120 (APP_CI_ENFORCEMENT_ERROR)|SLK / zkušební načítání se nepovoluje||
|130 (APP_CI_ENFORCEMENT_ERROR)|Instalace licence MSADP se nepodařila||
|Bez stavu (APP_CI_ENFORCEMENT_UNKNOWN)|není k dispozici|Stav je momentálně neznámý.|

### Přístup k prostředkům společnosti (běžné chyby)

|Stavový kód|Chybová zpráva|
|---------------|------------------|
|-2016281101|Nenašla se žádost MDM CRP.|
|-2016281102|Nenašla se adresa URL služby NDES.|
|-2016281103|Nenašly se informace o certifikátu MDM CRP.|
|-2016281104|Nenašly se informace o certifikátu MDM CI.|
|-2016281105|Pravidlo se nepodařilo vyhodnotit.|
|-2016281106|Nedá se použít kvůli ztrátě při řešení konfliktů.|
|-2016281107|Nepodporovaný zdroj nastavení zjišťování|
|-2016281108|Odkazované nastavení se nepodařilo ve službě CI najít.|
|-2016281109|Převod datového typu se nepodařil.|
|-2016281110|Neplatný parametr pro nastavení služby CIM|
|-2016281111"|Neplatí pro toto zařízení.|
|-2016281112|Náprava se nepodařila.|
|-2016330905|Stav aplikace je neznámý.|
|-2016330906|Aplikace je spravovaná, ale uživatel ji odebral.|
|-2016330907|Zařízení uplatňuje kód.|
|-2016330908|Aplikaci se nepovedlo nainstalovat.|
|-2016330909|Uživatel odmítl nabídku na aktualizaci aplikace.|
|-2016330910|Uživatel odmítl nabídku na instalaci aplikace.|
|-2016330911|Uživatel nainstaloval aplikaci dřív, než se mohla provést instalace spravované aplikace.|
|-2016330912|Instalace aplikace je naplánovaná, ale aby se dala dokončit transakce, potřebuje se kód, který by se dal uplatnit.|
|-2016341109|Zařízení s platformou iOS vrátilo chybu.|
|-2016341110|Zařízení s platformou iOS zamítlo příkaz kvůli nesprávnému formátu.|
|-2016341111|Zařízení s platformou iOS vrátilo neočekávaný stav nečinnosti.|
|-2016341112|Zařízení s platformou iOS je momentálně zaneprázdněné.|

### Chyby vrácené v zařízeních s iOS

|Stavový kód|Chybová zpráva|
|---------------|------------------|
|-2016299111|Vnitřní chyba|
|-2016299112|Vnitřní chyba|
|-2016300111|36001:(vnitřní chyba)|
|-2016300112|36000:Mobilní připojení už je nakonfigurované.|
|-2016301110|35002:V jedné datové části je víc písem.|
|-2016301111|35001:Instalace písma selhala.|
|-2016301112|35000:Neplatná data písma|
|-2016302109|34003:Neplatný hlavní název protokolu Kerberos|
|-2016302110|34003:Chybí hlavní název protokolu Kerberos.|
|-2016302111|34001:Neplatný vzor pro shodu adresy URL|
|-2016302112|34000:Neplatný vzor pro shodu identifikátoru aplikace server|
|-2016304112|32000:Moc aplikací|
|-2016305111|31001:Nastavení nejde použít.|
|-2016305112|31000:Přihlašovací údaje nejde použít.|
|-2016306111|30001:Vypršel časový limit.|
|-2016306112|30000:Ověření se nepovedlo.|
|-2016307109|29003:Chybná data certifikátu|
|-2016307110|29002:|
|-2016307111|29001:|
|-2016307112|29000:Zařízení není pod dohledem.|
|-2016308110|28002:Nejde nastavit tapetu.|
|-2016308111|28001:Chybný obrázek tapety|
|-2016308112|28000:Neznámá položka|
|-2016310111|26001:Nepodporované šifrování na úrovni souborů|
|-2016310112|26000:Nepodporované šifrování na úrovni bloků|
|-2016311110|25002:Nejde odebrat.|
|-2016311111|25001:Nejde nainstalovat.|
|-2016311112|25000:Chybný profil|
|-2016312109|24003:Chybný finální profil|
|-2016312110|24002:Chybná datová část identity|
|-2016312111|24001:Nejde podepsat slovník atributů.|
|-2016312112|24000:Nejde vytvořit slovník atributů.|
|-2016313110|23002:Neplatný certifikát serveru|
|-2016313111|23001:Chybná odpověď serveru|
|-2016313112|23000:Chybná identita|
|-2016314099|22013:Neplatná odpověď PKIOperation|
|-2016314100|22012:Nejde uložit CACertificate.|
|-2016314101|22011:Nejde vygenerovat CSR.|
|-2016314102|22010:Nejde uložit dočasnou identitu.|
|-2016314103|22009:Nejde vytvořit dočasnou identitu.|
|-2016314104|22008:Nejde vytvořit identitu.|
|-2016314105|22007:Neplatný podepsaný certifikát|
|-2016314106|22006:Nedostatečné CACaps|
|-2016314107|22005:Chyba sítě|
|-2016314108|22004:Nepodporovaná konfigurace certifikátu|
|-2016314109|22003:Neplatná odpověď RAResponse|
|-2016314110|22002:Neplatná odpověď CAResponse|
|-2016314111|22001:Nejde vygenerovat pár klíčů.|
|-2016314112|22000:Neplatné použití klíče|
|-2016315105|21007:Nejde ověřit účet.|
|-2016315106|21006:Nejde dešifrovat certifikát.|
|-2016315107|21005:Účet není jedinečný.|
|-2016315108|21004:Nejde vytvořit účet.|
|-2016315109|21003:Žádný název hostitele|
|-2016315110|21002:Nejde dodržet zásadu šifrování ze serveru.|
|-2016315111|21001:Nejde dodržet zásadu ze serveru.|
|-2016315112|21000:Nejde získat zásadu ze serveru.|
|-2016316110|20002:Účet není jedinečný.|
|-2016316111|20001:Žádný název hostitele|
|-2016316112|20000:Nejde vytvořit účet.|
|-2016317110|19002:Účet není jedinečný.|
|-2016317111|19001:Žádný název hostitele|
|-2016317112|19000:Nejde vytvořit účet.|
|-2016318110|18002:Neplatné přihlašovací údaje|
|-2016318111|18001:Nedosažitelný hostitel|
|-2016318112|18000:Neznámá chyba|
|-2016319110|17002:Účet není jedinečný.|
|-2016319111|17001:Žádný název hostitele|
|-2016319112|17000:Nejde vytvořit účet.|
|-2016320110|16002:Účet není jedinečný.|
|-2016320111|16001:Žádný název hostitele|
|-2016320112|16000:Nejde vytvořit předplatné.|
|-2016321109|15003:Neplatný certifikát|
|-2016321110|15002:Nejde zamknout konfiguraci sítě.|
|-2016321111|15001:Nejde odebrat VPN.|
|-2016321112|15000:Nejde nainstalovat VPN.|
|-2016322110|14002:Konfigurace cloudu už existuje.|
|-2016322111|14001:Zařízení je zamčené.|
|-2016322112|14000:Neplatné pole|
|-2016323107|13005:Nejde nastavit proxy server.|
|-2016323108|13004:Nejde nastavit protokol EAP.|
|-2016323109|13003:Nejde vytvořit konfiguraci připojení WiFi.|
|-2016323110|13002:Heslo je povinné.|
|-2016323111|13001:Uživatelské jméno je povinné.|
|-2016323112|13000:Nejde nainstalovat.|
|-2016324070|12042:Neznámý kód národního prostředí|
|-2016324071|12041:Neznámý kód jazyka|
|-2016324072|12040:Vyžadují se přihlašovací údaje pro přihlášení do obchodu iTunes.|
|-2016324073|12039:(nepoužívá se)|
|-2016324074|12038:Aplikace není spravovaná.|
|-2016324075|12037:Neplatný kód pro uplatnění|
|-2016324076|12036:Aplikaci nejde odebrat v aktuálním stavu.|
|-2016324077|12035:Aplikaci nejde koupit.|
|-2016324078|12034:Adresa URL není adresa HTTPS.|
|-2016324079|12033:Neplatný manifest|
|-2016324080|12032:V manifestu je moc velký počet aplikací.|
|-2016324081|12031:Instalace aplikace je zakázaná.|
|-2016324082|12030:Neplatná adresa URL|
|-2016324083|12029:Aplikace není spravovaná.|
|-2016324084|12028:Nečeká se na uplatnění kódu.|
|-2016324085|12027:Nejde o aplikaci.|
|-2016324086|12026:Aplikace už je ve frontě.|
|-2016324087|12025:Aplikace už je nainstalovaná.|
|-2016324088|12024:Nepovedlo se ověřit manifest aplikace.|
|-2016324089|12023:Nepovedlo se ověřit ID aplikace.|
|-2016324090|12022:Neplatné téma|
|-2016324091|12021:Neplatný typ požadavku|
|-2016324092|12020:Neautorizované serverem|
|-2016324093|12019:Nejde zkopírovat tajný klíč v úschově.|
|-2016324094|12018:Nejde zkopírovat data úložiště šifrovacích klíčů v úschově.|
|-2016324095|12017:Nejde vytvořit úložiště šifrovacích klíčů v úschově.|
|-2016324096|12016:Chybí identita.|
|-2016324097|12015:Nejde získat token push.|
|-2016324098|12014:Profil zřizování není spravovaný.|
|-2016324099|12013:Profil není spravovaný.|
|-2016324100|12012:Neshoda pro nahrazení MDM|
|-2016324101|12011: Neplatná konfigurace MDM|
|-2016324102|12010:Vnitřní chyba kvůli nekonzistenci|
|-2016324103|12009:Neplatný profil nahrazení|
|-2016324104|12008: Chybně vytvořený požadavek|
|-2016324105|12007:Neautorizované|
|-2016324106|12006:Odmítnuté přesměrování|
|-2016324107|12005:Nejde najít certifikát.|
|-2016324108|12004:Neplatný certifikát push|
|-2016324109|12003:Neplatná výzva/odezva pro ověřování|
|-2016324110|12002:Nejde provést vrácení se změnami.|
|-2016324111|12001:Několik instancí MDM|
|-2016324112|12000:Neplatná přístupová práva|
|-2016325111|11001:Vlastní APN už je nainstalovaný.|
|-2016325112|11000:Nejde nainstalovat APN.|
|-2016326111|10001:Neplatná podepisující osoba|
|-2016326112|10000:Nejde nainstalovat výchozí.|
|-2016327106|9006:Certifikát není identita.|
|-2016327107|9005:Certifikát je chybně vytvořený.|
|-2016327108|9004:Nejde uložit kořenový certifikát.|
|-2016327109|9003:Nejde uložit data WAPI.|
|-2016327110|9002:Nejde uložit certifikát.|
|-2016327111|9001:V datové části je moc velký počet certifikátů.|
|-2016327112|9000:Neplatné heslo|
|-2016328112|8000:Nejde nainstalovat funkci Web Clip.|
|-2016329105|7007:Účet SMTP je špatně nakonfigurovaný.|
|-2016329106|7006:Účet POP je špatně nakonfigurovaný.|
|-2016329107|7005:Účet IMAP je špatně nakonfigurovaný.|
|-2016329108|7004:Certifikát SMIME je chybný.|
|-2016329109|7003:Certifikát SMIME se nenašel.|
|-2016329110|7002:Během ověřování došlo k neznámé chybě.|
|-2016329111|7001:Neplatné přihlašovací údaje|
|-2016329112|7000:Nedosažitelný hostitel|
|-2016330110|6002:Nejde vytvořit dotaz.|
|-2016330111|6001:Prázdný řetězec|
|-2016330112|6000:Systémová chyba řetězce klíčů|
|-2016331097|5015:Nejde nastavit období odkladu.|
|-2016331098|5014:Nejde nastavit heslo.|
|-2016331099|5013:Nejde vymazat heslo.|
|-2016331100|5012:(nepoužívá se)|
|-2016331101|5011:Nesprávné heslo|
|-2016331102|5010:Zařízení je zamčené.|
|-2016331103|5009:(nepoužívá se)|
|-2016331104|5008:Stejné heslo se použilo v nedávné době.|
|-2016331105|5007:Skončila platnost hesla.|
|-2016331106|5006:V hesle musí být alfanumerické znaky.|
|-2016331107|5005:V hesle musí být číslo.|
|-2016331108|5004:V hesle jsou znaky, které jdou po sobě (vzestupně nebo sestupně).|
|-2016331109|5003:V hesle jsou znaky, které se opakují.|
|-2016331110|5002:Moc málo složitých znaků|
|-2016331111|5001:Moc málo jedinečných znaků|
|-2016331112|5000:Heslo je moc krátké.|
|-2016332093|4019:Několik datových částí App Lock|
|-2016332094|4018:Několik datových částí pro APN / mobilní připojení|
|-2016332095|4017:Několik globálních datových částí HTTPProxy|
|-2016332096|4016:(vnitřní chyba)|
|-2016332097|4015:Profil nahrazení neobsahuje datovou část MDM.|
|-2016332098|4014:Není dostupná žádná identita zařízení.|
|-2016332099|4013:Aktualizace selhala.|
|-2016332100|4012:Profil nejde aktualizovat.|
|-2016332101|4011:Finální profil není konfigurační profil.|
|-2016332102|4010:Aktualizovaný profil nemá stejný identifikátor.|
|-2016332103|4009:Zařízení je zamčené.|
|-2016332104|4008:Neshoda certifikátů|
|-2016332105|4007:Nerozpoznaný formát souboru|
|-2016332106|4006:Datum odebrání profilu je v minulosti.|
|-2016332107|4005:Heslo nevyhovuje zásadám.|
|-2016332108|4004:Uživatel zrušil instalaci.|
|-2016332109|4003:Profil není ve frontě pro instalaci.|
|-2016332110|4002:Duplicitní UUID|
|-2016332111|4001:Selhání instalace|
|-2016332112|4000:Nejde analyzovat profil.|
|-2016333111|3001:Nekonzistení rozpoznávání porovnání hodnot (vnitřní chyba)|
|-2016333112|3000:Nekonzistení rozpoznávání omezení (vnitřní chyba)|
|-2016334108|2004:Nepodporovaná hodnota pole|
|-2016334109|2003:Chybný datový typ v poli|
|-2016334110|2002:Chybí hodnota v povinném poli.|
|-2016334111|2001:Nepodporovaná verze datové části|
|-2016334112|2000:Chybně vytvořená datová část|
|-2016335102|1010:Nepodporovaná hodnota pole|
|-2016335103|1009:Selhání instalace profilu|
|-2016335104|1008:Nejedinečné identifikátory datové části|
|-2016335105|1007:Nejedinečné identifikátory UUID|
|-2016335106|1006:Nejde dešifrovat.|
|-2016335107|1005:Prázdný profil|
|-2016335108|1004:Chybný podpis|
|-2016335109|1003:Chybný datový typ v poli|
|-2016335110|1002:Chybí hodnota v povinném poli.|
|-2016335111|1001:Nepodporovaná verze profilu|
|-2016335112|1000:Chybně vytvořený profil|

### Kódy odpovědí OMA

|Stavový kód|Chybová zpráva|
|---------------|------------------|
|-2016344008|(1404): Přístup k certifikátu zamítnutý|
|-2016344009|(1403): Certifikát se nenašel|
|-2016344010|DCMO(1402): Operace selhala|
|-2016344011|DCMO(1401): Uživatel reagoval na výzvu nepřijetím operace.|
|-2016344012|DCMO(1400): Chyba klienta|
|-2016344108|DCMO(1204): Funkce zařízení je vypnutá. Uživatel ji může znovu zapnout.|
|-2016344109|DCMO(1203): Funkce zařízení je vypnutá. Uživatel ji nemůže znovu zapnout.|
|-2016344110|DCMO(1202): Zapnutí proběhlo úspěšně, ale funkce zařízení je momentálně odpojená.|
|-2016344111|DCMO(1201): Zapnutí proběhlo úspěšně a funkce zařízení je momentálně připojená.|
|-2016344112|DCMO(1200): Operace probíhá úspěšně|
|-2016345595|Syncml(517): Odpověď na atomický příkaz byla tak velká, že se nevešla do jedné zprávy.|
|-2016345596|Syncml(516): Příkaz byl uvnitř elementu Atomic, a ten selhal. Příkaz se nepovedlo úspěšně vrátit zpátky.|
|-2016345598|Syncml(514): Příkaz SyncML se nedokončil úspěšně, protože operace byla zrušená ještě před jeho provedením.|
|-2016345599|Syncml(513): Příjemce nepodporuje nebo odmítá podporovat určenou verzi synchronizačního protokolu SyncML použitou ve zprávě SyncML žádosti.|
|-2016345600|Syncml(512): Při synchronizační relaci došlo k chybě aplikace.|
|-2016345601|Syncml(511): Při zpracování požadavku došlo na serveru k vážné chybě.|
|-2016345602|Syncml(510): Při zpracování požadavku došlo k chybě. Chyba se týká výpadku úložiště dat příjemce.|
|-2016345603|Syncml(509): Vyhrazeno pro budoucí použití.|
|-2016345604|Syncml(508): Došlo k chybě, která vyžaduje obnovení aktuálního stavu synchronizace klienta se serverem.|
|-2016345605|Syncml(507): Chyba způsobila selhání všech příkazů protokolu SyncML v typu elementu Atomic.|
|-2016345606|Syncml(506): Při zpracování žádosti došlo k chybě aplikace.|
|-2016345607|Syncml(505): Příjemce nepodporuje nebo odmítá podporovat určenou verzi souboru DTD protokolu SyncML použitou ve zprávě SyncML žádosti.|
|-2016345608|Syncml(504): Příjemce, který funguje jako brána nebo proxy, nedostal včas odpověď od nadřazeného příjemce určeného identifikátorem URI (třeba HTTP, FTP, LDAP) nebo od jiného pomocného příjemce (třeba DNS). Odpověď potřeboval pro přístup, když se pokoušel dokončit žádost.|
|-2016345609|Syncml(503): Příjemce v současnosti nemůže žádost zpracovat. Příčinou je dočasné přetížení nebo údržba na straně příjemce.|
|-2016345610|Syncml(502): Příjemce, který funguje jako brána nebo proxy, nedostal platnou odpověď od nadřazeného příjemce, na kterého se obrátil při pokusu o splnění žádosti.|
|-2016345611|Syncml(501): Příjemce nepodporuje příkaz potřebný ke splnění žádosti.|
|-2016345612|Syncml(500): U příjemce vznikl nečekaně stav, který brání splnění žádosti.|
|-2016345684|Syncml(428): Přesun se nepodařil.|
|-2016345685|Syncml(427): Nadřazený objekt nejde odstranit, protože obsahuje podřízené položky.|
|-2016345686|Syncml(426): Dílčí položka není přijatá.|
|-2016345687|Syncml(425): Požadovaný příkaz nejde provést, protože odesílatel nemá u příjemce odpovídající oprávnění pro řízení přístupu (ACL).|
|-2016345688|Syncml(424): Objekt v bloku byl přijatý, ale velikost přijatého objektu neodpovídá velikosti deklarované v prvním bloku.|
|-2016345689|Syncml(423): Požadovaný příkaz nejde provést, protože „logicky odstraněná“ položka už byla předtím na serveru trvale odstraněná.|
|-2016345690|Syncml(422): Požadovaný příkaz nejde na serveru provést kvůli nesprávně vytvořenému skriptování CGI v LocURI.|
|-2016345691|Syncml(421): Požadovaný příkaz nejde na serveru provést, protože byla zadaná neznámá gramatika vyhledávání.|
|-2016345692|Syncml(420): Pro zbývající synchronizovaná data příjemce nemá další úložný prostor.|
|-2016345693|Syncml(419): Žádost klienta způsobila konflikt, který se vyřešil předností pro serverový příkaz.|
|-2016345694|Syncml(418): Požadovaný příkaz Put nebo Add nejde provést, protože cíl už existuje.|
|-2016345695|Syncml(417): Žádost v této chvíli nejde provést, ale původce ji může zopakovat později.|
|-2016345696|Syncml(416): Žádost nejde provést, protože je v ní uvedená nadměrná velikost v bajtech.|
|-2016345697|Syncml(415): Nepodporovaný typ nebo formát média.|
|-2016345698|Syncml(414): Požadovaný příkaz nejde provést, protože cílový identifikátor URI je moc dlouhý na to, aby ho příjemce mohl nebo chtěl zpracovat.|
|-2016345699|Syncml(413): Příjemce odmítl provést požadovaný příkaz, protože požadovaná položka je větší, než jakou je příjemce schopný nebo ochotný zpracovat.|
|-2016345700|Syncml(412): Požadovaný příkaz se na straně příjemce nepodařilo provést, protože je neúplný nebo nesprávně vytvořený.|
|-2016345701|Syncml(411): Požadovaný příkaz musí doprovázet velikost v bajtech nebo informace o délce v typu elementu Meta.|
|-2016345702|Syncml(410): Požadovaný cíl už není u příjemce a není známý ani předávací identifikátor URI.|
|-2016345703|Syncml(409): Žádost nebyla úspěšná, protože došlo ke konfliktu aktualizací mezi klientskou a serverovou verzí dat.|
|-2016345704|Syncml(408): Očekávaná zpráva nebyla v požadované době přijatá.|
|-2016345705|Syncml(407): Požadovaný příkaz nejde provést, protože původce nezajistil správné ověření.|
|-2016345706|Syncml(406): Požadovaný příkaz nejde provést, protože volitelná funkce v žádosti nebyla podporovaná.|
|-2016345707|Syncml(405): Požadovaný příkaz není v cíli dovolený.|
|-2016345708|Syncml(404): Požadovaný cíl se nepovedlo najít.|
|-2016345709|Syncml(403): Požadovaný příkaz nejde provést, i když mu příjemce rozumí.|
|-2016345710|Syncml(402): Požadovaný příkaz nejde provést, protože je potřeba řádná platba.|
|-2016345711|Syncml(401): Požadovaný příkaz nejde provést, protože žadatel nezajistil správné ověření.|
|-2016345712|Syncml(400): Požadovaný příkaz nejde provést kvůli chybné syntaxi příkazu.|
|-2016345807|Syncml(305): Přístup k požadovanému cíli je možný přes zadaný identifikátor URI proxy serveru.|
|-2016345808|Syncml(304): Požadovaný příkaz SyncML se v cíli neprovedl.|
|-2016345809|Syncml(303): Požadovaný cíl se našel na jiném identifikátoru URI.|
|-2016345810|Syncml(302): Požadovaný cíl se dočasně přesunul na jiný identifikátor URI.|
|-2016345811|Syncml(301): Požadovaný cíl má nový identifikátor URI.|
|-2016345812|Syncml(300): Požadovaný cíl je jedním z několika alternativních požadovaných cílů.|
|-2016345896|Syncml(216): Příkaz byl uvnitř elementu Atomic, a ten selhal. Příkaz je úspěšně vrácený zpět.|
|-2016345897|Syncml(215): Příkaz se neprovedl kvůli zásahu uživatele, který nepotvrdil volbu.|
|-2016345898|Syncml(214): Operace je zrušená. Příkaz SyncML se úspěšně dokončil, ale v této relaci se další příkazy nezpracují.|
|-2016345899|Syncml(213): Položka v bloku je přijatá a uložená do vyrovnávací paměti.|
|-2016345900|Syncml(212): Ověření je přijaté. Zbytek synchronizační relace nevyžaduje další ověřování. Kód odpovědi jde použít jenom v odpovědi na žádost, ve které byly přihlašovací údaje poskytnuté.|
|-2016345901|Syncml(211): Položka není odstraněná. Požadovaná položka se nenašla. Možná se odstranila dřív.|
|-2016345902|Syncml(210): Odstranění bez archivace. Z odpovědi vyplývá, že požadovaná data se úspěšně odstranila, ale nearchivovala se předtím, protože implementace tuto VOLITELNOU funkci nepodporuje.|
|-2016345903|Konflikt se vyřešil vytvořením duplicitních dat. Z odpovědi vyplývá, že žádost způsobila aktualizační konflikt, který se vyřešil vytvořením duplicitních klientských dat v serverové databázi. Odpověď obsahuje cílový identifikátor URI duplicitních dat v položce stavu. V případě obousměrné synchronizace je navíc vrácený příkaz Add s definicí duplicitních dat.|
|-2016345904|Konflikt se vyřešil tím, že „vyhrál“ příkaz klienta. Z odpovědi vyplývá, že při aktualizaci došlo ke konfliktu, který se vyřešil vítězstvím příkazu klienta.|
|-2016345905|Konflikt se vyřešil sloučením. Z odpovědi vyplývá, že žádost vytvořila konflikt, který se vyřešil sloučením klientských a serverových instancí dat. Odpověď obsahuje v položce stavu zdrojové i cílové adresy URL. Se sloučenými daty je dál vrácený příkaz Replace.|
|-2016345906|Z odpovědi vyplývá, že je dokončená jenom část příkazu. Jestli může být zbytek příkazu dokončený později, tak při dokončení by se MĚL vytvořit další odpovídající stavový kód žádosti o dokončení.|
|-2016345907|Zdroj by MĚL aktualizovat obsah. Odesílatel požadavku dostane informaci, že by MĚL synchronizovat obsah, aby získal aktuální verzi.|
|-2016345908|Žádost se úspěšně dokončila, ale nevrátila se žádná data. Když v cíli není obsah, vrátí se v reakci na příkaz Get kód odpovědi.|
|-2016345909|Nespolehlivá odpověď. Na žádost odpověděla jiná entita, než jaké byla určená. Odpověď se vrátí jenom tehdy, když důvěryhodný cíl vrátí na žádost kód odpovědi 200.|
|-2016345910|Přijaté ke zpracování. Žádost o vzdálené spuštění aplikace nebo o upozornění uživatele nebo aplikace se úspěšně provedla.|
|-2016345911|Požadovaná položka se přidala.|
|-2016345912|Příkaz SyncML se úspěšně dokončil.|
|-2016346011|Zadaný příkaz SyncML se provádí, ale zatím není dokončený.|

## Viz také
[Povolení přístupu k prostředkům společnosti se službou Microsoft Intune](../Topic/Enable_access_to_company_resources_with_Microsoft_Intune_-_deleted.md)

