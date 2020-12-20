---
description: 'Scen 7 Bildredigering består av följande komponenter '
seo-description: 'Scen 7 Bildredigering består av följande komponenter '
seo-title: Bildserverkomponenter
solution: Experience Manager
title: Bildserverkomponenter
topic: Scene7 Image Serving - Image Rendering API
uuid: 84e04972-32ce-4aca-aae6-d5b8bbe761e6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%

---


# Image Serving components{#image-serving-components}

Scen 7 Image Serving består av följande komponenter:

<table id="table_534AF33FE5C4453EACAE0DF35E8E3B63"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Komponent </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Serveransvarig </p> </td> 
   <td colname="col2"> <p>Fristående körbar fil som ansvarar för att starta, stoppa och säkerställa de andra komponenternas hälsa. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Apache Tomcat </p> </td> 
   <td colname="col2"> <p>Innehåller miljön för de flesta Java-baserade komponenter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Övervaknings-/aviseringstjänst </p> </td> 
   <td colname="col2"> <p>J2EE-applikation. Tillhandahåller serverövervakning och e-postvarningar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Plattformsserver </p> </td> 
   <td colname="col2"> <p>J2EE-applikation. Hanterar klientanslutningar, loggning och kommunikation med andra komponenter. HTTP-åtkomst på <span class="filepath"> /is/image</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Cachelagringstjänst </p> </td> 
   <td colname="col2"> <p>J2EE-applikation. Hanterar plattformsserverns datacache. HTTP-åtkomst vid /is/cache. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Bildserver </p> </td> 
   <td colname="col2"> <p>Utför alla bildbehandlings- och bildfils-I/O-åtgärder. Både 32-bitars och 64-bitars körbara filer är tillgängliga för Linux (32-bitars endast för Windows). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>ATE-textåtergivningskomponent </p> </td> 
   <td colname="col2"> <p>En eller flera instanser av textrenderingstjänsten kan vara aktiva när <span class="codeph"> textPs=</span>-åtgärder körs. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>SVG-återgivningskomponent </p> </td> 
   <td colname="col2"> <p>Fristående Java-program (inte värd för Tomcat). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scene7 Image Rendering (även kallat Återgivningsserver) </p> </td> 
   <td colname="col2"> <p>Kräver en separat licens för aktivering. HTTP-åtkomst vid <span class="filepath"> /ir/render</span>. Alla funktioner för bildåtergivning är integrerade i plattformsservern och bildservern, utan separata körbara komponenter. </p> </td> 
  </tr> 
 </tbody> 
</table>

Ytterligare konfigurationsinställningar tillhandahålls av standardkatalogen ( [!DNL default.ini]) eller specifika bildkataloger (mer information finns i [Bildkataloger](../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-overview.md#concept-9ce2b6a133de45f783e95cabc5810ac3)).
