---
description: Liknande krav som exempel A, men använd en enfärgad bakgrund och låt höjden på den sammansatta bilden variera, så att bilder med olika proportioner får plats.
seo-description: Liknande krav som exempel A, men använd en enfärgad bakgrund och låt höjden på den sammansatta bilden variera, så att bilder med olika proportioner får plats.
seo-title: Exempel B
solution: Experience Manager
title: Exempel B
topic: Scene7 Image Serving - Image Rendering API
uuid: 13120562-9201-4733-bd9d-4a54eac913e9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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

Bilden placeras i lager 0 och höjdvärdet för `size=` är 0, vilket gör att den faktiska höjden bestäms av höjden på bilden när den skalats till 800 pixlar bred.

`extend=` lägger till 100 pixlar i över- och underkant och 200 pixlar till höger.

Ursprunget för både lager 0 och lager 1 placeras i mitten till höger i sammansättningsområdet för att uppnå önskad textposition.

Följande bild visar det sammansatta resultatet för olika bildproportioner och olika textsträngar.

![](assets/exampleb.png)

