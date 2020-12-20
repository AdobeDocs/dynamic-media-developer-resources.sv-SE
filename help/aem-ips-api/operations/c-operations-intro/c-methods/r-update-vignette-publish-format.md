---
description: Uppdaterar inställningarna för publiceringsformat för vinjettering.
seo-description: Uppdaterar inställningarna för publiceringsformat för vinjettering.
seo-title: updateVinjettPublishFormat
solution: Experience Manager
title: updateVinjettPublishFormat
topic: Scene7 Image Production System API
uuid: ef8ae609-56e8-4ed6-906b-0668c5873946
translation-type: tm+mt
source-git-commit: 55015831ed1971a305ddbd8085c95626507355e0
workflow-type: tm+mt
source-wordcount: '441'
ht-degree: 0%

---


# updateVinjettPublishFormat{#updatevignettepublishformat}

Uppdaterar inställningarna för publiceringsformat för vinjettering.

## Auktoriserade användartyper {#section-2f2ad136d2884dc9bfef6da008196ed0}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-8c7ba8d2bce14071b21fccb11f44749f}

**Indata (updateVignettePublishFormatParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Företagshandtag. |
| ` *`vinjetteringFormatHandtag`*` | `xsd:string` | Ja | Publicera formatreferens. |
| ` *`name`*` | `xsd:string` | Nej | Publicera formatnamn. |
| ` *`targetWidth`*` | `xsd:int` | Ja | Anger målbredden för den resulterande vinjetteringsvyn i pixlar. Använd noll så att utdatavärjningen har samma storlek som den primära vinjetteringen. |
| ` *`targetHeight`*` | `xsd:int` | Ja | Anger målhöjden för den resulterande vinjetteringsvyn i pixlar. Använd noll så att utdatavärjningen har samma storlek som den primära vinjetteringen. |
| ` *`createPyramid`*` | `xsd:boolean` | Ja | Skapar en pyramidvinjettering som är optimerad för zoomning på servern för bildåtergivning. Med början från den maximala storleken, som anges av fälten Storlek på målvinjett, skapas vyer i flera storlekar i en enda vinjettutdatafil. Varje efterföljande visningsstorlek halveras tills bredden och höjden är inom 128 x 128 pixlar. |
| ` *`thumbWidth`*` | `xsd:int` | Ja | Anger bredden på varje miniatyrbild i pixlar. Den här inställningen är valfri. Använd noll om du inte har någon miniatyrfil. |
| ` *`saveAsVersion`*` | `xsd:int` | Ja | Anger filformatet för de publicerade vinjetterna. Om du har en ny version av Image Authoring och en äldre version av Image Rendering Server måste du ange en vinjettversion som ImageRendering Server kan läsa. Om du anger en senare version kan inte servern för bildåtergivning läsa de publicerade vinjetterna. Ange noll om du vill publicera vinjetter i den senaste versionen. |
| ` *`sizeSuffixSeparator`*` | `xsd:string` | Ja | Anger det tecken som skiljer vinjettnamnet och suffixet åt med dess bredd. |
| ` *`skärpa`*` | `xsd:int` | Nej | Använder skärpa på huvudvisningsbilden för varje storlek på publiceringsvinjett. Skärpa kan kompensera för oskärpa när vinjetterna skalas. |
| ` *`usmAmount`*` | `xsd:double` | Ja | Digital oskarp maskning är ett flexibelt och kraftfullt sätt att öka skärpan, särskilt i skannade bilder. Detta styr storleken på varje överskjutande del (hur mycket mörkare och ljusare kanterna blir). |
| ` *`usmRadius`*` | `xsd:double` | Ja | Påverkar storleken på kanterna som ska förbättras eller hur breda kanterna blir, så en mindre radie förbättrar detaljskärpan i mindre skala. Högre radievärden kan orsaka glorior vid kanterna. För fina detaljer krävs en mindre radie, eftersom små detaljer av samma storlek eller mindre än radien förloras. |
| ` *`usmThreshold`*` | `xsd:int` | Ja | Styr den minsta intensitetsändring som ska göras skarpare eller hur långt ifrån intilliggande tonvärden måste vara innan filtret fungerar. Den här inställningen kan göra mer skarpa kanter skarpare samtidigt som mer subtila kanter lämnas orörda. Det tillåtna tröskelintervallet är 0 till 255. |

**Utdata (updateVinjettPublishFormatReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`vinjetteringFormatHandtag`*` | `xsd:string` | Ja | Hantera det uppdaterade vinjettpubliceringsformatet. |

## Exempel {#section-fcba4bf2b7264786a676e315a35dbe43}

Det här kodexemplet uppdaterar ett vinjetteringsformat och returnerar handtaget till det uppdaterade formatet.

**Begäran**

```java
<updateVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|283</vignetteFormatHandle>
   <name>APIcreateVignettePublishFormat2</name>
   <targetWidth>1000</targetWidth>
   <targetHeight>800</targetHeight>
   <createPyramid>false</createPyramid>
   <thumbWidth>100</thumbWidth>
   <saveAsVersion>0</saveAsVersion>
   <sizeSuffixSeparator>-</sizeSuffixSeparator>
   <sharpen>50</sharpen>
   <usmAmount>240.0</usmAmount>
   <usmRadius>3.1</usmRadius>
   <usmThreshold>150</usmThreshold>
</updateVignettePublishFormatParam>
```

**Svar**

```java
<updateVignettePublishFormatReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <vignetteFormatHandle>v|21|283</vignetteFormatHandle>
</updateVignettePublishFormatReturn>
```

