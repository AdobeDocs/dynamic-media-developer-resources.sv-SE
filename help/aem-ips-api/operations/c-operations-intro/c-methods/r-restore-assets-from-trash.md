---
description: Återställer resurser från papperskorgen.
solution: Experience Manager
title: restoreAssetsFromTrash
feature: Dynamic Media Classic,SDK/API,Resurshantering
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '166'
ht-degree: 0%

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
| `*`companyHandle`*` | `xsd:string` | Ja | Referensen till ett företag med de resurser som du vill återställa. |
| `*`assetHandleArray`*` | `types:HandleArray` | Ja | En array med handtag för de resurser som du vill återställa. |

**Utdata (restoreAssetsFromTrashReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Ja | Antal resurser som tagits bort från papperskorgen. |
| `*`warningCount`*` | `xsd:int` | Ja | Antal varningar som genererades när åtgärden försökte återställa resurser från papperskorgen. |
| `*`errorCount`*` | `xsd:int` | Ja | Antal fel som genererats vid försök att återställa resurser från papperskorgen. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nej | Arrayen med information som är associerad med resurserna som genererade varningar när åtgärden försökte återställa resurser från papperskorgen. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | Nej | Arrayen med information som är associerad med resurserna som genererade fel när åtgärden försökte återställa resurser från papperskorgen. |

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

