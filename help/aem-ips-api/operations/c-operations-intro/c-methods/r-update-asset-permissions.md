---
description: Uppdaterar resursbehörigheter.
seo-description: Uppdaterar resursbehörigheter.
seo-title: updateAssetPermissions
solution: Experience Manager
title: updateAssetPermissions
uuid: feb2faf3-81de-436e-82de-1e41df03508f
feature: Dynamic Media Classic,SDK/API,Resurshantering
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

---


# updateAssetPermissions{#updateassetpermissons}

Uppdaterar resursbehörigheter.

Syntax

## Auktoriserade användartyper {#section-3928e9badc3842e1859af4ed362df719}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-392cb3076cf84790a32fd913f2b111a3}

**Indata (updateAssetPermissionsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Företagshandtag. |
| `*`assetHandle`*` | `xsd:string` | Ja | Resurshandtag. |
| `*`updateArray`*` | `types:PermissionUpdateArray` | Ja | Behörigheter som du vill använda för resursen. |

**Utdata (updateAssetPermissionsReturn)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-1b7b7dbfdab34c819a53f3d33004e1f9}

**Begäran**

```java
<ns1:updateAssetPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:assetHandle>15674|25|1062</ns1:assetHandle>
   <ns1:updateArray>
      <ns1:items>
         <ns1:groupHandle>225</ns1:groupHandle>
         <ns1:permissionType>Read</ns1:permissionType>
         <ns1:isAllowed>true</ns1:isAllowed>
         <ns1:isOverride>false</ns1:isOverride>
      </ns1:items>
   </ns1:updateArray>
</ns1:updateAssetPermissionsParam>
```

**Svar**

Ingen.
