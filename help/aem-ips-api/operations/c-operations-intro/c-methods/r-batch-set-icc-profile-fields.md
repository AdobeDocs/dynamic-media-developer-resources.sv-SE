---
description: Anger metadatafält för ICC-profil.
solution: Experience Manager
title: batchSetIccProfileFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d10a30ca-afa7-4ef0-8cef-0329b0068bf3
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 0%

---

# batchSetIccProfileFields{#batchseticcprofilefields}

Anger metadatafält för ICC-profil.

Syntax

## Auktoriserade användartyper {#section-f6f7caf9434b4f469518dab64b76c0f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-75a02b55ae0d444ca26b59aac6e86d6f}

**Indata (batchSetIccProfileFields)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Hantera till företaget som innehåller ICC-profilerna. |
| `*`uppdateringsmatris`*` | `xsd:string` | Ja | Matris med ICC-profiluppdateringar. |

**Utdata (batchSetIccProfileFields)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Ja | Antalet ICC-profilfält som har angetts. |
| `*`warningCount`*` | `xsd:int` | Ja | Antalet varningar som genererades när åtgärden försökte ange ICC-profilfälten. |
| `*`errorCount`*` | `xsd:int` | Ja | Antalet fel som genererades när åtgärden försökte ange ICC-profilfält. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nej | Arrayen med information som är associerad med resurserna som genererade varningar när åtgärden försökte tillämpa uppdateringarna. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Nej | Arrayen med information som är associerad med resurserna som genererade fel när åtgärden försökte tillämpa uppdateringarna. |

## Exempel {#section-5dc90cfbd9b1411485b44859032f7cb9}

**Begäran**

```java
<batchSetIccProfileFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|1808|13|169</assetHandle>
         <class>Output</class>
         <colorSpace>CMYK</colorSpace>
         <pcsType>Luv</pcsType>
      </items>
   </updateArray>
</batchSetIccProfileFieldsParam>
```

**Svar**

```java
<batchSetIccProfileFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetIccProfileFieldsReturn>
```
