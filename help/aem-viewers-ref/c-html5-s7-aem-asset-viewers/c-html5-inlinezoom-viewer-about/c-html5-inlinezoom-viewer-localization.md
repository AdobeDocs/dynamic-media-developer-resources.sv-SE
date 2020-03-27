---
description: Visst innehåll som visas i visningsprogrammet kan lokaliseras. Det här innehållet innehåller funktionsbeskrivningar och informationsmeddelanden för användargränssnittselement som visas i den utfällbara zoomvyn vid inläsningen.
seo-description: Visst innehåll som visas i visningsprogrammet kan lokaliseras. Det här innehållet innehåller funktionsbeskrivningar och informationsmeddelanden för användargränssnittselement som visas i den utfällbara zoomvyn vid inläsningen.
seo-title: Lokalisering av användargränssnittselement
solution: Experience Manager
title: Lokalisering av användargränssnittselement
topic: Dynamic media
uuid: d824c0c3-3606-4903-96f7-de26a61a8f65
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Lokalisering av användargränssnittselement{#localization-of-user-interface-elements}

Visst innehåll som visas i visningsprogrammet kan lokaliseras. Det här innehållet innehåller funktionsbeskrivningar och informationsmeddelanden för användargränssnittselement som visas i den utfällbara zoomvyn vid inläsningen.

Varje textinnehåll i visningsprogrammet som kan lokaliseras representeras av den speciella SDK-identifieraren för visningsprogrammet som kallas SYMBOL. Alla SYMBOL har ett standardvärde för associerad text för ett engelskt språk ( `"en"`) som levereras med visningsprogrammet som inte är installerat och kan även ha användardefinierade värden för så många språkområden som behövs.

När visningsprogrammet startas kontrolleras det aktuella språkområdet för att se om det finns ett användardefinierat värde för varje SYMBOL som stöds för sådana språkområden. I så fall används det användardefinierade värdet. i annat fall återställs den till standardtexten som inte finns i kartongen.

Användardefinierade lokaliseringsdata kan skickas till visningsprogrammet som ett JSON-lokaliseringsobjekt. Det här objektet innehåller en lista med språkområden som stöds, SYMBOL-textvärden för varje språkområde samt standardspråkområdet.

Ett exempel på ett sådant lokaliseringsobjekt är följande:

```
{ 
"en":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Mouse over to zoom", 
"FlyoutZoomView.TIP_BUBBLE_TAP":"Tap and hold to zoom" 
 }, 
 "fr":{ 
"FlyoutZoomView.TIP_BUBBLE_OVER":"Passez la souris sur pour zoomer", 
"FlyoutZoomView.TIP_BUBBLE_TAP":"Appuyez et maintenez pour agrandir" 
}, 
defaultLocale:"en" 
}
```

I ovanstående exempel definierar lokaliseringsobjektet två språkområden ( `"en"` och `"fr"`) och tillhandahåller lokalisering för två element i användargränssnittet i varje språkområde.

Webbsideskoden ska skicka ett sådant lokaliseringsobjekt till visarkonstruktorn, som ett värde i konfigurationsobjektets `localizedTexts` fält. Ett annat alternativ är att skicka lokaliseringsobjektet genom att anropa `setLocalizedTexts(localizationInfo)` metoden.

Följande SYMBOL stöds:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SYMBOL </p> </th> 
   <th colname="col2" class="entry"> <p>Beskrivning </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p>ARIA-etikett för visningsprogramelementet på den översta nivån. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p>ARIA-rollbeskrivning för huvudvykomponent. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p>ARIA-användningstips för tangentbordsanvändare. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_OVER </span> </p> </td> 
   <td colname="col2"> <p>Informationsmeddelande för datorer. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FlyoutZoomView.TIP_BUBBLE_TAP </span> </p> </td> 
   <td colname="col2"> <p>Informationsmeddelande för pekenheter. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollLeftButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Verktygstips för att rulla vänster knapp. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollRightButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Verktygstips för att rulla höger knapp. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollUpButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Verktygstips för att rulla uppåt. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ScrollDownButton.TOOLTIP </span> </p> </td> 
   <td colname="col2"> <p>Verktygstips för rullningsknapp. </p> </td> 
  </tr> 
 </tbody> 
</table>

