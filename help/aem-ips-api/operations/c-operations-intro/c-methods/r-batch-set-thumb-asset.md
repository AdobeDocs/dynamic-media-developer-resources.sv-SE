---
description: Anger miniatyrbilden för en eller flera resurser.
seo-description: Anger miniatyrbilden för en eller flera resurser.
seo-title: batchSetThumbAsset
solution: Experience Manager
title: batchSetThumbAsset
topic: Scene7 Image Production System API
uuid: 16c298a7-bb07-4643-824b-8f864d7f0290
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# batchSetThumbAsset{#batchsetthumbasset}

Anger miniatyrbilden för en eller flera resurser.

Syntax

## Miniatyrresurstyper {#section-4edc2a6a8f824213b0aaddb1d437268c}

Följande miniatyrresurstyper tillåts:

* Bild
* JusteradVisa
* Mask
* Mall
* PsdTemplate

## Auktoriserade användartyper {#section-5fc988e3d6384968b86fd9fe363658c0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Användaren måste ha läs- och skrivåtkomst till målresursen och läsåtkomst till tumresursen.

## Parametrar {#section-9c6efa000b384b3db6c013def20cf40b}

**Indata (batchSetThumbAssetParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Handtaget till företaget som innehåller tillgångarna. |
| ` *`updateArray`*` | `types:ThumbAssetUpdateArray` | Ja | Arrayen med uppdateringar. |

**Utdata (batchSetThumbAssetParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Ja | Antal miniatyrbilder som angetts. |
| ` *`warningCount`*` | `xsd:int` | Ja | Antalet varningar som genererades när åtgärden försökte ange miniatyrbilderna. |
| ` *`errorCount`*` | `xsd:int` | Ja | Antalet fel som genererades när åtgärden försökte ange miniatyrbilder. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nej | Arrayen med information som är associerad med resurserna som genererade varningar när åtgärden försökte tillämpa uppdateringarna. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | Nej | Arrayen med information som är associerad med resurserna som genererade fel när åtgärden försökte tillämpa uppdateringarna. |

## Exempel {#section-6de69a8680c24c1486c5f01488393381}

**Begäran**

```java
<batchSetThumbAssetParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|234</assetHandle>
         <thumbAssetHandle>a|189</thumbAssetHandle>
      </items>
   </updateArray>
```

**Svar**

```java
<batchSetThumbAssetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetThumbAssetReturn>
```

