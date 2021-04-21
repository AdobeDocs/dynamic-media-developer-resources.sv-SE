---
description: Cachekontroll. Tillåter selektiv inaktivering av cachelagring på klientsidan (webbläsare, proxyservrar, nätverkscachningssystem) och cachelagring i den interna plattformsservercachen.
solution: Experience Manager
title: cache
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---


# cache{#cache}

Cachekontroll. Tillåter selektiv inaktivering av cachelagring på klientsidan (webbläsare, proxyservrar, nätverkscachningssystem) och cachelagring i den interna plattformsservercachen.

`&cache= *`cacheControl`*`

`&cache= *``*, *`clientControlserverControl`*`

<table id="simpletable_DA4D92F0AEF84FD49953876796058B7F"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cacheControl</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> clientControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> serverControl</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> on|off</span> </p></td> 
 </tr> 
</table>

Om bara ett *`cacheControl`*-värde har angetts tillämpas det på både klient- och servercachen.

Begär attribut. Ignoreras när begäran inte returnerar en svarsbild. *`clientControl`* ignoreras när cachelagring på klientsidan inaktiveras av bildkatalogen (om  `catalog::Expiration` den har ett negativt värde).

Standardvärdet är `cache=on,on`.
