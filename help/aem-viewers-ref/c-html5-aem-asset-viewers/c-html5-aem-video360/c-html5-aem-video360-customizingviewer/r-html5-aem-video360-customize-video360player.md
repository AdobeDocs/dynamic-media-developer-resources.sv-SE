---
description: Videospelaren är det rektangulära området där videoinnehållet visas i visningsprogrammet.
solution: Experience Manager
title: Video360-spelare
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,Business Practitioner
exl-id: 54ccf872-2d24-4d3f-9808-6d0e2558f5a5
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%

---

# Video360-spelare{#video-player}

Videospelaren är det rektangulära området där videoinnehållet visas i visningsprogrammet.

<!--<a id="section_061E550C1C1D4DB2BD663A898895B38C"></a>-->

Om dimensionerna för videon som spelas upp inte matchar dimensionerna för videospelaren centreras videoinnehållet i videospelarens rektangulära visningsområde.

Följande CSS-klassväljare styr videospelarens utseende:

```
.s7video360viewer .s7video360player
```

**CSS-egenskaper för videospelaren**

<table id="table_C48C56E696304C9BAFEE71BA9EA9A174"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color  </span> </p> </td> 
   <td colname="col2"> <p>Huvudvyns bakgrundsfärg. </p> </td> 
  </tr> 
 </tbody> 
</table>

Du kan lokalisera det felmeddelande som visas om systemet inte kan spela upp videon.

Se [Lokalisering av element i användargränssnittet](../../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-localization.md#concept-16262b8096474d6c9c018c3e99110dd1).

Exempel - Om du vill ställa in ett videovisningsprogram med videospelarens storlek inställd på 512 x 288 pixlar.

```
.s7video360viewer .s7video360player{ 
background-color: transparent; 
}
```

<!--<a id="section_5B82913FF3C44B7B8187969CB15E9560"></a>-->

Utseendet på buffringsanimeringen styrs med följande CSS-klassväljare:

```
.s7video360viewer .s7video360player .s7waiticon
```

**CSS-egenskaper för vänteikonen**

<table id="table_8DB41A0FF2A746F78B763564C4F3EBE0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>CSS-egenskap </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> Animeringsikonens bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height  </span> </p> </td> 
   <td colname="col2"> <p> Höjd på animeringsikonen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal-vänster  </span> </p> </td> 
   <td colname="col2"> <p> Animeringsikonens vänstermarginal, normalt minus halva ikonens bredd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> marginal-top  </span> </p> </td> 
   <td colname="col2"> <p> Animeringsikonens övre marginal, normalt minus halva ikonens höjd. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-image  </span> </p> </td> 
   <td colname="col2"> <p> Knacka teckningar. </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel - för att ställa in en buffringsanimering som 101 pixlar bred och 29 pixlar hög:

```
.s7video360viewer .s7video360player .s7waiticon { 
 width: 101px; 
 height: 29px; 
 margin-left: -50px; 
 margin-top: -15px; 
 background-image: url(images/sdk/busyicon.gif); 
}
```
