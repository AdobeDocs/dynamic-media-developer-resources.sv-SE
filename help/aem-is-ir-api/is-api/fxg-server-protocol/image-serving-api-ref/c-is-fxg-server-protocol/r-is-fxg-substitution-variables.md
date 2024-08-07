---
description: Ersättningsvariabeln används för att överföra värden från begärande-URL:en till FXG-mallar som lagras på servern.
solution: Experience Manager
title: Ersättningsvariabler
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 539d8863-e94d-45dc-bb8c-3db7bead0051
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 0%

---

# Ersättningsvariabler{#substitution-variables}

Ersättningsvariabeln används för att överföra värden från begärande-URL:en till FXG-mallar som lagras på servern.

` $ *`var`*= *`value`*`

<table id="simpletable_76B381800C0D411F87CD551FC30B0579"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> var </span> </span> </p> </td> 
  <td class="stentry"> <p>Variabelnamn. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> value </span> </span> </p> </td> 
  <td class="stentry"> <p>Värdet som variabeln ska anges till (sträng). </p> </td> 
 </tr> 
</table>

* Variabeldefinitioner och referenser kan förekomma i frågedelen av begäran-URL:en.
* Variabler definieras enligt ovan, ungefär som andra IS-kommandon. Med radavståndet &#39;$&#39; identifieras kommandot som en variabeldefinition.
* Variabelnamnet `*`var`*` är skiftlägeskänsligt och kan bestå av en kombination av bokstäver, siffror, &#39;-&#39; och &#39;_&#39;.
* Viktigt värde måste vara en URL-kodad enpass för säker HTTP-överföring.
