---
description: Uppdatera mappbehörigheter.
solution: Experience Manager
title: updateFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 4e4f382e-4339-4b9d-a721-d33a4fa8be6b
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 0%

---

# updateFolderPermissions{#updatefolderpermissions}

Uppdatera mappbehörigheter.

Syntax

## Auktoriserade användartyper {#section-e5c2217231bf4b3386e0ab3f2e9aca0b}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametrar {#section-339e6e17c5504e1ea79fbdc05f618050}

**Indata (updateFolderPermissionsParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Företagshandtag. |
| `*`folderHandle`*` | `xsd:string` | Ja | Mappreferens. |
| `*`updateChildren`*` | `xsd:boolean` | Ja | Avgör om underordnade med behörigheter för den översta mappen ska uppdateras. |
| `*`updateArray`*` | `types:PermissionUpdateArray` | Ja | Arrayen med behörighetsuppdateringar som du vill tillämpa på mappen. |

**Utdata (updateFolderPermissionsReturn)**

IPS API returnerar inget svar för den här åtgärden.

## Exempel {#section-c3fe4d4388674870a3856c35ef66b631}

**Begäran**

```java
<ns1:updateFolderPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/eCatalogs/</ns1:folderHandle>
   <ns1:updateChildren>false</ns1:updateChildren>
   <ns1:updateArray>
      <ns1:items>
         <ns1:groupHandle>225</ns1:groupHandle>
         <ns1:permissionType>Read</ns1:permissionType>
         <ns1:isAllowed>true</ns1:isAllowed>
         <ns1:isOverride>true</ns1:isOverride>
      </ns1:items>
   </ns1:updateArray>
</ns1:updateFolderPermissionsParam>
```

**Svar**

Ingen.
