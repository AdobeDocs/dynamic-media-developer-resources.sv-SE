---
description: Parametern är gemensam för alla visningsprogram.
solution: Experience Manager
title: bildtext
feature: Dynamic Media Classic,visningsprogram,SDK/API
role: Developer,User
exl-id: 06ce5520-944b-4ab0-8f59-67c273bd8314
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 1%

---

# bildtext{#caption}

Parametern är gemensam för alla visningsprogram.

>[!NOTE]
>
>Det här kommandot gäller inte för Video Image Viewer.

` caption= *`fil`*[,0|1]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fil  </span> </span> </p> </td> 
   <td colname="col2"> <p> Anger en URL eller sökväg till WebVTT-bildtextinnehållet. Image Serving visar WebVTT-filen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p> Anger standardbildtextläget. Aktiverad är <span class="codeph"> 1 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Det här visningsprogrammet stöder undertextning via WebVTT-filer på webben. De bildtexter som anges med den här parametern gäller för den video som kommer först i medieuppsättningar. efterföljande videofilmer spelas upp utan bildtexter. Överlappande tecken och regioner stöds inte. Operatorer för cue-positionering:

<table id="table_E752D7D8C1AA40C6B8A7057D2BB379C1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nyckel </p> </th> 
   <th colname="col2" class="entry"> <p>Namn </p> </th> 
   <th colname="col3" class="entry"> <p>Värden </p> </th> 
   <th colname="col4" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> A  </span> </p> </td> 
   <td colname="col2"> <p>testjustering </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> left|right|middle|start|end  </span> </p> </td> 
   <td colname="col4"> <p> Styr textens justering. </p> <p>Standardvärdet är <span class="codeph"> mittersta </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T  </span> </p> </td> 
   <td colname="col2"> <p>textposition </p> </td> 
   <td colname="col3"> <p> 0 %-100 % </p> </td> 
   <td colname="col4"> <p> Procentandel indrag i VideoPlayer-komponenten för bildtextens början. </p> <p>Standardvärdet är <span class="codeph"> 0% </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S  </span> </p> </td> 
   <td colname="col2"> <p>radstorlek </p> </td> 
   <td colname="col3"> <p> 0 %-100 % </p> </td> 
   <td colname="col4"> <p> Procentandel av videobredden som används för bildtexter. </p> <p>Standardvärdet är <span class="codeph"> 100 % </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L  </span> </p> </td> 
   <td colname="col2"> <p>linjeposition </p> </td> 
   <td colname="col3"> <p> 0%-100%|heltal </p> </td> 
   <td colname="col4"> <p> Anger linjens position på sidan. </p> <p>Om det uttrycks som ett heltal utan procenttecken är det antalet rader från den övre delen där texten visas. </p> <p>Om det uttrycks som ett procenttecken är procenttecknet det sista tecknet, så visas bildtexten i procent nedåt i visningsområdet. </p> <p>Standardvärdet är <span class="codeph"> 100 % </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Observera att om det finns andra WebVTT-funktioner i WebVTT-filen stöds de inte. De kommer dock inte att störa bildtexter.

<table id="table_CB7B4DFC6B654AECA1AF6594E3FD5C46"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fil  </span> </span> </p> </td> 
   <td colname="col2"> <p> Anger en URL eller sökväg till WebVTT-bildtextinnehåll. WebVTT-filen hanteras av Image Serving. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1  </span> </p> </td> 
   <td colname="col2"> <p> Anger standardbildtextläget. </p> <p>Aktiverad är <span class="codeph"> 1 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-10ee45d637134e0fbcd943c62578cb78}

Valfritt.

## Standard {#section-d411e450028c460392cb8508f8ccc5d9}

Ingen.

## Exempel {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
caption=Scene7SharedAssets/adobe_qbc_final_cc,1
```
