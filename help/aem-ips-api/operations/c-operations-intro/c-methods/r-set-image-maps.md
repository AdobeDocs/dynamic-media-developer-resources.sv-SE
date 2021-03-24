---
description: Anger bildschemat för en resurs.
solution: Experience Manager
title: setImageMaps
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 0%

---


# setImageMaps{#setimagemaps}

Anger bildschemat för en resurs.

Du måste ha skapat bildscheman. Bildscheman används i den ordning som de hämtas från arrayen. Det innebär att det andra bildschemat övertäcker det första, det tredje övertäcker det andra och så vidare.

## Auktoriserade användartyper {#section-adb21c5b679249939dd83816e4a0ee97}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-2292ec1aead947ef8741dd0653a41f42}

**Indata (setImageMapsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Företagshandtag. |
| `*`assetHandle`*` | `xsd:string` | Ja | Resurshandtag. |
| `*`imageMapArray`*` | `types:ImageMapDefinitionArray` | Ja | Array med fördefinierade bildscheman. |

**Utdata (setImageMapsReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`imageMapHandleArray`*` | `types:HandleArray` | Ja | En array med bildmappshandtag tillämpade på resursen. |

## Exempel {#section-fe2e35662a6a4ee29cf250c9fd180371}

I det här kodexemplet anges 2 bildscheman för en bildresurs. Koden anger formtyp, region och åtgärd som vidtas när bildscheman anropas. Svaret innehåller en array med handtag till bildscheman.

**Begäran**

```java
<setImageMapsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|739|1|537</assetHandle>
   <imageMapArray>
      <items>
         <name>ImageMap2</name>
         <shapeType>Rectangle</shapeType>
         <region>40</region>
         <action>400</action>
         <enabled>true</enabled>
      </items>
      <items>
         <name>ImageMap3</name>
         <shapeType>Rectangle</shapeType>
         <region>40</region>
         <action>400</action>
         <enabled>false</enabled>
      </items>
   </imageMapArray>
</setImageMapsParam>
```

