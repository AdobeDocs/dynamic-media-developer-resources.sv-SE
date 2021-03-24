---
description: Tar bort behörigheter från markerade resurser.
solution: Experience Manager
title: removeAssetPermissions
feature: Dynamic Media Classic,SDK/API,Resurshantering
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---


# removeAssetPermissions{#removeassetpermissions}

Tar bort behörigheter från markerade resurser.

Syntax

## Auktoriserade användartyper {#section-239058fdb4454e519ac327e621cb3abc}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-b70bf3b033ca45b396964baf2ab1fb0f}

**Indata (removeAssetPermissionsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handtaget till företaget. |
| `*`assetHandle`*` | `xsd:string` | Ja | Referensen till resursen med behörigheter som du vill ta bort. |

**Utdata (removeAssetPermissionsReturn)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-238fa7bb091548f5ba72ced11fc92d4f}

Det här kodexemplet tar bort behörigheter från en resurs.

**Begäran**

```java
<ns1:removeAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
</ns1:removeAssetPermissionsParam>
```

**Svar**

Ingen.
