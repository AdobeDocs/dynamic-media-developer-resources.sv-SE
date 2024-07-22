---
description: Image Serving source data files include image and mask files, fonts, and ICC profiles.
solution: Experience Manager
title: Source data
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d7e9c101-8d34-4241-b03c-131f31c25933
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# Source data{#source-data}

Image Serving source data files include image and mask files, fonts, and ICC profiles.

Alla källdatafiler måste vara tillgängliga för Image Server. Image Serving innehåller ett antal alternativ för att ange platsen för datafiler:

`*`install_folder`*/ *`rootPath`*/ *`filePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> filePath </span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> catalogPath </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph">-katalog::Path|catalog::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> relativ sökväg och namn för bildfil har angetts i en Image Serving HTTP-begäran </span> </p></td> 
 </tr> 
</table>

Servern kombinerar sökvägssegment från höger till vänster tills en absolut filsökväg har upprättats.

Alla `*`rootPath`*`-segment kan vara tomma, relativa eller absoluta sökvägssegment.

`*`catalogPath`*` är antingen en absolut eller relativ sökväg/namn. `*`requestPath`*` måste vara en relativ filsökväg/namn.

`Multiple IS::RootPath` värden kan definieras i ImageServerRegistry.xml (eller via administratörsgränssnittet). Detta gör att källdatafiler kan distribueras över flera filsystem. Image Server försöker med alternativa sökvägar i den ordning som anges tills datafilen hittas.

Nya datafiler kan läggas till när som helst utan att servern stoppas.
