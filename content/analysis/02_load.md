---
Title: Analysis 02
Description: Analysis 02 - Loadtime
Template: analysis
---

<div class="kmom-sidenav">
    <p><a href="01_colors"><i class="fas fa-dice-one"></i> Colors</a></p>
    <p><a href="02_load"><i class="fas fa-dice-two"></i> Load</a></p>
    <p><a href="03_design_principles"><i class="fas fa-dice-three"></i> Design Principles</a></p>
</div>     

Loadtime
===========

Tre Webbplatser ska analyseras.
Jag har valt att fokusera på de tre webbplatserna; 
> **[SJ.se](https://www.sj.se/#/)**    
> **[NRK.no](https://www.nrk.no/)**    
> **[DBA.dk](https://www.dba.dk/)**     


Urval av webbsidor
=====================

Tre webbsidor som är väldigt välbesökta har valts, men selektionen begränsades medvetet till att inkludera tre så skilda verksamhetskategorier som möjligt. Anledningen till att sprida kategorierna var för skribenten att få en så god överblick som möjligt över representativa exempel från de olika kategorierna "Transport", "Media" och "Shopping".      

I urvalet finns SJ.se först på listan.      
Det statligt ägda Aktiebolaget SJ (inte att förväxla med det statliga *verket* "Statens Järnvägar") med sina dotterbolag, bedriver persontågsverksamhet. I miljömedvetna tider, när människor försöker så gott en kan att minska sitt koldioxidutsläpp, har SJ.se valt att profilera sig som det mest miljömedvetna valet. Detta är ett väl underbyggt val, då tågresor bevisligen i idealfallet släpper ut långt mindre mängd koldioxid, sett till antal förflyttade passagerare, jämfört med exempelvis förbränningsmotordrivna bilar eller flygplan, för samma mängd passagerare.      
SJ är på sin hemsida och även andra medier väldigt tydliga med att de planerar bygga ut och förbättra Sveriges järnvägsnät inom kommande år, samt att de planerar bygga s.k. höghastighetståg, vilka kommer kunna halvera restiden mellan de tre till populationen största städerna i Sverige.      
I media har ovan nämnda faktum varit en brännande fråga på sistone, vilket också gjort att intresset väckts att utvärdera SJ's hemsida och tjänster.     

På listan av utvalda hemsidor finnes även NRK.no, som på nätet representerar 'Norges Rikskringkastning', Norges Public service- Radio och Television. Verksamheten är av Norge Statligt Finansierad och stödjs även av TV- licens, liksom dess Svenska motsvarighet, SVT (Sveriges Television, svt.se).       
Sidan nrk.no visar nyheter och medier såsom streamade filmer, tv-program, ljudklipp och radio, såväl som skrivna nyhetsartiklar, krönikor, debattinlägg, underhållning och sport, allt i enlighet med dess statliga public service- uppdrag.      
Hemsidan nrk.no valdes då mediakategorin behövde en representant, och det föreföll något mindre troligt (enligt skribentens högst subjektiva övertygelse) att sidan redan skulle ha blivit analyserad av någon annan student/analytiker vid kursen. Det var åtminstone skribentens förhoppning.       

Sist på listan, i kategorin "Shopping", finner vi dba.dk, en sida för att lägga ut annonser och köpa/sälja begagnade saker. Den svenska motsvarigheten heter blocket.se och har troligtvis redan recenserats av andra elever, varför valet föll på denna, en av Danmarks mest välbesökta webbplatser (37:e plats på https://www.alexa.com/topsites/countries/DK).
Dba.dk har som ovan nämnt, väldigt många besökare, vilket gör det intressant at utvärdera sidans prestanda, såväl som dess tillgänglighet. 


Metod
========

Det verktyg som främst använts för att insamla mätvärden över webbsidorna i analysen har varit Google Lighthouse (https://developers.google.com/web/tools/lighthouse), ett webbläsarinstick specifikt skapat för Googles Chrome- webbläsare.      
I verktyget kan man göra utvärderingar över den valda hemsidans Prestanda (Performance), Tillgänglighet (Accessibility), Bästa Praxis  (Best Practices), samt Sökmotoroptimering (SEO).     
När en utvärdering över hemsidan utförts tillhandahåller Lighthouse en utförlig rapport av data, vilket i ett selektivt urval kommer presenteras i närmare analys och förklaring, såväl i ett Excel- ark med informationen, såsom en genomgripande text.
För att få en rättvis bedömning görs utvärderingen på tre undersidor för varje vald hemsida, tre gånger vardera. Ett medelvärde från de tre mätningarna tas ut och presenteras.
För att få en snabb överblick har skärmbilder av de olika sidorna tagits med. 
De förbättringar som analysen visat kan göras för hemsidornas prestanda nämns och följs därpå av en rangordning av de olika hemsidornas mätvärden.


Utvärderingsdata
============================
I detta **[Kalkylark](https://docs.google.com/spreadsheets/d/1-mT7wwDFTBl7LbKIZsYxx2FiojuGesvlSK5iJalDNB8/edit?usp=sharing)** finns data över de tre webbsidornas laddninstid, antal inlästa resurser, deras sammanlagda storlek och även sidans totala storlek i KiB. De gulfärgade kolumnerna representerar värden för när sidan laddas för mobila enheter och de vita kolumnerna är för PC. Alla numeriska värden är medelvärden ifrån tre separata mätningar, som adderats och sedan delats med tre (antalet mätningar).    
Mätningarna utfördes under samma dygn, en mätning för vardera sida på morgonen (mellan 07.00 och 08.00), en mätning vid lunchtid (mellan 12.30 och 13.30), samt en mätning vid kvällstid (mellan 17.00 och 18.00). Att sprida ut mätningarnas tidsspann anses av skribenten ge ett rättvist resultat över sidornas laddningshastighet under olika tiders serverbelastning.     


**[SJ.se](https://www.sj.se/#/)**
========
![SJ Screenshot](../assets/img/loadtime/sj_screenshot.png)

SJ.se laddar in i runda slängar 50 olika resurser till startsidan. Det tar ungefär 4 sekunder att ladda sidan, och klickar man runt lite grand blir man snart varse att lång laddningstid är ett återkommande mönster för samtliga undersidor. Det tar helt enkelt en stund att ladda in de dryga tretusen Kilobyte som index-sidan väger.     
Värt att lägga märke till är att den mobilanpassade indexsidan faktiskt är större än den för PC! Detta märks också på resultatet i kolumnen "Time to interactive (Mobile)", där SJ.se tar hela 22.9 sekunder att ladda in! Den mobila versionen av sidan slår faktiskt rekord i längst "blocking time" (i genomsnitt 7340ms), alltså tiden mellan att första texten eller bilden ritas på skärmen tills sidan är helt och hållet interaktiv.    

Sidan läser in en hel del javascript som (JS) inte används, vilket om det togs bort hade sparat ca 1.12 sekunder i laddningstid.
Att minimera storleken på JS- paketen och eventuellt dela upp dem, hade enligt Google Lighthouse kunnat spara upp mot 3.7 sekunder laddningstid för PC, vilket hade förbättrat upplevelsen avsevärt.
Sånär som på en rätt så stor header-bild (103 KiB) är det i princip enbart JS som saktar ner inläsningen av sidan. Google Lighthouse rekommenderar att korta ner och undvika stora inlästa tredjeparts- JS som inte verkar fylla någon funktion för sidan.    

De undersidor som testas ger liknande resultat, med väldigt lång laddningstid (runt 15-20 sekunder) för mobilanpassade sidan, runt 50- talet resurser inladdade och en knappt märkbar skillnad i mobilanpassade sidans storlek, jämfört med den som läses in på PC.

Helhetsbetyget för SJ.se's indexsida (på PC) gällande prestanda hamnar på ett genomsnitt på 49 av 100. För de två övriga testade undersidorna på samma domän ligger helhetsbetyget runt 50 av 100.    
Inte speciellt bra betyg, med andra ord.


**[NRK.no](https://www.nrk.no/)**
============
![NRK Screenshot](../assets/img/loadtime/nrk_screenshot.png)

Nrk.no verkar ha satsat något mer på sidans prestanda än både SJ.se och DBA.dk. Sidan laddas in på 1 sekund blankt på PC, trots att den använder i genomsnitt 136 inlästa resurser, däribland javascript. Total Blocking Time kan inte bantas ner mer, då den ligger på 0ms.
Det något höga antalet inlästa resurser borde te sig problematiskt i mobil- läge, men någon överdrivet lång laddningstid finner vi inte ens där. Knappa 2.8 sekunder för första ritningen och visst, 8.9 sekunder får man vänta på en fullt interaktiv sida på mobilen, men i jämförelse med övriga analyserade sidor är det *"snabbare än tåget"* (pun intended).     

i förbättringsväg finns det inte överdrivet mycket att hämta för PC, annat än att en del bilder har s.k. no-cache-policy, vilket om det togs bort, skulle möjliggöra snabbare inläsning av sidan för återkommande besökare, då en del av bilderna redan lagrats i cache.    
För Mobilanpassade sidan skulle nrk.no kunna använda sig av en effektivare cachelagringspolicy och skjuta upp inläsningen av bilder som inte visas på skärmen. Dessa åtgärder hade sparat ca 3.7 sekunder, enligt mina beräkningar.

Helhetsbetyget för NRK.no's indexsida (på PC) gällande prestanda hamnar på ett genomsnitt på 98 av 100. För de två övriga testade undersidorna på samma domän ligger helhetsbetyget runt 95 av 100.


**[DBA.dk](https://www.dba.dk/)**
============
![DBA Screenshot](../assets/img/loadtime/dba_screenshot.png)

DBA.dk används av tusentals danskar varje dag för att köpa och sälja begagnade saker. Sidan har funnits sedan 1995 och har fler än 1.9 miljoner unika besökare i månaden, enligt dem själva.      
Indexsidan laddas in efter 3.1 sekunder på PC, vilket i det avseendet ger den längst laddningstid av alla tre analyserade domäner. Detta stämmer även för "first contentful paint"(Både PC och mobilt), "time to interactive" och det slutgiltiga helhetsbetyget. Siffrorna talar för sig själv; den här sajten tar tid att ladda in.
Endast "kontakt"- sidan ger ett bra utfall, då den inte läser in mer än 22 requests, och undersidan enbart ligger på runt 400 KiB. Då "kontakt"- undersidan inte ens innehåller ett kontaktformulär, utan endast maillänkar och telefonnummer är det inte så konstigt att det går snabbt där. 

Att snabba upp laddningstiden för DBA.dk bör inte vara omöjligt.     
Till att börja med ligger det kvar en hel del JavaScript som inte används av sidan. att ta bort och effektivisera detta hade inneburit ca 0.6 sekunder snabbare laddning av sidan.     
Sidan har en del bilder i .png- format. Som exempel kan nämnas en "login_expanded.png" som är 21 KiB stor. Att göra om filen till ett modernare bildformat (JPEG 2000, XR eller WebP, för att nämna några) hade besparat ca 16 KiB för användaren att ladda in. 

En hel del tredjepartskod läses in, vilket orsakar en "Blocking Time" på ca 500 ms. Att begränsa överflödig tredjepartskod på sidan eller att välja att ladda in den först när huvudinnehållet laddats in, hade minskat användarens väntetid med ungefär en tiondel, vilket i sammanhanget kan vara väldigt användbart.

Den stora flaskhalsen för DBA.dk verkar dock vara ovan nämnda JavaScript. att banta ner koden och undvika att låta merparten av koden gå genom "main thread" (se [guide här](https://developers.google.com/web/tools/chrome-devtools/speed/get-started#main)), hade besparat massvis med tid.

Helhetsbetyget för DBA.dk landar på 43 av 100. Undersidorna som inte är "kontakt"- sidan visar mer eller mindre gemensamt runt 10 av 100.
Prestandamässigt hamnar DBA.dk på sista plats i analysens lista.



Ranking
==========
![ranking](https://i.imgflip.com/4qnszd.jpg)

Överst på prispallen hamnar NRK.no, med sina näst intill perfekta resultat över mätningarna på PC. Då det fortfarande finns utrymme för förbättring mobilt hamnar den bara överst med en hårsmån i det avseendet, men är ändock en klar vinnare i det stora hela.      
På andra plats finner vi SJ.se, som sammanfattningsvis kan sägas ha ett acceptabelt resultat vad gäller prestanda, men inte mycket mer.
På tredje och sista plats, av förklarliga anledningar och förståeliga skäl, finner vi DBA.dk, vars sida slår flest rekord i långsam laddning. Inte nödvändigtvis någonting att vara nöjd över, men någon ska ju hamna sist och i det här fallet blev det DBA.dk.     

Gemensamt för de tre webbsidorna som analyserats är att de alla kan dra nytta av att effektivisera JavaScript- inläsningen, då den kräver en del bandbredd och processorkraft.     

Den generella smärtgränsen på ca 5 sekunder överstigs av samtliga sidor när det kommer till mobilt användande, vilket är synd, men ingen katastrof, då merparten av mobilanvändare inte förväntar sig samma hastigheter som en persondator kan generera.

Laddningstiden för DBA.dk ligger dock på gränsen till för långsam även på PC, vilket försämrar upplevelsen och gör användaren otålig.



Skrivet av:
==========
Joacim Holm