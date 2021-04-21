---
description: Om du klickar eller trycker på den här knappen kommer användaren till nästa sida i katalogen. Den här knappen visas i huvudkontrollfältet. Den här knappen visas inte på mobiltelefoner för att spara skärmutrymme. Du kan ändra storlek, skal och position för knappen med hjälp av CSS.
solution: Experience Manager
title: Knappen Nästa sida
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '298'
ht-degree: 0%

---


# Knappen Nästa sida{#next-page-button}

Om du klickar eller trycker på den här knappen kommer användaren till nästa sida i katalogen. Den här knappen visas i huvudkontrollfältet. Den här knappen visas inte på mobiltelefoner för att spara skärmutrymme. Du kan ändra storlek, skal och position för knappen med hjälp av CSS.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**CSS-egenskaper för huvudvisningsområdet**

Knappens utseende styrs med följande CSS-klassväljare:

`.s7ecatalogsearchviewer .s7toolbarrightbutton .s7panrightbutton`

<table id="table_94EE3F5BBE4547C0B4943471CEE7EDE4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p> CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> top  </span> </p> </td> 
   <td colname="col2"> <p>Placera från huvudkontrollfältets övre kant, inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> höger  </span> </p> </td> 
   <td colname="col2"> <p>Placera från den högra kanten av huvudkontrollfältet, inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vänster  </span> </p> </td> 
   <td colname="col2"> <p>Placera från vänster kant på huvudkontrollfältet, inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nederkant  </span> </p> </td> 
   <td colname="col2"> <p>Placera från den nedre kanten av huvudkontrollfältet, inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p>Knappens bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p>Knappens höjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p>Bilden som visas för ett visst knappläge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-position  </span> </p> </td> 
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se även <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-customizingviewer/c-html5-ecatsearch-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen stöder attributväljaren `state`, som kan användas för att tillämpa olika skal på olika knapplägen.

Knappens funktionsbeskrivning kan lokaliseras. Mer information finns i [Lokalisering av element i användargränssnittet](../../../c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Exempel - om du vill ställa in en knapp för nästa sida som är 28 x 28 pixlar, placerad 4 pixlar från nederkanten och 250 pixlar från den högra kanten av huvudkontrollfältet, och visa en annan bild för vart och ett av de fyra knapplägena.

```
.s7ecatalogsearchviewer .s7toolbarrightbutton .s7panrightbutton { 
bottom:4px; 
right:250px; 
width:32px; 
height:32px; 
} 
.s7ecatalogsearchviewer .s7toolbarrightbutton .s7panrightbutton [state='up'] { 
background-image:url(images/v2/ToolBarRightButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7toolbarrightbutton .s7panrightbutton [state='over'] {  
background-image:url(images/v2/ToolBarRightButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7toolbarrightbutton .s7panrightbutton [state='down'] {  
background-image:url(images/v2/ToolBarRightButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7toolbarrightbutton .s7panrightbutton [state='disabled'] { 
background-image:url(images/v2/ToolBarRightButton_dark_disabled.png); 
}
```

