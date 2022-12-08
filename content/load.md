---
Title: 2. laddningshastighet
Description: load.
Template: load
---

Hur är laddningshastigheten på olika hemsidor
=======================






Urval
-----------------------
De tre webbplatser jag valt att utvärdera är Clas Ohlson, Biltema och Jula. Anledningen är att de har ett liknande utbud
så tanken är att undersöka hur de beter sig i förhållande till varandra, vad skiljer dem åt och vad har de gemensamt?


Metod
-----------------------
För att göra denna undersökningen har jag använt google pagespeed och mätt sidornas laddningstid via dev-tools fliken networks.
Jag har även använt mig av google sheets för att skapa ett excel-ark där jag kunde sammanställa alla resultaten. För varje hemsida
mätte jag tre gånger per hemsida för att sedan ta ett medelvärde. Jag gjorde undersökningen på både desktop och mobilenheter. 


Resultat
-----------------------
<a href="https://www.clasohlson.com/se"><img class="flash-img" src="{{ base_url }}/../image/ch.jpg?h=300&w=500&crop-to-fit" aria-label="Bild på Clas Ohlson"></a><br>
<a href="https://www.biltema.se/"><img class="flash-img" src="{{ base_url }}/../image/bt.jpg?h=300&w=500&crop-to-fit" aria-label="Bild på Biltema"></a><br>
<a href="https://www.jula.se"><img class="flash-img" src="{{ base_url }}/../image/jula.jpg?h=300&w=500&crop-to-fit" aria-label="Bild på Jula"></a><br>

<div class="excel">
    <iframe src="https://docs.google.com/spreadsheets/d/e/2PACX-1vREcNNNnCCj_irKFcPDmjEFEhuvLZStozizftpQXOkVwABC4576FZBrD1BGeUNsOEOInzGcmtU59NeW/pubhtml?widget=true&amp;headers=false" height=250px width=585px title="myFrame"></iframe>
</div>

Den sida av de tre testade som laddades snabbast var Biltema. Den innehöll mer mängd MB än vad de övriga sidorna gjorde men bestod av färre resurser än samtliga andra.

Den sida som laddade långsammast i testet var Jula. Den innehöll betydligt fler resurser än de övriga sidorna, nästan dubbelt så många resurser
som några av de andra. 


Analys
-----------------------
En genomgående skillnad är att samtliga hemsidor laddas snabbare på desktop än vad de gör på mobila enheter. Anledningen till detta kan vara att
de mobila enheterna verkar i den här undersökningen i regel ha fler resurser på sina sidor än vad de har på desktop-sidorna. en slutsats som
man kan göra här är att om man minskar antalet resurser som webbplatsen har verkar det också som att laddningstiden går ner ordentligt. Detta blir också tydligt när man jämför alla desktop-sidorna för sig samt alla mobil-sidorna för sig. De sidor där minst antal resurer förekommer,  laddar i regel snabbare än de sidor med fler resurer. 

En annan sak som verkar som en genomgående skillnad för samtliga undersökta hemsidor är att de mobila enheterna laddar in mindre mängd (MB) än vad desktop-sidorna gör. Trots denna skillnaden så laddas desktop-sidorna alltid snabbare än vad de hade gjort på en mobilenhet. 

Enligt tabellen så har antalet resurser på en hemsida betydligt större påverkan för hur snabbt en sida ska ladda än mängden MB. Med det sagt
så kan stora bilder, eller andra media alternativ påverka laddningshastigheten då det blir många saker samtidigt som ska laddas in. Det kan även vara bra att tänka på att lägga eventuell JavaScript på hemsidorna längst ner då det kan blockera HTTP-requests, dvs bilder och annan CSS innan den har hunnit laddats klart. 

I detta testet vann Biltema med god marginal, Clas Ohlson kom på en okej andraplats och Jula kom på en avlägsen tredjeplats. 

Generellt så var det mycket som laddades in som man inte kunde visuellt se om man enbart tittade på hemsidan och inte i dev-tools, samtliga sidor laddades fram omgående ur en visuell vinkel, dvs man kunde inte för blotta ögat se någon överdriven fördröjning. Jag tycker dock att över 10 sekunder känns som en väldigt lång tid för en hemsida att behöva för att hinna ladda in allt sitt innehåll. Det är dock viktigt att nämna att samtliga sidor innehöll mycket och relativt stora bilder. Med det sagt skulle jag dra gränsen för att allt synligt bör laddas inom första eventuellt andra sekunden, därefter kan eventuella resurser eller funktioner laddas in några sekunder senare då användaren troligtvis behöver några sekunder på sig för att bestämma sig för var den vill ta vägen på sidan, därför är det dock viktigt att allt det synliga är synligt under den tiden. 



Referenser
-----------------------
clasohlson.com/se

biltema.se

jula.se

Medlemmar
-----------------------
Alexander Norrman