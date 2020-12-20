---
description: Visst innehåll som visas i det grundläggande zoomvisningsprogrammet kan lokaliseras, inklusive zoomknappar och en helskärmsknapp.
seo-description: Visst innehåll som visas i det grundläggande zoomvisningsprogrammet kan lokaliseras, inklusive zoomknappar och en helskärmsknapp.
seo-title: Lokalisering av användargränssnittselement
solution: Experience Manager
title: Lokalisering av användargränssnittselement
topic: Dynamic media
uuid: 842970d9-0882-4163-8c49-3ea35d372d35
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---


# Lokalisering av element i användargränssnittet{#localization-of-user-interface-elements}

Visst innehåll som visas i det grundläggande zoomvisningsprogrammet kan lokaliseras, inklusive zoomknappar och en helskärmsknapp.

Varje textinnehåll i visningsprogrammet som kan lokaliseras representeras av en SDK-identifierare för visningsprogrammet som kallas SYMBOL. Alla SYMBOL har ett standardvärde för associerad text för det engelska språket ( `"en"`) som medföljer visningsprogrammet som inte är installerat och kan även ha användardefinierade värden för så många språkområden som behövs.

När visningsprogrammet startas kontrolleras det aktuella språkområdet för att se om det finns ett användardefinierat värde för varje SYMBOL som stöds i språkområdet. I så fall används det användardefinierade värdet. i annat fall återställs den till standardtexten som inte finns i kartongen.

Användardefinierade lokaliseringsdata kan skickas till visningsprogrammet som ett JSON-lokaliseringsobjekt. Ett sådant objekt innehåller en lista med språkområden som stöds, SYMBOL-textvärden för varje språkområde samt standardspråkområdet.

Ett exempel på ett sådant lokaliseringsobjekt:

```
{ 
"en":{ 
"CloseButton.TOOLTIP":"Close", 
"ZoomInButton.TOOLTIP":"Zoom In" 
 }, 
 "fr":{ 
"CloseButton.TOOLTIP":"Fermer", 
"ZoomInButton.TOOLTIP":"Agrandir" 
}, 
defaultLocale:"en" 
}
```

I exemplet ovan definierar lokaliseringsobjektet två språkområden ( `"en"` och `"fr"`) och tillhandahåller lokalisering för två element i användargränssnittet i varje språkområde.

Webbsideskoden ska skicka ett sådant lokaliseringsobjekt till visningsprogramkonstruktorn som ett värde på `localizedTexts`-fältet i konfigurationsobjektet. Ett annat alternativ är att skicka lokaliseringsobjektet genom att anropa metoden `setLocalizedTexts(localizationInfo)`.

Följande SYMBOL stöds:

<table id="table_58C40353B7244335872350C98DF2CFB3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>SYMBOL </p> </th> 
   <th colname="col2" class="entry"> <p>Verktygstips för ... </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL  </span> </p> </td> 
   <td colname="col2"> <p>ARIA-etikett för visningsprogramelementet på den översta nivån. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>ARIA-rollbeskrivning för huvudvykomponenten. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p>ARIA-användningstips för tangentbordsanvändare. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> CloseButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Stängningsknapp. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomInButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Knappen Zooma in. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomOutButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Knappen Zooma ut. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomResetButton.TOOLTIP  </span> </p> </td> 
   <td colname="col2"> <p>Knappen Zoomåterställning. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_SELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Helskärmsknapp i normalt läge. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> FullScreenButton.TOOLTIP_UNSELECTED  </span> </p> </td> 
   <td colname="col2"> <p>Helskärmsknapp i helskärmsläge. </p> </td> 
  </tr> 
 </tbody> 
</table>

