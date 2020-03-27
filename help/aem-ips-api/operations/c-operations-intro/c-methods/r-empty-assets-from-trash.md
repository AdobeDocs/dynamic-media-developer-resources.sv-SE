---
description: Tömmer resurser från IPS-papperskorgen.
seo-description: Tömmer resurser från IPS-papperskorgen.
seo-title: emptyAssetsFromTrash
solution: Experience Manager
title: emptyAssetsFromTrash
topic: Scene7 Image Production System API
uuid: de11a7b0-cd4b-4717-8596-d39afbcf7e9c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# emptyAssetsFromTrash{#emptyassetsfromtrash}

Tömmer resurser från IPS-papperskorgen.

Resurserna finns i papperskorgen tills de töms manuellt eller tills de går ur papperskorgen. Om de töms manuellt bor de i papperskorgen till nästa rensningsjobb (normalt på kvällen) när de till slut tömts från systemet. Om de kommer ut i papperskorgen rensas resurserna bort som en del av samma rensningsaktivitet. Timeout-värdet kan konfigureras (standardvärdet är 7 dagar).

## Auktoriserade användartyper {#section-24dee2bf5f9f4714a64955c80f2803b4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`
* ``

## Parametrar {#section-8e1fb0ee3aae453581e99ef76e298569}

**Indata (emptyAssetsFromTrashParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Handtaget till det företag som äger tillgångarna. |
| ` *`assetHandleArray`*` | `types:HandleArray` | Ja | Arrayen med handtag som representerar objekt som ska tömmas från papperskorgen. |

**Utdata (emptyAssetsFromTrashParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`successCount`*` | `xsd:Int` | Ja | Antalet resurser som tömts från papperskorgen. |
| ` *`warningCount`*` | `xsd:Int` | Ja | Antalet varningar som genereras när åtgärden försökte tömma resurser från papperskorgen. |
| ` *`errorCount`*` | `xsd:Int` | Ja | Antalet fel som genererades när åtgärden försökte tömma resurser från papperskorgen. |
| ` *`warningDetailArray`*` | `types:AssetOperationFaultArray` | Nej | Arrayen med information som är associerad med resurserna som genererade varningar när åtgärden försökte tömma dem från papperskorgen. |
| ` *`errorDetailArray`*` | `types:AssetOperationFaultArray` | Nej | Arrayen med information som är associerad med resurserna som genererade fel när åtgärden försökte tömma dem från papperskorgen. |

## Exempel {#section-6154a873b6c342bf92e2036280cafdcf}

I det här kodexemplet används företagets handtag och en tillgångshandtag som innehåller handtag till de tillgångar som ska tömmas från papperskorgen.

**Begäran**

```java
<emptyAssetsFromTrashParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandleArray>
      <items>a|942|1|579</items>
      <items>a|943|1|580</items>
   </assetHandleArray>
</emptyAssetsFromTrashParam>
```

**Svar**

```java
<emptyAssetsFromTrashReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</emptyAssetsFromTrashReturn>
```

