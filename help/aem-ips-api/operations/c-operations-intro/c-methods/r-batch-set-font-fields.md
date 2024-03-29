---
description: Anger metadatafält för teckensnitt.
solution: Experience Manager
title: batchSetFontFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f38aa861-2a81-4663-967e-72611122f51b
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# batchSetFontFields{#batchsetfontfields}

Anger metadatafält för teckensnitt.

## Auktoriserade användartyper {#section-89eff13b5ed54cddb87b1304ba4eff0e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-836f5948d00a46e98ccb62f0573e4e68}

**Indata (batchSetFontFieldsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Hantera till företaget som innehåller teckensnitten. |
| updateArray | `types:FontFieldUpdateArray` | Ja | Matris med uppdateringar av teckensnittsfält. |

**Utdata (batchSetFontFieldsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| successCount | `xsd:int` | Ja | Antalet korrekt angivna teckensnittsfält. |
| warningCount | `xsd:int` | Ja | Antal varningar som genererades när åtgärden försökte ange teckensnittsfält. |
| errorCount | `xsd:int` | Ja | Antal fel som genererades när åtgärden försökte ange teckensnittsfält. |
| warningDetailArray | `types:AssetOperationFaultArray` | Nej | Arrayen med information som är associerad med resurserna som genererade varningar när åtgärden försökte tillämpa uppdateringarna. |
| errorDetailArray | `types:AssetOperationFaultArray` | Nej | Arrayen med information som är associerad med resurserna som genererade fel när åtgärden försökte tillämpa uppdateringarna. |

## Exempel {#section-0449c2e4ec534f4b8ee849ec4fe12c4e}

**Begäran**

```javascript {.line-numbers}
<batchSetFontFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
   <updateArray>
      <items>
          <assetHandle>a|450|14|19</assetHandle>
          <fontName>Bookman Old Style Font Name</fontName>
          <postscriptName>Bookman Old Style PostScript</postscriptName>
          <rtfName>Bookman Old Style RTF</rtfName>
          <fontFamily>Bookman Old Style Family</fontFamily>
          <style>BoldItalic</style>
          <typeName>Open Type</typeName><type>OTF</type>
      </items>
   </updateArray>
</batchSetFontFieldsParam>
```

**Svar**

```javascript {.line-numbers}
<batchSetFontFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetFontFieldsReturn>
```
