---
description: Ersättningsvariabeln används för att överföra värden från begärande-URL:en till FXG-mallar som lagras på servern.
solution: Experience Manager
title: Ersättningsvariabler
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 539d8863-e94d-45dc-bb8c-3db7bead0051
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---

# Ersättningsvariabler{#substitution-variables}

Ersättningsvariabeln används för att överföra värden från begärande-URL:en till FXG-mallar som lagras på servern.

` $ *``*= *`varvalue`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var  </span> </span> </p> </td> 
  <td class="stentry"> <p>Variabelnamn. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value  </span> </span> </p> </td> 
  <td class="stentry"> <p>Värdet som variabeln ska anges till (sträng). </p> </td> 
 </tr> 
</table>

* Variabeldefinitioner och referenser kan förekomma i frågedelen av begäran-URL:en.
* Variabler definieras enligt ovan, på samma sätt som andra IS-kommandon. radavståndet &#39;$&#39; identifierar kommandot som en variabeldefinition.
* Variabelnamnet `*`var`*` är skiftlägeskänsligt och kan bestå av en kombination av bokstäver, siffror, &#39;-&#39; och &#39;_&#39;.
* Viktigt värde måste vara en URL-kodad enpass för säker HTTP-överföring.
