---
description: Flytta en mapp till en ny plats.
solution: Experience Manager
title: moveFolder
feature: Dynamic Media Classic,SDK/API
role: Utvecklare,Administratör
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

---


# moveFolder{#movefolder}

Flytta en mapp till en ny plats.

Syntax

## Auktoriserade användartyper {#section-7f1979fb5e504bdea3a8df01101b50c3}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametrar {#section-473c2e68bcc14a9ea2593bee26e679dd}

**Indata (moveFolderParam)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Ja | Handla till företaget. |
| `*`folderHandle`*` | `xsd:string` | Ja | Mappreferens. |
| `*`destFolderHandle`*` | `xsd:string` | Ja | Hantera målmappen. |

**Utdata (moveFolderReturn)**

| Namn | Typ | Obligatoriskt | Beskrivning |
|---|---|---|---|
| `*`folderHandle`*` | `xsd:string` | Ja | Hantera den flyttade mappen. |

## Exempel {#section-6571c6ab89ce4cb9a139abdb29c6b279}

**Begäran**

```java
<moveFolderParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
   <companyHandle>c|101</companyHandle>
   <folderHandle>f|test/MoveTest/</folderHandle>
   <destFolderHandle>f|DevanCo/DestFolder/</destFolderHandle>
</moveFolderParam>
```

**Svar**

```java
<moveFolderReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
   <folderHandle>f|test/DestFolder/MoveTest/</folderHandle>
</moveFolderReturn>
```

