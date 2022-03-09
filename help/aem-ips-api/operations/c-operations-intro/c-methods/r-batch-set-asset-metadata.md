---
description: Ställer in metadata för resurser i batchläge.
solution: Experience Manager
title: batchSetAssetMetadata
feature: Dynamic Media Classic,SDK/API,Metadata,Asset Management
role: Developer,Admin
exl-id: 7393fa4f-71fb-48a5-a7f3-91eec82c88c1
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# batchSetAssetMetadata{#batchsetassetmetadata}

Ställer in metadata för resurser i batchläge.

Syntax

## Auktoriserade användartyper {#section-5310d9fd00604cbf9756944900378855}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-7111ac93bc7747f69ba14db4ac3912b0}

**Indata (batchSetAssetMetadataParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Referensen till det företag vars metadata du vill ange i en gruppåtgärd. |
| updateArray | `types:BatchMetadataUpdateArray` | Ja | Arrayen med metadatauppdateringar som används för resurserna. |

**Utdata (batchSetAssetMetadataParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| successCount | `xsd:int` | Ja | Antalet angivna metadata. |
| warningCount | `xsd:int` | Ja | Antalet varningar som genereras när åtgärden försökte ange metadata. |
| errorCount | `xsd:int` | Ja | Antalet fel som genererades när åtgärden försökte ange metadata. |
| warningDetailArray | `types:AssetOperationFaultArray` | Nej | Arrayen med detaljer som är associerade med resurserna som genererar varningar när åtgärden försökte batchställa in metadata för resurserna. |
| errorDetailArray | `types:AssetOperationFaultArray` | Nej | Arrayen med information som är associerad med resurserna som genererar fel när åtgärden försökte batchställa in metadata för resurserna. |

## Exempel {#section-2de798ac920e4b47b971b1729a64395b}

**Begäran**

```java
<batchSetAssetMetadataParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
<companyHandle>c|6</companyHandle>
<updateArray>
   <items>
      <assetHandleArray>
         <items>a|743|1|538</items>
         <items>a|744|1|539</items>
      </assetHandleArray>
      <updateArray>
         <items>
            <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
            <value>400</value>
         </items>
      </updateArray>
   </items>
   <items>
      <assetHandleArray>
         <items>a|732|1|535</items>
         <items>a|739|1|537</items>
      </assetHandleArray>
      <updateArray>
         <items>
            <fieldHandle>m|6|IMAGE|saveMetadataField</fieldHandle>
            <value>300</value>
         </items>
      </updateArray>
   </items>
</updateArray>
</batchSetAssetMetadataParam>
```

**Svar**

```java
<batchSetAssetMetadataReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>4</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetAssetMetadataReturn>
```
