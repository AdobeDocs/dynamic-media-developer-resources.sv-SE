---
description: Cachekontroll. Tillåter selektiv inaktivering av cachelagring på klientsidan (webbläsare, proxyservrar, nätverkscachningssystem) och cachelagring i det interna  [!DNL Platform Server] cacheminnet.
solution: Experience Manager
title: cache
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 622c36fa-c209-4149-a7db-85067215b5e5
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 0%

---

# cache{#cache}

Cachekontroll. Tillåter selektiv inaktivering av cachelagring på klientsidan (webbläsare, proxyservrar, nätverkscachningssystem) och cachelagring i det interna [!DNL Platform Server]-cachen.

`&cache= *`cacheControl`*`

`&cache= *`clientControl`*, *`serverControl`*`

<table id="simpletable_DA4D92F0AEF84FD49953876796058B7F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl </span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> på|av</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> på|av</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> på|av</span> </p></td> 
 </tr> 
</table>

Om bara ett *`cacheControl`*-värde anges används det på både klient- och servercachen.

Begär attribut. Ignoreras när begäran inte returnerar en svarsbild. *`clientControl`* ignoreras när cachelagring på klientsidan inaktiveras av bildkatalogen (om `catalog::Expiration` har ett negativt värde).

Standardvärdet är `cache=on,on`.
