---
description: Anger behörigheter för en enskild resurs genom att använda en behörighetsresurs.
solution: Experience Manager
title: setAssetPermissions
feature: Dynamic Media Classic,SDK/API,Resurshantering
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

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
| `*`companyHandle`*` | `xsd:string` | Ja | Referensen till det företag som innehåller mappen som du vill arbeta med. |
| `*`assetHandle`*` | `xsd:string` | Ja | Mappreferens. |
| `*`permissionArray`*` | `types:PermissionsUpdateArray` | Ja | Behörighetsmatris. |

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
