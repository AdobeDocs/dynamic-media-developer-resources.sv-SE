---
description: Skapar ett nytt publiceringsformat för en vinjett.
seo-description: Skapar ett nytt publiceringsformat för en vinjett.
seo-title: createVignettePublishFormat
solution: Experience Manager
title: createVignettePublishFormat
topic: Scene7 Image Production System API
uuid: 834ebe6a-e105-4075-8004-172237980933
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# createVignettePublishFormat{#createvignettepublishformat}

Skapar ett nytt publiceringsformat för en vinjett.

Vinjetteringsformaten anger storleken på publicerade vinjetteringar och deras miniatyrbilder samt zoomnivåer, skärpeparametrar och filformatsversionen för vinjetteringar som skapats från huvudvinjetteringar som publicerats på en bildåtergivningsserver från IPS.

Nya serverversioner för bildåtergivning har stöd för pyramidvinjettering, vilket eliminerar behovet av att definiera specifika vinjettformat för publicering.

## Auktoriserade användartyper {#section-f5c563e3695c4dba8df41e2a965aace7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-3a368186ec1d4005bca056fc9d9bacc7}

**Indata (createVignettePublishFormatParam)**

<table id="table_4D5B2913FA784EC09190F25223C1A680"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Namn </th> 
   <th colname="col2" class="entry"> Typ </th> 
   <th colname="col3" class="entry"> Obligatoriskt </th> 
   <th colname="col4" class="entry"> Beskrivning </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:sträng</span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Handtag till det företag som vinjetteringen tillhör. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> namn</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Kodfras </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Namn som identifierar vinjetteringens publiceringsformat. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetWidth</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Kodfras </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> <p>Anger målbredden för den resulterande vinjetteringsvyn i pixlar. </p> <p>Använd noll så att den resulterande vinjetteringen har samma storlek som huvudvinjetteringen. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> targetHeight</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Kodfras </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Skapar en pyramidvinjettering som är optimerad för zoomning på servern för bildåtergivning. Med början från den maximala storleken, som anges av fälten Storlek på målvinjett, skapas vyer i flera storlekar i en enda vinjettutdatafil. Varje efterföljande visningsstorlek halveras tills bredden och höjden är inom 128 x 128 pixlar. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createPyramid</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Kodfras </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Anger bredden på varje miniatyrbild i pixlar. Den här inställningen är valfri. Använd noll om du inte har någon miniatyrfil. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbWidth</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Kodfras </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Anger filformatet för de publicerade vinjetterna. Om du har en ny version av Image Authoring och en äldre version av Image Rendering Server måste du ange en vinjettversion som ImageRendering Server kan läsa. Om du anger en senare version kan inte servern för bildåtergivning läsa de publicerade vinjetterna. Ange noll om du vill publicera vinjetter i den senaste versionen. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> saveAsVersion</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Kodfras </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Anger det tecken som avgränsar vinjettnamnet och suffixet som anger bredden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sizeSuffixSeparator</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Kodfras </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Anger det tecken som avgränsar vinjettnamnet och suffixet som anger bredden. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> skärpa</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Kodfras </span> </td> 
   <td colname="col3"> Nej </td> 
   <td colname="col4"> Använder skärpa i huvudvisningsbilden för varje publik vinjettstorlek Skärpa kan kompensera för oskärpa när vinjetterarna skalas. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmAmount</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Kodfras </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Digital oskarp maskning är ett flexibelt och kraftfullt sätt att öka skärpan, särskilt i skannade bilder. Detta styr storleken på varje överskjutande del (hur mycket mörkare och ljusare kanterna blir). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmRadius</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Kodfras </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Påverkar storleken på kanterna som ska förbättras eller hur breda kanterna blir, så en mindre radie förbättrar detaljskärpan i mindre skala. Högre radievärden kan orsaka glorior vid kanterna. För fina detaljer krävs en mindre radie, eftersom små detaljer av samma storlek eller mindre än radien förloras. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> usmThreshold</span></span> </td> 
   <td colname="col2"> <span class="codeph"> Kodfras </span> </td> 
   <td colname="col3"> Ja </td> 
   <td colname="col4"> Styr den minsta intensitetsändring som ska göras skarpare eller hur långt ifrån intilliggande tonvärden måste vara innan filtret fungerar. Den här inställningen kan göra mer skarpa kanter skarpare samtidigt som mer subtila kanter lämnas orörda. Det tillåtna tröskelintervallet mellan 0 och 255. </td> 
  </tr> 
 </tbody> 
</table>

**Utdata (createVinjettPublishFormatReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`vinjetteringFormatHandtag`*` | `xsd:string` | Ja | Handtaget till det skapade vinjettformatet. |

## Exempel {#section-0564752d439642b9bb8de2903db6de1e}

Den här koden skapar ett format för vinjettering. Begäran om att skapa anger ett namn, målbredd och -höjd och andra obligatoriska värden.

**Begäran**

```java
<createVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <name>APIcreateVignettePublishFormat1</name>
   <targetWidth>1200</<targetWidth>
   <targetHeight>800</targetHeight>
   <createPyramid>true</createPyramid>
   <thumbWidth>400</thumbWidth>
   <saveAsVersion>0</saveAsVersion>
   <sizeSuffixSeparator>-</sizeSuffixSeparator>
   <sharpen>50</sharpen>
   <usmAmount>230.0</usmAmount>
   <usmRadius>1.1</usmRadius>
   <usmThreshold>130</usmThreshold>
</createVignettePublishFormatParam>
```

**Svar**

```java
<createVignettePublishFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</createVignettePublishFormatReturn>
```

