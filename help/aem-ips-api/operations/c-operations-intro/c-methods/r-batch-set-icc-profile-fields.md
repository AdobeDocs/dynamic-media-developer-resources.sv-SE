---
description: Anger metadatafält för ICC-profil.
seo-description: Anger metadatafält för ICC-profil.
seo-title: batchSetIccProfileFields
solution: Experience Manager
title: batchSetIccProfileFields
topic: Scene7 Image Production System API
uuid: 163b9b36-85b6-4880-8029-8421b04f4a08
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

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
| ` *`companyHandle`*` | `xsd:string` | Ja | Hantera till företaget som innehåller ICC-profilerna. |
| ` *`uppdateringsmatris`*` | `xsd:string` | Ja | Matris med ICC-profiluppdateringar. |

**Utdata (batchSetIccProfileFields)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Ja | Antalet ICC-profilfält som har angetts. |
| ` *`warningCount`*` | `xsd:int` | Ja | Antalet varningar som genererades när åtgärden försökte ange ICC-profilfälten. |
| ` *`errorCount`*` | `xsd:int` | Ja | Antalet fel som genererades när åtgärden försökte ange ICC-profilfält. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nej | Arrayen med information som är associerad med resurserna som genererade varningar när åtgärden försökte tillämpa uppdateringarna. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | Nej | Arrayen med information som är associerad med resurserna som genererade fel när åtgärden försökte tillämpa uppdateringarna. |

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

