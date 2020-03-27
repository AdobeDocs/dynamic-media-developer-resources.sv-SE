---
description: I det här avsnittet beskrivs de vanliga åtgärdsparametrarna som hanteras av API:t för IPS-webbtjänsten.
seo-description: I det här avsnittet beskrivs de vanliga åtgärdsparametrarna som hanteras av API:t för IPS-webbtjänsten.
seo-title: Operationsmetoder
solution: Experience Manager
title: Operationsmetoder
topic: Scene7 Image Production System API
uuid: 713646a7-1108-4f93-bec2-3fbe7e548515
translation-type: tm+mt
source-git-commit: 806e7e670ee98e1fb6adf52ffc95fb989fa69400

---


# Operationsmetoder{#operations-methods}

I det här avsnittet beskrivs de vanliga åtgärdsparametrarna som hanteras av API:t för IPS-webbtjänsten.

En fullständig beskrivning av varje åtgärdsparameter finns i [Åtgärdsparametrar](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md).

## Handtag: Om {#section-094ce1afa6244fa5b2c762f44ffdca1c}

Hanterar refererande IPS-objekt som returneras av vissa API-åtgärder. Du kan också skicka handtag som parametrar till efterföljande åtgärdsanrop. Handtag är strängdatatyper ( `xsd:string`).

Handtag är endast avsedda att användas under en enda programsession. Dessutom bör du göra handtagen beständiga eftersom deras format kan ändras mellan olika IPS-versioner. När du skriver interaktiva program implementerar du timeout för sessioner och tar bort alla referenser mellan sessioner, särskilt efter en IPS-uppgradering. När du skriver icke-interaktiva program anropar du lämpliga åtgärder för att hämta referenser varje gång programmet körs. I följande Java/Axis2-kodexempel visas felaktig och korrekt kodkörning:

**Felaktig handtagskod**

Det här kodexemplet är felaktigt eftersom det innehåller ett hårdkodat värde (555) för företagsreferensen.

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**Korrigera handtagskod**

Det här kodexemplet är korrekt eftersom det anropar `getCompanyInfo` för att returnera en giltig referens. Den förlitar sig inte på ett hårdkodat värde. Använd den här metoden eller någon annan IPS API-motsvarighet för att returnera den nödvändiga referensen.

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## Vanliga typer av handtag {#section-e683ac8283284f9688e63f51a494f7a0}

**companyHandle**

De flesta åtgärder kräver att du anger en företagskontext genom att ange en `companyHandle` parameter. Företagshandtaget är en pekare som returneras av vissa åtgärder som `getCompanyInfo`, `addCompany`och `getCompanyMembership`.

**userHandle**

Parametern `userHandle` är en valfri parameter för åtgärder som riktar sig till en viss användare. Som standard riktar dessa åtgärder sig till den anropande användaren (den användare vars inloggningsuppgifter skickas för autentisering). Administratörsanvändare med rätt behörighet kan dock ange en annan användare. Åtgärden anger till exempel vanligtvis lösenordet för den autentiserade användaren, men en administratör kan använda `setPassword` `userHandle` parametern för att ange lösenordet för en annan användare.

För åtgärder som kräver en företagskontext (med parametern `companyHandle` ) måste både autentiserade användare och målanvändare vara medlemmar i det angivna företaget. För åtgärder som inte kräver någon företagskontext måste både den autentiserade användaren och målanvändaren vara medlemmar i minst ett gemensamt företag.

Följande åtgärder kan hämta användarhandtag:

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle och accessGroupHandle**

Som standard används åtgärder som kräver åtkomstbehörighet (läsa, skriva, ta bort) i den anropande användarens behörighetskontext. Vissa åtgärder gör att du kan ändra den här kontexten med parametern `accessUserHandle` eller `accessGroupHandle` . Parametern `accessUserHandle` gör att en administratör kan personifiera en annan användare. Parametern `accessGroupHandle` gör att anroparen kan arbeta i kontexten för en viss användargrupp.

**responseFieldArray och excludeFieldArray**

Vissa åtgärder gör att anroparen kan begränsa vilka fält som ska inkluderas i svaret. Genom att begränsa fält kan du minska den tid och det minne som krävs för att bearbeta begäran och minska svarsdatans storlek. Anroparen kan begära en viss lista med fält genom att skicka en `responseFieldArray` parameter eller med en uppräknad lista med uteslutna fält via `excludeFieldArray` parametern.

Både `responseFieldArray` och `excludeFieldArray` anger fält genom att använda en nodsökväg som avgränsas med `/`. Om du till exempel anger att bara ska returnera namnet, det senaste ändringsdatumet och metadata för varje resurs, ska du referera till följande: `searchAssets`

```
<responseFieldArray> 
   <items>assetArray/items/name</items> 
   <items>assetArray/items/lastModified</items> 
   <items>assetArray/items/metadataArray</items> 
</responseFieldArray>
```

Om du vill returnera alla fält (förutom behörigheter):

```
<excludeFieldArray> 
   <items>assetArray/items/permissions</items> 
</excludeFieldArray>
```

Observera att nodsökvägarna är relativa till den returnerade nodroten. Om du anger ett komplext textfält utan något av dess underordnade element (till exempel `assetArray/items/imageInfo`), inkluderas alla dess underordnade element. Om du anger ett eller flera delelement i ett komplext typfält (till exempel `assetArray/items/imageInfo/originalPath`) inkluderas endast dessa delelement.

Om du inte tar med `responseFieldArray` eller `excludeFieldArray` i en begäran returneras alla fält.

**Språk**

Från och med IPS 4.0 har API:t för IPS stöd för att ställa in språkkontexten för en åtgärd genom att skicka parametern `authHeader` locale. Om parametern locale inte finns `Accept-Language` används HTTP-huvudet. Om den här rubriken inte heller finns kommer standardspråket för IPS-servern att användas.

Vissa åtgärder tar också explicita språkområdesparametrar, som kan skilja sig från åtgärdssammanhanget. Åtgärden tar till exempel en `submitJob` `locale` parameter som anger språkområdet som används för jobbloggning och e-postmeddelanden.

Språkparametrar använder formatet `<language_code>[-<country_code>]`

Om språkkoden är en gemen tvåbokstavskod som anges av ISO-639 och den valfria landskoden är en versal, tvåbokstavskod som specificeras av ISO-3266. Språksträngen för amerikansk engelska är till exempel `en-US`.
