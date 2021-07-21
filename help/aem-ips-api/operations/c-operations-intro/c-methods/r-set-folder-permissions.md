---
description: Anger mappbehörigheter.
solution: Experience Manager
title: setFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 0da05679-207e-4dc8-9bfe-2cf09a8c3f17
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 0%

---

# setFolderPermissions{#setfolderpermissions}

Anger mappbehörigheter.

Syntax

## Auktoriserade användartyper {#section-d3eb923fcf5741b99967634db809e09e}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-2a41135054954396b40f1228f2e63b42}

**Indata (setFolderPermissionsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Företagshandtag. |
| `*`folderHandle`*` | `xsd:string` | Ja | Mappreferens. |
| `*`setChildren`*` | `xsd:boolean` | Ja | Anger behörigheter för underordnade som tillhör mappen. |
| `*`permissionArray`*` | `types:PermissionUpdateArray` | Ja | Behörighetsmatris. |

**Utdata (setFolderPermissionsReturn)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-01730da4be874553ab44e3241cdf6357}

I det här kodexemplet anges en företagsreferens, en mappreferens och en behörighetsarray med detaljerad information om mappen. Samma behörigheter gäller för den överordnade mappens underordnade mappar.

**Begäran**

```java
<setFolderPermissionsParam xmlns="http://www.scene7.com/IpsApi/xsd">
   <companyHandle>64</companyHandle>
   <folderHandle>blackmesa/Awatermark/</folderHandle>
   <setChildren>true</setChildren>
   <permissionArray>
      <items>
         <groupHandle>521</groupHandle>
         <permissionType>Read</permissionType>
         <isAllowed>true</isAllowed>
         <isOverride>true</isOverride>
      </items>
   </permissionArray>
</setFolderPermissionsParam>
```

**Svar**

Ingen.
