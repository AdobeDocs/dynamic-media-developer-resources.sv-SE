---
description: Om du klickar eller trycker på den här knappen flyttas användaren till föregående sida i katalogen. Den här knappen visas i huvudkontrollfältet. Den här knappen visas inte på mobiltelefoner för att spara skärmutrymme. Du kan ändra storlek, skal och position för knappen med hjälp av CSS.
seo-description: Om du klickar eller trycker på den här knappen flyttas användaren till föregående sida i katalogen. Den här knappen visas i huvudkontrollfältet. Den här knappen visas inte på mobiltelefoner för att spara skärmutrymme. Du kan ändra storlek, skal och position för knappen med hjälp av CSS.
seo-title: Knappen Stor föregående sida
solution: Experience Manager
title: Knappen Stor föregående sida
topic: Dynamic media
uuid: 12e12b82-88f2-4fbf-bbbb-dea027eb6775
translation-type: tm+mt
source-git-commit: 90cbfca4533ca6639e561aa4e1344bdd20731eef
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 0%

---


# Stor knapp för föregående sida{#large-previous-page-button}

Om du klickar eller trycker på den här knappen flyttas användaren till föregående sida i katalogen. Den här knappen visas i huvudkontrollfältet. Den här knappen visas inte på mobiltelefoner för att spara skärmutrymme. Du kan ändra storlek, skal och position för knappen med hjälp av CSS.

<!--<a id="section_6C008EE11212461FA744F2540D38C295"></a>-->

**CSS-egenskaper för huvudvisningsområdet**

Knappens utseende styrs med följande CSS-klassväljare:

`.s7ecatalogviewer .s7ecatleftbutton .s7panleftbutton`

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
   <td colname="col2"> <p> Placera inuti en teckningssprite, om CSS-sprites används. </p> <p>Se även <a href="../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#section-9d570f95eb2443aca74c1b02f6e89aff" format="dita" scope="local"> CSS-fragment </a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Den här knappen stöder attributväljaren `state`, som kan användas för att tillämpa olika skal på olika knapplägen.

Knappens funktionsbeskrivning kan lokaliseras. Mer information finns i [Lokalisering av element i användargränssnittet](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-localization.md#concept-cbfc39344c494eb7b9f6a272cff0cc74).

Exempel - om du vill ställa in en stor knapp för föregående sida som är 56 x 56 pixlar lodrätt centrerad och förankrad vid den vänstra visningsprogrammets kant, och visa en bild för var och en av de fyra olika knapplägena.

```
.s7ecatalogviewer .s7ecatleftbutton .s7panleftbutton { 
bottom:50%; 
margin-bottom:-28px; 
left:0px; 
width:56px; 
height:56px; 
} 
.s7ecatalogviewer .s7ecatleftbutton .s7panleftbutton [state='up'] { 
background-image:url(images/v2/LeftButton_dark_up.png); 
} 
.s7ecatalogviewer .s7ecatleftbutton .s7panleftbutton [state='over'] {  
background-image:url(images/v2/LeftButton_dark_over.png); 
} 
.s7ecatalogviewer .s7ecatleftbutton .s7panleftbutton [state='down'] {  
background-image:url(images/v2/LeftButton_dark_down.png); 
} 
.s7ecatalogviewer .s7ecatleftbutton .s7panleftbutton [state='disabled'] { 
background-image:url(images/v2/LeftButton_dark_disabled.png); 
}
```

