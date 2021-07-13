---
description: Image Serving source data files include image and mask files, fonts, and ICC profiles.
solution: Experience Manager
title: Källdata
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: d7e9c101-8d34-4241-b03c-131f31c25933
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# Källdata{#source-data}

Image Serving source data files include image and mask files, fonts, and ICC profiles.

Alla källdatafiler måste vara tillgängliga för Image Server. Image Serving innehåller ett antal alternativ för att ange platsen för datafiler:

`*`install_`*/ *``*/ *`folderrootPathfilePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> filePath  </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> catalogPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> katalog::Path|catalog::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> relativ sökväg och namn för bildfilen som anges i en Image Serving HTTP-begäran</span> </p></td> 
 </tr> 
</table>

Servern kombinerar sökvägssegment från höger till vänster tills en absolut filsökväg har upprättats.

Alla `*`rootPath`*`-segment kan vara tomma, relativa eller absoluta sökvägssegment.

`*``*` catalogSöker antingen en absolut eller relativ sökväg/namn. `*`request`*` Path måste vara en relativ sökväg/namn.

`Multiple IS::RootPath` värden kan definieras i ImageServerRegistry.xml (eller via administratörsgränssnittet). Detta gör att källdatafiler kan distribueras över flera filsystem. Image Server kommer att försöka med alternativa sökvägar i den ordning som anges tills datafilen hittas.

Nya datafiler kan läggas till när som helst utan att servern stoppas.
