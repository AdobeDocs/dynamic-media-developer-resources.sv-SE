---
description: Viss information som visas i Interactive Image Viewer kan lokaliseras. Detta inkluderar funktionsbeskrivningar för användargränssnittselement och ett informationsmeddelande som visas i den utfällbara zoomvyn vid inläsningen.
seo-description: Viss information som visas i Interactive Image Viewer kan lokaliseras. Detta inkluderar funktionsbeskrivningar för användargränssnittselement och ett informationsmeddelande som visas i den utfällbara zoomvyn vid inläsningen.
seo-title: Lokalisering av användargränssnittselement
title: Lokalisering av användargränssnittselement
uuid: 1a22570b-8435-4e57-a022-34428bddc7f7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '337'
ht-degree: 0%

---


# Lokalisering av element i användargränssnittet{#localization-of-user-interface-elements}

Viss information som visas i Interactive Image Viewer kan lokaliseras. Detta inkluderar funktionsbeskrivningar för användargränssnittselement och ett informationsmeddelande som visas i den utfällbara zoomvyn vid inläsningen.

Varje textinnehåll i visningsprogrammet som kan lokaliseras representeras av den speciella SDK-identifieraren för visningsprogrammet som kallas SYMBOL. Alla SYMBOL har ett associerat standardtextvärde för en engelsk språkinställning ( `"en"`) som levereras med visningsprogrammet som inte är installerat och kan även ha användardefinierade värden för så många språkinställningar som behövs.

När visningsprogrammet startas kontrolleras det aktuella språkområdet för att se om det finns ett användardefinierat värde för varje SYMBOL som stöds för sådana språkområden. I så fall används det användardefinierade värdet. i annat fall återställs den till standardtexten som inte finns i kartongen.

Användardefinierade lokaliseringsdata kan skickas till visningsprogrammet som ett JSON-lokaliseringsobjekt. Det här objektet innehåller en lista med språkområden som stöds, SYMBOL-textvärden för varje språkområde samt standardspråkområdet.

Ett exempel på ett sådant lokaliseringsobjekt är följande:

```
{ 
"en":{ 
"Container.LABEL":"Interactive Image Viewer" 
 }, 
 "fr":{ 
"Container.LABEL":"Visionneuse d'images interactive" 
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
   <td colname="col1"> <p> <span class="codeph"> Container.LABEL  </span> </p> </td> 
   <td colname="col2"> <p>ARIA-etikett för visningsprogramelementet på den översta nivån. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.ROLE_DESCRIPTION  </span> </p> </td> 
   <td colname="col2"> <p>ARIA-rollbeskrivning för huvudvykomponent. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> ZoomView.USAGE_HINT  </span> </p> </td> 
   <td colname="col2"> <p>ARIA-användningstips för tangentbordsanvändare. </p> </td> 
  </tr> 
 </tbody> 
</table>

