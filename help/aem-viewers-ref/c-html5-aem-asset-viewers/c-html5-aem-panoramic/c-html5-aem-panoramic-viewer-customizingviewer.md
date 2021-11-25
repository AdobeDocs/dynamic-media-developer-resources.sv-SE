---
title: Anpassa panoramavisningsprogram
description: All visuell anpassning och de flesta beteendeanpassningar för panoramavyn görs genom att en anpassad CSS skapas.
keywords: responsiv
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: c9dda4e8-2781-4870-9ccb-707823c56490
source-git-commit: 7a3ba1cbe063603733a8ff03e8ef1277ec632ec5
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# Anpassa Video360 Viewer{#customizing-video-viewer}

All visuell anpassning och de flesta beteendeanpassningar görs genom att en anpassad CSS skapas.

Det föreslagna arbetsflödet är att ta standard-CSS-filen för rätt visningsprogram, kopiera den till en annan plats, anpassa den och ange platsen för den anpassade filen i `style=` -kommando.

CSS-standardfiler finns på följande plats:

`<s7viewers_root>/html5/PanoramicViewer.css`

Anpassad CSS-fil måste innehålla samma klassdeklarationer som standardklassdeklarationerna. Om en klassdeklaration utelämnas fungerar visningsprogrammet inte korrekt eftersom det inte innehåller inbyggda standardformat för elementen i användargränssnittet.

Ett annat sätt att tillhandahålla anpassade CSS-regler är att använda inbäddade format direkt på webbsidan eller i någon av de länkade externa CSS-reglerna.

Tänk på att visningsprogrammet tilldelar `.s7panoramicviewer` till behållar-DOM-elementet. Om du använder en extern CSS-fil som skickas med `style=` kommando, använda `.s7panoramicviewer` som överordnad klass i underordnad väljare för dina CSS-regler. Om du gör inbäddade format på webbsidan kan du även kvalificera den här väljaren med ett ID för behållar-DOM-elementet enligt följande:

`#<containerId>.s7panoramicviewer.`


## Allmän formatinformation och råd {#section-95855dccbbc444e79970f1aaa3260b7b}

* Alla sökvägar till externa resurser i CSS matchas mot CSS-platsen, inte mot visningsprogrammets HTML-sidplats. Ta hänsyn till detta när du kopierar standard-CSS till en annan plats: Det kan vara nödvändigt att antingen kopiera standardresurserna eller att uppdatera sökvägarna i den anpassade CSS:en.
* Du kan använda olika format för färgvärden som stöds av CSS. Om genomskinlighet behövs `rgba(R,G,B,A)` format föreslås. Annars krävs ingen genomskinlighet `#RRGGBB` kan användas.

När du anpassar visningsgränssnittet med CSS används `!IMPORTANT` regeln stöds inte för att formatera visningsprogramelement. I synnerhet `!IMPORTANT` ska inte användas för att åsidosätta standardformat eller körningsformat som tillhandahålls av visningsprogrammet eller visaren-SDK eftersom det kan påverka korrekt komponentbeteende. I stället bör CSS-väljare med rätt specificitet användas för att ange CSS-egenskaper som dokumenteras i den här referenshandboken.

## CSS för panoramavisningsprogram {#section-9b6d8d601cb441d08214dada7bb4eddc}

**Huvudvisningsområde**
Huvudvisningsområdet är det område som upptas av panoramabilden.  Den ställs vanligtvis in så att den passar den tillgängliga enhetsskärmen när ingen storlek har angetts.

Visningsområdets utseende styrs av CSS-klassväljaren:
`.s7panoramicviewer`

Tillämpliga CSS-egenskaper är:

<table id="table_panA68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> tittarens bredd, </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> tittarens höjd, </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel: Så här ställer du in ett visningsprogram med storleken 1 024 x 512 pixlar.

```
.s7panoramicviewer {
	width: 1024px;
	height: 500px;	
}
```

**Panoramavy**
Huvudvyn består av panoramabilden.

Utseendet på huvudvyn styrs av CSS-klassväljaren:
`.s7panoramicviewer .s7panoramicview`

Tillämpliga CSS-egenskaper är:
<table id="table_pann68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> background-color </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> Huvudvyns bakgrundsfärg. </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Exempel: Så här gör du huvudvyn genomskinlig:

```
.s7panoramicviewer .s7panoramicview {
	background-color: transparent;
}
```
