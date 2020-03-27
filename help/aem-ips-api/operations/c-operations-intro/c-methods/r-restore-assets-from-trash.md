---
description: Återställer resurser från papperskorgen.
seo-description: Återställer resurser från papperskorgen.
seo-title: restoreAssetsFromTrash
solution: Experience Manager
title: restoreAssetsFromTrash
topic: Scene7 Image Production System API
uuid: f7424d4c-7807-4de9-ad0c-f96364bf7b82
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# restoreAssetsFromTrash{#restoreassetsfromtrash}

Återställer resurser från papperskorgen.

Syntax

## Auktoriserade användartyper {#section-15e887782c7d4ace897ff02c6ad5baa0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-200a61d040c94e489a85241b29cd499a}

**Indata (restoreAssetsFromTrashParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Referensen till ett företag med de resurser som du vill återställa. |
| ` *`assetHandleArray`*` | `types:HandleArray` | Ja | En array med handtag för de resurser som du vill återställa. |

**Utdata (restoreAssetsFromTrashReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Ja | Antal resurser som tagits bort från papperskorgen. |
| ` *`warningCount`*` | `xsd:int` | Ja | Antal varningar som genererades när åtgärden försökte återställa resurser från papperskorgen. |
| ` *`errorCount`*` | `xsd:int` | Ja | Antal fel som genererats vid försök att återställa resurser från papperskorgen. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nej | Arrayen med information som är associerad med resurserna som genererade varningar när åtgärden försökte återställa resurser från papperskorgen. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | Nej | Arrayen med information som är associerad med resurserna som genererade fel när åtgärden försökte återställa resurser från papperskorgen. |

## Exempel {#section-98fe0394b0634ca397c395f14f8a9358}

Det här kodexemplet återställer resurser från papperskorgen. Svaret anger att åtgärden har slutförts.

**Begäran**

```java
<restoreAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</restoreAssetsFromTrashParam>
```

**Svar**

```java
<restoreAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</restoreAssetsFromTrashReturn
```

