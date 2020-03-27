---
description: Visst innehåll som visas i Carousel Viewer kan lokaliseras. Detta inkluderar navigeringsknappar för bildrutor.
seo-description: Visst innehåll som visas i Carousel Viewer kan lokaliseras. Detta inkluderar navigeringsknappar för bildrutor.
seo-title: Lokalisering av användargränssnittselement
solution: Experience Manager
title: Lokalisering av användargränssnittselement
topic: Dynamic media
uuid: 82e4dc72-cc12-4ab5-8370-6270f9a3d45f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Lokalisering av användargränssnittselement{#localization-of-user-interface-elements}

Visst innehåll som visas i Carousel Viewer kan lokaliseras. Detta inkluderar navigeringsknappar för bildrutor.

Varje textinnehåll i visningsprogrammet som kan lokaliseras representeras av den speciella SDK-identifieraren för visningsprogrammet som kallas SYMBOL. Alla SYMBOL har ett standardvärde för associerad text för ett engelskt språk ( `"en"`) som levereras med visningsprogrammet som inte är installerat och kan även ha användardefinierade värden för så många språkområden som behövs.

När visningsprogrammet startas kontrolleras det aktuella språkområdet för att se om det finns ett användardefinierat värde för varje SYMBOL som stöds för sådana språkområden. I så fall används det användardefinierade värdet. i annat fall återställs den till standardtexten som inte finns i kartongen.

Användardefinierade lokaliseringsdata kan skickas till visningsprogrammet som ett JSON-lokaliseringsobjekt. Det här objektet innehåller en lista med språkområden som stöds, SYMBOL-textvärden för varje språkområde samt standardspråkområdet.

Ett exempel på ett sådant lokaliseringsobjekt är följande:

```
{ 
"en":{ 
"PanLeftButton.TOOLTIP":"Left", 
"PanRightButton.TOOLTIP":"Right" 
 }, 
 "fr":{ 
"PanLeftButton.TOOLTIP":"Gauchiste", 
"PanRightButton .TOOLTIP":"Droit" 
}, 
defaultLocale:"en" 
}
```

I exemplet ovan definierar lokaliseringsobjektet två språkområden ( `"en"` och `"fr"`) och tillhandahåller lokalisering för två element i användargränssnittet i varje språkområde.

Webbsideskoden ska skicka lokaliseringsobjektet till visarkonstruktorn, som ett värde i `localizedTexts` fältet för konfigurationsobjektet. Ett annat alternativ är att skicka lokaliseringsobjektet genom att anropa `setLocalizedTexts(localizationInfo)` metoden.

Följande SYMBOL stöds:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SYMBOL </p> </th> 
   <th colname="col2" class="entry"> <p>Verktygstips för.. </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED </span> </p> </td> 
   <td colname="col2"> <p>Markerat läge för uppspelningsknappen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED </span> </p> </td> 
   <td colname="col2"> <p>Ovalt läge för uppspelningsknappen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CAROUSELVIEWER_TOOLTIP_GOTO </span> </p> </td> 
   <td colname="col2"> <p> Verktygstips och ARIA-etikett för föregående och nästa bildknappar. </p> <p>Accepterar två ersättningstoken: <span class="codeph"> $CURRENT_FRAME$ </span> för det aktuella bildindexet och <span class="codeph"> $TOTAL_FRAMES$ </span> för det totala antalet bilder. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL </span> </p> </td> 
   <td colname="col2"> <p> ARIA-etikett för visningsprogramelementet på den översta nivån. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.ROLE_DESCRIPTION </span> </p> </td> 
   <td colname="col2"> <p> ARIA-rollbeskrivning för huvudvykomponent. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.USAGE_HINT </span> </p> </td> 
   <td colname="col2"> <p> ARIA-användningstips för tangentbordsanvändare. </p> </td> 
  </tr> 
 </tbody> 
</table>

