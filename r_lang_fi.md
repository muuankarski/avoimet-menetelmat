---
title:  'Avoimet tutkimusmenetelmät yhteiskunta- ja humanistisissa tieteissä: R-kieli laskennallisen analyysin työkaluna'
author: Markus Kainu
date: Syyskuu 2013
affiliation: Turun yliopisto
tags: [r-kieli, avoin tiede]
bibliography: bibtex.bib
abstract: |
Tietotekniikan ja tietoverkkojen merkitys ihmisille kasvaa vuosi vuodelta. Yhteiskuntatieteiden näkökulmasta muutoksen voi tiivistää kahteen seikkaan: sähköisen aineiston rajuun kasvuun sekä akateemisen julkaisu- ja kustannustoiminnan murrokseen. Tässä esseessä väitän että tutkijalle murros on ennen kaikkea mahdollisuus, mutta vaatii toteutuakseen kriittisyyttä nykyisiä käytäntöjä kohtaan sekä tietoteknistä uteliaisuutta. Essee on temaattinen johdanto metodologiseen artikkeliin, jossa tulen käsittelemään datan louhintamenetelmien sovelluksia venäläisen avoimen datan sosiaalipoliittisessa analyysissä.
lang: finnish
tags: [R-kieli, avoin tiede, kvantitatiivinen tutkimus]
...

# Avoimet tutkimusmenetelmät yleisesti

<link href="http://markuskainu.fi/material/css/article.css" rel="stylesheet" type="text/css" title="compact"></link>

Uusi kappale @wiki_avoin_2013 sanoo tätä.

Keskustelu tutkimusmenetelmien avoimuudesta on ollut vähäistä yhteiskuntatieteiden ja humanististen tieteiden (YHT) piirissä. Keskeisin syy lienee se, että valtaosa YHT-tutkimuksesta on *laadullista*, jossa ei käytetä laskennallisia analyysimenetelmiä. Ajatus siitä että *diskurssianalyysin* käyttäminen velvoittaisi tiukkojen lisenssiehtojen hyväksymistä ja rahallisen maksun suorittamista on varmasti monelle vieras. Toisaalta määrällisessä tutkimuksessa analyysiohjelmistojen valintaa ovat ohjanneet muut seikat (perinteet, tuttuus) jolloin käytetyn ja opetetun analyysikielen valinnan eri ulottuvuuksia ja pitkäaikaisia vaikutuksia ei olla arvioitu. Joka tapauksessa 1) laskennallisen analyysin YHT-tieteellisten sovellusmahdollisuuksien lisääntymisen sekä 2) avointen analyysimenetelmien kehittymisen myötä on tutkimusmenetelmien avoimuus on nousemassa yhä tärkeämmäksi puheenaiheeksi.

## Avoimen koodin kehittyminen

Avoimilla tutkimusmenetelmillä tarkoitetaan laskennallisia ohjelmointikieliä, joiden on lähdekoodi on avointa ja jotka on lisensointu vapaasti. Vapaan ja avoimen lähdekoodin ohjelmistokehityksen ideana on että kuka tahansa voi muokata lähdekoodia haluamallaan tavalla sekä kopioida ja levittää sekä alkuperäistä että muokattua versiota ja käyttää ohjelmaa mihin tahansa tarkoitukseen [@wiki_avoin_2013]. 

Avointen tutkimusmenetelmien kehityksen arvioiminen on vaikeaa. Menetelmien käytön yleisyys on yksi tapa, johon paneudutaan tekstin toisessa luvussa r-kielen osalta. Avoimen koodin ympärille rakentuneet projektit ovat tulleet yhä paremmin näkyville. Kenties tunnetuin avoimeen lähdekoodin pohjautuva projekti on mobiililaitteiden *Android*-käyttöjärjestelmä, joka käyttää [linux-ydintä](http://en.wikipedia.org/wiki/Android_%28operating_system%29#Linux), on [avoimesti lisensointu](http://en.wikipedia.org/wiki/Android_%28operating_system%29#Licensing), ja josta on lyhyessä ajassa tullut [mobiilikäyttöjärjestelmien markkinajohtaja](http://en.wikipedia.org/wiki/Android_%28operating_system%29#Market_share_and_rate_of_adoption). Avoimeen lähdekoodiin perustuvat myös internet-palvelimissa suositut linux-käyttöjärjestelmät, samoin kuin niille talletettua tietoa hallinnoivat tietokantaohjelmat (MySql,MariaDB). Nopeasti yleistyvät julkaisujärjestelmät, kuten wordpress, drupal, tai joomla ovat myös suosittuja ja tavalliselle käyttäjälle tuttuja avoimen lähdekoodin projekteja. Tieteellisessä tutkimuksessa avoin lähdekoodin on ollut jo pitkään valtavirtaa. Yli [95 % maailman supertietokoneista toimii linux-käyttöjärjestelmällä](http://en.wikipedia.org/wiki/Usage_share_of_operating_systems#Supercomputers), *joku esimerkki geotieteistä* ja *esimerkki lääketieteestä*. Tilastollisen analyysin 

Yhteiskuntatieteissä kuitenkin luotetaan edelleen siihen että kaupalliset ohjelmistoratkaisut (esim. Stata,SPSS,SAS,Matlab, jne.) ovat paras tapa vastata muuttuvan yhteiskunnan ja muuttuvan yhteiskuntatieteen analyysitarpeisiin.

## Laskennallisen analyysin sovellusmahdollisuuksien lisääntyminen

Laskennallisen analyysin soveltamismahdollisuudet YHT-tutkimuksessa ovat lisääntyneet aineistojen digitalisoitumisen kautta. New York Times [@lohr_literary_2013] käsittelin keväällä artikkelissaan *Dickens, Austen and Twain, Through a Digital Lens* Matthew L Jockersin tuoretta kirjaa *Macroanalysis
Digital Methods and Literary History* [@jockers_macroanalysis_2013]. Kirjassaan Jockers analysoi vuosien 1780 - 1900 aikana 3592 englanniksi kirjoitettua novellia data-analyysiä ja tilastollisia menetelmiä yhdistelevällä metodilla paljastaen utta tietoa vaikutteiden leviämisestä sekä yksittäisten kirjailijoiden merkityksestä englantilaisen kaunokirjallisuuden historiassa.

<!--
Kirjojen digitalisointi ja kaiken kattavien kirjatietokantojen luominen on yksi esimerkki sähköisen datan mahdollisuuksista laadullisesti orientoituneella humanistisella tieteenalalla, kirjallisuudentutkimuksessa. Sähköisen datan nopea kasvu koskettaa kuitenkin likipitäen kaikkia tieteenaloja, mistä @lohr_literary_2013 kirjoittaa seuraavasti:


Data-centric specialties are growing fast, giving rise to a new vocabulary. In political science, this quantitative analysis is called political methodology. In history, there is cliometrics, which applies econometrics to history. In literature, stylometry is the study of an author’s writing style, and these days it leans heavily on computing and statistical analysis. Culturomics is the umbrella term used to describe rigorous quantitative inquiries in the social sciences and humanities. 

>Datakeskeiset tieteenalat kasvavat nopeasti vaatien uutta tieteellistä sanastoa. Politiikan tutkimuksessa määrillistä analyysiä kutsutaan politiikan metodologiaksi (political methodology). Historiassa puhutaan cliometriasta, joka soveltaa ekonometrisiä menetelmiä historian tutkimukseen. Kirjallisuustieteissä taas puhutaan *stylometriasta* (stylometry), jossa tutkimuksen kohteena on kirjailijan kirjoitustyyli ja jonka analytiikka nojaa nykyään pitkältä laskennalliseen ja tilastolliseen analyysiin. *Kulturometriasta* (culturometrics) puhutaan puolestaan sateenvarjokäsitteenä viitattaessa raskaisiin laskennallisiin menetelmiin yhteiskunta- ja humanistisissa tieteissä. 

-->

@lohr_literary_2013 jatkaa artikkelissaan tulevaisuuden visiointiaan olettaen että digitaaliset analyysimenetelmät tulevat leviämään internet-teollisuudesta ja luonnontieteistä yhä laajemmalle YHT-tutkimukseen.

> Uudet löytämisen työkalut tarjoavat tuoreen näkökulman kulttuuriin; pitkälti samaan tapaan kuin miten mikroskooppi auttoi näkemään elämän hienorakenteet ja miten teleskoopit avasivat näkymät kaukaisiin galakseihin.

Harvardin yliopiston [*Institute for Quantitative Social Science*](http://www.iq.harvard.edu/):n johtaja professori [Gary King](http://gking.harvard.edu/) korostaa artikkelissaan *Restructuring the Social Sciences: Reflections from Harvard’s Institute for Quantitative Social Science* [s. 3, @king_restructuring_2013] uuden avoimen datan merkitystä perinteiselle määrälliselle yhteiskuntatutkimukselle:

> An important driver of the change sweeping the field is the enormous quantities of highly informative data inundating almost every area we study. In the last half-century, the information base of social science research has primarily come from three sources: survey research, end of period government statistics, and one-off studies of particular people, places, or events. In the next half-century, these sources will still be used and improved, but the number and diversity of other sources of information are increasing exponentially, and are already many orders of magnitude more informative than ever before. 


Terveyden ja hyvinvoinnin laitoksen tutkimusprofessori Jussi @simpura_nakymattomien_2012 kirjottaa Tiedepolitiikka lehdessä samasta aiheesta:

>Näyttää siltä, että tietotekniikan kehittymisen seurauksena tietovarannot ovat räjähtämässä globaaliksi pilveksi ja että ketjureaktio on jo käynnissä. Se koskettaa yksittäisiä tietovarantoja ja pakottaa niitten kanssa työskenteleviä miettimään uusia toimintatapoja. Avoimen datan aalto etenee globaalin tietopilven tuntumassa. Suomessakin aalto on jo liikkeellä: vuonna 2012 avoimen datan edistämisen ja hyödyntämisen ympärillä on ollut tapahtumia lähes viikottain ja etenemisvauhti on kova. Avoimen datan pelisääntöjä rakenetaan tilanteessa, jossa avoimen datan aalto uhkaa edetä sääntelijöiden tavoittamattomiin. Tällä kaikella alkaa olla kiire, ja tiedemaailmankin on pysyttävä aallon harjalla.


...Tilastollisen tutkimuksen käsitettä käytetään suomen kielessä usein melko laveasti. Tässä tekstissä puhutaan laskennallisesta analyysistä, joka nähdään koostuvan yhtäältä tietojenkäsittelytieteellisestä data-analyysistä että toisaalta tilastotieteellisestä data-analyysistä. Määrällisen tutkimusprosessin työmäärästä usein vain pieni osa on varsinaista tilastotieteellistä analyysiä ja suurin osa työstä kuluu datan keräämiseen sekä muokkaamiseen.

Matthew L. Jonckers

---

@manovich_software_2013 [p. 22-23] sanoo että 


**Tässä esseessä** käsittelen avointa sähköistä dataa yhteiskuntatieteellisen tutkimuksen näkökulmasta. Avoin data tai *big data* tarkoittaa tässä yhteydessä verrattain uutta sähköiseen muotoon kertyvää dataa, jota ei kerätä jotain tiettyä tutkimuskysymystä silmällä pitäen, vaan data ikäänkuin *kertyy* esimerkiksi dokumentaation tai teknisen sovelluksen keräämänä. Tyypillisinä esimerkkeinä aineistoista voidaan pitää mm. *sosiaalista mediaa* [esim. @king_how_2012], *vaalidataa* [esim. @louhos_2013], *poliittisen päätöksenteon dataa* [esim. @hetherington_how_2012] tai vaikkapa *rikollisuuteen ja oikeuslaitoksen toimintaan liittyvää dataa* [esim. @lipsky_racial_2012]. Kaikille näille tutkimuksille yhteistä on avoiminen tietovirtojen tietotekninen hyödyntäminen tieteenalan perinteisiin tutkimuskysymyksiin vastaamiseksi.



**Suomalainen määrällinen yhteiskuntatutkimus** on edelleen vahvasti kiinni Kingin mainitsemissa *menneen puolivuosisadan* aineistoissa sekä menetelmissä. Menetelmällinen kehitys, sikäli kun sitä on ollut, on painottunut uusien *tilastollisten* menetelmien soveltamiseen aineistojen ja tutkimuskysymysten pysyttyä pitkälti ennallaan. Aineistojen osalta **viranomaisrekistereitä** on saatu tutkittavaksi yhä enemmän. Rekisteriaineistotutkimus on menetelmällisesti hyvin erityinen tutkimusala, jolla ei ole sovelluksia juuri pohjoismaita kauemmaksi.

Uudet sähköiset aineistot eivät ole ainoa syy päivittää teoreettista ja menetelmällistä osaamista. Etenkin survey-aineistojen käyttöä uhkaa yhtäältä resurssien väheneminen ja toisaalta ihmisten vähenevä osallistumisinto. Säästöpaineiden alla laajojen survey-aineistojen on uhattuna, etenkin kun uusien kyselytutkimusten vastausprosentit ovat tasolla, joka herättää kysymyksiä tulosten yleistämisestä ja siten koko tutkimusmenetelmän käyttökelpoisuudesta tulevaisuudessa.

**Siirtyminen tulevan puolivuosisadan** aineistojen hyödyntämiseen tulee olemaan kivinen tie. Se edellyttää merkittävää paradigma-tason muutosta läpi tieteenalan. Käytännössä muutos edellyttää tietotekniikan hyödyntämisen nostamista aivan uudelle tasolle. Menneen ajan aineistojen analysointiin on voinut hankkia yksityiseltä yritykseltä sovelluksen (esim. SPSS, Stata, SAS, jne.), jonka avulla kriteerit täyttävän mallin on voinut suorittaa. Nykyään tieteelliselle tutkimukselle relevantit uudet aineistot ja uudet analyysimenetelmät kehittyvät niin nopeasti, etteivät kaupalliset tuotteet edes yritä pysyä kehityksessä mukana, vaan keskittyvät palvelemaan yrityksiä joskin osin samoissa ison datan haasteissa.

Tieteellisten ohjelmistojen kehitys onkin siirtynyt yhä enemmän tiedeyhteisön varaan ja kehitystyöhön osallistumisesta tullut myös yksi keskeinen akateemisen meritoitumisen muoto. Viime vuosina yhdysvaltalaisten huippuyliopistojen professorirekrytoinneissa on toistuvasti painotettu aktiivisuutta avoimen koodin analyysiohjelmistojen kehitysyhteisöissä. 

Meritoitumisen näkökulmasta uudet aineistot ja menetelmien kehittäminen ovat kiinnostavia myös ns. tietovirtojen *ohjaamisen* kannalta. Tietovirroilla voidaan tarkoittaa esimerkiksi Venäjän tilastoviranomaisen Rosstatin jatkuvasti julkaisevaa uutta tilastotietoa tai vaikkapa Twitteriä. Mikäli tutkija onnistuu kehittämään nokkelan tavan hyödyntää tätä tietovirtaa ja jakaa menetelmänsä avoimesti tiedeyhteisön kesken, siirtyvät tutkijat helposti käyttämään tätä menetelmää päästäkseen käsiksi ko. tietoihin. Tietovirtojen kanavoinnista on tulossa myös yksi yliopistojen vetovoimaisuutta lisäävä tekijä. Sama logiikka on [R-kielen](http://www.r-project.org/) suosion  [nopean kasvun takana](http://r4stats.com/articles/popularity/). R:n suosiosta kertoo paljon myös se, että parhaillaan [Courserassa](https://www.coursera.org/) käynnissä olevalle *Computing for Data Analysis*-kursille oli ilmoittautunut yli 40 000 opiskelijaa.

**Internetissä jaetun datan** lisääntyminen ja kiinnostus sen hyödyntämiseen ovat yksi syy akateemisen julkaisutoiminnan ympärillä tapahtuneeseen liikehdintään. Avoimen tiedon helppo saatavuus on herättänyt kysymyksen siitä, miksi tutkijat eivät voisi yhtä lailla jakaa omia tutkimustuloksiaan avoimesti ilman tai minimaalisin välikäsin. *Elsevier*-kustannustalon liiketoimintamallin kritisoinnista lähtenyt  [Academic Spring](http://en.wikipedia.org/wiki/Academic_Spring)-liike on kuluneen vuoden aikana yhdistänyt laajasti eri maiden tutkijayhteisöjä kyseenalaistamaan nykyistä akateemista julkaisumallia (ks. [*Cost of knowledge*](http://thecostofknowledge.com/)). Kritiikin kärki kohdistuu siihen, että isot kustantamot myyvät kovaan hintaan takaisin yliopistoille tutkijoiden veronmaksajien rahoilla tekemiä julkaisuja ja samalla pidättävät tekijänoikeudet itsellään rajoittaen tutkijoiden mahdollisuuksia jakaa omia tuloksiaan vapaasti netissä. Liikehdintä sai alkunsa matemaatikko Timothy Gowersin [blogissaan julkaisemasta tekstistä](http://gowers.wordpress.com/2012/01/21/elsevier-my-part-in-its-downfall/). Blogin kommenteissa eräs lukija nasevasti tiivisti järjestelmän epäkohdat:

> It is utterly absurd that we still have publishers — we write for free (because we want our work read or known), we edit or referee for free and then pay large amounts of money to buy the work back. With the advent of the Web, authors should have eliminated publishers.

**Perinteinen akateeminen** julkaisumalli on monella tapaa jos ei tiensä päässä. Toiminnan liiketaloudellinen kannattavuus on monella tapaa uhattuna. Tutkimusjulkaisujen kysyntää siirtyy paperille painetusta sähköisiin dokumentteihin, joiden tuotannossa ei enää tarvita samanlaisia isoja pääomia kuin mitä esim. paperikirjojen. Uudet laitteet (tietokoneet, tabletit, älypuhelimet) yleistyvät nopeasti ja ovat osoittautuneet melko hyviksi artikkelikasojen korvaajiksi. Samalla myös kiinnostus [open access -lehdet](http://en.wikipedia.org/wiki/Open-access_journal) lehtiä kohtaan on lisääntynyt, olkookin että niiden arvo on vielä kaukana arvostettujen perinteisten lehtien tasosta. Kun taas ajatellaan kirjoja niin kustannustaloilla on vielä myös niiden *nimi* tai *maine*, jonka houkuttelemana ne säilyttävät asemansa vielä pitkään. Siitäkin huolimatta, että teknologinen kehitys on jo mitätöinyt kaikki muut kustantajien perinteiset vahvuudet. 

Määrällisen tutkimuksen näkökulmasta sähköinen julkaiseminen on noussut yhä kiinnostavammaksi ns. vuorovaikutteisen grafiikan kehittymisen myötä. Grafiikan lisäksi on mahdollista luoda myös laskennallisia analyysiympäristöjä raporttien lomaan, joita voi käyttää suoraan selaimesta käsin. Varsinaisiin julkaisuihin vuorovaikutteisella grafiikalla tai virtuaalisilla laskentaympäristöillä on vielä matkaa, mutta erilaisissa *harmaissa julkaisuissa* ja itse tutkimusprosessissa ne tulevat olemaan hyödyksi jo lähitulevaisuudessa.

<!--
**Tekniset edellytykset** avoimelle sähköiselle julkaisemiselle ovat jokaisen tutkijan käytettävissä ilman taloudellisia kustannuksia. Tämä essee on kirjoitettu käyttäen [Markdown](http://daringfireball.net/projects/markdown/)-merkintäkieltä, josta se on käännetty Berkeleyn yliopiston filosofian professorin [John MacFarlanen](http://johnmacfarlane.net/) kehittämän  [pandoc](http://johnmacfarlane.net/pandoc/):n avulla niin [nettisivuksi](http://research.muuankarski.org/kevatsemma/essee.html), [sähköiseksi kirjaksi](http://research.muuankarski.org/kevatsemma/essee.epub), [.pdf-muotoon](http://research.muuankarski.org/kevatsemma/essee.pdf) kuin toimisto-ohjelmien formaatteihin [LibreOfficelle](http://research.muuankarski.org/kevatsemma/essee.odt) ja [MS Wordille](http://research.muuankarski.org/kevatsemma/essee.docx). Onkin kiinnostavaa seurata pystyvätkö isot kustantajat säilyttämään asemansa uusissa olosuhteissa ja kilpailutilanteessa. Jos jokin on varmaa, niin se ettei pienen tiedekustantamon perustaminen ole koskaan aiemmin ollut yhtä helppoa ja ajankohtaista.
-->

**Uusien teknologisten sovellusten** ohella sähköistä julkaisumuotoa puoltavat myös etenkin laskennallisten tieteiden kohtaamat vaatimukset analyysien *toistettavuudesta* [ks. esim. @peng_reproducible_2011]. Toistettavuudella tarkoitetaan datan ja analyysialgoritmien avointa julkaisemista siten, että lukijan on mahdollista arvioida analyysin pätevyyttä ja johtopäätöksiä. Toistettavuudesta on alettu puhua enemmän myös yhteiskuntatieteellisen tutkimuksen parissa kun samojen isojen kansainvälisten tutkimusaineistojen parissa työskentelee tuhansia tutkijoita, joiden tutkimustulokset ja johtopäätökset ovat usein ristiriitaisia. 

**Palaan vielä johdannossa** viittaamaani New York Times artikkeliin laskennallisista tutkimusmenetelmistä kirjallisuudentutkimuksessa [@lohr_literary_2013]. Artikkelissa pohdittiin paljon myös sitä, tarkoittaako *määrän* lisääntyminen laadullisen tutkimuksen aseman heikentymistä. Professori Jonckerin mukaan oikeiden tutkimuskysymysten löytäminen ja analyysin virheiden näkeminen edellyttävät syvää perehtyneisyyttä tieteenalaan yhä edelleen. 

> Quantitative tools in the humanities and the social sciences, as in other fields, are most powerful when they are controlled by an intelligent human. Experts with deep knowledge of a subject are needed to ask the right questions and to recognize the shortcomings of statistical models.

> "You'll always need both," says Mr. Jockers, the literary quant. “But we’re at a moment now when there is much greater acceptance of these methods than in the past. There will come a time when this kind of analysis is just part of the tool kit in the humanities, as in every other discipline.” 

Yksittäisen tutkijan on vaikea vastata tähän haasteeseen ja määrällisen analyysin yleistyminen tuleekin vaatimaan kaikilla tieteenaloilla uudenlaista yhteistyötä tutkijoiden ja tieteenalojen kesken. Gary Kingin [s 3., @king_restructuring_2013] mukaan myös Yhdysvalloissa yhteiskuntatieteiden tutkijat ovat jo siirtymässä tutkijankammioista yhteistyöhön kannustaviin, laboratorio-tyyppisiin monitieteisiin tutkimusryhmiin. Laajan sähköisen datan analysointi edellyttää tietoa ja osaamista, jota ei löydy miltään yhteiskuntatieteiden perinteiseltä tieteenalalta.

> Through collaboration across fields, however, we can begin to address the interdisciplinary substantive knowledge needed, along with the engineering, computational, ethical, and informatics challenges before us. [s 3., @king_restructuring_2013]

Uusi digitaalinen data myös hämärtää yhteiskuntatieteissä perinteistä jakoa laadullisiin ja määrällisiin tutkimusotteisiin. Gary King [s 4., @king_restructuring_2013] ennustaa molempien tutkimussuuntien yhdistyvän yhdeksi yhteiskuntatieteeksi, jossa samoja ongelmia ratkotaan yhteistyössä.

> Instead of quantitative researchers trying to build fully automated methods and qualitative researchers trying to make due with traditional human-only methods, both now are heading toward, using, or developing computer-assisted methods that empower both groups. This development has the potential to end the divide, to get us working together to solve common problems, and to greatly strengthen the research output of social science as a whole.

Tällainen lähetyminen on ainakin suomalaisessa yhteiskuntatieteessä vielä utopistinen visio. Sähköisen datan yhteiskunnallisen hyödyntämisen kenties kiinnostavin avaus on Aalto-yliopiston ja Helsingin yliopiston tietojenkäsittelytieteen jatko-opiskelijoiden perustama [Louhos-projekti](http://louhos.github.com/). Hyvin kuvaavaa on se, ettei tässä projektissa ole lainkaan yhteiskuntatieteilijöitä, ei määrällisesti tai laadullisesti orientoituneita.

**Venäjän ja Itä-Euroopan** yhteiskuntatieteellisen tutkimuksen näkökulmasta uudet avoimet aineistot ja menetelmät ovat erityisen ajankohtaisia. Venäjällä viralliset tilastot ovat olleet avoimia vasta muutaman vuoden ajan ja tekniset ratkaisut datan avaamiselle ovat edelleen hyvin takapajuisia. Voidaankin sanoa että jo *menneen puolivuosisadan* aineistojen tehokas käyttö  edellyttää Venäjän kohdalla verrattain hyviä *tulevan puolivuosisadan* menetelmien osaamista. 

Samaan aikaan internetin merkitys kaikessa yhteiskunnallisessa näyttää voimistuvan. Sosiaalisen median rooli yhteiskunnallisen keskustelun ja jopa mobilisaation kanavana näyttää voimistuvan kaikkialla entisen Neuvostoliiton alueella. Ja yhteiskunnan tutkijan tulee tietysti olla paikalla siellä, missä yhteiskuntaa tehdään.



# Mikä on R? - Synty ja ominaispiirteet

>R has already won praise and plaudits from established media outlets such as the New York Times, Forbes, Intelligent Enterprise, InfoWorld and The Register. When you consider that R is a high-level computer programming language designed mostly for quants (the nickname for a subspecies of geeks who focus on quantitative analysis), the adoring media attention seems nothing short of astounding.

Joka tapauksessa @smith_r_2010 [s.23] kirjoittaa että paska on aina paskaa.

## Synty


- R-language was iniated by two 
- open source

## R-kieli ohjelmointikielenä
- object oriented, s-language bell laboratories
(G)UI's, IDE Rstudio, 
- contributed packages

## R-kieli tilastollisen laskennan työkaluna
- structure
- visual
- open source, community, licensing, teaching

## R-kielen suosio
- enterprise level services

# Miten R on mahdollinen? -  R-projekti

## Projektin organisaatio
- development vs. user help

## Kielen kehitys

## Käyttäjätuki
- mailing lists - general vs. special interest groups
blogs
- q & a sites

## Kontribuoidut paketit
- CRAN - task views
R-forge
- Github
- bioconductor

# Mihin R-kieltä käytetään? - R käytännön työssä
Why R-language is popular

## Tilastollisten menetelmien kehitys
- new methods implemented first in R

## Soveltava tilastotiede

### Bio/geo-tieteet
- Geograhical Information Systems

### Yhteiskuntatieteet

### Humanistiset tieteet - ihmiskielten analyysi

## Yritysanalytiikka
- insurance, big data, banking, industry
- social media: facebook, google, twitter

## Datajournalismi
- Guardian, New York Times, Chicago Herald Tribune

# Miten  R toimii käytännössä? - Yhteiskuntatieteellisten aineistojen analyysi R-kielellä.

## Sanapilvet

## Verkostokartat

## Spatiaalinen visualisointi

## Klusterointi

- insurance, big data, banking, industry
- social media: facebook, google, twitter

# Kirjallisuus

