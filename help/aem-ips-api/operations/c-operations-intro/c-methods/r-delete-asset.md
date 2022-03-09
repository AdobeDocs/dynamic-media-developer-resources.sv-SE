---
description: Tar bort en resurs.
solution: Experience Manager
title: deleteAsset
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: dacea36e-3d40-4aaf-94fd-f0709830caf9
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '92'
ht-degree: 0%

---

# deleteAsset{#deleteasset}

Tar bort en resurs.

Syntax

## Auktoriserade användartyper {#section-e913be43b684491daf02bc73211e4290}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Användaren måste ha läs- och borttagningsåtkomst till resursen.

## Parametrar {#section-0eed164e278b456fbdfb7a50727a0416}

**Indata (deleteAssetParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| companyHandle | `xsd:string` | Ja | Referensen till företaget som mappen tillhör. |
| assetHandle | `xsd:string` | Ja | Referensen till resursen som ska tas bort. |

**Utdata (deleteAssetParam)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-d5657289f5234bb0a613dcf691507958}

Den här exempelkoden tar bort alla typer av mediefiler från ett visst företag. Den kräver en resurshandtag som du måste hämta från en annan åtgärd.

**Begäran**

```java
<ns1:deleteAssetParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>24265|1|17061</ns1:assetHandle>
</ns1:deleteAssetParam>
```

**Svar**

Ingen.
