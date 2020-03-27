---
description: Anger behörigheter för en enskild resurs genom att använda en behörighetsresurs.
seo-description: Anger behörigheter för en enskild resurs genom att använda en behörighetsresurs.
seo-title: setAssetPermissions
solution: Experience Manager
title: setAssetPermissions
topic: Scene7 Image Production System API
uuid: 38f26482-bce9-4d2c-9714-e8c3ae40c2d1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# setAssetPermissions{#setassetpermissions}

Anger behörigheter för en enskild resurs genom att använda en behörighetsresurs.

Resurser ärver behörigheterna för sin överordnade mapp som standard. När du har angett behörigheter för en resurs ärver den inte längre behörigheten för dess överordnade såvida du inte anropar `removeAssetPermissions`.

## Auktoriserade användartyper {#section-91fafc170c734ed2a77beafda9221768}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-e05abbce6453450fb38747101cb5e228}

**Indata (setAssetPermissonsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Referensen till det företag som innehåller mappen som du vill arbeta med. |
| ` *`assetHandle`*` | `xsd:string` | Ja | Mappreferens. |
| ` *`permissionArray`*` | `types:PermissionsUpdateArray` | Ja | Behörighetsmatris. |

**Utdata (setAssetPermissonsReturn)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-38955bc330bb4909b6b06027ef2b143e}

Det här kodexemplet anger behörigheter för en resurs. Den innehåller företags- och tillgångshandtaget samt en permissions-matris.

**Begäran**

```java
<setAssetPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <assetHandle>97374|1|61046</assetHandle>
   <permissionArray>
      <items>
         <groupHandle>521</groupHandle>
         <permissionType>Read</permissionType>
         <isAllowed>true</isAllowed>
         <isOverride>true</isOverride>
      </items>
   </permissionArray>
</setAssetPermissionsParam>
```

**Svar**

Ingen.
