---
description: Byter namn på en mapp.
seo-description: Byter namn på en mapp.
seo-title: renameFolder
solution: Experience Manager
title: renameFolder
topic: Scene7 Image Production System API
uuid: 7d190a57-1d81-4f41-9205-b8ffdf7330ec
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# renameFolder{#renamefolder}

Byter namn på en mapp.

Syntax

## Auktoriserade användartyper {#section-5a252b00937d4befbec76fa23fbae9df}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>Användaren måste ha läs- och skrivåtkomst till resursen.

## Parametrar {#section-6fcee63dc3f74a5b90e1d71e59eb255c}

**Indata (renameFolderParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Ja | Hantera företaget med mappar som du vill byta namn på. |
| ` *`folderHandle`*` | `xsd:string` | Ja | Hantera till mappen. |
| ` *`folderName`*` | `xsd:string` | Ja | Nytt mappnamn. |

**Utdata (renameFolderReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| ` *`folderHandle`*` | `xsd:string` | Ja | Hantera den namnändrade mappen. |

## Exempel {#section-98bdd2f88d164f488676e90aba1dc864}

Det här kodexemplet byter namn på en mapp.

**Begäran**

```java
<ns1:renameFolderParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/PDF/</ns1:folderHandle>
   <ns1:folderName>My Newly Renamed PDF Folder</ns1:folderName>
</ns1:renameFolderParam>
```

**Svar**

```java
<renameFolderReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <folderHandle>MyCompany/My Newly Renamed PDF Folder/</folderHandle>
</renameFolderReturn>
```

