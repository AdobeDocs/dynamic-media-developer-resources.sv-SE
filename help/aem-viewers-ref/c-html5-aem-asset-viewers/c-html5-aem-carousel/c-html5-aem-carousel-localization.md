---
description: Visst innehåll som visas i Carousel Viewer kan lokaliseras. Detta inkluderar navigeringsknappar för bildrutor.
solution: Experience Manager
title: Lokalisering av användargränssnittselement
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,Business Practitioner
exl-id: 05f5abe0-1124-4114-864d-440699bcdc39
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 0%

---

# Lokalisering av element i användargränssnittet{#localization-of-user-interface-elements}

Visst innehåll som visas i Carousel Viewer kan lokaliseras. Detta inkluderar navigeringsknappar för bildrutor.

Varje textinnehåll i visningsprogrammet som kan lokaliseras representeras av den speciella SDK-identifieraren för visningsprogrammet som kallas SYMBOL. Alla SYMBOL har ett associerat standardtextvärde för en engelsk språkinställning ( `"en"`) som levereras med visningsprogrammet som inte är installerat och kan även ha användardefinierade värden för så många språkinställningar som behövs.

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

Webbsideskoden ska skicka lokaliseringsobjektet till visarkonstruktorn, som ett värde i fältet `localizedTexts` för konfigurationsobjektet. Ett annat alternativ är att skicka lokaliseringsobjektet genom att anropa metoden `setLocalizedTexts(localizationInfo)`.

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
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Markerat läge för uppspelningsknappen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> PlayPauseButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Ovalt läge för uppspelningsknappen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CAROUSELVIEWER_TOOLTIP_GOTO  </span> </p> </td> 
   <td colname="col2"> <p> Verktygstips och ARIA-etikett för föregående och nästa bildknappar. </p> <p>Accepterar två ersättningstoken: <span class="codeph"> $CURRENT_FRAME$ </span> för det aktuella bildindexet och <span class="codeph"> $TOTAL_FRAMES$ </span> för det totala antalet bilder. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL  </span> </p> </td> 
   <td colname="col2"> <p> ARIA-etikett för visningsprogramelementet på den översta nivån. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p> ARIA-rollbeskrivning för huvudvykomponent. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CarouselView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p> ARIA-användningstips för tangentbordsanvändare. </p> </td> 
  </tr> 
 </tbody> 
</table>
