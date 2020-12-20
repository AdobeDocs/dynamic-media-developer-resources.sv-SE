---
description: Om du klickar eller trycker på den här knappen flyttas användaren till den sista sidan i katalogen. Den här knappen visas i huvudkontrollfältet på stationära datorer och surfplattor. på mobiltelefoner läggs den till i ett sekundärt kontrollfält. Du kan ändra storlek, skal och position för knappen med hjälp av CSS.
seo-description: Om du klickar eller trycker på den här knappen flyttas användaren till den sista sidan i katalogen. Den här knappen visas i huvudkontrollfältet på stationära datorer och surfplattor. på mobiltelefoner läggs den till i ett sekundärt kontrollfält. Du kan ändra storlek, skal och position för knappen med hjälp av CSS.
seo-title: Knappen Sista sidan
solution: Experience Manager
title: Knappen Sista sidan
topic: Dynamic media
uuid: 4cdcd2b7-a6d3-48c0-ba65-5339d232a954
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---


# Knappen Sista sidan{#last-page-button}

Om du klickar eller trycker på den här knappen flyttas användaren till den sista sidan i katalogen. Den här knappen visas i huvudkontrollfältet på stationära datorer och surfplattor. på mobiltelefoner läggs den till i ett sekundärt kontrollfält. Du kan ändra storlek, skal och position för knappen med hjälp av CSS.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**CSS-egenskaper för huvudvisningsområdet**

Knappens utseende styrs med följande CSS-klassväljare:

`.s7ecatalogsearchviewer .s7lastpagebutton .s7panleftbutton`

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
   <td colname="col2"> <p>Placera från huvudkontrollfältets övre kant (på stationära datorer och surfplattor) eller sekundära kontrollfält (på mobiltelefoner), inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> höger  </span> </p> </td> 
   <td colname="col2"> <p>Placera från höger kant på huvudkontrollfältet (på stationära datorer och surfplattor) eller sekundärt kontrollfält (på mobiltelefoner), inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vänster  </span> </p> </td> 
   <td colname="col2"> <p>Placera från vänster kant på huvudkontrollfältet (på stationära datorer och surfplattor) eller sekundärt kontrollfält (på mobiltelefoner), inklusive utfyllnad. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> nederkant  </span> </p> </td> 
   <td colname="col2"> <p>Placera längst ned i huvudkontrollfältet (på stationära datorer och surfplattor) eller i det sekundära kontrollfältet (på mobiltelefoner), inklusive utfyllnad. </p> </td> 
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

Exempel - om du vill ställa in en sista sidknapp som är 28 x 28 pixlar, placerad 4 pixlar från nederkanten och 220 pixlar från vänsterkanten av huvudkontrollfältet, och visa en annan bild för vart och ett av de fyra knapplägena.

```
.s7ecatalogsearchviewer .s7lastpagebutton .s7panrightbutton { 
bottom:4px; 
right:220px; 
width:32px; 
height:32px; 
} 
.s7ecatalogsearchviewer .s7lastpagebutton .s7panrightbutton [state='up'] { 
background-image:url(images/v2/LastPageButton_dark_up.png); 
} 
.s7ecatalogsearchviewer .s7lastpagebutton .s7panrightbutton [state='over'] {  
background-image:url(images/v2/LastPageButton_dark_over.png); 
} 
.s7ecatalogsearchviewer .s7lastpagebutton .s7panrightbutton [state='down'] {  
background-image:url(images/v2/LastPageButton_dark_down.png); 
} 
.s7ecatalogsearchviewer .s7lastpagebutton .s7panrightbutton [state='disabled'] { 
background-image:url(images/v2/LastPageButton_dark_disabled.png); 
}
```

