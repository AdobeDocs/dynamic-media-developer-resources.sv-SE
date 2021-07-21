---
description: Returnerar publiceringshistoriken för en resurs.
solution: Experience Manager
title: getAssetPublishHistory
feature: Dynamic Media Classic,SDK/API,Resurshantering
role: Developer,Admin
exl-id: f337e7f9-1af6-4164-b9bd-e697548e2850
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# getAssetPublishHistory{#getassetpublishhistory}

Returnerar publiceringshistoriken för en resurs.

Syntax

## Auktoriserade användartyper {#section-3b9d6a129093458fa8890139a2718912}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-3541bd9914a44b89acfc1d419b560ee6}

**Indata (getAssetPublishHistoryParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Referensen till företaget med resursens publiceringshistorik. |
| `*`assetHandle`*` | `xsd:string` | Ja | Resursen med den publiceringshistorik som du vill granska. |

**Utdata (getAssetPublishHistoryReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`pubHistoryArray`*` | `types:PublishHistoryArray` | Ja | Resursens publiceringshistorik. |

## Exempel {#section-53897c51e5a047c5bd5ea5a6efb2d114}

Detta kodexempel returnerar publiceringshistoriken för en resurs. En resurs har aldrig publicerats om servern returnerar en tom array.

**Begäran**

```java
<getAssetPublishHistoryParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <assetHandle>a|732|1|535</assetHandle>
</getAssetPublishHistoryParam>
```

**Svar**

```java
<getAssetPublishHistoryReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <pubHistoryArray/>
</getAssetPublishHistoryReturn>
```
