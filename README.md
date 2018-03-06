# CryptoInvoice





<hr />
Octopus engine contribution:<br />
2016 - python + raspberry - simple crypto machine (communication with blockchain)<br />
https://github.com/octopusengine/cryptomat<br />
<br />
2017 - python - linux - private keys (BTC/LTC/VTC) QR code, wallet derivation, PK and picture noise<br />
https://github.com/octopusengine/virtualcoin<br />
<br />
2018 - php testing - QR / blockchain.. etc<br />
http://www.octopusengine.org/crypto/<br />
<br />
<hr />
PP projekt<br />
https://github.com/Learn-by-doing/crypto-terminal <br />


<hr />
<b>Zde je pouze raw-view zadáníCZ.doc k 28.2.2018</b><br />
CRYPTOINVOICE<br />

Cílem je vytvořit open source software pod MIT licencí, který bude sloužit osobám, které v rámci své podnikatelské nebo jiné činnosti chtějí přijímat kryptoměny, aniž by je potřebovali směnit do FIATu (dále jen „Uživatel“).
Paralelní Polis má zájem na vlastním HW zajistit provoz serveru, prostřednictvím kterého by Uživatelé měli možnost vytvořený SW využívat. Uživatelé by tedy měli možnost využívat předmětný SW jak na serveru Paralelní Polis (bez rozsáhlých technických znalostí za symbolický nebo žádný poplatek), tak i na vlastním serveru.<br />
ZÁKLADNÍ FUNKCE<br />
Základní funkce, které by předmětný SW měl splňovat:<br />
1) Účet Uživatele<br />
Uživatel si může vytvořit vlastní účet, prostřednictvím kterého bude odesílat žádosti o platby svým zákazníkům. V rámci účtu Uživatele jsou poskytovány zejména následující údaje:<br />
emailová adresa Uživatele,
identifikátor, prostřednictvím kterého jsou generovány adresy (např. xpub), resp. konkrétní adresy, na které má Uživatel zájem přijímat platby v kryptoměnách,
další volitelné údaje, jako např. název Uživatele a jeho identifikační údaje.<br />
2) Vytvoření žádosti o platbu částky ve FIAT měně prostřednictvím kryptoměn.
Při vytvoření žádosti o platbu Uživatel uvádí zejména následující údaje:
popis fakturované činnosti (předmět a volitelný bližší popis),
částka stanovená ve FIAT měně (základ v CZK, alternativně v EUR),
volba mezi fixací kurzů k okamžiku vystavení žádosti o platbu nebo k okamžiku platby osobou, které je žádost o platbu zasílána (dále jen „Plátce“),
variabilní symbol pro spárování s odpovídající fakturou, kterou Uživatel vytváří samostatně ve svém fakturačním systému,
emailovou adresu Plátce,
mimo uvedené údaje dále Uživatel může v UI vložit fakturu v pdf, tj. daňový doklad, který má být platbou v kryptoměně uhrazen.<br />
3) Realizace platby dle obdržené žádosti.<br />
Plátce na svůj email (který Uživatel uvedl při vytváření žádosti) obdrží žádost o platbu dle následujícího:
email s žádostí o platbu, který uvede název odesílajícího Uživatele, předmět fakturace, fakturovanou částku ve FIAT měně a variabilní symbol platby,
v příloze emailu bude daňový doklad, faktura, kterou Uživatel vložil při vytváření žádosti,
v emailu bude odkaz na provedení platby, který Plátce přesměruje na odpovídající server,
webová stránka k provedení platby bude obsahovat volbu způsobu platby mezi BTC, XMR a LTC,
po výběru kryptoměny bude na stránce vygenerován QR kód obsahující informace o placené částce (ve zvolené kryptoměně) a adrese, na kterou má být částka zaslána (tyto údaje budou uvedeny i samostatně mimo QR kód, aby je Plátce mohl manuálně zkopírovat),
vygenerované platební informace včetně kurzu budou zafixovány na dobu 15 minut, a to dle fakturované částky ve FIAT měně; po uplynutí této doby se objeví informace o nutnosti opětovně provést platbu (tj. opětovně otevřít emailem zaslaný odkaz); do 15 minut musí být transakce odeslána do sítě (nikoliv zapsána v blockchainu),
zvolil-li Uživatel při tvoření platby fixaci kurzu k okamžiku vytvoření žádosti o platbu, předchozí bod se neuplatní a Plátce na předmětné webové stránce vidí po celou dobu částku odpovídající předem zafixovanému kurzu,
po přijetí platby předmětná webová stránka zobrazí informaci o tom, že platba byla provedena v časovém limitu 15 minut; v návaznosti na uvedené bude Uživateli i Plátci doručen email s informací o provedení platby obsahující zejména informace o uhrazené částce v kryptoměně, odkazu na předmětnou transakci v některém z blockchain explorerů a návaznost na realizovanou žádost o platbu,
po získání konfirmace platby, tj. jejího zahrnutí v blockchainu bude Plátci zaslán email informující Plátce o tom, že jeho platba dle předmětné žádosti o platbu byla řádně uhrazena, v kopii emailu bude Uživatel. Toto potvrzení by mělo splnit požadavky na dokumentaci předmětné transakce pro účetní účely (tj. mělo by např. uvádět odkaz na fakturu, částku ve FIAT i v dané kryptoměně a odkaz na transakci do blockchainu a odpovídajícího bloku).<br />
VOLITELNÉ FUNKCE<br />
Volitelné funkce, které by řešení dále obohatily:<br />
možnost opakovaného a automatického vystavování žádostí o platbu (např. při pravidelných měsíčních platbách)
využití lightning network pro opakované platby
PGP šifrovaná emailová komunikace mezi Uživatelem, serverem a Plátcem<br />
TECHNICKÉ POŽADAVKY<br />
Technické požadavky, které by mělo řešení splňovat:<br />
<hr />
Octopus EDIT:<br />
Server - Client<br />
PHP? Linux - cron - JS - AJAX - JSON blockchain transaction parser - ...






