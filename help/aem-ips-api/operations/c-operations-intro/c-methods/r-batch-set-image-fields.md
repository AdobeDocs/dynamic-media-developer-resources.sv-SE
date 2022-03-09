---
description: Anger bildspecifika fält för en eller flera bildresurser.
solution: Experience Manager
title: batchSetImageFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8ea6dbb8-4d32-43e5-961f-31110f983663
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 0%

---

# batchSetImageFields{#batchsetimagefields}

Anger bildspecifika fält för en eller flera bildresurser.

Syntax

## Auktoriserade användartyper {#section-6b087bdcb7874c13acf76e113a093054}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-4969815cf67c4d11b13bb2017b3604e8}

**Indata (batchSetImageFields)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Handtaget till företaget som innehåller bildresurserna. |
| updateArray | `types:ImageFieldUpdateArray` | Ja | Arrayen med bildfält uppdateras. |

**Utdata (batchSetImageFields)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| successCount | `xsd:int` | Ja | Antalet bildfält som har angetts. |
| warningCount | `xsd:int` | Ja | Antalet varningar som genereras när åtgärden försökte ange bildfälten. |
| errorCount | `xsd:int` | Ja | Antalet fel som genererades när åtgärden försökte ange bildfälten. |
| warningDetailArray | `types:AssetOperationFaultArray` | Nej | Arrayen med information som är associerad med resurserna som genererade varningar när åtgärden försökte tillämpa uppdateringarna. |
| errorDetailArray | `types:AssetOperationFaultArray` | Nej | Arrayen med information som är associerad med resurserna som genererade fel när åtgärden försökte tillämpa uppdateringarna. |

## Exempel {#section-0476e3d6516a4f8bbaac9de983bc6d1e}

I det här exemplet anges data i fälten för två bilder i en uppdateringsarray. I arrayen anges bilderna med hjälp av deras resurshandtag och innehåller upplösning i pixlar, x- och y-positionskoordinater samt användardata. Svaret indikerar att fält för båda bilderna har angetts korrekt.

**Begäran**

```java
<batchSetImageFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|140626|1|102524</assetHandle>
         <resolution>72</resolution>
         <anchorX>50</anchorX>
         <anchorY>100</anchorY>
         <userData>nada1</userData>
      </items>
      <items>
         <assetHandle>a|96680|1|64865</assetHandle>
         <resolution>150</resolution>
         <anchorX>100</anchorX>
         <anchorY>50</anchorY>
         <userData>nada2</userData>
      </items>
   </updateArray>
</batchSetImageFieldsParam>
```

**Svar**

```java
<batchSetImageFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetImageFieldsReturn>
```
