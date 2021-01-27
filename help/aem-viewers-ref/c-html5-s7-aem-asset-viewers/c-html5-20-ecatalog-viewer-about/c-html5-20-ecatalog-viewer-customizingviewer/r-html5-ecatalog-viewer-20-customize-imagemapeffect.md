---
description: Beroende på värdet på parametern mode visar visningsprogrammet bildschemaikoner över huvudvyn på platser där kartor ursprungligen skapats i Dynamic Media Classic eller återger exakta områden som matchar formen på originalbildscheman.
solution: Experience Manager
title: Bildschemaeffekt
topic: Dynamic Media
translation-type: tm+mt
source-git-commit: dacd641302826196f4bf4c8d2dfc02d032d63487
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---


# Bildschemaeffekt{#image-map-effect}

Beroende på värdet på parametern mode visar visningsprogrammet bildschemaikoner över huvudvyn på platser där kartor ursprungligen skapats i Dynamic Media Classic eller återger exakta områden som matchar formen på originalbildscheman.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

**CSS-egenskaper för huvudvisningsområdet**

Utseendet på bildschemaikonen styrs av följande CSS-klassväljare:

```
.s7ecatalogviewer .s7imagemapeffect .s7icon
```

>[!NOTE]
>
>CSS-klassen `s7mapoverlay` som tidigare användes för att formatera bildschemaikoner är nu föråldrad. använd `s7icon` i stället.

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Bildschemaikoner </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se även <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Bildschemaikonens bredd i pixlar. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Bildschemats ikonhöjd i pixlar. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Bildschemaikonen stöder attributväljaren `state`, som du kan använda för att tillämpa olika skal på ikonlägena `default` och `active`.

Exempel - ställ in en bildschemaikon på 28 x 28 pixlar som visar en annan bild för vart och ett av de två olika ikonlägena.

```
.s7ecatalogviewer .s7imagemapeffect .s7icon { 
 height: 28px; 
 width: 28px;  
 background-image: url(images/v2/ImageMapEffect_dark_up.png); 
} 
.s7ecatalogviewer .s7imagemapeffect .s7icon[state="default"] { 
 opacity: 0.5; 
} 
.s7ecatalogviewer .s7imagemapeffect .s7icon[state="active"] { 
opacity: 1; 
}
```

Se även [Stöd för bildschema](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-image-map-support.md#concept-28759efae5014a1fa8b0fb14dc26812a).

Utseendet på bildschemaområdet styrs med följande CSS-klassväljare:

```
.s7ecatalogviewer .s7imagemapeffect .s7region
```

<table id="table_1FF98CE842604AAABD838FF528CDC4EF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background  </span> </p> </td> 
   <td colname="col2"> <p> Fyllningsfärg för bildschemaområde. </p> <p>Anges i formatet #RRGGBB, RGB(R,G,B) eller RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p> Fyllningsfärg för bildschemaområde. </p> <p>Anges i formatet #RRGGBB, RGB(R,G,B) eller RGBA(R,G,B,A). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> border  </span> </p> </td> 
   <td colname="col2"> <p> Områdesformat för bildschemat. </p> <p>Anges som <span class="codeph"> <span class="varname"> bredd </span> heldragen <span class="varname"> färg </span> </span>, där <span class="codeph"> bredd </span> </span> uttrycks i pixlar och <span class="codeph"> <span class="varname"> färg </span> </span> anges som #RRGGBB, RGB(R,G,B) eller RGBA(R,G,B,A).<span class="varname"> </span></p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - ställ in ett genomskinligt bildschemaområde med `1` pixelsvart kant:

```
.s7ecatalogviewer .s7imagemapeffect .s7region { 
 border: 1px solid #000000; 
 background: RGBA(0,0,0,0);  
}
```

