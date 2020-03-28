---
description: Huvudvisningsområdet upptas av videon. Den ställs vanligtvis in så att den passar den tillgängliga enhetsskärmen när ingen storlek har angetts.
seo-description: Huvudvisningsområdet upptas av videon. Den ställs vanligtvis in så att den passar den tillgängliga enhetsskärmen när ingen storlek har angetts.
seo-title: Huvudvisningsområde
solution: Experience Manager
title: Huvudvisningsområde
topic: Dynamic media
uuid: f395b22d-55b8-4422-9aa4-9dd4b7a24063
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef

---


# Huvudvisningsområde{#main-viewer-area}

Huvudvisningsområdet upptas av videon. Den ställs vanligtvis in så att den passar den tillgängliga enhetsskärmen när ingen storlek har angetts.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Följande CSS-klassväljare styr visningsområdets utseende:

```
.s7videoviewer 
```

## CSS-egenskaper för huvudvisningsområdet {#css-properties-of-the-main-viewer-area}

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bredd på visningsprogram. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p>Höjd på visningsprogram. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> Bakgrundsfärg i hexadecimalt format. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Exempel {#section-e8caea0a303c425a8a637c2a47c06355}

Så här ställer du in ett videovisningsprogram med en vit bakgrund (#FFFFFF) och gör storleken 512 x 288 pixlar:

```
.s7videoviewer { 
 background-color: #FFFFFF; 
 width: 512px; 
 height: 288px;  
}
```

