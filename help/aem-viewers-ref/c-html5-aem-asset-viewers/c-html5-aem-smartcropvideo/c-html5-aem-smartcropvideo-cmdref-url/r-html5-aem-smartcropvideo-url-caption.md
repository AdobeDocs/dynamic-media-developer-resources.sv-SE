---
title: bildtext
description: URL-kommando för visningsprogrammet för smart beskärning.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 0d7000d0-9181-4c6e-a94e-31ab5ad17fa4
source-git-commit: 1aa8be858b0ba8ec9b99753d43c202b35ed58c30
workflow-type: tm+mt
source-wordcount: '209'
ht-degree: 0%

---

# bildtext{#caption}

URL-kommando för visningsprogrammet för smart beskärning.

` caption= *`fil`*[,0|1]`

Visningsprogrammet har stöd för undertextning via WebVTT-filer på webben. Överlappande tecken och regioner stöds inte. Följande operatorer för cue-positionering stöds:

<table id="table_62D89A06EC9E4E7983D1F26A2C85A621"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Nyckel </p> </th> 
   <th colname="col2" class="entry"> <p>Namn </p> </th> 
   <th colname="col3" class="entry"> <p>Värde </p> </th> 
   <th colname="col4" class="entry"> <p>Beskrivning </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> A </p> </td> 
   <td colname="col2"> <p>textjustering </p> </td> 
   <td colname="col3"> <p><span class="codeph"> vänster|höger|mitten|start|slut</span> </p> </td> 
   <td colname="col4"> <p> Styr textjustering. </p> <p>Standardvärdet är <span class="codeph"> mitten</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>T </p> </td> 
   <td colname="col2"> <p>textposition </p> </td> 
   <td colname="col3"> <p> 0 %-100 % </p> </td> 
   <td colname="col4"> <p> Procentandel indrag i VideoPlayer-komponenten för bildtextens början. </p> <p>Standardvärdet är 0 %. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>S </p> </td> 
   <td colname="col2"> <p>radstorlek </p> </td> 
   <td colname="col3"> <p> 0 %-100 % </p> </td> 
   <td colname="col4"> <p> Procentandel av videobredden som används för bildtexter. </p> <p>Standardvärdet är 100 %. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>L </p> </td> 
   <td colname="col2"> <p>linjeposition </p> </td> 
   <td colname="col3"> <p> 0%-100%|heltal </p> </td> 
   <td colname="col4"> <p> Anger linjens position på sidan. </p> <p>Om det uttrycks som ett heltal (inget procenttecken) är det antalet rader uppifrån som texten visas på. </p> <p>Om det är ett procenttal (procenttecknet är det sista tecknet) visas bildtexten som procentandelen nedåt i visningsområdet. </p> <p>Standardvärdet är 100 %. </p> </td> 
  </tr> 
 </tbody> 
</table>

Andra WebVTT-funktioner i WebVTT-filen stöds inte, men bör inte störa bildtexten.

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> fil </span></span> </p> </td> 
   <td colname="col2"> <p> Anger en URL eller sökväg till WebVTT-bildtextinnehållet. Servera WebVTT-filen med ImageServing. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0|1</span> </p> </td> 
   <td colname="col2"> <p> Anger standardläget för bildtext (aktiverad är <span class="codeph"> 1</span>). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Egenskaper {#section-f42369774e2740dcb399626a0e4e930e}

Valfritt.

## Standard {#section-d016470e92a74f98a18c4ab3489410a5}

Ingen.

## Exempel {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
caption=Scene7SharedAssets/adobe_qbc_final_cc,1
```
