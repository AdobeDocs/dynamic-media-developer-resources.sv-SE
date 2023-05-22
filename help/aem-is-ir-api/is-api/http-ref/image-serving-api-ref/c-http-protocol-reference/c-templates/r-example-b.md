---
description: Liknande krav som exempel A, men använd en enfärgad bakgrund och låt höjden på den sammansatta bilden variera, så att bilder med olika proportioner får plats.
solution: Experience Manager
title: Exempel B
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90ef96fc-c12f-4fc8-b465-6520b71f4e7b
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# Exempel B{#example-b}

Liknande krav som exempel A, men använd en enfärgad bakgrund och låt höjden på den sammansatta bilden variera, så att bilder med olika proportioner får plats.

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> katalog::ID</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> katalog::Modifier</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+goes+here&amp; layer=0&amp;size=800,0&amp;extend=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp; layer=1&amp;text=rtf..$text$..rtf-encoding&amp;rotate=-90&amp;0 originN=.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

Bilden placeras i lager 0 och höjdvärdet för `size=` är inställd på 0. Den här inställningen gör att den faktiska höjden bestäms av bildens höjd efter att den skalats till 800 pixlar bred.

Variabeln `extend=` lägger till 100 pixlar i över- och underkant och 200 pixlar till höger.

Ursprunget för både lager 0 och lager 1 placeras i mitten till höger i sammansättningsområdet för att uppnå önskad textposition.

Följande bild visar det sammansatta resultatet för olika bildproportioner och olika textsträngar.

![Exempel B-bild](assets/exampleb.png)
